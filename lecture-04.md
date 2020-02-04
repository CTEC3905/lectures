# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

## **Front-End Web Development**

## Lecture 04

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

# REMINDERS
<!-- .slide: class="smalltext" -->

- **indent** your **code** properly: **2 spaces**!
- **align** opening and closing:
  - **HTML** &lt;tags&gt;&lt;/tags&gt;
  - **CSS** and **JavaScript** `{` braces `}`
- **lower-case** folder and filenames
- be sure to **complete** the **lab exercises**
- **read through** the **lecture** and **lab** notes
- `let no = [!templates, !JQuery, !Bootstrap];`

===

<!-- GIT AND GITHUB -->

# GIT: **01**
<!-- .slide: class="crammed" -->

**GIT** and **GitHub** are **used throughout the industry** including major companies like [Google](https://github.com/google/), [Linux](https://github.com/torvalds/linux/tree/master/kernel), [Microsoft](https://github.com/microsoft/), [Apple](https://github.com/apple), etc.

“**repo**” (short for “**repository**”) is a time-stamped **store for your code** to which you `add` and `commit` your code to the **repo** at *regular intervals* and `push` it to GitHub

- BlackBoard: [detailed GitHub guide](https://vle.dmu.ac.uk/webapps/blackboard/execute/content/file?cmd=view&content_id=_4498063_1&course_id=_551514_1&framesetWrapped=true)
- BlackBoard: [Video walkthrough guide](https://dmureplay.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=5ae4fefe-c3b9-4171-a381-f227e3e47c29)

**Who** still needs to get **set up** on **GitHub Classroom**?

---

# GIT **02**
<!-- .slide: class="crammed" -->

**GitHub classroom 1**

If you use your own computer [install GIT from here](https://git-scm.com/downloads)

- Go to **[GitHub classroom](https://classroom.github.com/a/u2ocjK6g)** (you may need to log into your GitHub account several times)
- **Find your P-number** from the list. This **generates a repo** in the 'ctec3905students' group with **some starter code**
- **Clone this repo** to your **working computer** and `cd` **into it**
- This is the *private* **repo for your assignment code** (accessible only for you and module staff)

---

# GIT **03**
<!-- .slide: class="crammed" -->

**GitHub classroom 2**

You can now **start work on your assignment** and **push your code commits** to **this repository**—this will be marked

- Your **GIT history** is part of the **marking scheme**
- The **starter files** contain **essential code** required for the assignment
- If you have **existing code** please examine it **carefully** against the **starter code files**
- If necessary **add your code** to the **starter files carefully**

===

<!-- ACCESSIBILITY: SHARED CTEC3905/MEDS2007 -->

# Accessibility **1**
<!-- .slide: class="crammed smalltext" -->

> Whatever your needs or preferences, there’s almost certainly a way to access the web. **Theoretically**.

> In reality, **the web is a mess**… accessibility options tend to be forgotten or stripped away, …though accessible websites and apps can… still be beautiful, innovative… user-friendly.
>
> …**This is a human rights issue**. Disabled people *need* these options in order to access the web.”

Mischa Andrews: [The inaccessible web](https://uxdesign.cc/the-inaccessible-web-how-we-got-into-this-mess-7cd3460b8e32)  

---

# Accessibility **2**

> “The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect”

Tim Berners-Lee (1997)  
[Web Accessibility Initiative announcement](https://www.w3.org/Press/IPO-announce)

---

# Accessibility **3**
<!-- .slide: class="crammed smalltext" -->

**Accessibility** has been **built into the web from the start**  
W3C (2005) [Introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php)

> “the **duty to make reasonable adjustments** requires providers to **ensure disabled people can access services**. Service providers should **anticipate the needs** of potential disabled customers…”  
—adapted from [Disabled access to websites under UK law](http://www.out-law.com/page-330)

The **Disability Equality Act (2010)** is law—you could be [sued for discrimination](http://www.seqlegal.com/blog/website-accessibility-and-equality-act-2010) if your website fails to meet [accessibility standards](https://www.abilitynet.org.uk/expert-resources/web-accessibility-resources)

---

  # Accessibility **4**

  How you can address **web access**:

  - Code accessibly, from `alt` image attributes to **semantic structure**
  - needs **incorporating from the start** of a project
  - Good **IA and navigation** help accessibility
  - HTML5 **semantic elements** are crucial
  - **valid HTML5** code is important
  - Use **[form field types](https://www.w3schools.com/html/html_form_input_types.asp)** and the `label` tag

---

# Accessibility **5**

Resources and research

- [WebAim](http://webaim.org/intro/)—**see this site first!**
- [Accessible Rich Internet Applications (ARIA)](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- [Notes on Using ARIA in HTML](https://www.w3.org/TR/aria-in-html/)—see the [1st to 5th](https://www.w3.org/TR/using-aria/#rule1) rules!
- [How to Use ARIA Effectively with HTML5](https://www.sitepoint.com/how-to-use-aria-effectively-with-html5/)

===

<!-- DESIGN PRINCIPLES: SHARED MEDS2007.02/CTEC3905.04-->

# DESIGN: **01**

Four basic principles:

- **P**roximity
- **A**lignment
- **R**epetition
- **C**ontrast

(The reverse of ‘**CRAP**’)

---

# DESIGN: **02**
<!-- .slide: class="smalltext" -->

**PROXIMITY** sets up *visual cues* that group similar items, suggesting how to ‘read’ content.

- **Group complex content** for legibility
- Display **related items** together
- Use **common styles** to connect similar items

[Guardian website](https://www.theguardian.com/uk): “most viewed” news is **grouped** together, and there‘s a **common menu style** with varying **section colours**

[BBC iPlayer website](http://www.bbc.co.uk/iplayer): **proximity** and **style** group related items

---

![a screenshot of the Guardian website](parc/guardian-230oct2018.png)

---

![a screenshot of the BBC iPlayer website](parc/bbc-iplayer-23oct2018.png)

---
<!-- 
<section title="a screenshot of the Guardian website" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/parc/guardian-230oct2018.png" data-background-size="80%"><div>&nbsp;</div></section>

<section title="a screenshot of the BBC iPlayer website" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/parc/bbc-iplayer-23oct2018.png" data-background-size="80%"><div>&nbsp;</div></section>					 -->

# DESIGN: **03**
<!-- .slide: class="smalltext" -->

**ALIGNMENT** makes page elements seem **part of a whole**, creating a **holistic feel** to the various pieces of information.

- Everything should be **placed thoughtfully** in the layout
- Every item is **connected visually** with other page elements

A strict use of **alignment** on a former version of the Oslo-based design agency Heydays website gives a pleasing sense of **coherence and simplicity**.

---

![a screenshot of the BBC iPlayer website](parc/heydays.jpg)

<!-- <section title="An obvious example of a grid-based website" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/parc/heydays.jpg" data-background-size="800px"><div>&nbsp;</div></section> -->

---

# DESIGN: **03a**

**ALIGNMENT**: **grids** are the **primary method** for achieving **alignment**.

- **The core text** on the history and use of grids in design is: Khoi Vinh and Mark Boulton (2007) [Grids Are Good](http://www.slideshare.net/huer1278ft/grids-are-good-right)
- Also see Vitaly Friedman (2007) [Designing With Grid-Based Approach](https://www.smashingmagazine.com/2007/04/designing-with-grid-based-approach/), Smashing Magazine

---

![Wireframe: stage 1](wireframes/wireframe-01.png)

---

![Wireframe: stage 2](wireframes/wireframe-02.png)

---

![Wireframe: stage 3](wireframes/wireframe-03.png)

---

![Wireframe: stage 4](wireframes/wireframe-04.png)

---

![Wireframe: finished comparison](wireframes/wireframe-finished.png)

---

<!-- <section title="Wireframe: stage 1" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/wireframes/wireframe-01.png" data-background-size="70%"><div>&nbsp;</div></section>

<section title="Wireframe: stage 2" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/wireframes/wireframe-02.png" data-background-size="70%"><div>&nbsp;</div></section>

<section title="Wireframe: stage 3" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/wireframes/wireframe-03.png" data-background-size="70%"><div>&nbsp;</div></section>

<section title="Wireframe: stage 4" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/wireframes/wireframe-04.png" data-background-size="70%"><div>&nbsp;</div></section>

<section title="Wireframe: finished comparison" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/wireframes/wireframe-finished.png" data-background-size="86%"><div>&nbsp;</div></section> -->

# DESIGN: **04**

**REPETITION** provides visual and cognitive **consistency** across common design elements

- Repeat **design themes** throughout the interface
- Consistent sizing and proportions strengthen **style**

Use: global **style rules** at the **top** of your CSS **before `@media` query breakpoints** to *style elements consistently* e.g. **colours**, image **widths** (not height), matching **heading** styles…

---

![An example of repetition in heading style](parc/karl-anders.png)

---

![Repetition used to display columns of images and titles](parc/creative-depart.jpg)

<!-- <section title="An example of repetition in heading style" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/parc/karl-anders.png" data-background-size="50%"><div>&nbsp;</div></section> -->

<!-- <section title="Repetition used to display columns of images and titles" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/parc/creative-depart.jpg" data-background-size="60%"><div>&nbsp;</div></section> -->

---

# DESIGN: **05**

**CONTRAST**

- Make **distinctly different** items *look* different
- Contrast makes content appear **visually inviting**

There are many ways to create contrast. For example:  
**colour, fonts, rules, column widths**, etc.

- Javascript plugin site [unheap.com](http://www.unheap.com/) uses **bold colours**
- A previous design for agency [Touch](http://www.thetouchagency.co.uk/) used nice **hover transitions** (the current site is slow and annoying!)

---

![A striking use of multiple kinds of contrast](parc/unheap.png)

---

![A stylish minimal use of contrast on hover](parc/touch-website.png)

<!-- <section title="A striking use of multiple kinds of contrast" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/parc/unheap.png" data-background-size="900px"><div>&nbsp;</div></section>					 -->

<!-- <section title="A stylish minimal use of contrast on hover" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/parc/touch-website.png" data-background-size="900px"><div>&nbsp;</div></section>					 -->

<!-- END DESIGN PRINCIPLES -->

===

<!-- WIREFRAMES: SHARED CTEC3905.04/MEDS2007.02 -->

# WIREFRAMES **01**
<!-- .slide: class="smalltext" -->

## **MOBILE FIRST** DESIGN

- assemble your **content** in a separate folder
- store written content in **plain text files**
- keep **unsized images** outside your web folder
- design your **mobile screens** first
- **think visually** before diving into code
- **map your content** onto your wireframes
- let your content form the **menu structure**
- how will **users navigate** through your site?

---

<!-- .slide: class="big-pic small-head crammed" -->
From simple **hand-drawn sketches**…

![sketches of mobile wireframes](wireframes/sketched-wireframes-01.png)

---

<!-- .slide: class="big-pic small-head crammed" -->
![sketches of mobile wireframes](wireframes/sketched-wireframes-02.jpg)

---

<!-- .slide: class="big-pic small-head crammed" -->
To complete **visual mock-ups**…

![digital mobile wireframes](wireframes/mobile-wireframe-userflow-01.jpg)

---

<!-- .slide: class="big-pic small-head crammed" -->
…for **complex interfaces** in fine detail

![digital mobile wireframes](wireframes/mobile-wireframe-userflow-02.jpg)

---

# WIREFRAMES **07**
<!-- .slide: class="smalltext" -->

Useful wireframe references - view the top one first:

- [User Experience Design – The importance of wireframe](https://cs2024.wordpress.com/2015/10/02/user-experience-design-the-importance-of-wireframe/)  
—Esmund Koh, 2015
- [HealthConnect – Responsive Website Design (case study)](https://britzerbo.wordpress.com/2013/06/10/healthconnect-responsive-website-design/)  
—Brit Zerbo, 2013
- [15 Beautiful Examples of Mobile App Wireframe Sketching](https://1stwebdesigner.com/mobile-app-wireframe-sketching/)  
—Ben Bate, 2017

**DO NOT** be tempted by any "website template" adverts!! Templates (and "build a responsive website" tutorials) may look fine, but **will not produce a good project**. Your **own code** is more impressive :-)

===

<!-- INFORMATION ARCHITECTURE: SHARED CTEC3905/MEDS2007 -->

# INFORMATION ARCHITECTURE (IA): **1**
<!-- .slide: class="smallhead" -->
  
> If you’ve ever tried to use something and thought, “where am I supposed to go next?” or “this doesn’t make any sense,” you are encountering an issue with an information architecture.  
—[What is Information Architecture?](http://www.iainstitute.org/what-is-ia)

---

# IA: **2**
<!-- .slide: class="smalltext" -->

## What is **Information Architecture**?

- The **art and science** of structuring and classifying websites/intranets/apps to help people find and manage information
- A **discipline** and community of practice bringing principles of design and architecture to online development

Entire university courses cover Information Architecture—[search for "library science and information architecture"](https://www.google.co.uk/search?q=librry+science+and+information+archtectre&oq=librry+science+and+information+archtectre&aqs=chrome..69i57.7711j0j7&sourceid=chrome&ie=UTF-8#q=library+science+and+information+architecture)

---

<h2>IA: <strong>3</strong> - How did <strong>IA</strong> begin?</h2>

<img style="float:left;" src="https://raw.githubusercontent.com/front-end-materials/images/master/ia/information-architecture-book.jpg" alt="Information Architecture book cover">

<p style="width: 58%; float: right; margin-top: .2em;">In 1998 Peter Morville and co-author Louis Rosenfeld wrote <a href="https://wordery.com/information-architecture-louis-rosenfeld-9781491911686?currency=GBP" title="Cheapest copy of 'Information Architecture' we could find">Information Architecture for the World Wide Web</a>
<br>
(4th edition 2015)
<br>
<br>
Known as <em>The Polar Bear Book</em> it is considered to be <strong>the</strong> essential text on the subject.</p>

---

# IA: **4**

Information Architecture has origins in **library science**

- The development of “**knowledge-organization** systems”
- Study of how to **categorize**, **catalogue**, **locate** resources

So it's a kind of cognitive and visual **data structure**

---

# IA: **4a**
<!-- .slide: class="smalltext" -->

Information Architecture uses **Cognitive Psychology** research

- **Cognitive load**: how much information we can process at any time—avoiding information overload ([rule of 7](http://neuromavin.com/cognitive-limits-social-networks-and-dunbars-number/)).
- **Mental models**: the assumptions users have—information is easier to discover in familiar places.
- **Decision making**: the cognitive process of making a choice or selecting an option—IA helps make decisions by providing contextual information at key points.

[The Magical Number Seven… George A. Miller (1956)](http://psychclassics.yorku.ca/Miller/ "…Plus or Minus Two: Some Limits on our Capacity for Processing Information. A classic text.")

[Complete Beginners Guide to Information Architecture](http://www.uxbooth.com/articles/complete-beginners-guide-to-information-architecture/ "A summary of the above findings")

---

<style>
.ia-diagram {
	position: relative;
	box-sizing: border-box;
	top: .6em;
	padding: 8px;
	width: 360px;
	height: 350px;
	background: #ccc;
	color: #666;
	float: left;
}
.ia-diagram div {
	position: absolute;
	width: 200px;
	height: 200px;
    text-align: center;
	box-sizing: border-box;
	border-radius: 50%;
}
</style>

<h1>IA: <strong>5</strong></h1>
  
<div class="ia-diagram">
<div style="left: 76px; top: 8px; background: rgba(256,100,100,0.5); line-height: 170px;">Users</div>
<div style="bottom: 8px; left: 8px; background: rgba(100,256,100,0.5); line-height: 240px; transform: rotate(32deg);">Content</div>
<div style="bottom: 8px; right: 8px; background: rgba(100,100,256,0.5); line-height: 240px; transform: rotate(-32deg);">Context</div>
<strong style="position: absolute; text-align: center; left: 43%; top: 44%; font-size: 1.5em; color: #444; text-shadow: 0 0 4px #fff">IA</strong>
</div>

<ul style="width: 56%; margin-left: 10px; margin-top: -0.28em; float: right;">
<li><strong>Users</strong>: who they are, what are their information-seeking behaviours and needs</li>
<li><strong>Content</strong>: volume, format, metadata, structure, labels (e.g. menus)</li>
<li><strong>Context</strong>: business model, aim of website, cultural background, constraints</li>
</ul>

---

![Classic Informaiton Architecture infographic by Louis Rosenfeld](ia/rosenfeld-users-content-context.png)

<!-- <section title="Classic Informaiton Architecture infographic by Louis Rosenfeld" data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/ia/rosenfeld-users-content-context.png" data-background-size="800px"><div>&nbsp;</div></section> -->
    
---

# IA: **6**
<!-- .slide: class="smalltext" -->

**the information backbone of a website**

- **Content inventory/audit**  
locate and identify and check site content
- **Information grouping**  
connect content with user-centered relationships
- **Taxonomy development**  
a controlled vocabulary throughout  

Jennifer Cardello: [The Difference Between IA and Navigation](https://www.nngroup.com/articles/ia-vs-navigation/)  

---

# IA: **7**
<!-- .slide: class="smalltext" -->

**What is Architecture?**

Condensed from Cal Henderson, [Building Scalable Web Sites](http://shop.oreilly.com/product/9780596102357.do) (2006)

**if buildings were like software**, the architect would be involved in the actual building process, from … foundations … to … fixtures. …starting with a couple of rooms and basic amenities, **people would… start living there before the building was complete**. When the building work was about to finish …more people would turn up and start living there, too.

---

## Building around users
<!-- .slide: class="smalltext" -->

…new residents need **new features**. The architect would design these, augmenting the original design. But the **current residents** would **continue using the house** while it was extended, all the time complaining about the building work.

In fact… **more people would move in** while extensions were being built. When the modifications were complete, the the newcomers would **request more changes**.

---

## Plan from the start
<!-- .slide: class="smalltext" -->

The key… is **planning for all this from the start**. If thean architect started out by building a huge, complex house, it would be **overkill**. By the time it was ready, the residents **would have gone elsewhere** to live in a smaller house built in a fraction of the time.

If extending our house (website) takes too long, **people might move elsewhere**. We need start at the right scale and design things to be **extended as easily as possible**.

---

## Minimize effort
<!-- .slide: class="smalltext" -->

We're **not going to get anything right first time**. In the [scaling](https://www.nngroup.com/articles/scaling-user-interfaces/ "Scaling User Interfaces: An Information-Processing Approach to Multi-Device Design") of a typical application, **every aspect and feature** is probably going to be **revisited and [refactored](http://www.refactoring.com/ "a change made to the internal structure of software to make it easier to understand and cheaper to modify without changing its observable behavior")**.

That's fine—the task of an application architect is to **minimize the time it takes to [refactor](https://sourcemaking.com/refactoring "A big site about refactoring") each component**, through **careful initial and ongoing design**.

===

<!-- COLOUR SCHEME LINK -->

Online **colour scheme** chooser: [Paletton](http://paletton.com/)

![Paletton.com colour scheme designer](general/paletton.png)

===

<!-- CODE COMEDY -->

<!-- .slide: class="big-pic small-head crammed" -->

## **GIT** might make you go \*\*\*\*\*!

![Git commit messages with swearing](comedy/shithub-commits.png)
