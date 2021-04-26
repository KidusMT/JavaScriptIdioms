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

## Hoisting
 - [Hoisting is JavaScript's default behavior of moving declarations to the top](https://gomakethings.com/function-expressions-vs-function-declarations/#hoisting)

## Function Expression vs Function Declaration
 - [Declaration](https://medium.com/@mandeep1012/function-declarations-vs-function-expressions-b43646042052): defining a function for later use
    - `hoisted` to the top
 ```js
 function foo(){
     console.log("foo here");
 }
 
 // called with the name of the function
 foo();
 ```
 - [Expression](https://medium.com/@mandeep1012/function-declarations-vs-function-expressions-b43646042052): storing a function in a variable
    - `not hoisted` to the top
 ```js
 var x = function (a, b) {return a * b};
 
 // called using the vairable name
 x(4,5);//20
 ```
