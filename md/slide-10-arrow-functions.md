##Arrow Functions
Rules of Arrow Functions
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
// Nicer looking, and more succinct style
let odds = arrOfNumbers.filter(n => n % 2 !== 0);

// The following are NOT allowed with arrow functions

// TypeError
let IllegalConstructor = () => {};
new IllegalConstructor;

let unknownArgNumber = () {
  // Can't use arguments keyword
  let numberOfArgs = arguments.length;
}

// prototype not available on arrow functions
myArrowFunc.prototype.someMethod = function() {}
```

Note:
- Identical to a function except for following
  - cannot use the 'arguments' keyword in function body
  - arrow functions cannot be used as generators (we'll touch on those later)
  - Like built in functions, they lack '.prototype' and a 'Constructor', so you can't call 'new' on them -> TypeError
