# Immediately Invoked Function Expression

```javascript
var greeting = function(name) {
    return 'Hello' + name;
}('John');

console.log(greeting);
```

```javascript
var firstname = 'John';
// function statement in parenthesis is valid
(function(name) {
    var greeting = 'Hello';
    console.log(greeting + ' ' +name);
}(firstname)); //IIFE

// also valid in this way
(function(name) {
    var greeting = 'Hello';
    console.log(greeting + ' ' +name);
})(firstname); //IIFE
```



