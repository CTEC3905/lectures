# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

## **Front-End Web Development**

### Lecture 06

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

# DO IT!

- **[validate your HTML](https://validator.w3.org/)** before committing
- add [`"use strict";`](https://javascript.info/strict-mode) at the top of your .js

Just **DO IT**. You should know why by now.

===

# GIT/GITHUB: **1**
<!-- .slide: class="crammed" -->

- **GitHub classroom** is for your **assignment code**
- **accepting** the assignment **creates a repo**:
  - it’s in the **CTEC3905 account** (*not* your account)
  - **sign in** to see it on your **GitHub home page**
  - `git push` to it regularly
  - **do not “upload” via GitHub**—use `git push`
  - **edit/delete** files **locally** (*not* on GitHub), `commit`, `push`
  - to work on another machine, first **clone the repo**
- use the `command-line` and **get used to it**!

---

# GIT/GITHUB: **2**
<!-- .slide: class="crammed" -->

- use your **own account** for **lab exercises**
- **clone** lab exercise code into your **local work folder**
- `cd` into the **repo folder after cloning** and:
  - `git remote set-url origin your_repo_here.git`
  - check `git remote -v` **before pushing**
- **make repos** for **your own code** on GitHub first:
  - **new?** `git remote add origin your_repo_here`

---

# GIT/GITHUB: **3**

use `git` carefully:

- **check first** you're **in the right folder**!
- **do not** put git repos **inside other git repos**!
- build a **library** of **re-usable code** this way

---

# GIT/GITHUB: **4**
<!-- .slide: class="crammed smalltext smallcode" -->
  
How to **clone a repo** into a **new repo of your own**: 1:

- open a **location for** the cloned folder
- in the folder window, **shift+right click: open in command window here**
-	**clone** the **GitHub repo** you want to copy (e.g.):  
	`git clone https://github.com/MODULE/REPO_NAME.git`
-	`cd REPO_`… (**tab** complete) into the **cloned repo folder**
- `dir` (Win) or `ls -al` (\*nix/OS X) to **see the cloned files**

---

# GIT/GITHUB: **5**
<!-- .slide: class="crammed smalltext smallcode" -->
  
How to **clone a repo** into a **new repo of your own**: 2:

- **on GitHub**, make a new repo, then **reset the remote** to the **new repo**:  
	`git remote set-url origin NEW_REPO.git`
- **push** the **cloned files** to your **new repo**:  
	first time: `git push -u origin master`  
  then (after more changes) just: `git push`

---

# GIT/GITHUB: **6**
<!-- .slide: class="crammed smalltext smallcode" -->

How to **upload your changes** to **your GitHub repository**

- have an **open command prompt** in the **directory with the changed files**
- **check where** you’re **pushing to** with `git remote -v`
-	`git status` will **show the files** you have **changed** (in *red*)
-	`git add .` (the “`.`” means “all”) to **add your changes** to GIT
-	`git status` will show **your added files** (in *green*)
-	**commit** the change with a **brief message**:  
  `git commit -m "changed title"`
- `git push` will **push** the **changed files** to **your GitHub repo**

===

<!-- RESPONSIVE DESIGN -->

# RESPONSIVE DESIGN: **1**
<!-- .slide: class="crammed smalltext" -->

CSS **media queries** can respond to many factors. The main three are:

| `@media` | for: |
|:--|:--|
| `print` |	printers |
| `screen` | computer screens, tablets, phones… |
| `speech` | text-to-speech screen readers |

but there's also…

`width`/`height`, `orientation`, `hover`, `light-level`… and more... see [Using media queries (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)

---

# RESPONSIVE DESIGN: **2**
<!-- .slide: class="crammed smalltext smallcode" -->

`@media` queries in CSS **apply styles conditionally**

For example, when **printing** you can add styles that **remove** navigation, dark backgrounds, ads…

```css
@media print {
  body {
    background: #fff; /* white */
  }
  nav,
  footer,
  .promo {
    display: none;
  }
}
```

---

# RESPONSIVE DESIGN: **3**
<!-- .slide: class="crammed smalltext smallcode" -->

or more specific filtering

```css
@media screen and (orientation: landscape) {
  nav {
    display-flex;
  }
}

@media speech {
  .adverts,
  .banner {
    display: none;
  }
}

@media (hover: hover) {
  a:hover {
    background: yellow;
  }
}
```

---

# RESPONSIVE DESIGN: **4**

**However** get started with just  
`screen` and `min-width` e.g.

```css
@media screen and (min-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

Some [examples of RWD (mediaqueri.es)](https://mediaqueri.es/)

---

# RESPONSIVE DESIGN: **5**
<!-- .slide: class="smalltext smallcode" -->

Use **[NATURAL BREAKPOINTS](https://stackoverflow.com/a/20350990/123033)**!

- Design **mobile-first**, then **increase the screen width** by resizing the browser window and/or using the [Chrome inspector mobile icon](https://developers.google.com/web/tools/chrome-devtools/device-mode/).
- Add `min-width` **breakpoints** wherever the **design becomes “broken”** or fails when the viewport width increases—
- all content should **look good at any viewport** width/height

**Avoid** large **fixed width** elements.

See the [responsive starter code](https://github.com/CTEC3905/starter-code)…

---

# RESPONSIVE DESIGN: **6**
<!-- .slide: class="smalltext smallcode" -->

So mobiles just don't reduce the website down to phone screen width, the HTML `head` section needs special `meta` tag `viewport` and `content` attributes:

```html
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>P-Number</title>
  <link rel="stylesheet" href="css/styles.css">
</head>
```

---

# RESPONSIVE DESIGN: **7**
<!-- .slide: class="smalltext smallcode" -->

…the [responsive starter code](https://github.com/CTEC3905/starter-code) has a **mobile-first CSS structure** e.g.

```css
/* all general/mobile styles first: */

body { background: rgb(220,230,210); }
a:link, a:visited { color: #003; }
/* etc... */

/* next, the first breakpoint above mobile: */

@media screen and (min-width: 600px) {
  a:hover { color: #225; }
  /* override mobile styles here...
  and set styles for larger widths */
}

@media screen and (min-width: 1000px) {
/* then override previous styles for screens > 999px */
}
```

---

# RESPONSIVE DESIGN: **8**
<!-- .slide: class="smalltext" -->

- **Percentages** work well for setting basic element widths, but use `display: border-box` to ensure padding and borders **remain *inside* the element’s width**
- For **individual container elements** (e.g. a `main` tag) you can use `max-width` to keep them from **getting too wide**

> **45** to **80** characters (per line) is the ideal **line length** for text on websites  
—[The Readability Formula: Making Your Website Easy-to-Read](https://kickpoint.ca/the-readability-formula-making-your-website-easy-to-read/)

---

# RESPONSIVE DESIGN: **9**
<!-- .slide: class="smalltext" -->

**References**

- [Responsive Web Design](http://alistapart.com/article/responsive-web-design) (The first, Ethan Marcotte, 2010)
- [Responsive animations](http://www.fastcodesign.com/3038367/9-gifs-that-explain-responsive-design-brilliantly) (less reading more looking)
- [HTML Responsive Web Design](http://www.w3schools.com/html/html_responsive.asp) (W3 Schools)
- [Am I Responsive](http://ami.responsivedesign.is/?url=https%3A%2F%2Fswitchoff.nus.org.uk#) (with example site)
- [This Is Responsive](http://bradfrost.github.io/this-is-responsive/) (overload: patterns and resources)

**Books**

[Luke Wroblewski, 'Mobile First’](http://abookapart.com/products/mobile-first)  
[Ethan Marcotte, 'Responsive Web Design’](http://abookapart.com/products/responsive-web-design)

===

<!-- .slide: class="small-head crammed" -->
![NOT LIKE THIS!! How Responsive Web Design used to be](rwd/testing-devices.jpg)

===

<!-- GENERAL GUIDES -->

# ADVICE **1**
<!-- .slide: class="smalltext" -->

If you still feel that **this is *still* quite complex**…

I took the time to **answer two general questions** on Quora…

> I want to be a **web developer** but I know **absolutely nothing** about it. **What** should I learn and how and **where** can I learn it?

[See answer](https://qr.ae/TUhnLf)

---

# ADVICE **2**
<!-- .slide: class="smalltext" -->

These answers might **help you get an overview** of front-end web development code

> How much time does it takes to **learn & master HTML** + **CSS** + **JavaScript**?

[See answer](https://qr.ae/TUhnL4)

===

# QUESTIONS?

**please ask now…**

No crowding around the podium afterwards!

Talk to Graeme for module-related issues
