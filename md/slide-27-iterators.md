##Iterators + For..Of
Iterator objects enable custom iteration like Java Iterable
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
let fibonacci = {
    [Symbol.iterator]() {
        let pre = 0, cur = 1
        return {
           next () {
               [ pre, cur ] = [ cur, pre + cur ]
               return { done: false, value: cur }
           }
        }
    }
}

for (let n of fibonacci) {
    if (n > 1000)
        break
    console.log(n)
}
```

Iteration is based on these duck-typed interfaces
<!-- .element: class="small" -->

<div class="code-extra es6">
```js
interface IteratorResult {
  done: boolean;
  value: any;
}
interface Iterator {
  next(): IteratorResult;
}
interface Iterable {
  [Symbol.iterator](): Iterator
}
```

Note:
- An iterable object is any object that has an [iterator]() method that returns an iterator.

- An iterator is any object that has a .next() method. This method returns the next item, if any, and throws a StopIteration object if there are no more items
