**JavaScript** is a language standardised by ECMA as **ECMAScript** (latest ES17, 2026). It is **not Java**
- object-oriented **and** functional
- runs client-side (browser) or server-side (**Node.js**)
- used for Progressive Web Apps, desktop apps (**Electron**)
- **garbage collected**
- interpreted, so errors only show up at **run time**, in the browser dev tools console (`console.log`)

# Running JS in a page
Inline, with a `<script>` tag:
```html
<html>
  <script>
    console.log("Hello World")
  </script>
</html>
```
`console.log("Programming Black")` without quotes → error (it reads as undeclared variables)

External file with `src` (local file, http URL or a **CDN**), placed at the end of `<body>` or in `<head>`:
```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js"></script>
```
`alert("...")` pops up a browser dialog

# Syntax
- mostly ignores whitespace (unlike Python)
- **case sensitive**
- blocks use braces `{}` (like Java)
- semicolons can be inferred
- `"use strict";` at the top is good practice (forces declared variables, see [[Variables and Scope]])
- modules: `require` in Node.js, several ways in the browser

Next: [[Variables and Scope]], [[Types and Equality]], [[Control Structures]], [[JS Functions]], [[JS Objects]], [[DOM]]
