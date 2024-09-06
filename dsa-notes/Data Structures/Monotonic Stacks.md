- Stacks that are either increasing or decreasing 
- Useful for finding the next greater, previous greater, next lesser or previous lesser element in an array in linear time.
- For Example:
```
for this array
[1, 3, 10, 7, 5, 24, 4]

puhsing and popping a decresing monotonic stack would look like this. (popped items are in parenthesis)

1
(1) 3
(1) (3) 10 
(1) (3) 10 7
(1) (3) 10 7 5 
(1) (3) (10) (7) (5) 24
(1) (3) (10) (7) (5) 24 4

notice that at each iteration the "previous greater" element to the current element is always on the top of the stack. also notice that the current element is the next greater element to the element on the top of the stack if it is greater than the element on the top of the stack. Therefore, you can find previous greater and next greater elements in one iteration of the array. 

also note that the next greater can also be found by iterating from the end to the begining of the array.  

You can apply this same logic for previouse and next lesser elements by using an increasing stack instead of a decresing stack 
```