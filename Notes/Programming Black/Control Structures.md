`if/else`, `while`, `do...while`, `for`, `switch`, `throw/try/catch` ([[Try Catch Finally]]), ternary
Conditions use [[Types and Equality#Truthy and falsy|truthy/falsy]]

# if / else if / else
```js
if (condition) {
  statement_1;
} else if (condition2) {
  statement_2;
} else {
  statement_3;
}
```

# while
Checks the condition **before** each run (may run 0 times)
```js
while (condition) {
  statement_1;
}
```

# do...while
Checks the condition **after**, so it runs **at least once**
```js
do {
  statement_1;
} while (condition);
```

# for
```js
for (initialisation; condition; afterthought) {
  statement_1;
}
for (let i = 0; i < 10; i++) {
  console.log(i);  // 0..9: i never reaches 10 but there are 10 items
}
```
All 3 parts are optional. JS is **0-indexed**

# Ternary
```js
condition ? ifTrue : ifFalse
```
