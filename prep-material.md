===

# JSON and APIs

[JSPERF: Document fragment vs innerHTML vs looped appendChild](https://jsperf.com/document-fragment-vs-innerhtml-vs-looped-appendchild/2)

[JavaScript Fetch API and using Async/Await](https://dev.to/shoupn/javascript-fetch-api-and-using-asyncawait-47mp)

write both `.catch` and `.then` methods for all the promises.  
If something needs to be done in both the cases use `.finally`

---

## API

existing:  
https://github.com/CTEC3905/07-lab-json-ajax/blob/master/javascript/xmlhttp.js

===

# JAVASCRIPT BEST PRACTICE **01**

here's an excellent guide to [JavaScript Best Practices (W3.org)](https://www.w3.org/wiki/JavaScript_best_practices)

one example of [using shortcut notation](https://www.w3.org/wiki/JavaScript_best_practices#use-shortcut-notation-when-it-makes-sense):

```js
if(v){
  var x = v;
} else {
  var x = 10;
}

// The shortcut notation uses the double pipe character:
var x = v || 10;
// x equals v, if v is empty x equals 10
```

"It is amazing how many times you will build a massively convoluted JavaScript solution for a problem that can be solved easily without it."

---

# JAVASCRIPT BEST PRACTICE **02**

[Optimize loops](https://www.w3.org/wiki/JavaScript_best_practices#Optimize_loops) for speed. A common mistake is to make JavaScript read the array length **every time**:

```js
// given an array:
const names = ['Eazy-E', 'Dr. Dre', 'Ice Cube' ];

// we can time how long it takes
console.time();
for(let i=0;i<names.length;i++){
  console.log(names[i]);
}
console.timeEnd();
```

0.26123046875ms

instead, **store the length** in a variable:

```js
console.time();
const all = names.length;
for(let i=0;i<all;i++){
  console.log(names[i]);
}
console.timeEnd();
```

Faster: 0.197021484375ms

---

# JAVASCRIPT BEST PRACTICE **04**

[Keep DOM access to a minimum](https://www.w3.org/wiki/JavaScript_best_practices#Keep_DOM_access_to_a_minimum)

> keep computation-heavy code—including **regular expressions** and **DOM manipulation**—outside loops
---

# JAVASCRIPT BEST PRACTICE **05**

[Keep DOM access to a minimum](https://www.w3.org/wiki/JavaScript_best_practices#Keep_DOM_access_to_a_minimum)

> keep computation-heavy code—including **regular expressions** and **DOM manipulation**—outside loops
>
> …create DOM nodes in the loop but insert them into the document *outside the loop*.
>
> Instead of constantly creating and applying elements, create a **tool function** that **turns a string into DOM elements** to call at the end of your content generation process—disturb browser rendering once rather than frequently.

---

# JAVASCRIPT BEST PRACTICE **06**

> …avoid taking the easy path. JavaScript is a wonderfully versatile language and … the environment it is executed in is very forgiving and it is easy to *write sloppy code* that seemingly does the job. This same code however will **come back to bite you** a few months down the line.
>
> JavaScript development has mutated from a fringe knowledge area to an **absolute necessity** if you want to **have a job as a web developer**.

[From JavaScript Best Practices (W3.org, Christian Heilmann)](https://www.w3.org/wiki/JavaScript_best_practices#Summary)

===

## DESTRUCTURING OBJECT/ARRAYS

```js
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};

const { today: { low: lowToday, high: highToday }} = LOCAL_FORECAST;

console.log(lowToday); // 64
console.log(highToday); // 77
```

```js
let a = 8, b = 6;

[b, a] = [a, b]; // b = 8, a = 6
```

```js
const source = [1,2,3,4,5,6,7,8,9,10];
function removeFirstTwo(list) {
  "use strict";
  const [, , ...arr] = list;
  return arr;
}
const arr = removeFirstTwo(source);
console.log(arr); // should be [3,4,5,6,7,8,9,10]
console.log(source); // should be [1,2,3,4,5,6,7,8,9,10];
```

```js
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};
const half = ({ max, min }) => (max + min) / 2.0;
console.log(stats); // object
console.log(half(stats)); // 28.015
```

---

## CREATING OBJECTS

```js
const createPerson = (name, age, gender) => {
  return { name, age, gender };
};
console.log(createPerson("Zodiac Hasbro", 56, "male")); // creates new object
```

---

## FOR…OF and FOR…IN

```js
// `for...in` iterates over properties of an object in arbitrary order
// use `forEach()` or `for...of` to preserve order
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in
const result = {
  success: ["max-length", "no-amd", "prefer-arrow-functions"],
  failure: ["no-var", "var-on-top", "linebreak"],
  skipped: ["id-blacklist", "no-dup-keys"]
};
function makeList(arr) {
  const newArr = [];
  for (const n in arr) { newArr[n] = `${arr[n]}` };
  return newArr;
}
makeList(result.failure); // ["no-var", "var-on-top", "linebreak"]

for (const n of result.skipped) { console.log(n) }
// id-blacklist
// no-dup-keys

for (const n in result.skipped) { console.log(`${n} is ${result.skipped[n]}`) };
// 0 is id-blacklist
// 1 is no-dup-keys
```

---

## REDUCE

```js
let sum = [ 1, 2, 3 ].reduce(
  (accumulator, currentValue) => accumulator + currentValue, 0)
console.log(sum) // 6
```

===

## JS MEMORY LEAKS

Addy Osmani https://nolanlawson.com/2020/02/19/fixing-memory-leaks-in-web-applications/amp/

===

## Planning your site 01

gather all the **content** for your site:

- images
- movies
- text (see [Writing for the Web](https://www.usability.gov/how-to-and-tools/methods/writing-for-the-web.html))
- audio
- choosing data from APIs

---

## Planning your site 02

arrange your content into *logical groups*

**THINK:** will a group be **limited** or get **more content**?

this is the basis for your site structure, **navigation** and **menu**

Resources from [usability.gov](https://www.usability.gov/):

- [Content Strategy Basics](https://www.usability.gov/what-and-why/content-strategy.html)
- [Content Inventory](https://www.usability.gov/how-to-and-tools/methods/content-inventory.html)
- [Information Architecture](https://www.usability.gov/what-and-why/information-architecture.html)

---

## Planning your site 03

get input from others with an online tool:

[Online card sorting software](https://www.optimalworkshop.com/optimalsort): [free plan](https://www.optimalworkshop.com/register)

- [Card Sorting (usability.gov)](https://www.usability.gov/how-to-and-tools/methods/card-sorting.html)

---

## Planning your site 04

at the next stage, you will use **HTML5 tags** to **mark up** the basic areas for:

- each **kind** of page you have or...
- for one long **scrolling** page

---

## Planning your site 05

inside the `body` tag, use **HTML5 semantic tags** ([read more at W3Schools](https://www.w3schools.com/html/html5_semantic_elements.asp)) for **overall structure**

- `header` (optional but advised)
- `nav`
- `main`
- `footer` (optional)

*avoid div tags* and don't make up tags!

HTML5 semantic tags for **content** come later

===


<!-- CSS VARIABLES -->

# CSS VARIABLES **01**
<!-- .slide: class="smalltext crammed" -->
  
Being a style language based on key-value pairs, for a long time CSS had no variables. [LESS](http://lesscss.org/) and [Sass](https://sass-lang.com/) filled the gap and added other functionality, some of which is being **added to the CSS standard**

CSS **custom properties** are one example and are **usable in all modern browsers**. They **differ from LESS/Sass variables** (`@` and `$`) by being prefixed with “`--`” e.g. `--myPink: #fce;`

They are **scoped** to the **selector** in which they are defined, and inherited by the **descendants** of that selector

---

# CSS VARIABLES **02**
Because of this scope, the `:root` pseudo-element is often used in examples as a “global” selector…

```CSS
:root {
  --darkGreen: #051;
  --myPink: #fce;
}

main {
  color: var(--darkGreen);
  background: var(--myPink);
}
.my-class {
  border-color: var(--myPink);
}
```

SVG graphics need the variables at `:root` as they have their own DOM

---

# CSS VARIABLES **03**

…however, **any selector** (element, class, id) can be used to set **CSS Custom Properties** (not just `:root`) - you can then access them in **all child elements** of that selector

So CSS variables in `html` or `body` also mean that **any element** in your CSS file has access to them…

```CSS
body {
  --darkGreen: #051;
}

.my-class {
  color: var(--darkGreen);
}
```

---

# CSS VARIABLES **04**
<!-- .slide: class="crammed" -->

Elements **outside** the variable **selector** which contains the variables **cannot access them**:

```html
&lt;main>main content&lt;/main>
&lt;footer>footer content&lt;/footer>
```

```CSS
main {
  --darkGreen: #051;
}

footer {
  color: var(--darkGreen);
  /* OOPS: cannot see the variable in “main” */
}
```

---

# CSS VARIABLES **05**
<!-- .slide: class="crammed smallcode" -->

**store** an **attribute value** once, then **use elsewhere**:

```css
/* set the variables in a root element */
html {
  --myWidth: 360px;
  --myBorder: 4px solid var(--myPink);
  --codeFont: "Courier New", monospace;
}

/* use the variables anywhere */
section {
  border: var(myBorder);
}
figure {
  width: var(--myWidth);
}
code {
  font-family: var(--codeFont);
}
```

---

# CSS VARIABLES **06**
<!-- .slide: class="crammed smallcode" -->

For responsive design, you can **reset custom properties inside `@media` queries**. For example, you could **expand the margin** around major layout elements for **wider screen widths**:

```css
:root {
  --gutter: 4px;
}

section {
  margin: var(--gutter);
}

@media (min-width: 600px) {
  :root {
    --gutter: 16px;
  }
  /* this change is only activated above 600px */
}
```

---

# CSS VARIABLES **07**
<!-- .slide: class="crammed" -->
  
Resources:

- [CSS Variables: Why Should You Care?](https://developers.google.com/web/updates/2016/02/css-variables-why-should-you-care)
- [Using CSS custom properties (variables) (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_variables)
- [Browser support for CSS variables (Can I Use)](https://caniuse.com/#feat=css-variables)

<!-- END CSS VARIABLES -->

===

# QUESTIONNAIRE

one:

```js
if(condition){
  do stuff;
} else {
  do other stuff;
}
```

two:

```js
if(condition){
  do stuff;
}
else {
  do other stuff;
}
```

===

<!-- CODE COMEDY -->

<section data-markdown class="big-pic small-head crammed">
![Do I know it or do I say I know it???](images/two-types-cv.jpg)
</section>

===

