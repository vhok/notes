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
  
Unlike function declaration and function expression. Does not have its own binding for *this*.  
Therefore, *this* will refer to the *this* of the scope it's contained in.
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
- In addition to the callback function, an optional argument to initialize total can be passed.  
- If no value is specified, it defaults to the object type to match that of the array elements.
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
// return: removed element

array.indexOf(item); 
// description: Returns the index of the first occurrence of a searched item.

array.splice(index, numberOfItemsToRemove); 
// description: Removes elements from array. If index is negative, reads from end of array.
// optional: numberOfItemsToRemove
// return: new array with items removed

array.slice(indexStart, indexEnd); 
// description: If a negative indexStart is specified, will extract from last elemnent.
// optional: indexStart, indexEnd
// return: copy of array from indexStart (inclusive) to indexEnd(exclusive).
```
## Common String Methods & Properties
```javascript
string.length;

string[0]; 
// description: Iterable objects can have elements accessed.

string.indexOf(substring);
// return: index where occurance happens.

string.slice(indexStart, indexEnd);
// description: If indexStart is negative, it references from end of string.
// optional: indexEnd
// return: copy of substring from indexStart (inclusive) to indexEnd (exclusive).

string.toLowerCase();
// return: copy of string in lowercase.

string.toUpperCase();
// return: copy of string in uppercase.

string.startsWith(substring);
// return: boolean

string.endsWith(substring);
// return: boolean

string.includes(substring);
// return: boolean

string.charAt(index);
// return: character as a string

string.split(splitBefore);
// return: an array of substring elements where split occurs just before splitBefore.

string.replace(stringToReplace, stringThatReplaces);
// return: a new string where indicated substrings are replaced.

string.repeat(numCopies);
// return: a new string with concatenated original numCopies times.
```
## Primitive Types
| Type | Notes |
| --- | --- |
| number, NaN | number | NaN is a number because JavaScript expects a number. |
| string | string |
| boolean | true/false |
| BigInt | Enables expressions of numbers greater than 2⁵³ - 1. const bigNumber = BigInt(someBigNumber). |
| Symbol | Represents something unique. Primarily used as an identifier for object properties.<br />let sym = Symbol() or let sym = Symbol('foo'). |
| Null | Absence of a value where it's expected. Is a type object by lack of foresight in JavaScript implementation. |
| undefined | No value. Is a type undefined. |
