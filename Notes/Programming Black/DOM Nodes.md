**Node** is an abstract base class; there are no plain Node objects, only subclasses like `Document` and `Element`
All elements are nodes, but **not all nodes are elements** (text and comments are nodes too). `Element` inherits everything from Node and extends into `HTMLElement`

# Navigating the tree
| property | returns |
| --- | --- |
| `node.parentNode` | parent (`null` if not attached to the tree yet) |
| `node.parentElement` | parent, only if it is an Element |
| `node.childNodes` | **live** NodeList of **all** children (elements, text, comments), index from 0 |
| `element.children` | only **element** children |
| `node.firstChild` / `lastChild` | first/last child, or `null` |
| `node.baseURI` | base URL of the document |

Watch out: `childNodes` includes the whitespace **text** nodes between tags, so use `children` for elements only

# NodeLists
- **live**: updates automatically when the DOM changes (`childNodes`)
- **static**: a snapshot that doesn't change (`querySelectorAll`)

Matters when you add or remove nodes while looping over a list
Same idea as [[Types of Linked List|tree/list structures]] in ADS
