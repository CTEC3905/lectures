# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

## **Front-End Web Development**

## Lecture 05

===

# STAFF CONTACTS
<!-- .slide: class="crammed smalltext" -->

**Module leader:**

General queries and admin issues:

**Graeme Stuart**: gstuart@dmu.ac.uk

<hr>

<!-- **Tutors**

- Labs: **Graeme Stuart**: gstuart@dmu.ac.uk
- Labs: **Fania Raczinski**: fania.raczinski@dmu.ac.uk
- Lectures: **Dave Everitt**: deveritt@dmu.ac.uk

**Tutor contact outside classes is strictly by email** -->

===

# JAVASCRIPT TEACHING
<!-- .slide: class="smalltext crammed" -->

Reminders

- make separate GitHub repos for **re-usable lab code**
- make **one thing** work and test it
- Decide **how to use JavaScript** in your project
- check the **browser console** (f12/cmd-alt-i) for errors
- always **[validate your HTML](https://validator.w3.org/)** as you develop!

===

# JAVASCRIPT: THE DOM **01**
<!-- .slide: class="smalltext" -->

There is a predefined `document` object in JavaScript, which can be used to **access all elements** in the **DOM**.

This `document` object is the  **root** of **all objects** in your **webpage**.

To access HTML elements, start with the `document` object, e.g.:

```javascript
document.body.innerHTML = "Some text";
```

(`body` is an element of the DOM, so you access it with the `document` object, then you can **change the content** of its `innerHTML` property)

---

# JAVASCRIPT: THE DOM **02**
<!-- .slide: class="smalltext smallcode" -->

A more scalable example:

```javascript
function addTextNode() {
  const myheading = document.createElement("h1");
  const mytext = document.createTextNode("Hello Big Heading!");
  myheading.appendChild(mytext);
  document.body.appendChild(myheading);
}
```

---

# JAVASCRIPT: THE DOM **03**
<!-- .slide: class="smalltext smallcode" -->

You can get a reference to elements by `tag`, `id`, `class`:

```javascript
document.getElementsByTagName("section");  // returns a list

document.getElementById("my_id"); // no '#' needed && returns single item

document.getElementsByClassName("my_class"); // no '.' needed & returns a list
```

<small>W3Schools: <a href="https://www.w3schools.com/js/js_htmldom_elements.asp">JavaScript HTML DOM Elements</a></small>

---

# JAVASCRIPT: THE DOM **03**
<!-- .slide: class="smalltext smallcode" -->

`document.querySelectorAll` uses CSS-style selectors:

```javascript
document.querySelector("p#id");  // returns one item

document.querySelectorAll("p.intro");  // returns a list

document.querySelectorAll("main section:first-child");  // returns a list

document.querySelectorAll('.mydata [data-period="current"]');  // returns a list

```

<small>MDN: <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector">Document.querySelector()</a></small>

===

# JAVASCRIPT DEMOS: **01**
<!-- .slide: class="crammed smalltext smallcode" -->
      
The simplest possible example (in HTML/JS files):

<!-- In the **HTML** (.html) file: -->

```html
<p id="my-id">Click me!</p>
```

<!-- In the **JavaScript** (.js) file: -->

```javascript
// store a reference to the element to be clicked:
const clickThing = document.getElementById("my-id");

// what to do when the user clicks:
function do_stuff() {
  alert("You clicked me!");
}
// or you can use the simpler "fat arrow" syntax:
const do_stuff = () => { alert("You clicked me!"); }

// "listen" for the click:
clickThing.addEventListener("click", do_stuff);
```

---

# JAVASCRIPT DEMOS: **02**
<!-- .slide: class="smalltext smallcode" -->

**Get the date** and **display it** (HTML/JS):

```html
<button id="myBtn">What's the date?</button>

<p id="demo">I've no idea. Click the button.</p>
```

```javascript
document.getElementById("myBtn").addEventListener("click", showDate);
const dateDemo = document.getElementById("demo");

function showDate() {
  let d = new Date();
  dateDemo.innerHTML = `Oh, it’s: ${d.toDateString()}!`;
}
```

- DEMO: [Show date](https://front-end-materials.github.io/js-simple-examples/js-show-date/)
-	W3Schools: [JavaScript HTML DOM EventListener](http://www.w3schools.com/js/js_htmldom_eventlistener.asp)
- W3Schools: [JavaScript toDateString() Method](http://www.w3schools.com/jsref/jsref_todatestring.asp)

---

# JAVASCRIPT DEMOS: **03**
<!-- .slide: class="crammed smalltext smallcode" -->

get a name from a form and display it (HTML/JS):

```html
<form id="getName" action="#" method="post">
  <label for="userName">Enter name:</label>
  <input id="userName" type="text" placeholder="name here please :-)">
  <input type="submit">
</form>
<p>Hello, <span id="myName">anonymous user! Your name?</span></p>
```

```javascript
function PerformGreeting() {
  if(userName.value){
    myName.innerHTML = `<strong>${userName.value}</strong>!`;
  } else {
    myName.innerHTML = `<strong>person with no name</strong>!`;
  }
  event.preventDefault(); // disables default form submission
}

getName.addEventListener("submit", PerformGreeting);
```

[DEMO: get input](https://front-end-materials.github.io/js-simple-examples/js-get-input/)

---

# JAVASCRIPT DEMOS: **04**
<!-- .slide: class="smalltext smallcode" -->

You can also **manipulate CSS** with JavaScript…

```html
<p>A link <a class="thelinks" href="#">link 1 text</a>.</p>
<p>Another link <a class="thelinks" href="#">link 2 text</a>.</p>

<button id="changeLinks">Change link colours</button>
```

```css
.changeMe {
  background: #336; color: #fcc; transition: all 1s;
}
```

```javascript
const thelinks = document.getElementsByClassName('thelinks');

const addClass = () => {
  for(i in thelinks){
    thelinks[i].classList.toggle("changeMe");
  }
}
changeLinks.addEventListener("click", addClass);
```

[DEMO: change elements](https://front-end-materials.github.io/js-simple-examples/js-change-element/)

---

# JAVASCRIPT DEMOS: **05**
<!-- .slide: class="smalltext smallcode" -->

You can also **change CSS** with JavaScript… e.g. a **background image**:

```html
<p>See a: <span id="car">Tesla</span> / <span id="cat">kitten</span>!</p>

<p id="picture">your choice of picture here</p>
```

```javascript
function showImage() {
  picture.innerHTML = "";
  console.log(event.target.id);
  picture.classList = event.target.id;
}

[car,cat].forEach(c => c.addEventListener( "click", showImage ));
```

DEMO: [swap CSS class](https://front-end-materials.github.io/js-simple-examples/js-swap-class/)

---

# JAVASCRIPT DEMOS: **05a**
<!-- .slide: class="smalltext smallcode" -->

…and the **CSS** for styling, and the fade transition:
  
```css
#picture {
  font-size: 75%;
  text-align: center;
  line-height: 178px;
  height: 178px;
  width: 300px;
  background-repeat: no-repeat;
  border: solid #999 2px;
  transition: all 1s;
}
.car {
  background-image: url("images/tesla-model-s.jpg");
}
.cat {
  background-image: url("images/kitten.jpg");
}
```

===

<!-- SHARED WITH CTEC3905 - UPDATE CTEC USING THIS! -->

# JAVASCRIPT OBJECTS: **01**
<!-- .slide: class="crammed smalltext smallcode" -->

A [JavaScript object](http://www.w3schools.com/js/js_objects.asp) contains `name:value` pairs inside curly braces `{}`  

It can contain **nested objects**

IMPORTANT: **no comma** after the last items!

---

# JAVASCRIPT OBJECTS: **02**
<!-- .slide: class="crammed smalltext smallcode" -->

Here, the `range` object is a child of the `car` object:

```javascript
const car = {
  manufacturer: "Tesla",
  model: "Model S",
  range: { normal: "360", ludicrous: "200" },
  colour: "red",
  query: function(){
    answer.innerHTML = 
      `The <strong>${car.manufacturer} ${car.model}</strong> has a \ 
           <strong>${car.range.normal} mile</strong> normal range.`;
  }
};

question.addEventListener("click", car.query);

car.range.ludicrous; // returns: 200
```

---

# JAVASCRIPT OBJECTS: **02a**
<!-- .slide: class="smalltext smallcode" -->

Here’s the **HTML**:

```html
<p id="question">How far will the Tesla travel if you don’t drive like a maniac?</p>

<p id="answer"></p>
```

- DEMO: [Accessing object properties](https://front-end-materials.github.io/js-objects/js-object-properties/)
- DEMO: [Traversing items in a nested object](https://front-end-materials.github.io/js-objects/js-nested-object/)
- MDN: [Working with Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

---

# JAVASCRIPT OBJECTS: **03**
<!-- .slide: class="smalltext smallcode" -->

An **array of objects** is a common **JSON data format** used for exchanging data on the web e.g. from **APIs**

```javascript
const animals = [
  { cat: {
      horns: "none",
      fluff: "loads",
      eyes: "super-advanced, research this"
    }
  },
  { goat: {
      horns: "yes",
      fluff: "not really",
      eyes: "really weird, you should check"
    }
  }
];

animals[0].cat.horns // "none"
```

<!-- END SHARED WITH CTEC3905 -->

===

# END

Please discuss module-related issues and questions with your **module tutor** or **module leader**
