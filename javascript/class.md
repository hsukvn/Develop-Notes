# Class

only in ES6

```javascript
class Person { // this in an Object in javascript not just a template
    constructor(firstname, lastname) {
        this.firstname = firstname;
        this.lastname = lastname;
    }
    
    greet() {
        return 'Hi ' + firstname;
    }
}

var john = new Person('John', 'Doe');
```

```javascript
class InformalPerson extends Person { // Sets the prototype (__proto__)
    constructor(firstname, lastname) {
        super(firstname, lastname); // call the constructor of Person
    }
    
    greet() {
        return 'Yo ' + firstname;
    }
}
```



