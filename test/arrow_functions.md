### Arrow functions

- does not have `this` , takes `this`  from the parent scope

```js
const fn = () => {
  console.log(this); // window
};

fn();
```

- does not have `arguments` , take arguments from the parent scope

```js
const fn = () => {
  console.log(arguments);
};
fn(1, 2, 3); // ReferenceError
```