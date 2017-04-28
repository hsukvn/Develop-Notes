# Function Constructors

1. a normal function that is used to construct objects
2. the `this` variable points a new empty object, and that object is returned from the function automatically

## new

1. create empty object
2. assign `this` to this object
3. run the function
4. return the object

```javascript
function Person() { // just like constructor (function constructor)
    console.log(this);
    this.firstname = 'John';
    this.lastname = 'Doe';
    console.log('This function is invoked');
}

var john = new Person();
console.log(john)
```

## prototype

```javascript
function Person(firstname, lastname) { // just like constructor (function constructor)
    console.log(this);
    this.firstname = firstname;
    this.lastname = lastname;
    console.log('This function is invoked');
}

Person.prototype.getFullName = function() { // Person.prototype is the object that __proto__ of objects of john and jane point to
    return this.firstname + ' ' + this.lastname;
}

var john = new Person('John', 'Doe');
var john = new Person('Jane', 'Doe');

Person.prototype.getFormalFullName = function() { // Valid since __proto__ is just a pointer point to Person.prototype
    return this.lastname + ' ' + this.firstname;
}

console.log(john.getFormalFullName());
```

## Add method to primitive type

String will covert to object automatically but numbers don't

```javascript
String.prototype.isLengthGreaterThan = function(limit) {
    return this.length > limit;
}

console.log("John".isLengthGreaterThan(3)); // valid

Number.prototype.isPositive = function() {
    return this > 0;
}
3.isPositive(); // SyntaxError
var a = new Number(3);
a.isPositive(); // valid
```

## 



