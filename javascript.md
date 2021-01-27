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
```javascript
array.reduce( function(total, element) {
  return total + element;
});
```

## Common Array Methods & Properties
```javascript
array.lengthl

array.forEach( function(element, index, array) ) {

};

array.push(item);

array.pop();

array.shift();

array.unshift(item);

array.indexOf(item);

array.splice(index, numberOfItemsToRemove);

array.slice();
```
