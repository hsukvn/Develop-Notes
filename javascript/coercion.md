# Coercion

converting a value from one type to another

```
Number(undefined)
NaN
Number(null)
0
```

but not always coercion ...

```
false == 0
true
null == 0
false
null < 1
true
```

the better way is to use `===` to save your life.

