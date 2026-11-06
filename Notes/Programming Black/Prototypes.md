JS inheritance is **prototypal**: each object has an internal link to its **prototype**, another object it inherits features from

# Prototype chain
Each prototype has its own prototype, ending at `null`. Property lookups walk **up** the chain
```
Student → Person → Object.prototype → null
```
If `Person` has `name, familyName, dateOfBirth, gender` and `Student` has `studentID, coursecode`, a student can see all of them, but a person can't see `studentID`
`Object.getPrototypeOf(obj)` shows the prototype (`__proto__` is the old link)

**`Object.prototype`** is the default prototype before `null`. Every object gets its methods: `hasOwnProperty`, `isPrototypeOf`, `toString`, `valueOf`, `constructor`, `propertyIsEnumerable`, `toLocaleString`...

# Setting a prototype
```js
const obj = Object.create(proto);          // new object with prototype proto (most direct)
Object.setPrototypeOf(student, person);    // change an existing object's prototype (object or null)
```

# Checking
```js
staffRyan.hasOwnProperty("secondName");   // own property, not inherited?
person.isPrototypeOf(student);            // is person in student's chain?
```

# Shadowing
If an object and its prototype both have a property, the object's own one wins:
```js
const car = {make: "Honda"}
const car2 = {make: "notaHonda", __proto__: car}
car2.make  // "notaHonda"
```
Prototypes reduce **code redundancy**: shared methods live once on the prototype
Class syntax on top of this: [[JS Classes]]
