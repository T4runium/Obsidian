**`this`** refers to the object a piece of code is running on, so methods can be reused when the values change

Its value depends on **how the function is called** (runtime binding), not where it was defined:
- `object.method()` → `this` is `object`
- plain call outside an object → the **global object** (`undefined` in strict mode)
- [[JS Functions#Arrow functions|arrow functions]] have **no own `this`**; they use the surrounding one

```js
ball.draw = function () {
  alert("This ball's radius is: " + this.radius);
}
ball.draw();  // this === ball
```
See [[JS Objects#Methods]]
