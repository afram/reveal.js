##Destructuring
Parameter Matching
<!-- .element: class="small" -->

<div class="split-container">
```js
// array param
function f ([ name, val ]) {
    console.log(name, val)
}

// object param
function g ({ name, val }) {
    console.log(name, val)
}

// object param (rename)
function h ({ name: n, val: v }) {
    console.log(n, v)
}

f([ "bar", 42 ]);
g({ name: "bar", val: 42 });
h({ name: "foo", val:  7 });
```
```js
function f (arg) {
    var name = arg[0];
    var val  = arg[1];
    console.log(name, val);
};
function g (arg) {
    var name = arg.name;
    var val  = arg.val;
    console.log(name, val);
};
function h (arg) {
    var n = arg.name;
    var v = arg.val;
    console.log(n, v);
};
f([ "bar", 42 ]);
g({ name: "bar", val: 42 });
h({ name: "foo", val:  7 });
```
Note:
- Can destructure array and objects into param names

- can also rename object params as per second example 'g'
