# Hoisting

The variables and functions are setup during **Creation Phase** execution context. In this **Phase** the javascript engine will setup the memory.

```javascript
b();
console.log(a);

var a = 'hello world!';

function b () {
    console.log('Called b');
}
```

Console

```
app.js:7 Called b
app.js:2 undefined
```

The variable a and function b will be in the memory. But the assignment of variable a is not set yet. Instead it is set to **undefined**.

All javascript variables are set to undefined initially.

Then the javascript engine will run the code line by line in **Execution Phase**. 

