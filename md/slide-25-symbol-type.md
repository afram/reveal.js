##Symbols
Unique and Immutable
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
// symbols are unique
// 'foo' is just a description for debugging
Symbol('foo') !== Symbol('foo')

const foo = Symbol()
typeof foo === 'symbol'

let obj = {}
obj[foo] = 'foo';

// not treated as a string based key
JSON.stringify(obj) // {}
Object.keys(obj) // []
Object.getOwnPropertyNames(obj) // []

// new method to get symbol keys
Object.getOwnPropertySymbols(obj) // [ foo ]
```
Note:
- Symbol is a new primitive type

- Symbols allow properties to be keyed by either string (as in ES5) or symbol

- Can have an optional description, though only used for debugging.

- they are unique, but not private as can be reflected through getOwnPropertySymbols
