##New Built-in Methods

<div class="split-container es6">
```js
// Object Property Assignment
var dst  = { quux: 0 }
var src1 = { foo: 1, bar: 2 }
var src2 = { foo: 3, baz: 4 }
Object.assign(dst, src1, src2)
dst.quux === 0
dst.foo  === 3
dst.bar  === 2
dst.baz  === 4

// Array Element finding
[ 1, 3, 4, 2 ].find(x => x > 3) // 4

// String repeating
"foo".repeat(3) // foofoofoo

// String Searching
"hello".startsWith("ello", 1) // true
"hello".endsWith("hell", 4)   // true
"hello".includes("ell")       // true
"hello".includes("ell", 1)    // true

// Number.EPSILON
console.log(Math.abs((0.1 + 0.2) - 0.3) < Number.EPSILON) // true
```
```js
// Number type checking
Number.isNaN(42) === false
Number.isNaN(NaN) === true
Number.isFinite(Infinity) === false
Number.isFinite(NaN) === false
Number.isFinite(123) === true

// Number safe checking
Number.isSafeInteger(42) === true
Number.isSafeInteger(9007199254740992) === false

// Number Truncation
console.log(Math.trunc(42.7)) // 42
console.log(Math.trunc( 0.1)) // 0
console.log(Math.trunc(-0.1)) // -0

// Number sign Determination
console.log(Math.sign(7))   // 1
console.log(Math.sign(0))   // 0
console.log(Math.sign(-0))  // -0
console.log(Math.sign(-7))  // -1
console.log(Math.sign(NaN)) // NaN
```

Note:
- Object Property Assignment
  - Like lodash's 'extend'

- Array Element finding
  - returns first match
  - undefined if no match

- String repeating

- String searching

- Number.EPSILON for more precise floating point number comparison

- Number type checking

- Number safe checking
  - is integer correctly represented by JS (all numbers are technically floating points)

- Number Truncation
  - drop fractional part of a floating point number

- Number sign determination
  - positive = 1
  - positive zero = 0
  - negative zero = -0
  - negative = -1
  - NaN = NaN
