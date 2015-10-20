##Modules

<div class="split-container">
```js
// lib/math.js
export function sum(x, y) {
  return x + y;
}
export var pi = 3.141593;

// app.js
import * as math from 'lib/math';
alert('2π = ' + math.sum(math.pi, math.pi));

// otherApp.js
import {sum, pi} from 'lib/math';
alert('2π = ' + sum(pi, pi));

// export default and export star

// lib/mathplusplus.js
export * from 'lib/math';
export var e = 2.71828182846;
export default function(x) {
    return Math.log(x);
}
```
```js
//commonjs es5 equivalent
modules.exports.sum = function(x, y) {
  return x + y;
};
module.exports.pi = 3.141593;

// app.js
var math = require('lib/math');
alert('2π = ' + math.sum(math.pi, math.pi));

// otherApp.js
var sum = require('lib/math').sum;
var pi = require('lib/math').pi;
alert('2π = ' + sum(pi, pi));
```
Note:
- Use the 'export' keyword to export a function, or variable.

- export default and export star have special meaning
  - export default tells the loader what to import if you don't use destructuring syntax
  - export star exports all declared functions and variables in the scope of that module

- import star is equivalent to a commonjs require

- System.import
  - Module loader specification
  - Not part of es2015
  - The eventual standard will be WHATWG's Loader specification
  - Web Hypertext Application Technology Working Group (WHATWG)
