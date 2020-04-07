# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->
## **Front-End Web Development**
### Lecture 02

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

# Coursework **Important**

1. create GitHub account and login
2. follow instructions on this **[GitHub Classroom link](https://classroom.github.com/a/u2ocjK6g)**
  - find your name + P-number
  - make a note of the url or bookmark this page
3. GitHub will generate a private repository for you/us
4. use this repo ONLY to work on your assignment

===

# REMINDERS

- **indent** your code properly (2 spaces)!
- **read the links** to learn more!

Labs and lectures **always** have **extra links**

===

# A **history** of CSS: 1
<!-- .slide: class="crammed smalltext" -->

- **1994** first draft of **Cascading HTML Style Sheets**, [Håkon Wium Lie](https://dev.opera.com/articles/css-twenty-years-hakon/)
- **1995** discussions on the www-style mailing list influence CSS development
- HTML removed from name, style sheets also for **other markup languages**
- **1995** W3C HTML Editorial Review Board set up for HTML specifications
- **1996** Microsoft Internet Explorer is the first browser to support CSS
- **1996** CSS Level 1 W3C Recommendation (CSS1)
- **1996** W3C forms Cascading Style Sheets and Formatting Properties Working Group

[A Brief History of CSS](http://www.css-class.com/a-brief-history-of-css/)  

---

# A **history** of CSS: 2

> Tim Berners-Lee wrote his NeXT browser/editor in such a way that he could **determine the style with a simple style sheet**. However, he didn't publish the syntax for the style sheets, considering it a matter for each browser to decide how to best display pages to its users.

more…

---

# A **history** of CSS: 3
<!-- .slide: class="smalltext" -->

> In 1993, NCSA Mosaic, the browser that made the Web popular, came out. Stylewise, however, it was a backward step because it only allowed its users to change certain colors and fonts […] **writers of Web pages complained** that they didn't have enough influence over how their pages looked. One of the first questions from an author new to the Web was **how to change fonts and colors of elements**.

[A brief history of CSS until 2016](https://www.w3.org/Style/CSS20/history.html)

---

# A **history** of CSS: 4
<!-- .slide: class="crammed smalltext" -->

there were **tensions** between **authors** and **implementors**:

> …it has been a constant source of delight for me… to… tell hordes (literally) of people who want to -- strap yourselves in, here it comes -- control what their documents look like in ways that would be trivial in TeX, Microsoft Word, and every other common text processing environment: "**Sorry, you're screwed.**"

—Marc Andreessen, 1994, programmer NCSA **Mosaic** browser. Later co-founder of the **Netscape** browser, was more eager to please authors. In 1994, he announced the first beta release of **Mozilla** (later Netscape Navigator, and the code behind **Firefox**). In [The CSS saga](https://www.w3.org/Style/LieBos2e/history/Overview.html), chapter in: Håkon Wium Lie and Bert Bos, "CSS, designing for the Web".

---

# A **history** of CSS: 5
<!-- .slide: class="crammed smalltext" -->

- **1997** CSS Working Group creates **CSS 2 specification**
- **1998** CSS level 2 published as a **W3C Recommendation** (CSS2)
- **1998** the **Opera browser** supports CSS
- **2000** W3C CSS3 **Working Draft**
- **2011** W3C releases **CSS 2.1** fixed errors, better browser matching
- **2014** W3C Candidate Recommendation CSS Syntax Module **Level 3**
- **2017** **CSS 3** and browser support continues to **evolve**…

Warning! TMI: [W3C CSS Syntax Module Level 3](https://www.w3.org/TR/css-syntax-3/) (scroll to see the comments)

===

# **CSS 1** (1996)
<!-- .slide: class="crammed smalltext" -->

Supports: **font** properties, **text** attributes, text **alignment**, **tables**, **images**, text and background **color**, word/letter/line **spacing**, **margins**, **borders**, **padding**, **positioning**, **id**entification and **class**ification of groups of CSS styles.

In a **CSS file** (.css):
```css
.student { text-align: center; } /* all students */
#p12345678 { color: green; } /* only this student */
```

In an **HTML file** (.html):
```html
<p class="student"> <!-- all students -->
<span id="p12345678"> <!-- only this student -->
```

---

# **CSS 2** (1998)

New capabilities including: **z-index**, **media** types (e.g. *braille, print, speech, projection, tv*, etc.), **bidirectional** text, absolute, relative and fixed **positioning**, support for **aural** style sheets.

---

# **CSS 3** (2000, 2014…)
<!-- .slide: class="crammed smalltext" -->

Broken into **modules**. 2011-2012, four modules released as formal recommendations: color, selectors level 3, namespaces and **media queries**.

CSS3 now includes:  
**transitions**, **animation** and **transformations**.

Now CSS level 3 is separated into modules, there will be **no single CSS 4 release**—see the [W3C CSS Snapshot 2015](https://www.w3.org/TR/css3-roadmap/)

See W3Schools (*separate* from the W3C) guide for:  
[CSS transitions](http://www.w3schools.com/css/css3_transitions.asp), [CSS transforms](http://www.w3schools.com/cssref/css3_pr_transform.asp) and [CSS animation](http://www.w3schools.com/css/css3_animations.asp)

===

# CSS GOOD PRACTICE: **1**
<!-- .slide: class="crammed smalltext" -->

- Avoid IDs for selectors—they're **too tightly coupled** with HTML
- Avoid **`!important`**. It means the specificity of your CSS is **out of control!**
- **Don't use numbers** at the start of a class or ID name 
- **Avoid trailing zeros** in values e.g. **`2em`** not **`2.0em`**
- Use **hyphens**, not underscores, for multi-word ID or class names
- After global styles, **order styles as they appear** in the HTML
- **mobile** styles **first**, then **media queries** for larger screens
- The universal selector (wildcard) **`*`** is **slow**

See [Google's CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html) and its [CSS Formatting Rules](https://google.github.io/styleguide/htmlcssguide.html#CSS_Formatting_Rules) (**2 spaces!**)

---

# CSS GOOD PRACTICE: **2**
<!-- .slide: class="crammed smalltext" -->

**Browser** developers aim to **stop using** [vendor prefixes](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix)!  
So **do not use** them:

```css
-o-transform: rotate(7deg); /* NO! */
-ms-transform: rotate(7deg); /* AGAIN, NO! */
-moz-transform: rotate(7deg); /* JUST STOP IT! */
-webkit-transform: rotate(7deg); /* KILL IT WITH FIRE! */
```

We **avoid emerging CSS features** in this module until they have **widespread browser support**

Always see [Can I Use](https://caniuse.com/#feat=transforms2d) to check browser support.

===

# CSS RULES **1**
      
```css
selector { /* can be element, class… */
  property: value;
}
```

inside the curly braces `{ }`, the **property** and **value**  
together make a CSS **declaration** e.g.

```css
main {
  margin: 0 auto;
}
.sidebar {
  width: 50%;
}
body .contact-page {
  background: #666;
}
```

---

# CSS RULES **2**

A CSS **rule** inside `{}` can contain **multiple declarations**:


```css
main {
  margin: 0 auto;
  width: 50%;
  background: #666;
  font-family: Tahoma, Helvetica, sans-serif;
}
```

or be on **one line** (*harder to read* for developing):

```css
main { margin: 0 auto; width: 50%; }
```

---

# CSS RULES **3**

There are several **selector types**—they can also be:

- [pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) (e.g. `:hover` or `:checked`)
- [pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) (e.g. `::before` or `::first-line`)

CSS **selector references**:

- [List of selectors](http://www.w3schools.com/cssref/css_selectors.asp) (W3Schools)
- [Interactive page of CSS selectors](http://www.w3schools.com/cssref/trysel.asp) (W3Schools)

===

# BOX MODEL **1**

All **HTML tags** create a box or `block`:

![A diagram of the box model](boxmodel/boxmodel.png)

---

# BOX MODEL **2**

The **box dimensions** are controlled by the:

- **margin:** space ***outside***
- **padding:** space ***inside***
- **border:** line ***around***

*inline HTML* (e.g. `a` or `span`) also makes a box, but **may not show margin or padding** unless you set it’s CSS as `display: block;` or `display: inline-block;`

---

# BOX MODEL **3**: MARGIN

The **margin** makes an invisible **space around** an element  
usually set in **pixels**, **ems** or **percentages**:  
`1px`, `.5em`, `5%`

Can be zero: `margin: 0;`

**NOTE**: the following elements have **default margins**:  
`body`, `h1..h6`, `p`, `blockquote`, `form`, `fieldset`, and the list elements: `ul`, `ol`, `dl`, `dd`. You can reset these with CSS.

---

# BOX MODEL **4**: PADDING

**Padding** is **inside** the box, **around** the box **content**

padding includes the **background colour** and **background image** of a box

usually set in **pixels**, **ems** or **percentages**:  
`1px`, `.5em`, `5%`

Can be zero: `padding: 0;`

---

# BOX MODEL **5**: BORDER

The **border** goes **around the outside** of the box

best set in **pixels**, and easiest to set in one declaration:

`border: 1px solid silver;`  
`border-bottom: 3px dotted #999;`

Can be zero: `border-bottom: none;`

---

# BOX MODEL **6**: 3D

If you could **see HTML boxes**, they'd look like this!  
Note the **layers** are **nested** just as in the **HTML**

![3D box model image](boxmodel/3dview.png)

===

# BOX-MODEL **SYNTAX**: 1

By default, **padding and border** are **added** to the width and height of a box:

```css
main {
  width: 70%;
  padding: 1em;
  border: 2px;
}
```

width is 70% **+** 2em **+** 4px

---

# BOX-MODEL **SYNTAX**: 2

With `box-sizing` set to to `border-box` the **padding and border** are **included** in the width and height, making measurements easier:

```css
main {
  box-sizing: border-box;
  width: 70%;
  padding: 1em;
  border: 2px;
}
```

`border-box` means width **remains 70%**  
(not 70% + 2em + 4px)

---

# BOX MODEL **SYNTAX**: 3

## For both **margin** and **padding**

```css
header {
  margin: 2px; /* a 2-pixel margin all round */
  padding-top: 1em; /* one line of padding at top */
  margin-left: 5%; /* 5% of available space to left */
}
/* you can use: -top -right -bottom -left */
```

---

# BOX-MODEL **SYNTAX**: 4

**CSS shorthand**
- **4** values: **top, right, bottom, left** (clockface)
- **3** values: **top, left-right, bottom**
- **2** values: **top-bottom, left-right**

```css
header {
  padding: 1em 10px .5em 5px;
  /* 4: top right bottom left: */
  padding: 1em 10px .5em; /* an em is one line-height */
  /* 3: top 1em, l-r 10 pixels, bottom .5em */
  margin: 1em 0;
  /* 2: one line top+bottom, none left-right: */
}
```

---

# BOX-MODEL **SYNTAX**: 5

Set top, right, bottom, left, then **reset one**

```css
header {
  margin: 10px; /* 10 pixels all round… */
  margin-top: 0; /* …but no top margin */
}
```
The second line comes *after*—so **overrides**—the first

---

# BOX-MODEL **SYNTAX**: 6

To **centre** an block element by itself, set the  
**left** and **right** margins to `auto`:

```css
header {
  margin: 0 auto; /* zero top-bottom, auto l-r */
}
```
`auto` fills the available space to the left and right equally.

This is also a common way to **centre a page design** in the **browser window**, although current designs prefer to **fill the browser window** completely.

---

# BOX-MODEL **SYNTAX**: 7

`display: inline-block` turns **inline elements** into **blocks that line up horizontally**, often for `a` or `li` tags in menus or the `img` tag for images.

```css
a {
  display: inline-block;
}
/* 'block' makes inline 'a' elements into blocks */
```

[W3Schools: HTML Block and Inline Elements](http://www.w3schools.com/html/html_blocks.asp)

---

# BOX-MODEL **SYNTAX**: 9

- Learn about the box model with [exercises on W3Schools](http://www.w3schools.com/css/css_boxmodel.asp)
- Adjust sliders on an [Interactive box-model demo](http://guyroutledge.github.io/box-model/)

===

# BOX MODEL **BORDER**: 1
<!-- .slide: class="crammed smalltext" -->
box outline with three parameters:  `width`, `style`, `color`

```css
img {
  border-width: 2px;
  border-style: solid; /* none|solid|dotted|dashed */
  border-color: white;
}
.mybox img {
  border: 2px solid white; /* shorthand */
}
```
…if the image is inside a **figure** tag with a **class "mybox"**:
```html
<figure class="mybox">
  <img src="images/mypic.png" alt="my face">
</figure>
```

---

# BOX-MODEL **BORDER**: 2

Each property can have **one**, **two**, **three** or all  
**four** “clockface” values: **top**, **right**, **bottom**, **left**.

```css
header {
  border-color: white black; /* top, bottom */
  border-width: 2px 0 4px; /* top, r-l, bottom */
  border-style: solid dotted none dashed;
    /* top, right, bottom, left */
}
```

---

# BOX-MODEL **BORDER**: 3

**CSS shorthand** for a single border style all around:

```css
img {
  border: 1px #555 dotted;
  /* a grey dotted border */
}
```

---

# BOX-MODEL **BORDER**: 4

Boxes can be rounded with `border-radius`:

```css
aside {
  border-radius: 2px; /* slight corner curves */
}

img {
  border-radius: 50%; /* totally round */
}
```

---

# BOX-MODEL **BORDER**: 5

Or have one, two or three sides rounded…

```css
img {
  border-top-left-radius: 50%;
  border-bottom-left-radius: 50%;
  /* a semi-circle (if height=width) or half-ellipse */
}
img {
  border-top-right-radius: 100%;
  /* an arc (if height=width) */
}
```

---

<style>
  /* unique styles for this presentation */
  .borders div div {
    line-height: 2.5em;
    font-size: 0.8em;
    width: 700px;
    margin-top: 1em;
  }
  .border div {
    border: 4px solid #666; 
  }
  .borders .square div {
    height: 2.5em;
    width: 2.5em;
  }
  .radius-demo {
    width: 100%;
    text-align: center;
  }
  .radius-demo-div-l div {
    text-align: right;
    padding-right: 1em;
  }
  .radius-10 {
    background: #fcc;
    border-radius: 10px;
  }
  .radius-100 {
    background: #cfc;
    border-top-left-radius: 100%;
  }
  .radius-50 {
    background: #ccf;
    border-top-left-radius: 50%;
    border-bottom-left-radius: 50%;
  }
  .round {
    border-radius: 50%;
  }
</style>

# BOX-MODEL **BORDER**: 6
<!-- .slide: class="borders radius-demo" -->

**border-radius**, rectangles/squares, with  
`border-width: 4px; border-color: #666;`

<div class="float-l radius-demo-div-l border">
  <div class="radius-10">i’m 10px rounded, that square’s 50% rounded -></div>
  <div class="radius-100">one corner 100% rounded</div>
  <div class="radius-50">two corners 50% rounded</div>
</div>
<div class="square float-r border">
  <div class="radius-10 round"></div>
  <div class="radius-100"></div>
  <div class="radius-50"></div>
</div>

---

# BOX-MODEL **BORDER**: 7
<!-- .slide: class="borders radius-demo" -->

**border-radius**, rectangles/squares, **no border-style/color**

<div class="float-l radius-demo-div-l">
  <div class="radius-10">i’m 10px rounded, that square’s 50% rounded -></div>
  <div class="radius-100">one corner 100% rounded</div>
  <div class="radius-50">two corners 50% rounded</div>
</div>
<div class="square float-r">
  <div class="radius-10 round"></div>
  <div class="radius-100"></div>
  <div class="radius-50"></div>
</div>
</section>

---

# BOX-MODEL **BORDER**: 8

## more information on borders

Reference: [W3Schools: CSS Borders](http://www.w3schools.com/css/css_border.asp)

Or (if you like) play with [CSS shapes](https://css-tricks.com/examples/ShapesOfCSS/)

===

# FLEXBOX **1**: INTRODUCTION

**CSS flexbox** enables the **arrangement of boxes** inside a container:

```css
.my-boxes {
  display: flex;
}
```

---

# FLEXBOX **2**: HORIZONTAL

for **horizontal alignment** use the `justify-content:` property, with values:

- `flex-start` group items to **left** (the start) of container
- `flex-end` group items to **right** of container
- `center` group items in the **center** of a container
- `space-between` **distribute** items: first/last are left/right others are equally between
- `space-around` **distribute** and space items **evenly**

---

# FLEXBOX **3**: VERTICAL

for **vertical alignment** use the `align-items:` property, with values:

- `flex-start` across top
- `flex-end` across bottom
- `center` in center
- `baseline` across baseline
- `stretch` space items or stretch item to fill

---

# FLEXBOX **4**: ORDER

for the **order of boxes** use the `flex-direction:` property, with values:

- `row` flow left to right
- `row-reverse` flow right to left
- `column` stack top to bottom
- `column-reverse` stack bottom to top

---

# FLEXBOX **5**: EXAMPLE

In this example, the **parent element** `.my-boxes` contains  
several **child elements** to arrange:

```css
.my-boxes {
  display: flex; /* set to display as flexbox */
  justify-content: space-around; /* even spacing */
  align-items: center; /* align vertical center */
  flex-direction: row-reverse; /* wrap last-first */
}
```

---

# FLEXBOX **6**: EXAMPLE

The HTML just needs a **selector** e.g. `class="my-boxes"` for the CSS to **identify the element** to be **styled as flexbox**:

```html
<section class="my-boxes">
  <div>Box one</div>
  <div>Box two</div>
  <div>Box three</div>
</section>
```

---

<style>
  .my-boxes {
    display: flex; /* set to display as flexbox */
    justify-content: space-around; /* even spacing */
    align-items: center; /* align vertical center */
    flex-direction: row-reverse; /* wrap last-first */
    background:#ccc;
    height: 300px;
  }
  .my-boxes div {
    background: #9c5;
    border: 1px solid #999;
    width: 200px;
    height: 200px;
    text-align: center;
    padding-top: 1em;
  }
</style>

# FLEXBOX **7**: EXAMPLE

The `.my-boxes` section tag contains the boxes to arrange

<div class="my-boxes">
  <div>Box one</div>
  <div>Box two</div>
  <div>Box three</div>
</div>

Try the CSS game [Flexbox Defence](http://www.flexboxdefense.com/).

===

# Questions?
<!-- .slide: class="centered" -->

**Ask now**  
no crowding around  
the podium after, please!