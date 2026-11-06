An **object** models a real thing (ball, car, person): a non-primitive, **mutable** collection of named **properties**. Properties can be any type, including objects and functions
OOP = system as objects with data + methods, a public interface and private internal state

# Creating objects
**Object literal**: `{}` with comma-separated `name: value` pairs. Quick, but duplicates code if you need many of the same type
```js
let ball = {x: 200, y: 300, radius: 50, purpose: "any"};
```
**`Object()` constructor**: empty object, then add properties
```js
let myCar = new Object();
myCar.make = "VW";
myCar.model = "Touran";
```
**Constructor function**: a "blueprint" for many objects of the same type, called with `new`
```js
function Person(name, age) {
  this.firstName = name;
  this.age = age;
}
var myBFF = new Person("Tara", 26);
```
Modern version: [[JS Classes]]

# Properties
Get, set, add, delete with **dot** or **bracket** notation:
```js
ball.x += 5;            // set
ball.z = 8;             // add a new property
ball["colour"] = "red"; // bracket (key as a string)
myCar["make"];          // get, same as myCar.make
delete ball.z;          // delete
```

# Methods
A function stored as a property is a **method**. Methods that use the object's own data (via [[this]]) are **instance methods**
```js
const ryan = {
  name: "Ryan",
  sayHello: function () { console.log("Hello my name is", this.name) }, // function expression (pre-ES6)
  sayHi() { console.log("Hi, I'm", this.name) },                       // ES6 shorthand
  sayBye: () => { console.log("Bye from", this.name) }                  // arrow: NO own this → undefined
}
```

# Object scope
Anything declared inside a method with `let`/`const`/`var` is local to that method, **not** a property:
```js
const ryan = {
  name: "Ryan",
  sayHello() { console.log(this.name, this.secondName) }, // "Ryan undefined"
  exampleFunction() { let secondName = "crosby" }         // local variable, not this.secondName
}
```
Inheritance: [[Prototypes]]
