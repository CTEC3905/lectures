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

**Tutors**

- Labs: **Graeme Stuart**: gstuart@dmu.ac.uk
- Labs: **Fania Raczinski**: fania.raczinski@dmu.ac.uk
- Lectures: **Dave Everitt**: deveritt@dmu.ac.uk

**Tutor contact outside classes is strictly by email**

===

# JAVASCRIPT TEACHING
<!-- .slide: class="smalltext crammed" -->

Reminders

- make **separate** GitHub repos for **lab code**
- make **one thing** work and test it
- decide **how to use JavaScript** in your project
- check the **browser console** (f12/cmd-alt-i) for errors
- always **[validate your HTML](https://validator.w3.org/** as you develop!

===

# JAVASCRIPT: THE DOM **01**
<!-- .slide: class="smalltext" -->

There is a predefined `document` object in JavaScript, which can be used to **access all elements** in the **DOM**.

This `document` object is the owner (or **root**) of **all objects in your webpage**.

So to access objects in an HTML page, you always start with the `document` object, e.g.:

```javascript
document.body.innerHTML = "Some text";
```

`body` is an element of the DOM so you access it using the `document` object, then you can change the content of its `innerHTML` property.

---

# JAVASCRIPT: THE DOM **02**
<!-- .slide: class="smalltext smallcode" -->

A more scalable example:

```javascript
function addTextNode() {
  const myheading = document.createElement("h1");
  let mytext = document.createTextNode("Hello Big Heading!");
  myheading.appendChild(mytext);
  document.body.appendChild(myheading);
}
```

---

# JAVASCRIPT: THE DOM **03**
<!-- .slide: class="smalltext smallcode" -->

You can get a reference to elements by `tag`, `id`, `class`:

```javascript
document.getElementsByTagName("HTML_tag");

document.getElementById("my_id"); // no '#' needed

document.getElementsByClassName("my_class"); // no '.' needed
```

<small>W3Schools: <a href="https://www.w3schools.com/js/js_htmldom_elements.asp">JavaScript HTML DOM Elements</a></small>

---

# JAVASCRIPT: THE DOM **03**
<!-- .slide: class="smalltext smallcode" -->

`document.querySelectorAll` uses CSS-style selectors:

```javascript
document.querySelectorAll("p.intro");
document.querySelectorAll("main section:first-child");
document.querySelectorAll('.mydata [data-period="current"]');

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

``` javascript
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

<!-- <section> -->

<h1>JAVASCRIPT DEMOS: <strong>02</strong></h1>

<p id="my-id" style="cursor: pointer;">Click me!</p>

<script>
	const clickThing = document.getElementById("my-id");
  const do_stuff = () => { alert("You clicked me!"); }
  // const do_stuff = () => { console.log("You clicked me!"); }
  clickThing.addEventListener("click", do_stuff);      
</script>

<!-- </section> -->

---
 
<h1>JAVASCRIPT DEMOS: <strong>03</strong></h1>

<button id="myBtn" style="cursor: pointer; border-radius: 4px; background: #aaa;">What's the date?</button>

<p id="demo">I've no idea. Click the button.</p>

<script>
document.getElementById("myBtn").addEventListener("click", showDate);
const dateDemo = document.getElementById("demo");

function showDate() {
	let d = new Date();
	dateDemo.innerHTML = `Oh, it’s: ${d.toDateString()}!`;
}
</script>

<h4 style="margin-top: 4em">REFERENCES:</h4>
<p><small>
	<a href="http://www.w3schools.com/js/js_htmldom_eventlistener.asp">W3Schools: JavaScript HTML DOM EventListener</a><br>
  <a href="http://www.w3schools.com/jsref/jsref_todatestring.asp">W3Schools: JavaScript toDateString() Method</a>
</small></p>

---

# JAVASCRIPT DEMOS: **04**
<!-- .slide: class="smalltext smallcode" -->

Here’s the **code** that **showed the date** (HTML/JS):

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

---

<h1>JAVASCRIPT DEMOS: <strong>05</strong></h1>

<form id="getName" action="#" method="post">
	<label for="userName">Enter name:</label>
	<input id="userName" type="text" placeholder="name here please :-)" style="font-size: 1em">
	<input type="submit" style="background: #ccc; color: #666; border-radius: 10%; font-size: 1em;">
</form>

<p style="margin-top: 1em;">Hello, <span id="myName">anonymous user! Your name?</span></p>

<script>
	function PerformGreeting() {
    if(userName.value){
      myName.innerHTML = `<strong>${userName.value}</strong>!`;
    } else {
      myName.innerHTML = `<strong>person with no name</strong>!`;
    }
    event.preventDefault(); // disables default form submission
    // return false; // prevents further "bubbling" up of event
	}

	getName.addEventListener("submit", PerformGreeting);
</script>

---

# JAVASCRIPT DEMOS: **06**
<!-- .slide: class="crammed smalltext smallcode" -->

code that grabbed the name and displayed it (HTML/JS):

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

---

<style>
  #question, #photo1, #photo2 {
    text-decoration: underline;
    cursor: pointer;
  }
  #question:hover, #photo1:hover, #photo2:hover {
    text-decoration: none;
    color: #ccc;
  }
  #picture {
    font-size: 75%;
    text-align: center;
    line-height: 178px;
    height: 178px;
    width: 300px;
    background-repeat: no-repeat;
    border: solid silver 4px;
    transition: all 1s;
  }
  #picture.car {
    border-color: green;
    background-image: url("images/tesla-model-s.jpg");
  }
  #picture.cat {
    border-color: pink;
    background-image: url("images/kitten.jpg");
  }
