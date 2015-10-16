##Tagged Template Strings
Dynamic strings?
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
let a = 5;
let b = 10;

function tag(strings, ...values) {
  console.log(strings[0]); // "Hello "
  console.log(strings[1]); // " world "
  console.log(values[0]);  // 15
  console.log(values[1]);  // 50

  return "Bazinga!";
}

tag`Hello ${ a + b } world ${ a * b}`;
// "Bazinga!"
```

Note:
- Allow you to modify the output of a template string using a function

- 'tag' is just an arbitrary name. Pick whatever makes sense

- First param is array of strings in the template string

- Second and every other param are values of processed substitution expressions

- Conceivable to use this for Internationalisation
