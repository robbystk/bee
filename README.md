# bee
a bash script for submitting data to beeminder
## Usage
```
> bee <goal> <day> <data> [comment]
```
Tells when datapoint has been created and then summarizes the goal status.  
`<day>` should be the day of the month or `^` for today.  Multiple `^` (e.g. 
`^^` for yesterday) are not supported

## Errors
Exit status | Meaning
----------: | :---------
0           | everything went properly
1           | goal not found
2           | invalid day argument
3           | datum is not a number
4           | wrong number of arguments
