# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->
## **Front-End Web Development**
### Lecture 03

===

# STAFF CONTACTS
<!-- .slide: class="crammed smalltext" -->

**Module leader:**

General queries and admin issues:

**Graeme Stuart**: gstuart@dmu.ac.uk

<hr>

**Tutors**

- Labs: **Graeme Stuart**: gstuart@dmu.ac.uk
- Labs: **Fania Raczinski**: fania.raczinski@dmu.ac.uk
- Lectures: **Dave Everitt**: deveritt@dmu.ac.uk

**Tutor contact outside classes is strictly by email**

===

# RATIONALE

- **No JQuery or CSS frameworks** (e.g. Bootstrap)—it’s impossible to mark the resulting sites as **independent code**
- Some tools are widespread in industry, but it’s important to **understand the core languages**
- this avoids **over-dependence on poorly understood 3rd-party code** ([JQuery source code](https://github.com/jquery/jquery/blob/master/src/core.js "JQuery source code is… JavaScript") is… JavaScript).
- you can gain a **solid foundation in the languages** from lab and lecture code

===

# JAVASCRIPT TEACHING: **1**
<!-- .slide: class="smalltext" -->

## There's a **lot** to learn

This is **not a dedicated JavaScript** module so instead we:

- get you started with the **fundamentals**
- highlight **good practice** with examples
- supply exercise code you can **experiment** with
- provide curated links to **online learning** materials  
- provide an **overview** of the current state of JS
- **we won't cover**: Node, Web Sockets, JQuery, Bootstrap…

---

# JAVASCRIPT TEACHING: **2**

## **VARIOUS** SKILLS/INTERESTS, **THE PLAN**

1. build on the **lab and lecture examples**
3. make **working examples** to re-use in your project
4. build up a set of **re-usable js code** on GitHub 

---

We can't do detailed `code-fixing` in labs or by email  
The real learning process **is debugging/researching**

---

# JAVASCRIPT TEACHING: **3**

- After the JavaScript basics, **follow your interests**
- **Keep things simple**, make **one thing** work well first
- Work out **how to use JavaScript** in your project:  
it can be practical/functional or a bit clever
- check the **browser console** (f12) for errors
- always **validate your HTML** as you develop!

---

Check **dates** to avoid **old/bad code** on the web:  

- ~~`var`~~ -> `let/const`
- ~~`onclick`~~ -> `addEventListener()`

===

## **`JavaScript !== Java;`**

this deserves its own %$@**& slide…

===

# JAVASCRIPT **HISTORY**: 01
<!-- .slide: class="smalltext" -->

- **created in 10 days** in May **1995** by [Brendan Eich](https://brendaneich.com/), then at Netscape (now Mozilla). Original name **Mocha**, chosen by [Marc Andreessen](https://en.wikipedia.org/wiki/Marc_Andreessen), founder of [Netscape](https://www.engadget.com/2014/05/10/history-of-netscape/).
- In 1995 the name became **LiveScript** then, after a trademark license from [Sun](https://www.oracle.com/sun/) it became **JavaScript**—a **marketing move** as Java was then a popular way of running applets in browsers.

**Beginners** still **confuse** the two languages.

<small>[A Short History of JavaScript (W3C)](https://www.w3.org/community/webed/wiki/A_Short_History_of_JavaScript)</small>

---

# JAVASCRIPT **HISTORY**: 02
<!-- .slide: class="smalltext" -->

- **1995:** JavaScript created in 10 days as “Mocha”
- **1997:** ECMAScript standard established ([see ECMA](http://www.ecma-international.org/ "Standardization of Information and Communication Technology and Consumer Electronics: an international private (membership-based) non-profit standards organization for information and communication systems"))
- **1999:** ES3 - Microsoft discover www. IE5 everywhere.
- **2000–2005:** [XMLHttpRequest](https://hpbn.co/xmlhttprequest/) (AJAX): Outlook Web Access (2000), Gmail (2004), Google Maps (2005)
- **2009:** ES5 - established JavaScript, and standard [JSON](http://www.w3schools.com/js/js_json_intro.asp "JSON: the nice introduction")
- **2015:** ES6/ECMAScript2015 - some is syntactic sugar, no firm agreement on anything more radical yet
- **NOW:** [ES7/ECMAScript2016](http://exploringjs.com/es2016-es2017/ "Dr. Axel Rauschmayer is a trusted source on JavaScript") - go no further!

Reference: [benmccormick.org](https://benmccormick.org/2015/09/14/es5-es6-es2016-es-next-whats-going-on-with-javascript-versioning/) (2015)

---

# JAVASCRIPT **HISTORY**: 03

**JavaScript** is an *implementation* of **ECMAScript**

[ActionScript](http://www.adobe.com/devnet/actionscript.html "Remember Flash? And Adobe AIR") is/was another (["whatever happened to ES4?"](http://www.mikechambers.com/blog/2008/08/14/actionscript-3-and-ecmascript-4/ "YAWN. The whining."))

## The **ECMA standards** (PDFs):

- [The ECMA-262 6th Edition / June 2015](http://www.ecma-international.org/ecma-262/6.0/ECMA-262.pdf)
- [The ECMA-262 7th Edition / June 2016](http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-262.pdf)
- [The ECMA JSON standard](http://www.ecma-international.org/publications/files/ECMA-ST/ECMA-404.pdf)

---

# JAVASCRIPT **HISTORY**: 04
<!-- .slide: class="crammed smalltext" -->

## ES6: JavaScript in **transition**

e.g. [`promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise "ext: example shows multiple fast clicking"),
[`const`](https://blog.mariusschulz.com/2015/12/31/constant-variables-in-javascript-or-when-const-isnt-constant "ext: why const is not for constant values"),
[`let`](https://davidwalsh.name/for-and-against-let "ext: for and against let"),
[`modules`](http://exploringjs.com/es6/ch_modules.html#sec_basics-of-es6-modules "ext: really good chapter on modules"), … 

~~**ES5** concatenation:~~
```javascript
var name = 'My name is ' + first + ' ' + last + '.'
```
**ES6** template Literals (interpolation). Note *backticks*:
```javascript
let name = `My name is ${first} ${last}.`
```

See [ES6 browser support (TL;DR warning: BIG table!)](http://kangax.github.io/compat-table/es6/)

===

# JS **HOW IT WORKS**: 1
<!-- .slide: class="crammed smalltext" -->

- translated into **machine instructions** by the **syntax parser**
- creates a **global execution context** in the browser window…
- …with `window` as the global object and `this` as a special variable
- runs in an **[event loop](#/5/5)** to check if **user events** need **action**

**global**: not in a function, available **everywhere in a window**

---

Even with an empty browser tab (or blank .js file) e.g. type `this.innerWidth;` into an empty browser console

---

# JS **HOW IT WORKS**: 2
<!-- .slide: class="crammed smalltext" -->

1. builds an **execution stack** to handle your code
2. executes your code **synchronously** (one thing at a time)
3. the browser adds user events (e.g. click) to an **event queue**
4. if the **execution stack** is empty…
5. …JavaScript **checks** the event queue for **actionable events**

---

The browser does things *asynchronously* (**rendering the page**, making **HTTP calls**, storing **user events** in the queue…) while JavaScript handles things *synchronously*…

…except for `async` (see [js Goes Async](https://www.sitepoint.com/javascript-goes-asynchronous-awesome/) and [MDN/async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function))

---

# JS **HOW IT WORKS**: 3
<!-- .slide: class="crammed smalltext smallcode" -->

- you use it to access the **Document Object Model** (DOM)
- you **make changes** and **get information** from the DOM

Example:

```css
a.highlight {
  background: yellow;
}
```
```js
const myLinks = document.getElementsByTagName('a');

for(let i=0; i < myLinks.length; i++){
  myLinks[i].classList.add("highlight");
}

```

See [Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction "Mozilla Web Docs")

---

# JS **HOW IT WORKS**: 4
<!-- .slide: class="float-l-img" -->

![](dom/dom-model.svg)
<object data="https://raw.githubusercontent.com/front-end-materials/images/master/dom/dom-model.svg"></object>
<object data="dom/dom-model.svg" type="image/svg+xml">
  <img src="dom/dom-model.svg" />
</object>

The first few branches on a **Document Object Model** (DOM) tree

There are **parent**, **child** and **sibling** nodes

From: [Document Object Model Structure](http://www.corelangs.com/js/dom/domtree.html) (corelangs.com)

---

## JS **HOW IT WORKS**: 5

![Document Object Model diagram with hand-drawn annotations](dom/dom.png "From a JQuery course http://cs.wellesley.edu/~cs110/reading/DOM-JQ.html")

---

# JS **HOW IT WORKS**: 6

## THE BROWSER EVENT LOOP

In a browser, everything runs in an **event loop** so you use **event listeners** to errr… **listen** for **events** triggered by the **user** or **other processes**:

``` javascript
myElement.addEventListener("click", MyFunction);
```

---

While **CSS** can be triggered by focus/hover/etc.  
**JavaScript** can listen for **hundreds** of events.

See: [Web Event reference (MDN)](https://developer.mozilla.org/en-US/docs/Web/Events)

---

# JS **HOW IT WORKS**: 7
<!-- .slide: class="crammed" -->

## How is JavaScript used?

- form **validation** of user input
- handling **data** (e.g. **JSON**)
- interactive **user interfaces** and feedback
- web-based **apps** (mobile and desktop)
- web and mobile **frameworks**
- **applications** built on web technologies
- **games** with HTML5 canvas ([HTML5 Games website](http://html5games.com/Best/702b9531-c136-437a-ab97-0b209d893b55))
- **[3D animations](https://tutorialzine.com/2013/09/20-impressive-examples-for-learning-webgl-with-three-js)** with canvas and WebGL e.g. [cars](http://carvisualizer.plus360degrees.com/threejs/), [Aquarium](http://webglsamples.org/aquarium/aquarium.html)

===

# JAVASCRIPT SYNTAX: **1**

## Blank console in Chrome:

- type `about:blank` in the address bar
- type in JavaScript and **try things** out
- **shift-return**: new line without executing

---

A demo, if there's time…

![console log for experimenting with JavaScript](general/chrome-about-blank.png)

---

# JAVASCRIPT SYNTAX: **2**
<!-- .slide: class="smallcode" -->

## **C-FAMILY** STYLE SYNTAX

familiar if you've used C-family languages:

``` javascript
const myArray = ["Julia", "C++", "Ruby", "R", "Go", "Python", "Rust"];

// These are not all C-family languages!
```
[Array methods (W3Schools)](http://www.w3schools.com/js/js_array_methods.asp)

---

# JAVASCRIPT SYNTAX: **3**

## DYNAMIC TYPING

- 6 **primitive types** (not objects):  
  `undefined`, `null`, `boolean`, `number` (always a float), `string`, [`symbol` (ES6)](https://docs.microsoft.com/en-us/scripting/javascript/reference/symbol-object-javascript "For creating a unique identifier for object properties")
- JavaScript **works out the type** for a variable value
- you can change a `let` value from **one type to another**

---

# JAVASCRIPT SYNTAX: **4**
<!-- .slide: class="crammed smallcode" -->

### VARIABLES (`var`), `let`, `const`

```javascript
let greet, helloUser; // initialise two variables
greet = "hello";  // assign a value
let userInput = // get user input from the DOM  
helloUser = `Oh, ${greet} ${userInput}`;

let myVar = // can be: string, number, boolean
const myVar = // can be: array, object, function…

myVar === myVar01; // true if the same
myVar !== myVar01; // true if different
```

`const` can store an **immutable type** (e.g. array, function), the **elements** or **properties** of which can change.

We will see that `let` has **tighter scope** than `var`…

---

# JAVASCRIPT SYNTAX: **5**
<!-- .slide: class="crammed smalltext smallcode" -->

## VARIABLE scope: **var** and **let**

```javascript
function demoLet() {
  //tuce is *not* visible out here
  for( let tuce = 0; tuce < 5; tuce+=1 ) {
    //tuce is only visible in here (in the for())
  }
  //tuce is *not* visible out here
}
function demoVar() {
  //nish *is* visible out here
  for( var nish = 0; nish < 5; nish++ ) {
    //nish is visible to the whole function
  }
  //nish *is* visible out here
}
```
[…difference between using “let” and “var” to declare a variable?](http://stackoverflow.com/a/11444416/123033)

---

# JAVASCRIPT SYNTAX: **6**
<!-- .slide: class="smallcode" -->

## FUNCTIONS

function **declaration** || **expression** (as a `const` variable):

```javascript
function multiplyNums(x, y) {
  return x * y;
} // function declaration

// function expression (as an arrow function)
const multiplyNums = (x, y) => x * y;
```

Nearly everything in JavaScript is an **object**, including functions which can be used _as variables_ **including function call parameters**. ([MDN functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions))

---

# JAVASCRIPT SYNTAX: **7**
<!-- .slide: class="smallcode" -->

## **ARROW** FUNCTIONS: **COMPACT**

```javascript
const multiplyNums = (x, y) => x * y;

const square = x => multiplyNums (x, x);
square(8);

const squares = [1,2,3,4,5];
squares.map(num => square(num));
// [1, 4, 9, 16, 25] much better than a for loop!
```

…so you can use **function composition**, with **pure functions** (same input \> same output, self-contained).

[MDN arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

---

# JAVASCRIPT SYNTAX: **8**

## **PURE** FUNCTIONS: **COMPACT** AND **SAFE**

```javascript
const hexagrams = square(8); // hexagrams is 64

console.log(`I Ching: always ${hexagrams} hexagrams!`);
// I Ching: always 64 hexagrams!
```

A pure function with **parameters** in a template literal:

```javascript
console.log(`This is not a ${square(4)}-bit laptop!`);
// This is not a 16-bit laptop!
```

---

# JAVASCRIPT SYNTAX: **9**
<!-- .slide: class="smallcode" -->

## **GENERATOR** FUNCTIONS\*

Example: a simple counter limiter:

```javascript
function* count () {
  let index = 1;
  while (index < 4) {
    yield index++;
  }
}
const upTo3 = count();

upTo3.next(); // value: 1, done: false
upTo3.next(); // value: 2, done: false
upTo3.next(); // value: 3, done: false
upTo3.next(); // value: undefined, done: true
```

---

# JAVASCRIPT SYNTAX: **10**
<!-- .slide: class="crammed smallcode" -->

## JavaScript [Math](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Math "Moxilla Developer Netwrork detailed JS Math Reference") Object e.g.

```javascript
Math.round(4.5); // 5
Math.pow(8,2); Math.sqrt(64); // 64, 8
Math.abs(-4.7); // 4.7
Math.ceil(4.4); Math.floor(4.7); // 5, 4
Math.max(0, 150, 30, 20, -8, -200); // 150 (and min)
Math.random(); // a float from 0 to (almost) 1
Math.floor(Math.random() * 10); // number between 0 and 9
```

if you get `NaN` and you (know/want/think it is) a number:  
```javascript
parseFloat(aFloatYouThink); parseInt(AnIntegerYouThink);
```

Read W3Schools: [JavaScript Math Reference](http://www.w3schools.com/jsref/jsref_obj_math.asp),  
[JavaScript Number Methods](http://www.w3schools.com/js/js_number_methods.asp), 
[JavaScript Type Conversion Table](http://www.w3schools.com/jsref/jsref_type_conversion.asp)

---

# JAVASCRIPT SYNTAX: **11**
<!-- .slide: class="crammed smallcode" -->

### Array **[…]**

'array literal' - create and populate:

```javascript
const myArray = [1, 2, "free",  multiplyNums(8, 8)];
myArray[3]; // 64
```

**No comma** after the **last element**!

```javascript
myArray[3] = multiplyNums; // no parameters
myArray[3](2, 2); // 4
```

**omit trailing brackets()** in functions with **no parameters** when inside an array - you can pass them later

---

# JAVASCRIPT SYNTAX: **12**
<!-- .slide: class="smallcode smalltext" -->

### OBJECT **{…}** (ASSOCIATIVE ARRAY)

Contains **key value** pairs. This is declared as an 'object literal':  

```javascript
const myObject = {key1: 64, key2: "text"};
```

Access/change: **square brackets** or **dot** (property) syntax:
```javascript
alert(myObject['key2']); // [] syntax… but dot is best:
alert(myObject.key2); // key2 is a property of myObject
myObject.key2 = 'More text'; // change the value of key2
```

add a new key/value pair:  
```javascript
myObject.key3 = Math.PI;
```

---

# JAVASCRIPT SYNTAX: **13**
<!-- .slide: class="smallcode" -->

**Object keys** _look_ like names (as in variables), but *keys are strings*, which allow expressions such as:

```javascript
let myKey = 2;

console.log(myObject["key"+myKey]);
console.log(myObject["key"+2]);
console.log(myObject["key2"]); // same as both above
```

Key strings (as in **JSON**) mean JavaScript loose typing turns `"key"+2` to `"key"+"2"`, evaluating to the string `"key2"`

```javascript
const myObject = {
  "key1": 64,
  "key2": "text"
};
```

---

# JAVASCRIPT SYNTAX: **14**

## conditionals

```javascript
if (condition is true) {
  // do stuff once here
}
```

```javascript
if (condition is true) {
  // do stuff
} else {
  // condition is false, do other stuff
}
```

---

# JAVASCRIPT SYNTAX: **15**

## LOOPS **1** (FOR)
```javascript
for (counter; condition; increment/decrement) {
  // do stuff using the counter
}
```

```javascript
for (let i = 0; i < myArray.length; i += 1) {
  console.log(myArray[i]);
}
```

…but `map` with an **anonymous function** is cleaner:

```javascript
myArray.map(i => console.log(i));
```

---

# JAVASCRIPT SYNTAX: **16**

## LOOPS **2** (WHILE)

```javascript
while (condition is true) {
  // do stuff until it's false
}
```

or

```javascript
do {
  // some stuff at least once, then…
}
while (condition); // …do it again IF condition is true
```

---

# JAVASCRIPT SYNTAX: **17**

## SWITCH/CASE

```javascript
switch (new Date().getDay()) {
  case 6:
    text = "Today is Saturday";
  break; 
  case 0:
    text = "Today is Sunday";
  break; 
  default: 
    text = "Looking forward to the Weekend";
}
```

[W3Schools switch statment](http://www.w3schools.com/js/js_switch.asp)

---

# JAVASCRIPT SYNTAX: **18**
<!-- .slide: class="crammed smalltext smallhead" -->

## **OBJECT**===ES6 **CLASS**  
  (+SYNTACTIC SUGAR)

> JavaScript uses a **prototypal inheritance model** with **object prototypes** as "classes". New objects inherit methods and attributes of their parent object through the prototype chain. It’s possible to modify an object’s prototype at any time, making JavaScript very flexible and dynamic.

[ES6 classes and JavaScript prototypes (Sebastian Porto)](https://reinteractive.com/posts/235-es6-classes-and-javascript-prototypes)  
**But** [Think twice about ES6 classes (Christian Alfoni)](http://christianalfoni.github.io/javascript/2015/01/01/think-twice-about-classes.html)

===

# TO BE CONTINUED…

The next lecture will continue **JavaScript syntax**, with some examples
