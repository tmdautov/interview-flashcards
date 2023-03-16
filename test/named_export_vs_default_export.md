### Named export vs default export

- You can have both named exports and a default export in the same module, but you can only have one default export.

```js
export function MyComponent() {}
vs;
export default MyComponent;
```


::


**Default export**

- default exports allow you to export a single value as the default export from a module, which can then be imported in another module without naming it. For example:

```js
// moduleC.js
export default MyComponent() { ... };

// moduleD.js
import MyComponent from './moduleC.js';
```

**Named export**

- Named exports allow you to export multiple values from a single module, which can then be imported in another module using the same names. For example:

```js
// moduleA.js
export const value1 = "Value 1";
export const value2 = "Value 2";

// moduleB.js
import { value1, value2 } from "./moduleA.js";
console.log(value1, value2); // "Value 1", "Value 2"
```