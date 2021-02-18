# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

### **Front-End Web Development**

<h2>Guest Session 2:<br>
<strong>Accessible Information</strong></h2>

===

# OVERVIEW

- [Accessibility, Information Architecture, wireframes](#/2)
- [Information Architecture (IA)](#/3)
- [Wireframes](#/4)
- [Information Design](#/5)
- [Eye-tracking studies](#/6)

===

<!-- ACCESSIBILITY 13oct2020: SHARED CTEC3905.04/MEDS2007.02-->

## ACCESSIBILITY 01

> “The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect”

Tim Berners-Lee (1997)  
[Web Accessibility Initiative announcement](https://www.w3.org/Press/IPO-announce)

---

## ACCESSIBILITY 02

> “**the web is a mess**… accessibility options tend to be forgotten or stripped away, …though accessible websites and apps can… still be beautiful, innovative… user-friendly.
>
> …**This is a human rights issue**. Disabled people *need* these options in order to access the web.”

Mischa Andrews: [The inaccessible web](https://uxdesign.cc/the-inaccessible-web-how-we-got-into-this-mess-7cd3460b8e32)  

---

## ACCESSIBILITY 03
<!-- .slide: class="crammed" -->

**Accessibility** was **built into the web from the start**  
W3C (2005) [Introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php)

> “the **duty to make reasonable adjustments** requires providers to **ensure disabled people can access services**. Service providers should **anticipate the needs** of potential disabled customers…”  
—adapted from [Disabled access to websites under UK law](http://www.out-law.com/page-330)

**Disability Equality Act (2010)**—you can be [sued for discrimination](http://www.seqlegal.com/blog/website-accessibility-and-equality-act-2010) if your website fails [accessibility standards](https://www.abilitynet.org.uk/expert-resources/web-accessibility-resources)

---

## ACCESSIBILITY 04

How you can address **web access**:

- accessible code from `alt` image attributes to **semantic structure**
- needs **incorporating from the start** of a project
- good **IA and navigation** help accessibility
- HTML5 **semantic elements** are crucial
- **valid HTML5** code is important
- use **[form field types](https://www.w3schools.com/html/html_form_input_types.asp)** and the `label` tag

---

## ACCESSIBILITY 05

Resources and research

- [WebAim](http://webaim.org/intro/)—**see this site first!**
- [Accessible Rich Internet Applications (ARIA)](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- [Notes on Using ARIA in HTML](https://www.w3.org/TR/aria-in-html/)—see rules [1–5](https://www.w3.org/TR/using-aria/#rule1) rules!
- [How to Use ARIA Effectively with HTML5](https://www.sitepoint.com/how-to-use-aria-effectively-with-html5/)

<!-- INFORMATION ARCHITECTURE: SHARED CTEC3905.04/MEDS2007.02 THIS: updated 2feb2021 -->
===

## INFORMATION ARCHITECTURE (IA): 01

> If you’ve ever tried to use something and thought, “where am I supposed to go next?” or “this doesn’t make any sense,” you are encountering an issue with an **information architecture**.

<small>[What is Information Architecture?](http://www.iainstitute.org/what-is-ia)</small>

---

## IA: 02
<!-- .slide: class="crammed" -->

Information Architecture is:

- the **art and science** of structuring and classifying websites to help people find and manage information
- a **discipline** and community bringing principles of design and architecture to online development

Entire university courses cover IA—[search "library science and information architecture"](https://www.google.co.uk/search?q=librry+science+and+information+archtectre&oq=librry+science+and+information+archtectre&aqs=chrome..69i57.7711j0j7&sourceid=chrome&ie=UTF-8#q=library+science+and+information+architecture)

More information: [Presenting Information Architecture](https://webstyleguide.com/wsg3/3-information-architecture/4-presenting-information.html)

---

<h2>IA: 03 - How did <strong>IA</strong> begin?</h2>

<img style="float:left;" src="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/wireframes/information-architecture-book.jpg" alt="Information Architecture book cover">

<p style="width: 58%; float: right; margin-top: .2em;">In 1998 Peter Morville and co-author Louis Rosenfeld wrote <a href="https://www.amazon.co.uk/Information-Architecture-Beyond-Louis-Rosenfeld/dp/1491911689/">Information Architecture for the World Wide Web</a>
<br>
(4th edition 2015)
<br>
<br>
Known as <em>The Polar Bear Book</em> it is considered to be <strong>the</strong> essential text on the subject.</p>

---

## IA: 04

Information Architecture has origins in **library science**

- The development of “**knowledge-organization** systems”
- Study of how to **categorize**, **catalogue**, **locate** resources

So it's a kind of *cognitive* and *visual* **data structure**

…now **pick a number** between **one** and **10**…

---

## IA: 05
<!-- .slide: class="crammed" -->

Information Architecture uses **Cognitive Psychology**

- **Cognitive load**: how much information we can process at any time—avoiding information overload ([rule of 7](http://neuromavin.com/cognitive-limits-social-networks-and-dunbars-number/), [The Magical Number Seven… George A. Miller (1956)](http://psychclassics.yorku.ca/Miller/ "…Plus or Minus Two: Some Limits on our Capacity for Processing Information. A classic text.")).
- **Mental models**: the assumptions users have—information is easier to discover in familiar places.
- **Decision making**: the cognitive process of making a choice or selecting an option—IA helps make decisions by providing contextual information at key points.

<small>[Complete Beginners Guide to Information Architecture](http://www.uxbooth.com/articles/complete-beginners-guide-to-information-architecture/ "A summary of the above findings")</small>

---

<style>
	.ia-diagram {
		position: relative;
		box-sizing: border-box;
          text-align: center;
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
		box-sizing: border-box;
		border-radius: 50%;
	}
</style>

<h2>IA: 06</h2>

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

## IA: 07

the information backbone of a website:

- **Content inventory/audit**  
	locate and identify and check site content
- **Information grouping**  
	connect content with user-centered relationships
- **Taxonomy development**  
	a controlled vocabulary throughout  

<small>[The Difference Between IA and Navigation](https://www.nngroup.com/articles/ia-vs-navigation/) —Jennifer Cardello</small>

---

<!-- .slide: class="crammed" -->
## IA: 08

What is Architecture? (Cal Henderson (2006) [Building Scalable Web Sites](http://shop.oreilly.com/product/9780596102357.do))

> **if buildings were like software**, the architect would be involved in the actual building process, from … foundations … to … fixtures. …starting with a couple of rooms and basic amenities, **people would… start living there before the building was complete**. When the building work was about to finish …more people would turn up and start living there, too.

<!-- ---
## Building around users…

> …new residents need **new features**. The architect would design these, augmenting the original design. But the **current residents** would **continue using the house** while it was extended, all the time complaining about the building work.
>
> In fact… **more people would move in** while extensions were being built. When the modifications were complete, the the newcomers would **request more changes**.
-->

---

<!-- .slide: class="crammed" -->
## …plan from the start

> The key… is **planning for all this from the start**. If an architect started out by building a huge, complex house, it would be **overkill**. By the time it was ready, the residents **would have gone elsewhere** to live in a smaller house built in a fraction of the time.
>
> If extending our house (website) takes too long, **people might move elsewhere**. We need start at the right scale and design things to be **extended as easily as possible**.

---

<!-- .slide: class="crammed" -->
## IA 09

### Minimize effort

> You're **not going to get everything right first time**. In the [scaling](https://www.nngroup.com/articles/scaling-user-interfaces/ "Scaling User Interfaces: An Information-Processing Approach to Multi-Device Design") of a typical website, **every aspect and feature** is probably going to be **revisited and [refactored](http://www.refactoring.com/ "a change made to the internal structure of software to make it easier to understand and cheaper to modify without changing its observable behavior")**.
> 
> That's fine—the task of an application architect is to **minimize the time it takes to [refactor](https://sourcemaking.com/refactoring "A big site about refactoring") each component**, through **careful initial and ongoing design**.

---

## IA 10
<!-- .slide: class="left-align" -->

Good article and video—you can **double-check** your site's **Information Architecture**:

[An Excellent Beginner's Guide To Information Architecture](https://careerfoundry.com/en/blog/ux-design/a-beginners-guide-to-information-architecture/)

<!-- INFORMATION ARCHITECTURE END -->

===

<!-- WIREFRAMES 13oct2020: SHARED CTEC3905.04/MEDS2007.02 -->

## WIREFRAMES 01

Mobile First Design

- design your **mobile screens** first
- let your content form the **menu structure**
- how will **users navigate** through your site?
- **think visually** *before* diving into *code*

---

## WIREFRAMES 02

Content Preparation

- assemble raw **content** in a separate folder
- store written content in **plain text files**
- keep **unsized images** outside your web folder
- **map your content** onto your wireframes

<!-- CHECK: DUPLICATED ELSEWHERE -->

---

<!-- .slide class="big-pic crammed" -->

From simple **hand-drawn sketches**…

![sketches of mobile wireframes](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/wireframes/sketched-wireframes-01.png)

---

![sketches of mobile wireframes](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/wireframes/sketched-wireframes-02.jpg)

---

To complete **visual mock-ups**…

![digital mobile wireframes](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/wireframes/mobile-wireframe-userflow-01.jpg)

---

…for **complex interfaces** in fine detail

![detailed digital mobile wireframes](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/wireframes/mobile-wireframe-userflow-02.jpg)

---

## WIREFRAMES 03
<!-- .slide: class="crammed" -->

Useful wireframe references - view the top one first:

- [HealthConnect – Responsive Website Design (case study)](https://britzerbo.wordpress.com/2013/06/10/healthconnect-responsive-website-design/)  —Brit Zerbo, 2013
- [15 Beautiful Examples of Mobile App Wireframe Sketching](https://1stwebdesigner.com/mobile-app-wireframe-sketching/)  
—Ben Bate, 2017
- [User Experience Design – The importance of wireframe](https://cs2024.wordpress.com/2015/10/02/user-experience-design-the-importance-of-wireframe/)  
—Esmund Koh, 2015

**DO NOT** be tempted by "website template" adverts!! Templates (and "build a responsive website" tutorials) may look fine, but your **own code** will make **a better project**

<!-- END WIREFRAMES -->

===

## INFORMATION DESIGN **01**

Information **Architecture** is *getting around*  
Information **Design** is good *visual presentation*

![Information Design diagram](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/information-design.png)

<small>[What is Information Design?](https://online-learning.com/information-design/)</small>

---

## INFORMATION DESIGN **02**
<!-- .slide: class="crammed" -->

Information Architecture **makes foraging easier**  
**Information Design** conveys *meaning*

> Information design is the skill and practice of **preparing information** so people can use it with **efficiency** and **effectiveness**. Where data is **complex** or **unstructured**, **visual representation** expresses meaning more clearly

---

## INFORMATION DESIGN **03**
<!-- .slide: class="crammed" -->

We **forage** for information like we do for **resources**

![food/information foraging comparison table](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/information-foraging.png)

<small>[Information Foraging: A Theory of How People Navigate on the Web](https://www.nngroup.com/articles/information-foraging/)</small>

---

## INFORMATION DESIGN **04**
<!-- .slide: class="crammed" -->

**Small changes**: give users a brief cue about what's in the text, **before they commit to reading** it, then use a **longer headline**

![Eyebrow headline example](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/eyebrow-headline.png)

<small>[Aid User Scanning by Using Eyebrow Headlines](https://uxmovement.com/content/how-you-can-aid-user-scanning-by-using-eyebrow-headlines/)</small>

---

## INFORMATION DESIGN **05**
<!-- .slide: class="crammed" -->

**Vast information**: simple surface, drill-down for more

![Periodic table](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/periodic-table.png)

<small>[Interactive Periodic Table](https://ptable.com/)</small>

---

## INFORMATION DESIGN **06**
<!-- .slide: class="crammed" -->

![Information Design examples](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/information-design-pinterest.png)

<small>[Pinterest: Information Design](https://www.pinterest.com/search/pins/?q=information%20design&rs=typed)</small>

---

## INFORMATION DESIGN **07**
<!-- .slide: class="crammed" -->

![Information Design examples](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/information-design-pinterest-daniel.png)

<small>[Pinterest: Daniel Hunley Information Design](https://www.pinterest.com/danielhunley/information-design/)</small>

---

## INFORMATION DESIGN **08**
<!-- .slide: class="crammed" -->

![Laws of Simplicity website](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/laws-of-simplicity.png)

<small>[John Maeda's Laws of Simplicity](http://lawsofsimplicity.com/)</small>

===

## EYE-TRACKING **1**

**We tend to follow the gaze of others**

and since birth we follow directions as to  
**where we should be looking/going**

The following two examples show a baby and a headline for baby skin care.

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/eye-tracking/eyetracking-baby-face.jpg" data-background-size="contain" alt="baby looking out from an advert" -->

---

## EYE-TRACKING **2**

**the baby’s face draws attention away from the message**

This is a problem because the message isn’t commanding attention

Now see the browsing pattern with baby facing the text:

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/front-end-materials/images/master/eye-tracking/eyetracking-baby-look.jpg" data-background-size="contain" alt="baby looking at a headline in an advert" -->

---

## EYE-TRACKING **3**

users focused on the baby’s face again (from the side) and **followed the baby’s line of sight** to the **headline** and **opening text**.

Even the area of text that the baby’s chin was pointing to had more attention!

<small><a href="https://neilpatel.com/blog/eye-tracking-studies/">https://neilpatel.com/blog/eye-tracking-studies/</a>Neil Patel: 7 Marketing Lessons from Eye-Tracking Studies<br>
(*dismiss loading screen*)</small>

<small>—Neil Patel: [7 Marketing Lessons from Eye-Tracking Studies](https://neilpatel.com/blog/eye-tracking-studies/)<br>
(*dismiss loading screen*)</small>

===

# QUESTIONS?

