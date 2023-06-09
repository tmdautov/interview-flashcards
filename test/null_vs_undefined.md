### null vs undefined

- In JavaScript, two values discretely represent nothing - `undefined` and `null`.
- The concrete difference between them is that `null` is explicit, while `undefined` is implicit.
- When a property does not exist or a variable has not been given a value, the value is `undefined`.
- `null` is set as the value to explicitly indicate “no value”. In essence, `undefined` is used when the nothing is not known, and `null` is used when the nothing is known.

Summary

- `typeof undefined` evaluates to `"undefined"`.
- `typeof null` evaluates `"object"`. However, it is still a primitive value and this is considered an implementation bug in JavaScript.
- `undefined == null` evaluates to `true`.