# Object.create

```javascript
var person = {
    firstname: 'Default',
    lastname: 'Default',
    greet: function() {
        return 'Hi ' + this.firstname;
    }
}

var john = Object.create(person); // set person as the prototype of john
john.firstname = 'John';
john.lastname = 'Doe';
console.log(john);
```



