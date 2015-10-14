##Arrow Functions
Syntax of Arrow Functions
<!-- .element: class="small" -->

<div class="split-container">
```js
// Empty arrow function returns undefined
let empty = () => {};

// Single param case needs no
// parentheses around param list
let identity = x => x;

// No need for parentheses for expression statement body
// if single expression
let cube = x => x * x * x;

// Parenthesize the body to return an
// object literal expression. More than one
// param will require parentheses around param list
let myObj = (key, val) => ({key, val})

// Must use return statement when using curly braces
let myArr = () => {
  return [1, 2, 3];
}
```
```js
// Empty function -> returns undefined
var empty = function() {};

// Single param
// must use parentheses
var identity = function(x) { return x; };

// cube equivalent
// must use return statement
var cube = function(x) { return x * x * x; };

// return an object literal in es5
// no need to use parentheses
// around object literal
var myObj = function(key, val) { return {key: val} };

// Always have to explicitly return in classic functions
function myArr() {
  return [1, 2, 3];
}
```

Note:
- JavaScript is lexically scoped, however the binding of the 'this' keyword can be set dynamically at run time.

- Arrow functions bind 'this' to the lexical scope they are created.

- Support statement block bodes and expression statement bodies.

- The last line or result of expression is automatically returned

- For single arguments, can omit parentheses

- Must use parentheses when returning an object literal
