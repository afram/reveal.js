##let: Closures in loops
Using let makes it easier to create closures within loops
<!-- .element class="small" -->

<div class="split-container">
```js
for (let i = 0; i < n; i++) {
    let x = a[i];
    element.onclick = function() {
        ... x ...
    };
}
```
```js
function bindClick(x) {
  element.onclick = function() {
      ... x ...
  };
}

for (var i = 0; i < n; i++) {
    bindClick(a[i]);
}
```

Note:
- Using 'LET' makes it easier to create closures within loops

- es6: 'x' is block scoped

- es5: 'i' is function scoped, need to create new function for closure
