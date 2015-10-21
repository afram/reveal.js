##let
A better var
<!-- .element class="small" -->

```js
{
  let name = 'Bob';
  console.log(name); // Bob
  {
    // does not affect outer block scope
    let name = 'not Bob';
    console.log(name); // not Bob
  }
  console.log(name); // Bob
}
```
```js
{
  var name = 'Bob';
  console.log(name); // Bob

// must wrap in a function to create new scope
  (function() {
    var name = 'not Bob';
    console.log(name); // not Bob
  })();

  console.log(name); // Bob
}
```

Note:
- LET is basically a better VAR

- Using let in place of var makes it easier to define block-local variables without worrying about them clashing with variables elsewhere in the same function body.

- es6 example uses destructuring to import the methods on the Math object.
