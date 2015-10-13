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

// No need for parentheses for expression body
// if single expression
let cube = x => x * x * x;

// Parenthesize the body to return an
// object literal expression. More than one
// param will require parentheses around param list
let myObj = (key, val) => ({key, val})

let myArr = (x, y) => {

}
```
```js
// Empty function -> returns undefined
var empty = function() {};

// Single param
var identity = function(x) { return x; };

// cube equivalent
var cube = function(x) { return x * x * x; };

// return an object literal in es5
var myObj = function(key, val) { return {key: val} };
```

Note:
- JavaScript is lexically scoped for the most part, however the binding of the 'this' keyword could be set dynamically at run time.

- Arrow functions bind 'this' to the lexical scope they are created.

- The last line or result of expression is automatically returned

- For single arguments, can omit parentheses

- Must use parentheses when returning an object literal
