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
