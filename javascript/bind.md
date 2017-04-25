# Bind

change "this"

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
```



