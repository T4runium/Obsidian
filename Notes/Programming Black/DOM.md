The **Document Object Model (DOM)** is the browser's internal, object-oriented representation of a web page as a **tree of nodes**. JS can use it to read and change the page's structure, style and content

- the DOM is **not part of JavaScript**; it's a **web API** (also usable from other languages, e.g. Python)
- the HTML DOM API defines each HTML element's functionality and gives access to form data
- every property, method and event is an object, accessed with `.`
- historically messy, so **jQuery** was popular; modern ES6+ browsers make plain JS fine

```js
const paragraphs = document.querySelectorAll("p");
paragraphs[0].nodeName;  // "P"
```
Nodes can have **event handlers** attached ([[DOM Events]])

# When to run DOM code
Accessing elements before they've loaded returns `null`. Wait for the DOM:
```js
document.addEventListener("DOMContentLoaded", () => {
  // safe to query elements here
})
```
(older: `<body onload="...">` or `window.onload`)

Next: [[DOM Nodes]], [[Selecting Elements]], [[Modifying the DOM]], [[DOM Events]]
