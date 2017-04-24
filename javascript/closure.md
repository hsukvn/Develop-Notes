# Closure![](/assets/closure_01.png)

```javascript
function buildFunctions() {
    var arr = [];

    for (var i = 0; i < 3; i++) {
        arr.push(
            // just create function
            function() {
                console.log(i);
            }
        )
    }

    return arr;
}

var fs = buildFunctions();
fs[0](); // invoke function
fs[1]();
fs[2]();
```

![](/assets/closure_02.png)

```javascript
function buildFunctions() {
    var arr = [];

    for (var i = 0; i < 3; i++) {
        let j = i; // in es6, block scope, create new variable in every round of the loop
        arr.push(
            // just create function
            function() {
                console.log(j);
            }
        )
    }

    return arr;
}

var fs = buildFunctions();
fs[0](); // invoke function
fs[1]();
fs[2]();
```

```javascript
function buildFunctions() {
    var arr = [];
    for (var i = 0; i < 3; i++) {
        arr.push(function(j) {
            return function() {
                console.log(j);
            }
        }(i));
    }
    return arr;
}

var fs = buildFunctions();
fs[0](); // invoke function
fs[1]();
fs[2]();
```

## Function Factories

```javascript
function makeGreeting(language) {
    return function(firstname, lastname) {
        if (language === 'en') {
            console.log('Hello ' + firstname + ' ' + lastname);
        }
        if (language === 'es') {
            console.log('Hola ' + firstname + ' ' + lastname);
        }
    }
}

var greetEnglish = makeGreeting('en');
var greetSpanish = makeGreeting('es');

greetEnglish('John', 'Doe');
greetSpanish('John', 'Doe');
```



