# bee
A bash script for submitting data to beeminder
## Usage
### Submit a data point
```
> bee <goal> <day> <datum> [comment]
```
Tells when datapoint has been created. 
`<day>` should be the day of the month or `^` for today.  Multiple `^` (e.g. 
`^^` for yesterday) are not supported.  

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
2           | Invalid day argument
3           | Datum is not a number
4           | Wrong number of arguments

Errors are checked in descending order, so if multiple errors exist, the largest
exit status takes precedence.  

## Feedback
I would love to hear all the ways this could be better, so if you think my code 
is bad, email me at [robbystk@gmail.com](mailto:robbystk@gmail.com).  
