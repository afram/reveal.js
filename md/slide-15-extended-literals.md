##Extended Literals
10 kinds of people in this world. Those that know binary, and those that don't
<!-- .element: class="small" -->

<div class="split-container">
```js
0b101010 === 42;
0o52 === 42;

'\u{20BB7}' === '𠮷' === '\uD842\uDFB7'

// regex on unicode on es5 works fine (sort of)
/𝄞/.test( "𝄞-clef" );  // true

// The length of the match is what matters. For example:
/^.-clef/ .test( "𝄞-clef" );  // false
/^.-clef/u.test( "𝄞-clef" );  // true

// new in es6
'𠮷'.codePointAt(0) == 0x20BB7

// for-of iterates code points
for(var c of '𠮷') {
  console.log(c);
}
```
```js
parseInt('101010', 2) === 42;
parseInt('52', 8) === 42;

// no unicode syntax in es5
'𠮷' === '\uD842\uDFB7'
```
Note:
- Support for Binary and Octal literals.

- Extended support for unicode within strings and regular Expressions

- 'u' treats unicode as 1 character as opposed to 2.

- The codePointAt() method returns a non-negative integer that is the UTF-16 encoded code point value.

- can iterate codepoints with for..of (new syntax)
