# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

## **Front-End Web Development**

## Guest Session 1: Design Principles

===

# OVERVIEW

- [PARC design principles](https://tech3015.github.io/presents?lecture-04)
- [Dark UI](https://tech3015.github.io/presents?lecture-07)
- plus basic RWD page layout demo

===

<!-- NEW -->
<!-- DESIGN PRINCIPLES: SHARED MEDS2007.02/CTEC3905.04-->

## DESIGN PRINCIPLES

Four basic principles:

- [**P**roximity](#/3)
- [**A**lignment](#/4)
- [**R**epetition](#/5)
- [**C**ontrast](#/6)

(The reverse of ‘**CRAP**’)

===

## DESIGN: **01**
<!-- .slide: class="crammed" -->

**PROXIMITY** sets up *visual cues* that group similar items, suggesting how to ‘read’ content.

- **Group complex content** for legibility
- Display **related items** together
- Use **common styles** to connect similar items

[Guardian website](https://www.theguardian.com/uk): “most viewed” news **grouped** together, **common menu style** has **section colours**

[BBC iPlayer website](http://www.bbc.co.uk/iplayer): **proximity** and **style** group related items

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/guardian-230oct2018.png" data-background-size="contain" -->

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/bbc-iplayer-23oct2018.png" data-background-size="contain" -->			

===

## DESIGN: **02**
<!-- .slide: class="crammed" -->

**ALIGNMENT** makes page elements seem **part of a whole**, creating a **holistic feel** to the various pieces of information.

- Everything should be **placed thoughtfully** in the layout
- Every item is **connected visually** with other page elements

A strict use of **alignment** on a former version of the Oslo-based design agency Heydays website gives a pleasing sense of **coherence and simplicity**.

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/heydays.jpg" data-background-size="contain" -->		

===

## DESIGN: **03**

**ALIGNMENT**: **grids** are the **primary method** for achieving **alignment**.

- **The core text** on the history and use of grids in design is: Khoi Vinh and Mark Boulton (2007) [Grids Are Good](http://www.slideshare.net/huer1278ft/grids-are-good-right)
- For web-based grids see Sean Hodge (2008) [Grid-Based Design](https://www.smashingmagazine.com/2008/03/grid-based-design-six-creative-column-techniques/), Smashing Magazine

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/grids/wireframe-01.png" data-background-size="contain" -->	

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/grids/wireframe-02.png" data-background-size="contain" -->	

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/grids/wireframe-03.png" data-background-size="contain" -->	

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/grids/wireframe-04.png" data-background-size="contain" -->	

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/grids/wireframe-finished.png" data-background-size="contain" -->	

===

## DESIGN: **04**

**REPETITION** provides visual and cognitive **consistency** across common design elements

- Repeat **design themes** throughout the interface
- Consistent sizing and proportions strengthen **style**

Use: global **style rules** at the **top** of your CSS **before `@media` query breakpoints** to *style elements consistently* e.g. **colours**, image **widths** (not height), matching **heading** styles…

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/karl-anders.png" data-background-size="contain" -->	

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/creative-depart.jpg" data-background-size="contain" -->	

===

## DESIGN: **05**
<!-- .slide: class="crammed" -->

**CONTRAST**

- Make **distinctly different** items *look* different
- Contrast makes content appear **visually inviting**

There are many ways to create contrast. For example:  
**colour, fonts, rules, column widths**, etc.

- Javascript plugin site [unheap.com](http://www.unheap.com/) uses **bold colours**
- A previous design for agency [Touch](http://www.thetouchagency.co.uk/) used nice **hover transitions** (the current site is slow and annoying!)

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/unheap.png" data-background-size="contain" --> 

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/design/touch-website.png" data-background-size="contain" -->

===

<!-- SIMPLICITY QUOTES -->

### SIMPLICITY
<!-- .slide: class="crammed smalltext" -->

- **“Simplicity is the ultimate form of sophistication.”** —Leonardo da Vinci
- **“Don’t make me think.”** —Steve Krug

### COMMUNICATION

- **“People react positively when things are clear and understandable.”**  
—Dieter Rams

- **“The main goal is not to complicate the already difficult life of the consumer.”** —Raymond Loewy

### DESIGN

- **“White space is to be regarded as an active element, not a passive background.”** —Jan Tschichold
- **“A lot of what we are doing is getting design out of the way.”** —Jonathan Ive

<!-- /NEW -->


<!-- DARK UI: SHARED TECH3015.7 -->
===

## DARK UI **01**
<!-- .slide: class="crammed" -->

> **Dark Patterns** are UI tricks that make you do things you didn't mean to, like **opting in** or **signing up**.
>
> …because you **skim read** and **make assumptions**… companies take advantage by **tricking you** into doing things, e.g. by making page elements **appear** to say one thing when they **really** mean another.  
>
> **Defend yourself** by learning about Dark Patterns.

<small>condensed from [DarkPatterns.org](https://www.darkpatterns.org/), Harry Brignull (2019)</small>

---

## DARK UI **04**

A brief explanation with examples:

<iframe width="740" height="416" src="https://www.youtube.com/embed/kxkrdLI6e6M" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

## DARK UI **05**
<!-- .slide: class="crammed" -->

- [**Trick Questions**](https://www.darkpatterns.org/types-of-dark-pattern/trick-questions) - giving answers you didn't mean
- [**Sneak into Basket**](https://www.darkpatterns.org/types-of-dark-pattern/sneak-into-basket) - additional items on checkout
- [**Crap Hotel**](https://www.darkpatterns.org/types-of-dark-pattern/roach-motel) - you can't easily get out of something
- [**Privacy Zuckering**](https://www.darkpatterns.org/types-of-dark-pattern/privacy-zuckering) - tricked into sharing information
- [**Price comparison**](https://www.darkpatterns.org/types-of-dark-pattern/price-comparison-prevention) - hard to compare a price with others
- [**Misdirection**](https://www.darkpatterns.org/types-of-dark-pattern/misdirection) - a highlighted thing distracts from another

<small>Adapted from [Types of Dark UI Pattern](https://www.darkpatterns.org/types-of-dark-pattern)…</small>

---

## DARK UI **06**
<!-- .slide: class="crammed" -->

- [**Hidden Costs**](https://www.darkpatterns.org/types-of-dark-pattern/hidden-costs) - the final checkout has unexpected charges
- [**Bait and Switch**](https://www.darkpatterns.org/types-of-dark-pattern/bait-and-switch) - doing one thing makes another happen
- [**Confirmshaming**](https://www.darkpatterns.org/types-of-dark-pattern/confirmshaming) - guilts you into opting in
- [**Disguised Ads**](https://www.darkpatterns.org/types-of-dark-pattern/disguised-ads) - ads disguised as content or navigation
- [**Forced Continuity**](https://www.darkpatterns.org/types-of-dark-pattern/forced-continuity) - no-warning charges after a free trial
- [**Friend Spam**](https://www.darkpatterns.org/types-of-dark-pattern/friend-spam) - email/permissions then spam your contacts

<small>…Adapted from [Types of Dark UI Pattern](https://www.darkpatterns.org/types-of-dark-pattern)</small>

---

## DARK UI **07**
<!-- .slide: class="crammed" -->

[@darkpatterns Twitter feed](https://twitter.com/darkpatterns) collects examples!

![DarkPatterns on Twitter](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-patterns-twitter.png)

---

**MISDIRECTION 1**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-allow-all.jpg)

---

**MISDIRECTION 2**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-buy-now.jpg)

---

**PRE-SELECTED CONFUSING OPTIONS**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-confusing-cookies.jpg)

---

**ARE YOU SURE?**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-jump-hoops.jpg)

---

**DON'T MISS OUT!**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-miss-out.jpg)

---

**NO MEANS YES**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-no-yes.jpg)

---

**shhh… opt out**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-opt-out.jpg)

---

**Arrggh… opt out??**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/cookie-overload.png)

---

**FAKE PANIC!**

examination of the JavScript shows numbers calculated at random intervals

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-panic.png)

---

**EMOTIONAL BLACKMAIL…**

![](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/dark-ui-shame.jpg)

---

## ~DARK~ LIGHT UI **08**
<!-- .slide: class="crammed" -->

A good adaptation to user scanning and presumptions:

![left-to-right bias](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/signup-vs-signin.png)

<small>[Why ‘Sign Up’ and ‘Sign In’ Button Labels Confuse Users](https://uxmovement.com/buttons/why-sign-up-and-sign-in-button-labels-confuse-users/)</small>

---

## ~DARK~ LIGHT UI **09**
<!-- .slide: class="crammed" -->

Left is *past*, right is *future*:

![dialog box buttons](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/left-to-right-mapping.png)

<small>[Why ‘Ok’ Buttons in Dialog Boxes Work Best on the Right](https://uxmovement.com/buttons/why-ok-buttons-in-dialog-boxes-work-best-on-the-right/)</small>

===

# QUESTIONS?

