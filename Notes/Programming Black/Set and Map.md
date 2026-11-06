# Set
Collection of **unique** values (no duplicates), any type, keeps insertion order ([[Set Theory]])
Uses: removing duplicates from an array, fast membership checks
```js
let ids = new Set([1, 2, 2, 3, 3, 3]);  // Set(3) {1, 2, 3}
ids.add(4);
ids.has(2);      // true
ids.delete(1);
ids.size;        // 3
```

# Map
Key/value pairs like an object, but:
- keys can be **any type** (object keys are strings)
- keeps insertion order
- has a real `.size`
```js
let ages = new Map();
ages.set("Ryan", 30);
ages.set("Tara", 26);
ages.get("Ryan");  // 30
ages.size;         // 2
```
Both are built on hashing ([[Hash Tables]])
