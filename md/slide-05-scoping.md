##Block Scoping
####Block scoping introduces new declaration forms for defining variables scoped to a single block. This includes:

<div class="small">
- **let**: syntactically similar to *var*, but defines a variable in the current block
- **function**: allow *function* declarations in nested blocks
- **const**: like *let*, but for read-only constant declarations

Note:
- A quick breakdown of the difference between function scoping and block scoping.
Before es6, only function scope existed - so, you would have to create a new function in order to create a closure

- Have to deal with hoisting in function scope, whereas block scoped variables are NOT hoisted.
- We will see in a moment how that allows us to write cleaner code.
