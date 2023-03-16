### call/apply/bind

**`fn.call(this, args)`**

- attaches **_this_** into function and executes the function immediately

Example:

```js
const person = {
  name: "John",
  age: 30,
  greet: function (greeting) {
    console.log(`${greeting}, ${this.name} I am ${this.age}`);
  },
};

const employee = {
  name: "Bob",
  age: 25,
};

// Hello, Bob I am 25
person.greet.call(employee, "Hello");
```

**`fn.apply(this, args)`**

- apply is similar to **call** except that it takes an array-like object instead of listing the arguments out one at a time:

```js
const numbers = [1, 2, 3, 4, 5];

const sum = function () {
  let total = 0;
  for (let i = 0; i < arguments.length; i++) {
    total += arguments[i];
  }
  return total;
};

// equivalent to calling sum(1, 2, 3, 4, 5)
const result = sum.apply(null, numbers);
console.log(result); // 15
```

**`bind`**
attaches `this` into function and it needs to be invoked in the future

```js
const person = {
  name: "John",
  age: 30,
  greet: function (greeting) {
    console.log(`${greeting}, ${this.name}, I am ${this.age}`);
  },
};

const employee = {
  name: "Bob",
  age: 25,
};

const greetEmployee = person.greet.bind(employee, "Hello");
// outputs "Hello, my name is Bob and I am 25 years old."
greetEmployee();
```