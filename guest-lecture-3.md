# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

## **Front-End Web Development**

<h2>Guest Session 3:<br>
<strong><small>MOBILE NAV, DESIGN TRENDS</small></strong></h2>

===

# OVERVIEW

- [Mobile Navigation Research](#/2)
- [The Website Timeline](#/3)
- [Content Strategy](#/4)
- [Style Guides](#/5)
- [Design Trends (links)](#/6)
- [Web Typography](#/7)

<!-- MOBILE NAVIGATION: shared with TECH3015 lecture 6 -->
===

## MOBILE NAVIGATION **01**
<!-- .slide: class="crammed" -->

Tapping, screen size, thumb reach affect mobile navigation

![In-place drill down example](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/mobile-finger-thumb.png)

<small>[Bottom Navigation Pattern On Mobile Web Pages: A Better Alternative? (2019)](https://www.smashingmagazine.com/2019/08/bottom-navigation-pattern-mobile-web-pages/)</small>

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/mobile-thumb-reach-01.png" data-background-size="contain" -->

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/mobile-thumb-reach-02.png" data-background-size="contain" -->

---

## MOBILE NAVIGATION **02**
<!-- .slide: class="crammed" -->

![Bottom navigation bar](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/mobile-bottom-nav.png)

Bottom navigation bars (iOS Tab Bar, Android Bottom Nav) stay in place and should be limited to five items

<small>[Design for Mobile (DZone 2016)](https://dzone.com/articles/design-for-mobile-app-ui-best-practices-part-2)</small>

---

## MOBILE NAVIGATION **03**
<!-- .slide: class="crammed" -->

Optimal button size:

![Optimal button size](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/optimal-button-size.png)

> users had the **lowest touch accuracy** on buttons **less than 42 pixels**. Buttons **over 72 pixels** also had low accuracy.

---

> The **highest accuracy** was found with buttons **between 42-72 pixels** — 42 pixels is the minimum and 72 pixels is the maximum button size.

---

> The **most preferred button size was 60 pixels**, which is about the middle of the range. The 72 pixel button produced the **highest touch accuracy** and was **preferred by older users**.

---

## MOBILE NAVIGATION **04**
<!-- .slide: class="crammed" -->

Optimal button spacing:

![Optimal button spacing](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/optimal-button-spacing.png)

<small>[Optimal Size and Spacing for Mobile Buttons (UX Movement, 2019)](https://uxmovement.com/mobile/optimal-size-and-spacing-for-mobile-buttons/)</small>

---

## MOBILE NAVIGATION **05**

For **good** and **bad** examples of **mobile navigation**

see [Design for Mobile: App UI Best Practices: Part I](https://dzone.com/articles/design-for-mobile-app-ui-best-practices-part-1)

---

## MOBILE NAVIGATION **06**

- [complex navigation patterns for responsive design](https://bradfrost.com/blog/post/complex-navigation-patterns-for-responsive-design/)
- [Luke Wroblewski: Mobile First (free to read)](http://mobile-first.abookapart.com/)

---

## MOBILE FRIENDLY TEST
<!-- .slide: class="crammed" -->

Once your website is live, for a deeper dive into  
mobile-freindly design and building, check it with  
Google's [Is your web page mobile-friendly?](https://search.google.com/test/mobile-friendly)

===

## THE WEBSITE TIMELINE

IA, research, wireframes, coding… fall into five areas:

1. **planning**: who is this for?
2. **content**: preparing and sorting
3. **design**: the PARC principles+
4. **development**: coding the site
5. **deployment**: launching on the web

These will overlap!

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/website-process.png" data-background-size="contain" -->

===

## CONTENT STRATEGY **01**
<!-- .slide: class="crammed" -->

> “when you’re designing a website, you should think about your content first.”
> 
> “we often created sites without thinking about strategy at all … we would first design a site that looked nice and matched our branding. Next, we made a list of all the stuff we wanted to put on the site (content), and then tried to fit all of our stuff into the newly designed site.”

<small>Clarissa Peterson (2014), [Learning Responsive Web Design](http://www.learningrwd.com/)</small>

---

## CONTENT STRATEGY **02**
<!-- .slide: class="crammed" -->

The infinite "chicken and egg" loop:

- **Project manager:** We need a website for client X
- **Designer:** I can’t start the design until I see some content!
- **Programmer:** I can’t code the design without a style guide
- **Writer:** I can’t start writing until I know the strategy
- **Project manager:** (stressed) we need a website…

Content strategy is the chicken *and* the egg…

---

## CONTENT STRATEGY **03**

labels, headings, URLs (CSS classes, JavaScript functions)…

> There are only two hard things in Computer Science: cache invalidation and **naming things**

<small>—Phil Karlton (Netscape engineer)</small>

---

## CONTENT STRATEGY **04**
<!-- .slide: class="crammed" -->

![Job Stories diagram](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/job-story.png)

Are **Job Stories** the new **User Stories**?

[Designing features using *Job Stories*](https://www.intercom.com/blog/using-job-stories-design-features-ui-ux/)

---

## CONTENT STRATEGY **05**
<!-- .slide: class="crammed" -->

Writing **text content**:

- use **subheadings** and **brief paragraphs**!
- some sites need long, detailed copy 
- others must be stripped to the bare minimum 
- or you can strike a balance between the two:
  - up-front **simplicity** > **details** on request

**drill down**: a user-interface *design pattern*—users see a summary but can view more detail—you write text for both

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/spotify-drill-down-tree.jpg" data-background-size="contain" -->

---

Simple In-Place Drill Down:

![In-place drill down example](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/ui/ux_in_place_drill_down.gif)

<small>[Appian UX Design Guide](https://docs.appian.com/suite/help/19.3/drilldown-pattern.html)</small>

---

## CONTENT STRATEGY **06**
<!-- .slide: class="crammed" -->

Search Engine Optimisation (**SEO**)

> Never, ever pay for SEO! Instead, build it in

- **tiered headings**: one `h1` tag per page, `h2` for each section
- **semantic HTML5 tags** are essential
- **structured content** (subheadings, lists, tables…)

The [Google SEO Starter Guide](https://support.google.com/webmasters/answer/7451184) is excellent!

---

## CONTENT STRATEGY **07**
<!-- .slide: class="crammed" -->

Are your audience:

- **Educated** and/or sophisticated?
- Have **specific interests** or focus?
- Are just **casually browsing**?
- Are from a certain **demographic/gender/nationality**?

> Make every design and content decision align with your overall website strategy

---

## CONTENT STRATEGY **08**
<!-- .slide: class="crammed" -->

Getting your message across:

- What is the **most important** thing to convey?
- The **least** important?
- What needs to be said **first** (the hook)?
- What leads visitors to click a **call to action**?

---

## CONTENT STRATEGY **09**
<!-- .slide: class="crammed" -->

**Calls to action**—help visitors make a decision

- What do you **want people to do** when visiting your site?
- Do you have a **simple and prominent** call to action?
- What is the precise **call to action wording**?
- What emotional/mental factors **motivate people** to act?

---

## CONTENT STRATEGY **10**
<!-- .slide: class="crammed" -->

> When Steve Jobs returned to Apple in 1997, there were **sixteen to eighteen models** of computer… even he couldn’t give clear advice to a friend on which Mac model she should buy. He **cut the number of models to four**: two desktop and two laptop computers. The Apple product line then reflected this **strategic focus on real user needs** and a meaningful product differentiation.

<small>—abbreviated from: Web Style Guide, Patrick J. Lynch and Sarah Horton</small>

---

## CONTENT STRATEGY **11**
<!-- .slide: class="crammed" -->

> There’s **no such thing as “mobile content”**. What all readers and users need is **good content**, available **wherever and whenever** they need it, **on any device**. If some of your content looks superfluous on a mobile device, it’s certainly superfluous for desktop users as well. **Get rid of the useless fluff!**

---

## CONTENT STRATEGY **12**
<!-- .slide: class="crammed" -->

> The measure of good editorial style is whether the content is useful… Content should meet real, carefully researched **user needs**. Too often corporate and institutional web teams produce content designed primarily around **internal** goals and **organization** charts, forgetting that **users couldn’t care less** what your mission statement is, or how you are organized.  
> —[Editorial Style (Web Style Guide)](https://webstyleguide.com/10-editorial-style.html)

Also see [Writing for the Web](https://www.usability.gov/how-to-and-tools/methods/writing-for-the-web.html)

---

## CONTENT STRATEGY **13**
<!-- .slide: class="crammed" -->

Read more from these articles and sites:

- [UX Movement has helpful menus](https://uxmovement.com/)
- [Content Strategy Within The Design Process](https://www.business2community.com/brandviews/ceros/content-strategy-within-design-process-01400789)
- [Web Style Guide, Chapter 1: "Strategy"](https://webstyleguide.com/1-strategy.html)

The *Web Style Guide* also has a good section on  
**Social Media Strategy**

===

## STYLE GUIDES **01**

A **style guide document** keeps an organisation’s printed and web materials within their style

- layout
- graphics
- colours
- fonts
- logo
- photos

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/nus-style-guide.png" data-background-size="contain" -->

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/dmu-ug-campaign-2012.png" data-background-size="contain" -->

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/dmu-style-guide-2017.png" data-background-size="contain" -->

---

## STYLE GUIDES **02**

Download PDFs of these three style guides:

- [NUS Brand Guidelines](https://raw.githubusercontent.com/TECH3015/lectures/master/pdf/nus-guidelines-oct13.pdf)
- [DMU 2012 Undergrad Campaign Guidelines](https://raw.githubusercontent.com/TECH3015/lectures/master/pdf/ug-2012-campaign-guidelines.pdf)
- [DMU Brand Guidelines June 2017](https://raw.githubusercontent.com/TECH3015/lectures/master/pdf/dmu-brand-guidelines-june-2017.pdf)

---

<!-- .slide: class="crammed" -->
## STYLE GUIDES **03**

The [Campaign Energy Dashboard](https://switchoff.nus.org.uk/) used NUS guidelines

![NUS energy dashboard screenshot](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/saves-home-screen-oct2019.png)

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/saves-cambridge-amiresponsive.png" data-background-size="contain" -->

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/saves-cambridge-bigscreen-amiresponsive.png" data-background-size="contain" -->

---

<!-- .slide: data-background-image="https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/saves-home-screen-amiresponsive-nov2017.png" data-background-size="contain" -->

---

## STYLE GUIDES **04**

three big tech companies have **interface guidelines**

- [Google Material Design](https://material.io/design/introduction/)
- [Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)
- [Microsoft User Interface Principles](https://docs.microsoft.com/en-us/windows/win32/appuistart/-user-interface-principles#the-basic-principles-of-proper-ui)

They’re long, detailed and technical so just scan through

---

<!-- .slide: class="crammed" -->
[Google Material Design](https://material.io/design/introduction/)

![Google Material Design, screenshot](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/google-material-design.png)

---

<!-- .slide: class="crammed" -->
[Apple Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)

![Apple Human Interface Guidelines, screenshot](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/apple-interface-guidelines.png)

---

<!-- .slide: class="crammed" -->
[Microsoft User Interface Principles](https://docs.microsoft.com/en-us/windows/win32/appuistart/-user-interface-principles)

![Microsoft User Interface Principles, screenshot](https://raw.githubusercontent.com/TECH3015/lectures/master/imgs/design/guides/microsoft-ui-principles.png)

===

<!-- .slide: class="crammed" -->
## DESIGN TRENDS **01**

[UXPin Studio](https://www.uxpin.com/studio/) have some great resources:

- [free design e-books](https://www.uxpin.com/studio/ebooks/)
- a [guide to creating style guides](https://www.uxpin.com/studio/blog/everything-content-styleguides/)
- articles on:
    - [web design](https://www.uxpin.com/studio/blog/category/web-design/)
    - [User Experience (UX) design](https://www.uxpin.com/studio/blog/category/ux-design/)
    - [User research](https://www.uxpin.com/studio/blog/category/user-research/)

(you can by-pass promotional material for the UXPin interface builder)

---

## DESIGN TRENDS **02**

Download PDFs of these three style guides:

- [Web design trends 2015-16](https://raw.githubusercontent.com/TECH3015/lectures/master/pdf/uxpin-web-design-trends-2015-16.pdf)
- [Web design trends 2018](https://raw.githubusercontent.com/TECH3015/lectures/master/pdf/uxpin-web-design-trends-2018.pdf)
- [Web design trends 2019](https://raw.githubusercontent.com/TECH3015/lectures/master/pdf/uxpin-web-design-trends-2019.pdf)

===

## TYPOGRAPHY **01**
<!-- .slide: class="left-align" -->

> **95%** of the information on the web is **written language**. It is only logical to say that a web designer should get good training in the main discipline of **shaping written information**, in other words: **Typography**.
> 
> —Oliver Reichenstein, "[Web Design is 95% Typography](https://ia.net/topics/the-web-is-all-about-typography-period)”, 2006

---

## TYPOGRAPHY **02**
<!-- .slide: class="left-align" -->

> our harassed contemporaries simply **cannot take everything** that is printed today.
> 
> It is the typographer’s task to **divide up, organize** and **interpret this mass** of printed matter in such a way that **the reader** will have a **good chance of finding what is of interest**
>
> —Emil Ruder, famous Swiss typographer, 1969

---

## TYPOGRAPHY **03**
<!-- .slide: class="left-align crammed" -->

recommended **web typography primary sources**:

- [The Elements of Typographic Style Applied to the Web](http://webtypography.net/toc/)
- [Typography chapter, Web Style Guide](https://webstyleguide.com/9-typography.html)  
—Patrick J. Lynch and Sarah Horton, 2016

---

## TYPOGRAPHY **04**
<!-- .slide: class="left-align" -->

> Choosing a Typeface Is **Not Typography**

but here's a little inspiration: [Beautiful Web Type](http://hellohappy.org/beautiful-web-type/)

---

## TYPOGRAPHY **05**
<!-- .slide: class="left-align crammed" -->

optimum **line length for readablity** was supposed to be 50-75 characters…

…but [The Line Length Misconception](https://www.viget.com/articles/the-line-length-misconception/) draws on more recent research, although `line-spacing`, `letter-spacing` and `font-family` helps—see [Optimal Text Layout Line Length](https://www.paulolyslager.com/optimal-text-layout-line-length/)

…and the advice continues **in more detail** for **mobile devices** in [How To Set Perfect Line Lengths For The Web](http://www.simon-li.com/design-and-code/how-to-set-perfect-line-lengths-for-your-webpages/)

…and finally [Letterspacing Makes ALL CAPS Easier to Read](https://uxmovement.com/content/how-letterspacing-can-make-all-caps-easier-to-read/)

---

## TYPOGRAPHY **06**

Technical (CSS) information here: https://tech3015.github.io/presents/?lecture-17#/4/5

And see:

- [Tips For Setting Up A Baseline Grid (CSS)](https://vanseodesign.com/web-design/baseline-grid/)
- [Typesetting Body Text (loooong educational video)](https://vimeo.com/156203722)

===

# QUESTIONS?

Discuss visual ideas for your website?
