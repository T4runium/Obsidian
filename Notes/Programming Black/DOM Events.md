An **event** is something that happens in the system (click, keypress, focus, submit, input, error...). The browser **fires** a signal, usually on a specific element
An **event handler** (= **event listener**) is code that runs when the event fires. Attaching one is **registering** it

# Option 1: HTML attribute
```html
<button onclick="alert('You have clicked a button');">Click</button>
```
Note the single quotes inside the double quotes. Mixes JS into HTML, so avoid it

# Option 2: addEventListener
```js
addEventListener(type, listener)
```
- `type`: case-sensitive event name, e.g. `"click"`
- `listener`: a function (or an object with `handleEvent`, or `null`)
```js
const btn = document.querySelector("button");
function handler(e) { console.log("clicked", e.target); }
btn.addEventListener("click", handler);
btn.removeEventListener("click", handler);  // must be the SAME function reference
```
Pass the function itself (`handler`), not a call (`handler()`)

# preventDefault
`event.preventDefault()` says you're handling the event yourself, so the browser skips its default action (following a link, submitting a form, scrolling, pasting)
```js
form.addEventListener("submit", e => {
  e.preventDefault();  // stop the page reloading
});
```
See [[DOM#When to run DOM code|DOMContentLoaded]]
