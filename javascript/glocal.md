# Global

Every thing not inside a function then it is global.

The Javascript code is running on an **Execution Context**. When javascript code is executed, a execution context is created. Javascript engine will then create an GlobalObject and "this" automatically. The global variable will attach to the GlobalOject.

For example, In the browser the GlobalObject will be the "window". The global object will attach to it.

```javascript
<html>
    <head>
    </head>
    <body>
        <script src="app.js"></script>
    </body>
</html>
```

```
var a = 'hello world!';
```

In the console

```
a
"hello world!"
window.a
"hello world!"
```



