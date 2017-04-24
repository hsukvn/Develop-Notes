# Callback

a function you give to another function to be run when the other function is finished

```javascript
function sayHiLater() {
    var greeting = 'Hi!';

    setTimeout(function() {
        console.log(greeting);
    }, 3000);
}

sayHiLater();

// jQuery uses function expressions and first-class functions!
$("button").click() {

});

function tellMeWhenDone(callback) {
    var a = 1000; // some work
    var b = 2000;
    
    callback(); // the 'callback', it runs the function I give it
}

tellMeWhenDone(function() {
    console.log('I am done');
})

tellMeWhenDone(function() {
    console.log('All done');
})
```



