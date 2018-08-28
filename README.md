# bee
A bash script for submitting data to [beeminder](https://www.beeminder.com/)
## Usage
### Submit a data point
```
> bee <goal> <day> <datum> [comment]
```
Tells when datapoint has been created. 
`<day>` should be the day of the month or `^` for today.  Multiple `^` (e.g. 
`^^` for yesterday) are not supported.  

### Configuration File
The username and API key to be used for the transaction
should be stored in a configuration file, `~/.beeminder` by default.
The format should be a shell script which puts the credentials in the variables
`key`, and `user`.
e.g.
```
# ~/.beeminder
------
user='some_user_name'
key='Jqt6szDj5WJfm2YyBANU'
```

### Viewing goal status
```
> bee <goal>
```
Displays a summary of where you are with respect to the goal, e.g., "On 
track", "In the wrong lane", "In danger of derailing tomorrow".  

## Errors
Exit status | Meaning
----------: | :---------
0           | Everything went properly
1           | Goal not found
2           | Configuration file not found
3           | Invalid day argument
4           | Datum is not a number
5           | Wrong number of arguments

Errors are checked in descending order, so if multiple errors exist, the largest
exit status takes precedence.  

## Feedback
I would love to hear all the ways this could be better, so if you think my code 
is bad, email me at [robbystk@gmail.com](mailto:robbystk@gmail.com).  
