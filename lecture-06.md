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

# GIT/GITHUB: **1**
<!-- left-align crammed -->

- **GitHub classroom** is for your **assignment code**
- **accepting** the assignment **creates a repo**:
  - it’s in the **CTEC3905 account** not yours
  - **sign in** to see it on your **GitHub home page**
  - `git push` to it regularly
  - **do not** “upload” via GitHub, use `git push`
  - **edit/delete** files locally, **not on GitHub**
  - **clone** the repo to work on multiple machines
- use the `command-line`

---

# GIT/GITHUB: **2**

- use your **own account** for **lab exercises**
- **clone** lab exercise code into your **local work folder**
- `cd` into the **repo folder after cloning**:
  - **cloned?** `git remote set-url origin your_repo_here`
- **make repos** for **your own lab code** on GitHub first:
  - **new?** `git remote add origin your_repo_here`
- check `git remote -v` **before pushing**

---

# GIT/GITHUB: **3**

- use `git` carefully, be sure you're **in the right folder**!!
- **do not** put git repos **inside other git repos**!
- **[validate your HTML](https://validator.w3.org/)** before committing
- build an **archive** of **re-usable code** this way

---

# GIT/GITHUB: **4**
<!-- .slide: class="crammed smalltext" -->
  
How to **clone a repo** to a **new repo of your own**:

- on your machine, **open a location** where you want the clone’s folder to go
- in the folder window, **shift+right click -> open in command window here**
-	**clone** the **GitHub repo** you want to copy (e.g.):  
	`git clone https://github.com/CTEC3905/REPO_NAME_HERE.git`
-	`cd RE`… (tab to complete) into the **folder containing the cloned files**
- `dir` (Win) or `ls -al` (\*nix/OS X) to **see the cloned files**
- make a **new repo on GitHub**, then **reset the remote link** to your **new repo**:  
	`git remote set-url origin YOUR_NEW_REPO_URL_HERE.git`
- **push** the **cloned files** to your **new repo**:  
	first time: `git push -u origin master`  
  then just: `git push`

---

# GIT/GITHUB: **5**

How to **upload your changes** to **your GitHub repository**

- have an **open command prompt** in the **directory with the changed files**
- **check where** you’re **pushing to** with `git remote -v`
-	`git status` will **show the files** you have **changed** (in *red*)
-	`git add .` (the “`.`” means “all”) to **add your changes** to the git repository
-	`git status` will show **your added files** (in *green*)
-	**commit** the change with a **brief message**:  
  `git commit -m "changed title"`
- `git push` will **push** the **changed files** to **your GitHub repo**

===

<!-- RESPONSIVE DESIGN -->

# RESPONSIVE DESIGN: **1**

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

# RESPONSIVE DESIGN: **2**

Apart from the default `all` (which you can ignore) there are **three kinds** of CSS `@media` queries:

| `@media` | for: |
|:--|:--|
| `print` |	printers |
| `screen` | computer screens, tablets, phones… |
| `speech` | screenreaders that speak the page content |

---

# RESPONSIVE DESIGN: **3**

```css
@media only screen and (orientation: landscape) {
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

but **WAIT!!** …

---

# RESPONSIVE DESIGN: **4**

## **HOWEVER**…

to get started, here’s **all you need**…

- **mobile first** design using CSS (**top** of the .css file)
- [**natural** breakpoints](http://stackoverflow.com/questions/6370690/media-queries-how-to-target-desktop-tablet-and-mobile/20350990#20350990 "Follow the links and go down the rabbit-hole in this StackOverflow answer") (**not** device-specific)
- `min-width` up (**not** max-width) for **increasing widths**
- `&lt;meta name="viewport" content="width=device-width, initial-scale=1.0">` in the HTML `head`

See the [responsive starter code](https://github.com/CTEC3905/starter-code)!

---

# RESPONSIVE DESIGN: **5**

… which shows a **mobile-first CSS example**:

```css
body {
  margin: 0;
  /* more mobile/global body styles */
}
/* more mobile/global styles here &lt; 499px */

@media screen and (min-width: 500px) {
/* override mobile styles screens > 499px */
}

@media screen and (min-width: 1000px) {
/* override previous styles for screens > 999px */
}
```

---

# RESPONSIVE DESIGN: **6**

Use **[NATURAL BREAKPOINTS](https://stackoverflow.com/a/20350990/123033)**!

Design **mobile-first**, then **increase the screen width** by resizing the browser window.

Add `min-width` **breakpoints** wherever the **design becomes “broken”** or fails when the viewport width increases—  
all content should **look good in any viewport** width/height

**Avoid** large **fixed width** elements.

The [Chrome inspector mobile icon](https://developers.google.com/web/tools/chrome-devtools/device-mode/) is good for certain tests.

---

# RESPONSIVE DESIGN: **7**

- **Percentages** work well for setting basic element widths, but use `display: border-box` to ensure padding and borders **remain *inside* the element’s width**
- For **individual container elements** (e.g. a `main` tag) you can use `max-width` to keep them from **getting too wide**

> **45** to **80** characters (per line) is the ideal **line length** for text on websites  
—[The Readability Formula: Making Your Website Easy-to-Read](https://kickpoint.ca/the-readability-formula-making-your-website-easy-to-read/)

---

# RESPONSIVE DESIGN: **8**

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
![NOT LIKE THIS!! How Responsive Web Design used to be](images/testing-devices.jpg)

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

===

<!-- GENERAL GUIDES -->

# ADVICE **1**

You may still feel that **this is *still* all a bit complicated** so…

I took the time to **answer two general questions** on Quora…

> I want to be a **web developer** but I know **absolutely nothing** about it. **What** should I learn and how and **where** can I learn it?

[See answer](https://qr.ae/TUhnLf)

---

# ADVICE **2**

These answers might **help you get an overview** of front-end web development code

> How much time does it takes to **learn & master HTML** + **CSS** + **JavaScript**?

[See answer](https://qr.ae/TUhnL4)

===

<!-- CODE COMEDY -->

<section data-markdown class="big-pic small-head crammed">
![Do I know it or do I say I know it???](images/two-types-cv.jpg)
</section>

===

(see TECH3015_lecture-02, 10)

===

# QUESTIONS?

**please ask now…**

No crowding around the podium afterwards!

Talk to Graeme for module-related issues

