##Arrow Functions
Rules of Arrow Functions
<!-- .element: class="small" -->

<div class="split-container">
```js
// Empty arrow function returns undefined
let empty = () => {};

// Single param case needs no
// parentheses around param list
let identity = x => x;

// No need for parentheses for expression body
let square = x => x * x;

// Parenthesize the body to return an
// object literal expression. More than one
// param will require parentheses around param list
let myObj = (key, val) => ({key, val})
```
```js
// Empty function -> returns undefined by default
var empty = function() {};

// Single param
var identity = function(x) { return x; };

// square equivalent
var square = function(x) { return x * x; };

// return an object literal in es5
var myObj = function(key, val) { return {key: val} };
```




Note:
- Identical to a function except for following
  - cannot use the 'arguments' keyword in function body
  - arrow functions cannot be used as generators (we'll touch on those later)
  - Like built in functions, they lack '.prototype' and a 'Constructor', so you can't call 'new' on them -> TypeError
