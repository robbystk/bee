# bee
a bash script for submitting data to beeminder
## Usage
```
> bee <goal> <day> <data> [comment]
```
Tells when datapoint has been created and then summarizes the goal status

## Errors
Exit status | meaning
----------: | :---------
0           | everything went properly
1           | goal not found
2           | invalid day argument
3           | data is not a number
4           | wrong number of arguments
