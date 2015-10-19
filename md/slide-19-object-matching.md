##Destructuring
Object Matching
<!-- .element: class="small" -->

<div class="split-container">
```js
// object matching shorthand
let {Component, createClass} = require('react');

// nested object matching
let { op: a, lhs: { op: b }, rhs: c } = getASTNode();
```
```js
var React = require('react');
var Component = React.Component;
var createClass = React.createClass;

var tmp = getASTNode();
var a = tmp.op;
var b = tmp.lhs.op;
var c = tmp.rhs;
```
Note:
- left hand side is original prop name
