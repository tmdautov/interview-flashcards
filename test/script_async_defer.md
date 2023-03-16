### script async/defer

There are 3 possible options:

```html
<script src="script.js"></script>
<script async src="script.js"></script>
<script defer src="script.js"></script>
```

- Without `async` or `defer`, browser will run your script immediately, before rendering the elements that's below your script tag.
- With `async` (asynchronous), browser will continue to load the HTML page and render it while the browser load and execute the script at the same time.
- With `defer`, browser will run your script when the page finished parsing. (not necessary finishing downloading all image files. This is good.)

Difference between async and defer:

- Async scripts are executed as soon as the script is loaded, so it doesn't guarantee the order of execution (a script you included at the end may execute before the first script file )
- Defer scripts guarantees the order of execution in which they appear in the page.

Links:

- https://javascript.info/script-async-defer
- https://flaviocopes.com/javascript-async-defer/

## Promise