A **class** is a template for creating objects that encapsulates data and methods. It is syntax on top of [[Prototypes]]

```js
class Ball {
  constructor(x, y, r) {   // runs automatically on `new`
    this.x = x;
    this.y = y;
    this.radius = r;
  }
  ballInfo() {             // instance method
    alert("I am a ball this big: " + this.radius);
  }
}
let b1 = new Ball(400, 300, 20);
b1.ballInfo();
```
- `constructor()` sets up properties; if missing, JS adds an empty one
- **class expression**: `let Car = class { constructor() {} }`
- classes are **not hoisted**, so define before `new` ([[Hoisting]])

# Instance vs static
- **instance method**: called on an object, uses its data (`myCar.drive()`)
- **static method/field**: called on the **class**, not instances; for utilities
```js
class Point {
  constructor(x, y) { this.x = x; this.y = y; }
  static displayName = "Point";
  static distance(a, b) { return Math.hypot(a.x - b.x, a.y - b.y); }
}
const p1 = new Point(5, 5), p2 = new Point(10, 10);
p1.distance;               // undefined
Point.distance(p1, p2);    // 7.0710678118654755
```

# Private fields
```js
class Box {
  #height = 0;  // private: only usable inside the class
  width = 0;    // public
}
```

# Inheritance
`extends` inherits all methods of another class. A subclass constructor must call **`super()`** before using `this`; `super.method()` calls the parent's version
```js
class SmallBall extends Ball {
  constructor(x, y) {
    super(x, y, 5);
  }
}
```

# Class-based vs prototypal
- **class-based** (Java, C#): every object belongs to a class; behaviour lives on classes
- **prototypal** (JS): more flexible; each object can define its own behaviour and inherits through prototypes

**Why classes:** reusable components, easier maintenance, less copy-paste, encapsulation, no global variables
