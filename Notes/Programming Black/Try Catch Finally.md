Error handling so code **fails safely** (exits cleanly instead of crashing)
- **try**: run the code; if it fails an exception is **thrown** (usually an Error object)
- **catch**: runs with the error if one was thrown
- **finally**: **always** runs before leaving the structure

```js
try {
  incorrectFunction()
} catch (error) {
  console.log(error)
} finally {
  console.log("exiting")
}
```
Valid forms: `try...catch`, `try...finally`, `try...catch...finally`. `try` must have a `catch` or `finally`
Throw your own: `throw new Error("message")`
