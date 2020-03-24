
# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

## **Front-End Web Development**

### Lecture 10

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

# CORONA VIRUS
<!-- .slide: class="smalltext" -->

COVID-19 has meant **all teaching is now online**

- Fania and Graeme will be present in one of the 14 BlackBoard **[Online Classroom](https://vle.dmu.ac.uk/webapps/collab-ultra/tool/collabultra?course_id=_551514_1&mode=cpview)** sessions during the **usual lab times**
- Please **be patient with emails**, we have **many queries** across modules!
- **Double-check** your **website** in various **browsers** (NOT IE!) to be sure **everything works**

Please **attend online**, even briefly, if only to email later with **specifics**  
if you **really need to**—only **one or two issues** at a time, please!

===

# ONLINE LABS

For those **who turn up**(!) these have been **very useful**

See Graeme's announcement to [choose a lab time](https://vle.dmu.ac.uk/webapps/blackboard/execute/announcement?method=search&context=course_entry&course_id=_551514_1&handle=announcements_entry&mode=view) - there are **14 online labs** each week, which you can join from the [Online Classroom link](https://vle.dmu.ac.uk/webapps/collab-ultra/tool/collabultra?course_id=_551514_1&mode=view)

===

# WEBSITE HAND-IN **01**

Make sure:

- you read the [marking criteria (BlackBoard: Assessment)](https://vle.dmu.ac.uk/webapps/blackboard/content/listContent.jsp?course_id=_551514_1&content_id=_4247904_1&mode=reset) on Blackboard and [examples](https://ctec3905.github.io/examples/)
- you **push all files** to your GitHub classroom repo
- your `index.html` file is in the **root directory**
- `index.html` and folders are **all lower-case**
<!-- - check your site on **GitHub pages** to make sure it’s okay…  
  …if not, check your **file paths**! -->

---

# WEBSITE HAND-IN **02**
<!-- .slide: class="smalltext" -->

We will mark your code from **GitHub classroom**

**NOT** from your personal GitHub account.

**You can check this:**  
your GitHub Classroom repo name starts with  
**"CTEC3905/website-"** e.g.

`github.com/CTEC3905/website-myRandomNameHere`

---

# WEBSITE HAND-IN **03**
<!-- .slide: class="smalltext" -->

**QUALITY** NOT *QUANTITY*

There's **no definite limit** to features, commits, JavaScript functions/functionality.

So use what will show your knowledge and demonstrate **"USUP"**:

- **Understanding** of HTML, CSS and JavaScript
- **Structure**, validity and tidiness of code
- **Usability** of website (PARC, IA)—ask people!
- **Progression** of development (commits, branches)

…in a coherent, error-free, validated, well-organised site.

---

# WEBSITE HAND-IN **04**

## FEW, MEANINGFUL **COMMENTS**

Keep your code comments brief and meaningful. Although, when well-written…

> the code is the comment

See [The Pragmatic Programmer](https://pragprog.com/book/tpp20/the-pragmatic-programmer-20th-anniversary-edition),  
—Andrew Hunt and David Thomas

===

# README **01**
<!-- .slide: class="smalltext" -->

## It's **NOT AN ESSAY!**

You can use **Markdown**, a simple ‘language’ that ensures **semantic markup** in a **plain-text format**, for your readme file

You can use [GitHub-flavoured Markdown (see guide)](https://guides.github.com/features/mastering-markdown/)  
for your **readme.md** file

---

# README **02**
<!-- .slide: class="smalltext" -->

You can use an image or two, for example to:

- **illustrate something you solved**
- show how you **improved an earlier version**

[resize images and screenshots](https://www.freeonlinephotoeditor.com/) **before adding them** to your website  
or to your readme.md file

This Markdown creates an HTML "img" tag:  
`![alt text](images/myimage.png)`

---

# README **03**
<!-- .slide: class="smalltext" -->

- **Don't** credit images
- **Do** reference code you've used
- **Don't** write an essay
- **Do** briefly explain your thinking

**References can just be a link**—no need for Harvard format.  
This Markdown will create an HTML link ("a" tag):  
`[Some tutorial](https://sometutorial.com/)`

===

# GIT BRANCH: 1
<!-- .slide: class="smalltext" -->

- use branches for **developing a feature**
- branches **preserve** the "master" branch from harm
- **develop** the new feature on the branch **until it works**
- **push** the branch to the GitHub classroom
- you can then **merge the branch** back into "master"
- `git branch` shows **all branches** with a `*` on the current one

Here's **how to use git branch**…

---

# GIT BRANCH: 2
<!-- .slide: class="smalltext" -->

- **save** all the files in your **master branch**
- `git add .` and `git commit -m "message here"`
- now **create and checkout** a **new branch** with:  
  `git checkout -b my-new-branch`
- **work** on the code, check **it works**
- then **push** the **new branch** with:  
  `git push -u origin my-new-branch`
- finally: `git checkout master`
- `git merge my-new-branch`
- `git add .` then `git commit -m "merge new branch"`

---

# GIT BRANCH: 3
<!-- .slide: class="smalltext" -->

If you have **uncommitted changes on master** there will be **conflicts**.
These are marked by GIT like this:

```
 <<<<<< HEAD
 new code (keep)
 ======
 old code (delete if you’re sure)
 >>>>>> master
```

- edit files and **remove the old code**
- all good? `git add .` and **commit**!

===

# HTML5 MOBILE: **01**
<!-- .slide: class="smalltext" -->

## “WRITE **ONCE** DEPLOY **ANYWHERE**”

Many frameworks *promised* to deliver this idea (e.g. [Meteor](https://www.meteor.com/), [Ionic](http://ionicframework.com), [Appcelerator Titanium](http://www.appcelerator.com/mobile-app-development-products/), [Sencha](https://www.sencha.com/products/extjs/), [React Native](https://facebook.github.io/react-native/) (Adobe [PhoneGap](http://phonegap.com/) is a *distribution* of Apache's [Cordova](https://cordova.apache.org/))

- [Swift](https://developer.apple.com/swift/)/[Java](https://developer.android.com/) **vs** HTML5+native wrapper **vs** PWAs

Increased browser functionality, advances in JavaScript, HTML and CSS drove a *significant shift* towards using **web technologies for mobile development**, so Google introduced a concept…  
**Progressive Web Apps** (PWAs), which took off quickly!

---

# HTML5 MOBILE: **02**
<!-- .slide: class="smalltext" -->

## **native** vs **webapp**

> When dealing with clients… by far the most common thing I’ve noticed is: **they do not care if it’s HTML5 or native**. In fact, despite explanation, they rarely ever understand the difference. **Deliver what they want** and they will be happy no matter what you make it with.

[7 Lessons from 3 Years of HTML5 Mobile App Dev (2017)](https://www.joshmorony.com/7-lessons-from-3-years-of-html5-mobile-application-development/ "this is from a dev who uses a chosen framework")

---

# HTML5 MOBILE: **03**
<!-- .slide: class="smalltext" -->

## ACCESSING DEVICE HARDWARE

HTML5/CSS/JS can access/do many things e.g.  
**location**, **camera**, **push messages**, **file access**…  
see [What Web Can Do Today](https://whatwebcando.today/)

- [“Progressive Web Apps vs. native”… the wrong question…](https://medium.com/dev-channel/why-progressive-web-apps-vs-native-is-the-wrong-question-to-ask-fb8555addcbb)
- [Progressive Web Apps vs Native Apps](https://www.codica.com/blog/progressive-web-apps-vs-native/)
- [Progressive Web Apps: When Short on Resources](https://insanelab.com/blog/web-development/progressive-web-apps-pwa-vs-native/)

===
<!-- PROGRESSIVE WEBAPPS -->

# **PROGRESSIVE** WEBAPPS: **1**
<!-- .slide: class="crammed smalltext" -->

Can give users an **app-like experience** from a **SPA** website

- Save to **home screen** with an icon
- Will now show among **open apps**
- Can increasingly **access device hardware**
- Are based on the **open web**
- **By-pass** the App Store, Google Play
- Are **securely served** ([SSL](https://www.digicert.com/ssl/)—[free SSL with LetsEncrypt](https://letsencrypt.org/))

[**progressive web apps**](https://web.dev/progressive-web-apps/) start **mobile-freindly**, go **much further**

---

# **PROGRESSIVE** WEBAPPS: **2**
<!-- .slide: class="centered smalltext" -->

![Web App Vs Native App](pwa/install-a-web-app.gif)

Are **enabled** by—and **compete with**—native Apple and Google apps

---

# **PROGRESSIVE** WEBAPPS: **3**
<!-- .slide: class="centered smalltext" -->

![Web App Vs Native App](pwa/webapp-v-app.jpg)

have code telling the device they’re **PROGRESSIVE**, so are “installed” when saved to the home screen. This means they’re **full screen**, and stay in **open apps** separate from the browser.

---

# **PROGRESSIVE** WEBAPPS: **4**
<!-- .slide: class="smalltext" -->

> The fact that web apps are on the **open web** allows developers to **publish anything they want** (and compete with anyone they want) and charge for their own in-app purchases or even “downloads,” **without paying fees** to Apple or Google…
>
> …developers can create an app as a side project **and actually “ship” it**.

[Installable Web Apps May Be the Future of the Open Web](http://brolik.com/blog/installable-web-apps-open-web/)  
—Drew Thomas, 2014.

---

# **PROGRESSIVE** WEBAPPS: **5**
<!-- .slide: class="crammed smalltext" -->

## WHAT YOU **NEED**

- **single-screen** navigation (a SPA or JavaScript navigation)
- fully **responsive design** (see [RWD best practices](https://uxplanet.org/responsive-design-best-practices-c6d3f5fd163b#.o))
- various **icons** and **splash screen** graphics
- wipe **cookies** and **local data** if required
- some understanding of [offline storage](https://medium.com/dev-channel/offline-storage-for-progressive-web-apps-70d52695513c "Addy Osmani")

---

# **PROGRESSIVE** WEBAPPS: **6**
<!-- .slide: class="crammed smalltext" -->

## GOING **FURTHER**

- use **HTTPS** and and **SSL certificate** ([LetsEncrypt](https://letsencrypt.org/) is free)
- a [valid **manifest** file](https://manifest-validator.appspot.com/) (replaces `&lt;meta>` tags) for offline use
- server **config** code for the manifest (e.g. [Apache](https://github.com/h5bp/server-configs-apache/blob/master/src/media_types/media_types.conf))
- [**service workers**](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers): cache assets, **offline data** and **push notifications**
- read up on [IndexedDB](https://developers.google.com/web/fundamentals/instant-and-offline/web-storage/offline-for-pwa) and an [offline data comparison](https://nolanlawson.com/2015/09/29/indexeddb-websql-localstorage-what-blocks-the-dom/)

See [Native Apps are Doomed](https://medium.com/javascript-scene/native-apps-are-doomed-ac397148a2c0)

---

# **PROGRESSIVE** WEBAPPS: **7**
<!-- .slide: class="crammed smalltext" -->

## A **TUTORIAL**

[Your First Progressive Web App](https://codelabs.developers.google.com/codelabs/your-first-pwapp/)

===

# STAY SAFE

COVID-19 is a **serious threat** to people of **all ages**

Remember to **help and protect your older relatives and friends**, and anyone with a **pre-existing condition**
