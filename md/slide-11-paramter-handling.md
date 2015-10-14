##Paramter Handling
Default, Rest, Spread
<!-- .element: class="small" -->

<div class="split-container">
```js
// default paramter values
function f(x, y='bar') {
  // y is 'bar' if not passed (or passed as undefined)
  return x + y;
}
f('foo ') === 'foo bar'

// rest
function f(x, ...y) {
  // y is an Array
  return x * y.length;
}
f(3, 'foo', true) === 6

// spread
function f(x, y, z) {
  return x + y + z;
}
// Pass each elem of array as argument
f(...[1,2,3]) === 6
```
```js
// must check for valid value of 'y'
function f(x, y) {
  y = y || 'foo';
  return x + y;
}
f('foo ') === 'foo bar'

// 'rest'
function f() {
  var x = arguments[0];
  var y = Array.prototype.slice.call(arguments, 1);
  return x * y.length;
}
f(3, 'foo', true) === 6

// 'spread'
function f(x, y, z) {
  return x + y + z;
}
f.apply(null, [1, 2, 3]) === 6;
```

Note:
- Three new ways of handling function parameters
  - Default
  - Rest
  - Spread

- Default
  - Used when declaring function
  - Define a default value for when a parameter is missing or passed in as undefined

- Rest
  - Used when declaring function
  - Group the rest of the args into one array

- Spread
  - Not just for use with functions
  - can be used more than once
  - Pass an array of elements as function args
