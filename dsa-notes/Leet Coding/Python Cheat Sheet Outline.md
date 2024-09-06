
### Constants
- Infinity: 
### Types
- Double to Int 

### Numbers
- 

### ASCII
-  `chr(97) == 'A' chr(65) == 'a'`
- `ord('a') == 97` `ord('A') == 65`
### Slicing

### Using lists like arrays
- fixed size array full of zeros: `lst = [0]*SIZE`

### Strings
- split: `txt.split("<separator>") can be a full string or char`
- join: `"<delimiter>".join(itemsToJoin)`
- replace: `txt.replace("replaceThis", "withThis")`

### Lists 
- list comprehension
- counter
- accumulate
### Graphs
- map comprehension
### Dictionaries
- del key
- iterating over each key value pair
- find max value and return it's key
```python
max_key = max(my_dict, key=lambda k: my_dict[k]) 
max_value = my_dict[max_key]
```
- max value in dict: `max(myDict.value())`
- Ordered Dictionary: `lru = OrderedDict([keys])`
	- `lru.move_to_end(last=True)`: move to right end
	- `lru.popitem(last=False)`: remove item from left end 
### Sets 
### Priority Queues
### Intervals
### Binary Search 
- Basic Template
- mid without overflow: `(high - low)//2 + low`
### Trees

