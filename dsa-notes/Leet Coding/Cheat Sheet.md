
### Constants
- Infinity: `Double.POSITIVE_INFINITY`
### Types
- Double to Int: `myDouble.intValue()` 

### Slicing
```java
// Copy a subarray using Arrays.copyOfRange
int[] subArrayCopyOfRange = Arrays.copyOfRange(originalArray, arrayStart, arrayEnd);

// Sub Lists
List<Integer> subList = originalList.subList(listStart, listEnd);

// Substring
String substring = originalString.substring(stringStart, stringEnd);
```
### Arrays
```java
// Array Copy 
int[] newArr = Arrays.copyOf(arr3, arr3.length); 
int[] subArrayCopyOfRange = Arrays.copyOfRange(originalArray, arrayStart, arrayEnd);

// Sorting 
Arrays.sort(arr3); 
// Binary Search 
int index = Arrays.binarySearch(arr3, 3); 
// Convert to String 
String arrString = Arrays.toString(arr3);
// Fill an Array 
Arrays.fill(arr3, 10); 
// Compare Arrays 
boolean areEqual = Arrays.equals(arr3, copiedArr);
// Stream Operations 
int sum = Arrays.stream(arr3).sum(); 
int max = Arrays.stream(arr3).max().getAsInt(); 
int min = Arrays.stream(arr3).min().getAsInt(); 
double average = Arrays.stream(arr3).average().getAsDouble(); 
int[] filtered = Arrays.stream(arr3).filter(x -> x % 2 == 0).toArray();
```
### Strings

### Lists 
### Graphs
### Maps
### Sets 
### Priority Queues
### Intervals
### Binary Search 
- Basic Template
```java
int left = 0, right = nums.size() - 1;  
while(left <= right){  
// Prevent (left + right) overflow  
int mid = left + (right - left) / 2;  
if(nums[mid] == target){ return mid; }  
else if(nums[mid] < target) { left = mid + 1; }  
else { right = mid - 1; }  
}  
  
// End Condition: left > right  
return -1;
```
### Trees

