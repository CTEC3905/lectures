===

# JSON and APIs

existing:  
https://github.com/CTEC3905/07-lab-json-ajax/blob/master/javascript/xmlhttp.js

[JSPERF: Document fragment vs innerHTML vs looped appendChild](https://jsperf.com/document-fragment-vs-innerhtml-vs-looped-appendchild/2)

[JavaScript Fetch API and using Async/Await](https://dev.to/shoupn/javascript-fetch-api-and-using-asyncawait-47mp)

write both `.catch` and `.then` methods for all the promises.  
If something needs to be done in both the cases use `.finally`

===

# JAVASCRIPT BEST PRACTICE **01**

here's an excellent guide to [JavaScript Best Practices (W3.org)](https://www.w3.org/wiki/JavaScript_best_practices)

one example of [using shortcut notation](https://www.w3.org/wiki/JavaScript_best_practices#use-shortcut-notation-when-it-makes-sense):

```js
// long version:
if(v){
  let x = v;
} else {
  let x = 10;
}
// shortcut notation uses the double pipe character:
var x = v || 10;
// x equals v, but if v is empty, x equals 10
```

"It is amazing how many times you will build a massively convoluted JavaScript solution for a problem that can be solved easily without it."

---

# JAVASCRIPT BEST PRACTICE **02**

[Optimize loops](https://www.w3.org/wiki/JavaScript_best_practices#Optimize_loops) for speed. A common mistake is to make JavaScript read the array length **every time**:

```js
// given an array:
const names = ['Eazy-E', 'Dr. Dre', 'Ice Cube'];

// we can time how long it takes
console.time();
for(let i=0;i<names.length;i++){
  console.log(names[i]);
}
console.timeEnd();
// time: 0.26123046875ms
```


instead, **store the length** in a variable:

```js
console.time();
const all = names.length;
for(let i=0;i<all;i++){
  console.log(names[i]);
}
console.timeEnd();
// faster: 0.197021484375ms
```

---

# JAVASCRIPT BEST PRACTICE **04**

> keep computation-heavy code—including **regular expressions** and **DOM manipulation**—outside loops
>
> …create DOM nodes in the loop but insert them into the document *outside the loop*.
>
> Instead of constantly creating and applying elements, create a **tool function** that **turns a string into DOM elements** to call at the end of your content generation process—disturb browser rendering once rather than frequently.

---

# JAVASCRIPT BEST PRACTICE **6**

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

---

```js
let a = 8, b = 6;

[b, a] = [a, b]; // b = 8, a = 6
```

---

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

---

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

===

## CREATING OBJECTS

```js
const createPerson = (name, age, gender) => {
  return { name, age, gender };
};
console.log(createPerson("Zodiac Hasbro", 56, "male")); // creates new object
```

===

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

===

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


## PRACTICAL PLANNING **01**
<!-- .slide: class="crammed" -->

gather all the **content** for your site:

- images
- movies
- text (see [Writing for the Web](https://www.usability.gov/how-to-and-tools/methods/writing-for-the-web.html))
- audio
- data URLs from APIs

---

## PRACTICAL PLANNING **02**
<!-- .slide: class="crammed" -->

arrange your content into *logical groups*

**THINK:** will a group be **limited** or get **more content**?

this is the basis for your site structure, **navigation** and **menu**

Resources from [usability.gov](https://www.usability.gov/):

- [Content Strategy Basics](https://www.usability.gov/what-and-why/content-strategy.html)
- [Content Inventory](https://www.usability.gov/how-to-and-tools/methods/content-inventory.html)
- [Information Architecture](https://www.usability.gov/what-and-why/information-architecture.html)

---

## PRACTICAL PLANNING **03**

get input from others with an online tool:

[Online card sorting software](https://www.optimalworkshop.com/optimalsort): [free plan](https://www.optimalworkshop.com/register)

- [Card Sorting (usability.gov)](https://www.usability.gov/how-to-and-tools/methods/card-sorting.html)

---

- THE WEBSITE PROCESS (2 screens): https://tech3015.github.io/presents/?lecture-05#/3
- STYLE GUIDES (13 screens): https://tech3015.github.io/presents/?lecture-05#/4
- DESIGN TRENDS? (two link screens): https://tech3015.github.io/presents/?lecture-05#/5

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

<!-- .slide class="crammed nopadding" -->
![Classic Information Architecture infographic by Louis Rosenfeld](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/wireframes/rosenfeld-users-content-context.png)<!-- .element: class="nomargin" -->
