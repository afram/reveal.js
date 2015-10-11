##let: A better *var*
Using let in place of var makes it easier to define block-local variables without worrying about them clashing with variables elsewhere in the same function body.
<!-- .element class="small" -->

```js
function log(msg) { ... }

function f(x) {
    if (...) {
        let { log, sin, cos } = Math;
        ... log(x) ...
    }
    log("done computing f()");
}
```
```js
function log(msg) { ... }

function f(x) {
    var mathLog = Math.log;
    if (...) {
        ... mathLog(x) ...
    }
    log("done computing f()");
}
```

Note:
- LET is basically a better VAR

- You can reuse variable names for more concise code - where it makes sense

- es6 example uses destructuring to import the methods on the Math object. Will touch on it more later
