##Sets (& WeakSets)

<div class="code-extra es6">
```js
var s = new Set();

var x = { id: 1 },
    y = { id: 2 };

s.add( x );
s.add( y );
s.add( x );

s.size; // 2

s.has( x ) // true

s.delete( y );
s.size; // 1

s.clear();
s.size; // 0
```
Note:
- Collection of unique values (duplicates are ignored).

- can mix values (not that you should)

- Similar api to Map
  - no get method
  - add replaces set

- no 'get' because you test if a set has a value using 'has' method

- WeakSet holds its values weakly
  - values MUST be objects in weakSet
