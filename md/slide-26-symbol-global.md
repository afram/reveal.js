##Symbols
Global Symbol Registry
<!-- .element: class="small" -->

The global symbol registry is a list with the following record structure and it is initialized empty:
<!-- .element: class="small" -->

Field name  | Value
----------- | -------------
[[key]]     | A string key used to identify a symbol
[[symbol]]  | A symbol that is stored globally
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
// rerieve symbol from key
Symbol.for('foo'); // create a new global symbol
Symbol.for('foo'); // retrieve the already created symbol

// Same global symbol, but not locally
Symbol.for('bar') === Symbol.for('bar'); // true
Symbol('bar') === Symbol('bar'); // false

// The key is also used as the description
let sym = Symbol.for('mario');
sym.toString(); // 'Symbol(mario)'

// retrieve key for symbol in global registry
let sym2 = Symbol.for('foo');
Symbol.keyFor(sym2) // 'foo'
```

Note:
- Global registry is available runtime-wide

- Symbol.for will create a new symbol if it doesn't exist in the registry
otherwise it will retrieve an existing symbol

- Good idea to namespace symbols to prevent clashing with other libs/frameworks
