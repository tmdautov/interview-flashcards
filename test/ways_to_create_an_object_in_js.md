### Ways to create an Object in JS

There are 4 general ways to create an Object in JS:
**1. Object literal**

```js
const myObject = {
  name: "John",
  age: 30,
};
```

**2. Contstructor Function**

```js
function Person(name, age) {
  this.name = name;
  this.age = age;
}

let person = new Person("John", 30);
```

**3. Object.create()**

```js
let person = {
  name: "John",
  age: 30,
};

let newPerson = Object.create(person);
```

**4. Classes**

```js
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

let person = new Person("John", 30);
```

## Events