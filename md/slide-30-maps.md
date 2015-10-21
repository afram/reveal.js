##Maps (& WeakMaps)

<div class="code-extra es5">
```js
// Could only use strings for keys
var m = {};

var x = { id: 1 },
    y = { id: 2 };

m[x] = "foo";
m[y] = "bar";

// Wait, whaa...?
m[x]; // "bar"
m[y]; // "bar"
```
</div>
<div class="code-extra es6">
```js
// Map to the rescue!
let m = new Map();

let x = { id: 1 },
    y = { id: 2 };

m.set( x, "foo" );
m.set( y, "bar" );

m.get( x ); // "foo"
m.get( y ); // "bar"

m.size; // 2

m.delete( x );
m.size; // 1

m.clear();
m.size; // 0

```
Note:
- previously only Strings allowed as keys on objects

- x and y stringify to '[object Object]'

- can use other objects besides strings as keys in Maps

- get/set/delete/clear methods

- size instead of length

- More related to retrieving keys/values consumed as iterators not covered

- WeakMaps very similar but limited in scope and api
  - differ in how Garbage Collection works on them
  - Take only Objects as keys
  - Keys held weakly, if GC'd entry is also removed
  - only applies to keys, not values
