# Asynchronize

1. There are different engines in browser
2. They communicate with javascript engine via event queue.
3. The javascript will check event queue only if the execution context stack is empty
4. The event may trigger execution context
   1. for example `onClick` will trigger `clickHandler()`
5. The code is still running synchronously

```javascript
function waitThreeSeconds() {
    var ms = 3000 + new Date().getTime();
    while (new Date() < ms) {}
    console.log('funished function');
}

function clickHandler() {
    console.log('click event');
}

document.addEventListener('click', clickHandler);

waitThreeSeconds();
console.log('funished execution');
```

```
app.js:4 funished function
app.js:14 funished execution
app.js:8 click event
```

Since the javascript engine won't look the event queue util the current execution context finished. The `clickHandler` will be execute after `waitThreeSeconds` done.

