##Classes
Class Definitions
<!-- .element: class="small" -->

<div class="split-container">
```js
class Shape {
    constructor (id, x, y) {
        this.id = id
        this.move(x, y)
    }
    move (x, y) {
        this.x = x
        this.y = y
    }
}
```
```js
var Shape = function (id, x, y) {
    this.id = id;
    this.move(x, y);
};
Shape.prototype.move = function (x, y) {
    this.x = x;
    this.y = y;
};
```
Note:
- Sugar over prototype based OO pattern.

- use the 'class' keyword

- constructor function called when instantiating a new instance

- method shorthand syntax for class methods

- can only define function methods