</style>

<h1>JAVASCRIPT DEMOS: <strong>07</strong></h1>

<p>You can also <strong>manipulate CSS</strong> with JavaScript…<br>
e.g. to change a <strong>background image</strong>:</p>

<p>See a: <span id="photo1">Tesla</span> / <span id="photo2">kitten</span>!</p>

<p id="picture" class="text">picture will appear</p>
  
<script>
  function showImage(whichPic) {
    picture.innerHTML = "";
    if (whichPic === "photo1") {
      picture.classList.remove("cat");
      picture.classList.add("car");
    } else {
      picture.classList.remove("car");
      picture.classList.add("cat");
    }
  }
  photo1.addEventListener("click", function(){ showImage(this.id) });
  photo2.addEventListener("click", showImage);
</script>

---

# JAVASCRIPT DEMOS: **08**
<!-- .slide: class="smalltext smallcode" -->

Here’s the **HTML** and the **JavaScript:**

```html
<p>See a: <span id="photo1">Tesla</span>  /  <span id="photo2">kitten</span>!</p>

<p id="picture" class="text">picture will appear</p>
```

```javascript
function showImage(whichPic) {
  picture.innerHTML = "";
  if (whichPic === "photo1") {
    picture.classList.remove("cat");
    picture.classList.add("car");
  } else {
    picture.classList.remove("car");
    picture.classList.add("cat");
  }
}

photo1.addEventListener("click", function(){ showImage(this.id) });
photo2.addEventListener("click", showImage);
```

---

# JAVASCRIPT DEMOS: **09**
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
  border: solid green 4px;
  transition: all 1s;
}
#picture.car {
  border-color: silver;
  background-image: url("images/tesla-model-s.jpg");
}
#picture.cat {
  border-color: pink;
  background-image: url("images/kitten.jpg");
}
```

===

<!-- SHARED WITH CTEC3905 - UPDATE CTEC USING THIS! -->

# JAVASCRIPT OBJECTS: **01**
<!-- .slide: class="crammed smalltext smallcode" -->

A [JavaScript object](http://www.w3schools.com/js/js_objects.asp) contains `name:value` pairs inside curly braces `{}`  
It can contain nested objects (**no comma** after the last items!):

```javascript
const animals = {
  cat: {
    horns: "none",
    fluff: "loads",
    eyes: "super-advanced, read up on this"
  },
  goat: {
    horns: "yes",
    fluff: "not really",
    eyes: "really weird, you should check"
  }
};
```

An **array of objects** - `[{},{}]` - is a common **JSON data format** used for exchanging data on the web e.g. from **APIs**

---

# JAVASCRIPT OBJECTS: **02**
<!-- .slide: class="crammed smalltext smallcode" -->

Here, the `range` object is a child of the `car` object:

```javascript
const car = {
  manufacturer: "Tesla",
  model: "Model S",
  range: {
    normal: "360",
    ludicrous: "200"
  },
  colour: "red",
  start: function() { function_code_here } // only in JS, NOT JSON
};

car.range.ludicrous; // returns: 200
```

An **array of objects** is a common **JSON data format** used for exchanging data on the web e.g. from **APIs**

---

<h1>JAVASCRIPT OBJECTS: <strong>03</strong></h1>

<p>Now we have made a <code>car</code> object we can <strong>use it’s data</strong>:</p>

<p id="question">How far will the Tesla travel if you don’t drive like a maniac?</p>

<p id="answer"></p>

<script>
  const car = {
    manufacturer: "Tesla",
    model: "Model S",
    range: {
      normal: "360",
      ludicrous: "200"
    },
    colour: "red",
    start: function() { function_code_here }
  };

  let info = function() {
    answer.innerHTML = `The <strong>${car.manufacturer} ${car.model}</strong> has a <strong>${car.range.normal} mile</strong> normal range.`;
  }
  
  question.addEventListener("click", info);
</script>

---

# JAVASCRIPT OBJECTS: **04**
<!-- .slide: class="crammed smalltext smallcode" -->

Here’s the **HTML**:

```html
<p id="question">How far will the Tesla travel if you don’t drive like a maniac?</p>

<p id="answer"></p>

```

Here’s the **JavaScript**:

```javascript
// this gets details from the object
let info = function() {
  answer.innerHTML = `The <strong>${car.manufacturer} ${car.model}</strong> has a <strong>${car.range} mile</strong> normal range.`;
}

// this captures the click
question.addEventListener("click", info);
```
<!-- END SHARED WITH CTEC3905 -->

===

# DEMO

- [Store a name with local storage from an input form](https://front-end-materials.github.io/local-storage/js-local-storage-form/)
- [code](https://github.com/front-end-materials/local-storage/js-local-storage-form)

OR

DEMO: store multiple names in localStorage??

===

# QUESTIONS?

**please ask now…**

No crowding around the podium afterwards!

Talk to Graeme for module-related issues

