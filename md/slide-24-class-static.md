##Classes
Static Members
<!-- .element: class="small" -->

<div class="split-container">
```js
class Rectangle extends Shape {
    …
    static defaultRectangle () {
        return new Rectangle("default", 0, 0, 100, 100)
    }
}
class Circle extends Shape {
    …
    static defaultCircle () {
        return new Circle("default", 0, 0, 100)
    }
}
var defRectangle = Rectangle.defaultRectangle()
var defCircle    = Circle.defaultCircle()
```
```js
var Rectangle = function (id, x, y, width, height) {
    …
};
Rectangle.defaultRectangle = function () {
    return new Rectangle("default", 0, 0, 100, 100);
};
var Circle = function (id, x, y, width, height) {
    …
};
Circle.defaultCircle = function () {
    return new Circle("default", 0, 0, 100);
};
var defRectangle = Rectangle.defaultRectangle();
var defCircle    = Circle.defaultCircle();
```
Note:
- Use 'static' keyword to create a static method on the class
