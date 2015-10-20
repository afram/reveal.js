##Spread operator fun
'Spread' makes some new things possible, and others easier
<!-- .element: class="small" -->

<div class="split-container">
```js
// use with array literals
let europe = ['London', 'Krakow'];
let world = ['Melbourne', ...europe, 'Tokyo'];
// ['Melbourne', 'London', 'Krakow', 'Tokyo'];

// use with 'new'
let props = ['foo', 42];
new ConstructorFunction(...props);

// a better push
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
arr1.push(...arr2);
// arr1 == [1, 2, 3, 4, 5, 6];
```
```js
// kinda awkward
var europe = ['London', 'Krakow'];
var world = ['Melbourne'];
world.push(europe[0], europe[1], 'Tokyo');

// You can't use apply with 'new'

// long way around to concatenate arrays
var arr1 = [1, 2, 3];
var arr2 = [4, 5, 6];
Array.prototype.push.apply(arr1, arr2);
// arr1 == [1, 2, 3, 4, 5, 6];
```

Note:
- Spread enables some new tricks

- can use with array literals

- use with the 'new' keyword to instantiate new objects

- a nicer way to concatenate 2 arrays
