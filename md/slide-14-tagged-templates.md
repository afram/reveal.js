##Tagged Template Strings
Dynamic strings?
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
let a = 5, b = 10;

function tag(strings, ...values) {
  console.log(strings[0]); // "Hello "
  console.log(strings[1]); // " world "
  console.log(values[0]);  // 15
  console.log(values[1]);  // 50
  return "Bazinga!";
}

tag`Hello ${ a + b } world ${ a * b}`; // "Bazinga!"

// Raw Method
function tag(strings, ...values) {
  console.log(strings.raw[0]);
  // "string text line 1 \\n string text line 2"
}
tag`string text line 1 \n string text line 2`;

// Also available on the String Object
String.raw`Hi \n ${2+3}!`; // "Hi \\n 5!"
```

Note:
- Allow you to modify the output of a template string using a function

- 'tag' is just an arbitrary name. Pick whatever makes sense

- First param is array of strings in the template string

- Second and every other param are values of processed substitution expressions

- Raw property allows access to strings as they were entered

- Conceivable to use this for Internationalisation

Security
- Be aware that you shouldn't let untrusted users create template strings as they
have access to functions and variables
