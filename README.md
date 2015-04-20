# bee
A bash script for submitting data to beeminder
## Usage
```
> bee <goal> <day> <data> [comment]
```
Tells when datapoint has been created and then summarizes the goal status.  
`<day>` should be the day of the month or `^` for today.  Multiple `^` (e.g. 
`^^` for yesterday) are not supported.  

## Errors
Exit status | Meaning
----------: | :---------
0           | Everything went properly
1           | Goal not found
2           | Invalid day argument
3           | Datum is not a number
4           | Wrong number of arguments

## Feedback
I would love to hear all the ways this could be better, so if you think my code 
is bad, email me at [robbystk@gmail.com](mailto:robbystk@gmail.com).  
