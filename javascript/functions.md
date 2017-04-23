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



