<!-- outline

Intro (5 minutes)
  * what this talk is and isn't (pat)
  * dont be overwhelmed (pat)
  * you are technically minded enough to learn this (john)

JavaScript is fun (and useful!)
Variables and Objects (5 minutes. jg)
operators
Arrays
loops
Functions (5 minutes, jg)

Closures and `this` (5 minutes, pat)
Async (5 minutes, pat)
Local Dev Environment, Install node, http-server, start a local server serving a basic html page (CDN) and an external script (5 minutes, jg) https://momentjs.com/docs/#/displaying/from/
The DOM and Browser Development (5 minutes, pat)
Debugging (5 minutes, pat)
Modules / libraries (5 minutes, pat)
Walk through a few JS API samples (5 minutes, jg) (with event and promise)
The JavaScript Ecosystem (5 minutes, pat)
A note about ES 2015 (pat)
“Opinions” About JavaScript (5 minutes, pat)
Resources to Keep Learning (2 minutes, jg)

https://twitter.com/hoverbird/status/750826785781063680
https://twitter.com/thomasfuchs/status/708675139253174273?lang=en

how can we help GIS folks identify?

variables pointing at something else - red exclamation points in .MXDs
strings, integers, booleans - datatypes for feature class attribute columns
conditional operators = field calculator / definition expressions

functions accepting arguments - gp tools with input parameters
asynchronous = background geoprocessing

project dependencies - ArcMap license level? (yuck)
dev Environment
  ArcMap
  ArcCatalog
  online documentation

opinions - GIS folks definitely know about those
 which projection is the best?
 back in the day

-->

<!-- .slide: data-background="../template/img/2019/devsummit/bg-1.png" -->

<!--div style="margin: auto; padding-top: 50px; padding-bottom: 50px; width: 80%; background: rgba(30,30,30,0.9)"/-->

<h1 style="text-align: left; font-size: 80px;"><b>JavaScript</b> <i>for Geographers</i></h1>
    <p style="text-align: left; font-size: 1.5em;">Patrick Arlt &amp; Allison Davis</p>
    <p style="text-align: left; font-size: 1.5em;">Slides: <a href="http://bit.ly/2T4zaKJ">http://bit.ly/2T4zaKJ</a>

<aside class="notes">

these are my notes!

</aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## Agenda

1. Fundamentals
2. <span style="white-space: nowrap;">Patterns</span>
3. Put it to use
4. Fatigue

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## JS can be overwhelming, but you're more equipped than you think!

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## declaring [variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)

```js
var dog;

> undefined

// new
let nifty;
const notGonnaChange;

> undefined
```

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## defining values

```js
var dogName = 'spot';

var age = 21;

var canBark = true;

```
value type is **not** explicitly declared
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [arithmetic](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators) operators

```js
(age / 7) // 3

5 + 5 // 10

3 - 2 // 1

3 * 2 // 6
```

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [arithmetic](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators) operators

```js
12 % 5 // 2 (modulus)

var x = 5;
x++ // 6

var y = 3;
y-- // 2

'foo' + 'bar' // 'foobar'
```

   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [comparison](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators) - operators

```js
3 === 3   // true
3 === '3' // false

'foo' != 'bar' // true

3 > 2 // true
3 >= 2 // true
```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [logical](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_Operators) operators
```js
// logical 'and'
true && anotherTruthy
> true

// 'or'
true || somethingFalsy
> true

// 'not'
!somethingTruthy
> false
```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
```js
var dogs = ['Spot', 'Lassie'];

dogs[0] // 'Spot'

dogs.push('Fido');

dogs.length // 3
```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

```js
function dogYears(age) {
  return age * 7;
}

dogYears(3);
> 21
```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## anonymous functions
```js
function () {
  return 2*2;
}
```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [arrow](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) functions
```js
function (age) {
  return age*2;
}
// ===
age => {
  age*2;
}
// ===
age => age*2;

```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

```js
let dog = {
  age: 7,
  canBark: true,
  _ssshhh: 'top secret'
}

> Object {age: 7, canBark: true, _ssshhh: 'top secret' }

```

   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

```html
<script src="./doglibrary.js"></script>
```

```js
let spot = new Dog()

> Object { canBark: true }

spot.age = 21;
```

   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## objects - methods

```
// Buffer point by 1000 feet
var ptBuff = geometryEngine.buffer(point, 1000, "feet");
```
   <aside class="notes">
     methods == functions!
   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## [for](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for) loops

```js
for (var i = 0; i < 6; i++) {
   console.log(i);
}

> 0
> 1
> 2
> 3
> 4
> 5
```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## looping through an array

```js
var dogs = ['Spot', 'Lassie', 'Fido'];

for (var i = 0; i < dogs.length; i++) {
   console.log(dogs[i]);
}

> 'Spot'
> 'Lassie'
> 'Fido'
```
   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## JavaScript is _Asynchronous_

