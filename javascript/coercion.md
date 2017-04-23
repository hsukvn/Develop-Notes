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

## In Comparison

the better way is to use `===` to save your life.

## In If Statement

The variable will automatically covert to boolean in the if statement.

```
Boolean(undefined)
false
Boolean(null)
false
Boolean("")
false
Boolean(0)
false
```

Since `undefined`, `null`, and `""` all converted as `false`, it is very convenient to check variable.

```javascript
var a;

// goes to internet to get the value

if (a) {
    console.log('something is here.');
}
```

But remember that `0` is also covert to `false`.

```javascript
var a;

// goes to internet to get the value

if (a || a === 0) {
    console.log('something is here.');
}
```

## Reference

* [https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Equality\_comparisons\_and\_sameness](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Equality_comparisons_and_sameness)
* [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality\_comparisons\_and\_sameness](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)



