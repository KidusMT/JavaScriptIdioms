<p align="center">
     <img width="200" height="200" src="https://user-images.githubusercontent.com/18373774/116816670-85fe2900-ab28-11eb-8518-31414cd6ddc9.png" alt="js logo"/>
<p>

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
 - [var hoisting](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var#var_hoisting)
 - [Hoisting is JavaScript's default behavior of moving declarations to the top](https://gomakethings.com/function-expressions-vs-function-declarations/#hoisting)
 - [Nice article from wsvincent](https://wsvincent.com/javascript-hoisting/)
 - [JavaScript Hoisting](https://www.javascripttutorial.net/javascript-hoisting/)
 - [DigitalOcean's explanation](https://www.digitalocean.com/community/tutorials/understanding-hoisting-in-javascript)
 - Hoisting precedence:
    - 1) Variable assignment takes precedence over function declaration
    - 2) Function declarations take precedence over variable declarations
    - `variable assignment` > `function declaration` > `variable declaration`
 - [To avoid Hoisting](https://medium.com/front-end-weekly/hoisting-in-javascript-f4a600a02a78):
    - 1) using `"use strict"` directive on top
    - 2) using `let` and `const` inplace of var
    - 3) declaring all variables on top

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
 
 ## [BEST: The Ultimate Guide to Execution Contexts, Hoisting, Scopes, and Closures in JavaScript](https://www.youtube.com/watch?v=Nt-qa_LlUH0)
 - [more on closures](https://robertnyman.com/2008/10/09/explaining-javascript-scope-and-closures/#highlighter_892783)
 
 ## `[[Prototype]]` vs `__proto__` vs `prototype`
 - [best stackoverflow summary](https://stackoverflow.com/a/32740085/6021740)
 - [nice article from levelup](https://levelup.gitconnected.com/the-javascript-object-paradigm-and-prototypes-explained-simply-e9cb9eaa49aa)
 - [understanding prototype](https://bytearcher.com/articles/understanding-prototype-property-in-javascript/)
 - awesome site: JS docs
     - [part 1](https://felix-kling.de/jsbasics/#/11): What exactly is a prototype?
     - [part 2](https://felix-kling.de/jsbasics/#/12): What does a prototype do?

## The `new` keyword in javascript
 - [What is the `new` keyword in JavaScript?](https://stackoverflow.com/a/3658673/6021740)
 - [mdn - doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new)
 - [Against `new` keyword](https://stackoverflow.com/a/4550435/6021740)
