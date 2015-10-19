##Destructuring
Array Matching
<!-- .element: class="small" -->

<div class="split-container">
```js
// destructure arrays
let arr = [1, 2, 3];
let [a, , b] = arr;

// can swap values
[ b, a ] = [ a, b ];

// fail-soft destructuring
let [a] = [];
a === undefined;

// fail-soft destructuring with defaults
let [a = 1] = [];
a === 1;
```
```js
// long way around
var arr = [1, 2, 3];
var a = arr[0], b = arr[2];

// longer way around
var tmp = a; a = b; b = tmp;

// fail-soft
var a = [][0];
a === undefined;

// don't have defaults
var a = [][0] || 1;
a === 1;
```
Note:
- First example doesn't create an array, assigns values to vars

- Destructuring is fail-soft - undefined if not found
