# getElementById
```js
const el = document.getElementById("title");  // one Element, or null
```
`id`s should be unique

# querySelector
**First** element matching a **CSS selector**
```js
document.querySelector("h1, h2").style.backgroundColor = "blue";
```

# querySelectorAll
**Static** NodeList of **all** matches ([[DOM Nodes#NodeLists]])
```js
const ps = document.querySelectorAll("p");
const boxes = document.querySelectorAll("div.note, div.alert");

for (let i = 0; i < boxes.length; i++) { let item = boxes[i]; }
boxes.forEach(item => { /* ... */ });
```
**Don't use `for...in`** on a NodeList: it also visits `length` and `item`, and the order isn't guaranteed (use `for`, `for...of` or `forEach`)

# data- attributes
Custom data on elements via `data-*` attributes, read through `.dataset`
```html
<li data-status="completed">Task 1</li>
<li data-status="pending">Task 2</li>
```
```js
const done = document.querySelectorAll('[data-status="completed"]');
done[0].dataset.status;  // "completed"
```
(the selector on the slide is mistyped; this is the correct form)

Then change them: [[Modifying the DOM]]
