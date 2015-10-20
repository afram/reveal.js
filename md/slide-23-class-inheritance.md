##Classes
Class Inheritance
<!-- .element: class="small" -->

<div class="split-container">
```js
class Rectangle extends Shape {
    constructor (id, x, y, width, height) {
        super(id, x, y)
        this.width  = width
        this.height = height
    }
}
class Circle extends Shape {
    constructor (id, x, y, radius) {
        super(id, x, y)
        this.radius = radius
    }
}
```
```js
var Rectangle = function (id, x, y, width, height) {
    Shape.call(this, id, x, y);
    this.width  = width;
    this.height = height;
};
Rectangle.prototype = Object.create(Shape.prototype);
Rectangle.prototype.constructor = Rectangle;
var Circle = function (id, x, y, radius) {
    Shape.call(this, id, x, y);
    this.radius = radius;
};
Circle.prototype = Object.create(Shape.prototype);
Circle.prototype.constructor = Circle;
```
Note:
- super method calls constructor of parent class
  - must call super when extending a class

- use the 'extends' keyword to extend a base class

- Built-ins like Array, Date and DOM Elements can be subclassed
  - Currently limited support due to es5 engine limitations
