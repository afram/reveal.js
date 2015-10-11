##let: Closures in loops
Using let makes it easier to create closures within loops
<!-- .element class="small" -->

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

<div class="code-extra es5">
```js
for (var i = 0; i < n; i++) {
    element.onclick = function() {
        ... a[i] ...
    };
}
// i now equals n, a[n] is out of range

element.click(); // simulate click element - uh oh!
```

Note:
- Using 'LET' makes it easier to create closures within loops

- es6: 'x' is block scoped, and so will not leak to the next run through the loop

- es5: Because 'i' is function scoped, you need to wrap that element in a new function scope in order to preserve the reference to it. Otherwise,
the loop will end, 'i' is now equal to 'n' (which is an undefined element) and the reference inside the 'onclick' function will break;

- Will not be touching on block scoping for 'functions' as they are identical in usage to 'let'
