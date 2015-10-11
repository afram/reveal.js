##Constants
Immutable variables
<!-- .element: class="small" -->

```js
const ROOT_2 = 1.414213562373095;
```
```js
Object.defineProperty(typeof global === "object" ? global : window, "ROOT_2", {
    value:        1.414213562373095,
    enumerable:   true,
    writable:     false,
    configurable: false
});
```

<div class="code-extra es6">
```js
// CONST BLOCK SCOPING EXAMPLE

// define PI constant
const PI = 3.14159;

function newPI() {
  // new Block scoped constant
  const PI = 4;
  console.log(PI);
}

console.log(PI); // 3.14159
newPI(); // 4
console.log(PI); // 3.14159
```

Note:
- Constants are immutable variables

- Was possible in es5, though verbose and cumbersome and only possible on the global object

- Important to note that only the variable is immutable. If it references an object, the underlying object can still be modified

- Block scoped
