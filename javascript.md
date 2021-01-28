# JavaScript Cheat Sheet

## 3 Methods for Writing Function Definition
Function Declaration  
- Assigns a value to a variable with identifier doSomething in the **current scope**.
- Variable is **hoisted** to the top of current slope.
  
Tips:  
- Useful for recursion
- Useful for detaching event listeners
```javascript
function doSomething(parameter) {
  return parameter;
};
```

Function Expression  
```javascript
const doSomething = function(parameter) {
  return parameter
  };
```

Arrow Function  
```javascript
const doSomething = (parameter) => {
  return parameter;
};
```

## Key Array Methods
Mapping
```javascript
array.map( function(element) {
  return element * 10;
});
```
Filter
```javascript
array.filter( function(element) {
  return element > 0 ? true : false;
});
```
Reduce  
-In addition to the callback function, an optional argument to initialize total can be passed.  
-If no value is specified, it defaults to the object type to match that of the array elements.
```javascript
array.reduce( function(total, element) {
  return total + element;
});
```

## Common Array Methods & Properties
```javascript
array.length

array.forEach( function(element, index, array) ) {}; 
// description: Loops over elements. Executes a callback with each iteration.
// optional: index, array

array.push(item); 
// description: Adds an element to the end of the array.

array.pop(); 
// description: Removes an element from the end of the array.
// return: removed element

array.unshift(item); 
// description:Adds an element to the the start of the array.

array.shift(); 
// description: Removes an element from the start of the array.
// return: removed elemenbt

array.indexOf(item); 
// description: Returns the index of the first occurrence of a searched item.

array.splice(index, numberOfItemsToRemove); 
// description: Removes elements from array. If index is negative, reads from end of array.
// optional: numberOfItemsToRemove
// return: new array with items removed

array.slice(indexStart, indexEnd); 
// description: Copies the array. If a negative indexStart is specified, will extract from last elemnent.
// optional: indexStart, indexEnd
// return: copied array

```
