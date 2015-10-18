##Regex Sticky mode

<div class="code-extra es6">
```js
let re = /\d+\.\s(.*?)(?:\s|$)/y
    str = "1. foo 2. bar 3. baz";

re.lastIndex;       // 0 -- initial position!
str.match( re );    // [ "1. foo ", "foo" ]

re.lastIndex;       // 7 -- correct position!
str.match( re );    // [ "2. bar ", "bar" ]

re.lastIndex;       // 14 -- correct position!
str.match( re );    // ["3. baz", "baz"]
```

Note:
- virtual anchor, rooted to matching only from 'lastIndex' property
  - if no match is found there, will reset 'lastIndex' back to 0

- Best used with text that has a predictable structure

- lastIndex is set to next char beyond successful match
