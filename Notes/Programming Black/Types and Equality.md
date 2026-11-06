# Dynamic typing
Values have types; variables and function parameters don't. Types are worked out at run time, so a variable can hold anything:
```js
let number = 10      // number
number = "ten"       // string
number = true        // boolean
```
`typeof x` gives the type of a value. Document intended types in comments

**Types:** 7 primitives (`number`, `string`, `boolean`, `undefined`, `null`, `bigint`, `symbol`) + `object` (arrays, functions etc. are objects). The slides' summary says "6 primitive and 2 non-primitive", which is an older way of counting

# Weak typing
JS converts types implicitly when they don't match:
```js
const number = 10
let result = number + "3"
console.log(result)  // "103" (number becomes a string)
```

# Operators
`=` assign · `+ - * / %` · `++ --` · `==` `!=` loose · `===` `!==` strict

**`==` loose equality** converts types first: `5 == "5"` is `true`
- objects: true only if both reference the **same object**
- strings: same characters in the same order
- numbers: same value; `+0 == -0`; `NaN` is never equal to anything (even `NaN`)
- booleans: both true or both false

**`===` strict equality** checks value **and** type, no conversion: `5 === "5"` is `false`
- different types → false
- objects → same object only
- `null === null` and `undefined === undefined` are true
- `NaN` → false

Use `===` by default

# Truthy and falsy
**Falsy** values: `false`, `0`, `""`, `null`, `undefined`, `NaN` (also `-0`, `0n`). Everything else is **truthy** (including `[]`, `{}`, `"0"`)
Useful for missing parameters or properties, and for defaults:
```js
var name = name || "guest";
```
Used in [[Control Structures]]
