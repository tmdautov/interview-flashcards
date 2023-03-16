### Prototypes. Prototypal inherritance

- Prototypes are a key concept in JS that are used to implement inheritance
- Every object in JS has a prototype, which is an object that it inherits properties and methods from
- Prototypes provide a way to share properties and methods between objects withouth having to defince them on each object individually

```js
function Person(name) {
  this.name = name;
}

Person.prototype.sayHello = function () {
  console.log("Hello, my name is " + this.name);
};

var person1 = new Person("John");
var person2 = new Person("Jane");

person1.sayHello(); // outputs "Hello, my name is John"
person2.sayHello(); // outputs "Hello, my name is Jane"
```