### spread vs rest

- rest parameter is used in functions to collect all remaining elements into array

```js
function print(...args) {
  console.log(args); // ["a", "b", "c", "d"]
}
print("a", "b", "c", "d");
```

- spread is used to spread(unpack) array into list

```js
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5];
console.log(newArr); // [1, 2, 3, 4, 5]
```