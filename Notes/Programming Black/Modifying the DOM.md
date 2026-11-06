# Changing content
| property | what |
| --- | --- |
| `el.innerText` | **rendered** (visible) text of the element and its descendants |
| `node.textContent` | **all** text of the node and descendants, hidden text included, no comments (`null` for document/doctype) |
| `el.innerHTML` | get/set the **HTML markup** inside, replacing all children; `+=` appends |

Prefer `textContent` for plain text. `innerHTML` with user input is an XSS risk

# Creating and adding
```js
const list = document.createElement("ol");   // unknown tag → HTMLUnknownElement
parent.appendChild(list);                    // adds to the END of parent's children
```
`appendChild` returns the **appended node** (not the parent), so you can create and keep it in one line:
```js
const p = document.body.appendChild(document.createElement("p"));
```

# Removing
```js
document.querySelector("li").remove();   // modern: call it on the element
parent.removeChild(child);               // older pattern, still seen in old code
```

# Attributes and style
```js
el.setAttribute("class", "big");
el.getAttribute("href");
el.style.color = "red";   // inline style (live CSSStyleProperties object)
el.hidden = true;         // hidden attribute: not shown to the user
```
Any `hidden` value (even an invalid one) hides the element; `hidden="until-found"` lets find-in-page reveal it

# Common DOM APIs
`querySelector`, `querySelectorAll`, `createElement`, `innerHTML`, `setAttribute`, `getAttribute`, `addEventListener` ([[DOM Events]]), `style`, `window.onload`, `window.scrollTo()`
