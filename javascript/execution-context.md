# Execution Context

## Creation Phase

* Variable Environment
* Outer Environment
* `this`

### this

```javascript
console.log(this); // Global (window)

function a() {
    console.log(this);
    this.newvariable = 'hello';
}

var b = function() {
    consloe.log(this);
}

a(); // Global (window)
consloe.log(newvariable);
b(); // Global (window)
```

```javascript
var c = {
     name: 'The c object',
     log: function() {
          this.name = 'Updated c object';
          consloe.log(this);
          
          var setname = function(newname) {
               this.name = newname; // this point to the global object ... wtf -.-
          }
          setname('Update again! The c object');
          console.log(this);
     }
}

c.log(); // Object
```

```javascript
var c = {
     name: 'The c object',
     log: function() {
          var self = this;
          
          self.name = 'Updated c object';
          consloe.log(self);
          
          var setname = function(newname) {
               self.name = newname;
          }
          setname('Update again! The c object');
          console.log(self);
     }
}

c.log(); // Object
```



