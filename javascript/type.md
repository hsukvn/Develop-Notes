# Type

```javascript
var d = [];
console.log(typeof d); // object
console.log(Object.prototype.toString.call(d));

function Person(name) {
    this.name = name;
}

var e = new Person('Jane');
console.log(typeof e);
console.log(e instanceof Person); // check Person is in the prototype chain of e

console.log(typeof undefined); // undefined
console.log(typeof null); // bug forever // gives an Object
```



