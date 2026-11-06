In strict mode variables must be declared. In non-strict mode an undeclared variable becomes **global** (avoid)

| keyword | scope | reassign? | hoisting |
| --- | --- | --- | --- |
| `var` | **function** (old style) | yes | hoisted, starts as `undefined` |
| `let` | **block** `{}` | yes | hoisted but not initialised (error if used early) |
| `const` | **block** `{}` | no | same as `let` |

Use `let`/`const`; `var` is old style

# Scope
**Scope** decides where a variable is visible. Three types:
- **block**: inside `{ }` (`let`, `const`)
- **function**: each function makes its own scope; variables inside aren't visible outside
- **global**: visible everywhere

Local scope lets different functions reuse the same variable names
Scope inside objects: [[JS Objects#Object scope]]

See [[Hoisting]]
