### Pass by reference vs pass by value

**Pass by value. Primitive data types (string, number, boolean)**

```js
let x = 10;

function fn(num) {
  num = 20;
  console.log(num); // 20
}

fn(x);
console.log(x); // 10
```

**Pass by reference. Non primitive data types**

- Example 1. When we pass an object to a function

```js
let obj = { name: "John", age: 30 };

function fn(person) {
  person.age = 40;
  console.log(person); // { name: "John", age: 40 }
}

fn(obj);
console.log(obj); // { name: "John", age: 40 }
```

- Example 2. Case when we need create a copy of an object

```js
const aObj = {
  name: "John",
};

const bObj = aObj; // Need to create a copy of an Object via Object.assign, JSON.stringify or Spread operator
bObj.name = "Sean";
console.log(aObj, bObj); // { name: 'Amir' } { name: 'Amir' }
```

**Links**

- [https://www.30secondsofcode.org/articles/s/javascript-pass-by-reference-or-pass-by-value](https://www.30secondsofcode.org/articles/s/javascript-pass-by-reference-or-pass-by-value)