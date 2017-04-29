# Array

Danger to use prop to get items in array since there might be extra property in prototype

```javascript
Array.prototype.myCustomFeature = 'cool!';

var arr = ['John', 'Jane', 'Jim'];

for (var prop in arr) { // danger cause array is object
    console.log(prop + ': ' + arr[prop]);
}
```





