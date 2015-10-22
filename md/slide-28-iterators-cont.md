##Iterators + For..Of
Iterating with For..Of continued
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
// for..of can also be used on Arrays
let arr = ['a', 'b', 'c'];

for (let val of arr) {
  console.log(val);
}
// 'a' 'b' 'c'

// for..in iterates over keys/indexes, for..of iterates over values
for (let idx in arr) {
  console.log(idx);
}
// 0 1 2
```

Note:
- For..Of iterates over values

- can be used with arrays
