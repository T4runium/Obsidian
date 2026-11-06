A **function** is a set of statements that does a task: inputs (parameters) → related output (`return`). Every JS function is a `Function` **object**, so functions are **first-class** (can be stored in variables, passed around, set as properties)

```js
function area(length) {
  return length * length
}
```

# Anonymous functions
No name, assigned to a variable (a **function expression**):
```js
const x = function (length) { return length * length }
const y = x(2)  // 4
```
Defining a function doesn't run it; you have to **call** it: `x(2)`, `obj.method()`

# Arrow functions
```js
const square = (length) => length * length
```
Shortest syntax, but **no own `this`** (see [[this]])

Functions as object properties are **methods**: [[JS Objects#Methods]]
Declarations are [[Hoisting|hoisted]]