* JavaScript is _single threaded_
* Only does 1 thing at a time
* Lots of things might happen at once
* This is the "Event Loop"

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## JavaScript Event Loop

1. Executes one function at a time
2. <span style="white-space: nowrap;">Run the entire function</span>
3. Start the next function

[Demo](http://jsbin.com/bezusuk/edit?js,console)

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## Callbacks

```html
<button id="button">Click Me!</button>
```

```js
let button = document.getElementById('button');

button.addEventListener('click', function () {
  console.log('The button was clicked');
});
```

Callback are functions that are called when things happen.

[Demo](http://jsbin.com/qovotex/edit?html,js,console,output)

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## Promises

```js
let user = fetch('https://randomuser.me/api/')
  .then(processResponse)
  .then(doSomethingWithUser)
  .catch(anyErrors);

function processResponse (response) {
  return response.json();
}

function doSomethingWithUser (user) {
  console.log(user); // prints a bunch of user info
}

function anyErrors (error) {
  console.error('what have you done!', error);
}
```

Promises represent a future value that will be "resolved".

[Demo](http://jsbin.com/qisiki/edit?js,console)

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## Function Scope

```
var message = 'Hello World!';

function go () {
  console.log(message);
}

go();
```

When functions are called they remember the variables around them, this is refered to as "lexical scope".

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## What is `this`?

```js
var user = {
  firstName: "Casey",
  lastName: "Jones",
  fullName: function () {
    console.log(this.firstName + " " + this.lastName);
  }
}

person.fullName() // > Casey Jones
```

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## What is `this`?

The value of `this` depends on how the function was called.

[Demo](http://jsbin.com/rowofi/edit?js,console)

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## lets set up a JS development environment

* [do i have a web server running?](https://gist.github.com/jgravois/5e73b56fa7756fd00b89)
* [`demo.html`](https://github.com/jgravois/presentations/blob/12ad63798193bd32950809996c9825067a742aa7/devsummit/2017/js/snippets/demo.html)
   <aside class="notes">
     good time to talk about CDNs
   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## debugging

Get familiar with your dev tools!

* `console.log` - print things to the console
* `debugger` - stops the application so you can look around

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## the DOM

* select elements
* listen for events
* change elements

[A simple form](http://jsbin.com/qojodez/edit?html,js,output);
[Finished example](http://jsbin.com/viconot/edit?html,js,output);

---



<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## sharing JavaScript - modules

As applications grow it is helpful to divide code into different files to organize. You can just use `<script>` tags for small apps.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## ES2015 Modules

```
import { something } from 'some-module';
```

This is the future as you learn JavaScript you will encounter this more often.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## AMD Modules (JS API)

```
require([
  "esri/Map",
  "esri/views/MapView",
], function (Map, MapView) {
  // Map and MapView have been loaded!
});
```

`require` is a fancy way of adding `<script>` tags to load code on demand.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## lets put all this to use!

* [../sample-code/tasks-query/](https://developers.arcgis.com/javascript/latest/sample-code/tasks-query/index.html)
* [../sample-code/chaining-promises/](https://developers.arcgis.com/javascript/latest/sample-code/chaining-promises/index.html)

   <aside class="notes">
     step through a JSAPI sample
   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## The JavaScript Language</small>

Updates every year (ES2015, ES2016, ES2017).

2015 had LOADS of new featues.

2017 had ~2 new features.

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## the JavaScript ecosystem

* Module Formats - CommonJS, **AMD**, **ES 2015**
* Compilers - Babel, **TypeScript**
* Bundlers - Rollup, **WebPack**, SystemJS
* Minifiers - UglifyJS

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## the JavaScript ecosystem

You don't know what you don't know.

<p class="fragment">and that is great.</p>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## JavaScript Fatigue

> Look, it’s easy. Code everything in Typescript. All modules that use Fetch compile them to target ES6, transpile them with Babel on a stage-3 preset, and load them with SystemJS. If you don’t have Fetch, polyfill it, or use Bluebird, Request or Axios, and handle all your promises with await.

> We have very different definitions of easy.

[How it feels to learn JavaScript in 2016](https://hackernoon.com/how-it-feels-to-learn-javascript-in-2016-d3a717dd577f#.sl06jvo9z)

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## Fight JavaScript Fatigue

* The JS API is MORE then enough for simple apps
* Add tools when you **KNOW** you will benefit from using them
* Too many tools === Lots of complexity to manage

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-2.png" -->

## learn more!

* [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS)
* [MDN: Learn web development](https://developer.mozilla.org/en-US/docs/Learn)
* [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
* [Eloquent JavaScript](http://eloquentjavascript.net/)
* http://wesbos.com/

   <aside class="notes">

   </aside>

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-esri.png" -->

<br><br><br><br><br><br>

Slides at http://bit.ly/2T4zaKJ

---

<!-- .slide: data-background="../template/img/2019/devsummit/bg-rating.png" -->
