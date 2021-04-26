# JavaScriptIdioms
Best JavaScript Idioms and some shortcusts

## Sites
- [From Mediasuite](https://www.mediasuite.co.nz/blog/javascript-idioms-part-1/)

##

Instead of this
```js
if("foobar".indexOf("foo") > -1) 
```

Do this
```js
if(~"foobar".indexOf("foo"))
```
## 
Instead of this
```js
var foo = Math.floor(2.333)
```

Do this
```js
var foo = ~~2.333
```
## 
Instead of this
```js
var foo = parseFloat("12.4")
var bar = parseInt("12", 10)
```

Do this
```js
var foo = +"12.4"
var bar = +"12"
```
## 
Instead of this
```js
if(isNaN(foo))
```

Do this
```js
if(foo != foo)
```
## 
Instead of this
```js
(function(){ ... })()
```

Do this
```js
!function(){ ... }()
```
## 
Convert anything to a boolean by prefixing it with `!!`
```js
var isFoo = !!foo
```


## `null` vs `undefined`
 - [best SO explanation](https://stackoverflow.com/a/5076962/6021740)
 - `null`: has type `object` but `no value`
 - `undefined`: has `no type` and `no value`

