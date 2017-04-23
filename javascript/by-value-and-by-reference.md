# By Value and By Reference

## By Value

Primitive type of value

![](/assets/by_value_01.png)

```javascript
var a = 3;
var b;

b = a;
a = 2;

console.log(a);
console.log(b);
```

## By Reference

Object![](/assets/by_reference_01.png)

```javascript
var c = { greeting: 'hi' }
var d;

d = c;
c.greeting = 'hello'; // mutate

console.log(c);
console.log(d);
```



