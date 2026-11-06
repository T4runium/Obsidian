**Hoisting**: memory for declarations is set up before the code runs, so some names can be used before the line that declares them

| declaration | before its line |
| --- | --- |
| `function f() {}` | fully usable (hoisted) |
| `var x` | exists, value `undefined` |
| `let` / `const` | `ReferenceError` (not initialised) |
| `class C {}` | `ReferenceError` (not hoisted) |

```js
let b1 = new Ball(); // ReferenceError
class Ball {}
```
Declare classes before you use them ([[JS Classes]])
