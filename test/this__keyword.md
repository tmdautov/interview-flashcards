### this  keyword

> **this**  keyword refers to the object from where it was called.

`this`  keyword has different value depending of where it used:

- alone or outside a function: window

```js
console.log(this); // window
```

- in function with strict mode = undefined

```js
"use strict";
function fn() {
  console.log(this); // undefined
}
```

- In a function = global object or window

```js
function fn() {
  console.log(this); // window
}
```

- in arrow function -> takes this from parent scope

```js
const fn = () => {
  console.log(this); // window. Takes this from parent scope
};
```

- in an object method e.g. `obj.fn()` , this refers to the object

```js
const obj = {
  name: "hello",
  fn: function () {
    console.log(this.name);
  },
};
obj.fn(); // hello
```

- in a method of class: refers to an owner object
- in an event: referse to an element that recieved the event

More

- [https://www.30secondsofcode.org/articles/s/javascript-this](https://www.30secondsofcode.org/articles/s/javascript-this)
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
- [https://www.w3schools.com/js/js_this.asp](https://www.w3schools.com/js/js_this.asp)