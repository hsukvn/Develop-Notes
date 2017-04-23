# JSON

* JavaScript Object Notation inspired by javascript object to replace xml
* It is a subset of javascript object \(ie. more strict\)

```javascript
var objectLiteral = {
    firstname: 'Mary',
    isAProgrammer: true
}

console.log(JSON.stringify(objectLiteral));
// '{ "firstname": "Mary", isAProgrammer: true }'

var jsonValue = JSON.parse('{ "firstname": "Mary", isAProgrammer: true }');
console.log(jsonValue);
```



