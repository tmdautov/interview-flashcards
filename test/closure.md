### Closure



> The Closure is a Javascript mechanism for sharing the scope of the outer-parent function with the inner-child function.

```js
function outer() {
  const num = 123;
  function inner() {
    // we can use num variable from the parent scope inside inner function
    console.log(num);
  }
  return inner;
}

const fn = outer();
fn(); // 123
```

#flashcards

**Usecases of Closure:**

- Emulate incapsulation as in OOP by creating private properties and methods which can be accessed
  through specific methods.
- In currying functions
- In a function factory design pattern
- In a Module design pattern