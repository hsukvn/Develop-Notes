# Functions

## First Class Functions

Everything you can do with other types you can do with functions.

* Assign them to variables
* pass them around
* create then on the fly

## Function is an Object

```javascript
function greet() {
    console.log('hi');
}

greet.language = 'english';
console.log(greet.language);
```

```javascript
function log(a) {
    console.log(a);
    a();
}

log(function() {
    console.log('hi');
});
```

## Expression

A unit of code that results in a value. It doesn't have to save to a variable.

```javascript
anouymousGreet(); // error since the function is not create until execution phase
var anouymousGreet = function() {
    console.log('hi');
}
anouymousGreet();
```

## Statement

```javascript
greet(); // its ok (hoisted)
function greet() {
    console.log('hi');
}
```

## call, apply, bind

```js
var person = {
    firstname: 'John',
    lastname: 'Doe',
    getFullName: function() {
        var fullname = this.firstname + ' ' + this.lastname;
        return fullname;
    }
}

var logName = function(lang1, lang2) {
    console.log('Logged: ' + this.getFullName());
    console.log(lang1 + ' ' + lang2);
}

var logPersonName = logName.bind(person); // copy a function with given object as "this" point to

logPersonName('gg', 'yy');
logName.call(person, 'gg', 'yy'); // execute with given object as "this" point to
logName.apply(person, ['gg', 'yy']); // exactly same as call except argument as array

// function borrowing
var person2 = {
    firstname: 'Johe',
    lastname: 'Doe'
}

console.log(person.getFullName.apply(person2));

// fuction currying
/* creating a copy of a function but with some preset parametes */
function multiply(a, b) {
    return a * b;
}

var multipleByTwo = multiply.bind(this, 2); // copy a function with permanent parameter
console.log(multipleByTwo(4)); // end up as second parameter b
```



