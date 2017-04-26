# Inheritance

One object gets access to the properties and methods of another object

## Prototypal Inheritance![](/assets/inheritance_01.png)

## Reflection and Extend

an object can look at itself, listing and changing its properties and methods

_Note: the sample uses extend from underscore.js instead of javascript original `extends`_

```javascript
var person = {
    firstname: 'Default',
    lastname: 'Default',
    getFullName: function() {
        return this.firstname + ' ' + this.lastname;
    }
}

var john = {
    firstname: 'John',
    lastname: 'Doe'
}
for (var prop in john) {
    if (john.hasOwnProperty(prop)) { // if not doing this, will show not only own property but also __proto__
        console.log(prop + ': ' + john[prop]);
    }
}

var jane = {
    address: '1111 Main St.',
    getFormalFullName: funtion() {
        return this.lastname + ' ' + his.firstname;
    }
}

var jim = {
    getFirstName: function() {
        return firstname;
    }
}

_.extend(john, jane, jim); // from underscore.js

console.log(john);
```



