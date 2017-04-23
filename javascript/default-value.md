# Default Value

It is good to give a default value to the variable of a function to avoid strange behavior.

_Note: there is a better way to give default value in ES6_

```javascript
function greet(name) {
    name = name || '<Some default value>';
    console.log('hello ' + name);
}

greet();
```

If the default value is not set, the `name` will be `undefined` and be convert to `'undefined'` thus get `hello undefined`

```
null || undefined || 0
0
null || undefined || 0 || 'hello'
"hello"
```



