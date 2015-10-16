##Template Strings
"No " + "More of" + " this!"
<!-- .element: class="small" -->

<div class="split-container">
```js
`Write template strings using backticks`
//Write template strings using backticks

var x = 'interpolation';

`String ${x} is a breeze`
// String interpolation is a breeze

`Expression interpolation is ${10 * 10} times easier`
//Expression interpolation is 100 times easier

`Multi-line strings
don't need special characters`
//Multi-line strings
//don't need special characters
```
```js
'This first example is not that exciting'
//This first example is not that exciting

var x = 'interpolation';

'String ' + x + ' is a bit cumbersome'
// String interpolation is a bit cumbersome

'Expression interpolation is not ' + (10 * 10) + ' times easier'
//Expression interpolation is not 100 times easier

'This is a little\n' +
'awkward'
//This is a little
//awkward
```

Note:
- Use backticks

- Can do string interpolation in an easy to understand way

- Able to have multi-line strings without escaping the new line
