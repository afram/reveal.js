##Promises

<div class="code-extra es6">
```js
let asyncAction = function() {
  return new Promise(resolve, reject) {
    ...
    resolve('foo');
  }
};

asyncAction()
  .then(function(result) {
    /// result === 'foo'
  })
  .catch(function(e) {
    // this block executes if 'reject' is executed above
  })

```

Note:
-
- Native support for Promises

- Follows Promises A+ Spec

- 3 states
  - pending
  - rejected
  - fulfilled
