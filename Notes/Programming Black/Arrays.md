Mutable, dynamic list that can mix types. Square brackets, like Python
```js
let arr = new Array(1, 2, 3);
let arr = Array(1, 2, 3);
let arr = [1, 2, 3];      // all equivalent; use this one
```
Iterate:
```js
arr.push(4);  // add to the end
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```
Other `Array` methods: `pop`, `map`, `filter`, `forEach`, `reduce`...

Practice task: from `const nums = [3, 7, 2, 9, 12, 5, 8];` write a function that finds the max and min, the average, and returns a new array with every value doubled

See also [[Set and Map]]
