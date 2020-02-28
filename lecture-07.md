# CTEC3905
<!-- .slide: class="centered" -->

![HTML, CSS, JavaScript logos](html-css-js-500.png)<!-- .element: class="imgBackground" -->

## **Front-End Web Development**

### Lecture 07

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

## ONLINE RESOURCES

**Codecademy** free courses:

- [Learn HTML](https://www.codecademy.com/learn/learn-html)
- [Learn CSS](https://www.codecademy.com/learn/learn-css)
- [Learn how to build websites](https://www.codecademy.com/learn/paths/learn-how-to-build-websites)
- [Introduction to JavaScript](https://www.codecademy.com/learn/introduction-to-javascript)

===

# ISSUES
<!-- .slide: class="smallcode crammed" -->

questions we have been asked:

- assignment instructions and **GitHub pages**
- maximum **number of pages**
- assingment deadline: BlackBoard or in Module Handbook

===

# REFACTORING! **01**
<!-- .slide: class="smallcode crammed" -->

The new [tesla/kitten code](https://front-end-materials.github.io/js-simple-examples/js-swap-class/) ([code](https://github.com/front-end-materials/js-simple-examples/tree/master/js-swap-class)) - [Lecture 05 slide updated](https://ctec3905.github.io/presents/?lecture-05#/4/4)

```js
function showImage() {
  picture.innerHTML = "";
  picture.classList = event.target.id;
}

[car,cat].forEach(c => c.addEventListener( "click", showImage ));
```

Changed `photo1`, `photo2` classes to `cat`, `car` to match IDs

---

# REFACTORING! **02**
<!-- .slide: class="smallcode crammed" -->

previous *horrible* code: lots of repetition,  
not DRY (**Do not Repeat Yourself!**)
 
```js
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

===

# STORING DATA **01**
<!-- .slide: class="smalltext crammed" -->

There a few ways to store data for browsing sessions:

- **cookies** and **databases** (server)
- **browser storage** (client):
  - `sessionStorage`
  - `localStorage`
  - `IndexedDB`

**client-side storage** holds **more data** ([devices/browsers vary](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API/Browser_storage_limits_and_eviction_criteria#Storage_limits)) than cookies (4Kb) ([Safari is preventing cookies3rd party tracking cookies](https://medium.com/@bluepnume/safaris-new-tracking-rules-and-enabling-cross-domain-data-storage-85241eea7483))

(If you see mention of *WebSQL*, it's old and dying)

---

# STORING DATA **02**
<!-- .slide: class="smalltext crammed" -->

the front-end (client) methods are:

- `sessionStorage`: per-page/tab, **deleted on close**
- `localStorage`: per-site, **stored permanently** as a string
- `IndexedDB`: structured data, **stored permanently** including **files/blobs**

In all these, data are stored as ‘NoSQL’ **key-value pairs**

Resources:

- [HTML5 Web Storage (W3Schools)](https://www.w3schools.com/html/html5_webstorage.asp)
- [IndexedDB (JavaSctip.info)](https://javascript.info/indexeddb)

---

# STORING DATA **03**
<!-- .slide: class="smalltext crammed" -->

[CORS](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) [same-origin policy](https://www.w3.org/Security/wiki/Same_Origin_Policy) is *domain-specific* so websites *can’t access* databases *on other sites*

- the **protocol/host/port** (if specified) must be the same
- storage can be **cleared** by the **user**, or **browser** (if limits are reached)

In production, some browser storage requires a site to run under `https` with an **SSL certificate**  
([LetsEncrypt](https://letsencrypt.org/) is free and can be set up on a server to auto-renew)

---

# STORING DATA **04**
<!-- .slide: class="smalltext crammed" -->

is **per-domain**

> Data is available to **all scripts** loaded from pages **from the same origin** that **previously stored the data**.
>
> It persists **after the browser is closed** and does not suffer cookie Weak Integrity/Weak Confidentiality issues. **Session storage** is per-origin and per-instance (window/tab) until the window/tab is closed; it allows **separate instances** of the **same web app** to run in different windows without interference, a use case not well supported by cookies.

[Web Storage (Wikipedia)](https://en.wikipedia.org/wiki/Web_storage)

---

# STORING DATA **05**
<!-- .slide: class="smalltext crammed" -->

- `localStorage` clashes: **check for a key** before writing
- `localStorage` and `indexedDB` **write to disc** (using browser internals)

## **Never trust user input!**

---

# STORING DATA **06**
<!-- .slide: class="smalltext smallcode crammed" -->

The StorageManager API is still experimental—[check browser support](https://caniuse.com/#search=StorageManager) before using in production.

check storage limits (rough estimate):

```html
<p>
  You're currently using about <span id="percent">
  </span>% of your available storage.
</p>
```

```js
navigator.storage.estimate().then(function(estimate) {
  document.getElementById("percent").innerHTML =
      (estimate.usage / estimate.quota * 100).toFixed(8);
});
```

---

# STORING DATA **07**
<!-- .slide: class="smalltext smallcode crammed" -->

check storage (complete readout):

```js
async function showEstimatedQuota(est) {
  return await navigator.storage && navigator.storage.estimate ?
    navigator.storage.estimate() :
    undefined;
}
console.log(showEstimatedQuota());
```

DEMO: [js-storage-check](https://front-end-materials.github.io/local-storage/browser-storage-check/)

---

# STORING DATA **08**
<!-- .slide: class="smalltext crammed" -->

> `IndexedDB` can be erased because of low disk space on a device—a database may be deleted without notifying the user to free up space for other website’s data used more recently.
>
> …a good thing, as end-users may not want everything stored forever for every site. So if `IndexedDB` is critical for your application, this browser behavior needs managing.

- [How To Use the StorageManager API](https://dexie.org/docs/StorageManager)
- [StorageManager (MDN)](https://developer.mozilla.org/en-US/docs/Web/API/StorageManager) 
- [StorageManager.estimate() (MDN)](https://developer.mozilla.org/en-US/docs/Web/API/StorageManager/estimate) 

===

# LOCAL STORAGE: **01**
<!-- .slide: class="crammed" -->

Browsers have **their own storage**

We're using one of the storage functions: `localStorage`

- it’s for **small amounts** of data (between 2Mb-10Mb)
- it stores data in **key value** pairs

`localStorage` is **insecure** (no good for ~~sensitive data~~ - see [Please Stop Using Local Storage](https://dev.to/rdegges/please-stop-using-local-storage-1i04)).  
However, it’s **good for non-critical data**.

---

# LOCAL STORAGE: **02**
<!-- .slide: class="crammed" -->

Instead of *cookies*, many websites now use **local storage** to keep small amounts of **data between visits**. It can:

- **store user preferences** 
- **personalise each visit**

You can **see what a website stores** in your own browser:

- open the **web inspector**
- select the **"Application" tab**…

---

![local storage in the browser Application tab](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/localstorage/local-storage-application-tab.png)

---

**Facebook** uses `localStorage` for several settings:

![Facebook local storage](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/localstorage/local-storage-facebook.png)

You can see stored **objects** (`{…}`) and **arrays** (`[…]`)  
We don’t know what most of those are!

---

# LOCAL STORAGE: **03**
<!-- .slide: class="crammed" -->

**Setting** and **getting** data:

```javascript
localStorage.setItem("name", "Dave");
localStorage.getItem("name"); // Dave
```

**Changing** data: **basic syntax**:

```javascript
localStorage["name"] = "Fania";
console.log(localStorage["name"]); // Fania
```

---

# LOCAL STORAGE: **04**
<!-- .slide: class="crammed" -->

Example: set a localStorage item from a **field value**:

```javascript
const theName = document.getElementById("name-field");

localStorage.setItem("name", theName.value);

myElement.innerText = localStorage.getItem("name");
```

---

# LOCAL STORAGE: **05**
<!-- .slide: class="crammed" -->

**remove** an item from `localStorage` or **clear all**:

```javascript
localStorage.removeItem("name");
localStorage.clear();
```

Attach an `eventListener` to use the data on **another page**:

```javascript
localStorage.addEventListener("change", myFunction);
```

`myFunction` handles **actions** on the `localStorage` data.

**NOTE** [browser support is still patchy for LocalStorage *events*](https://stackoverflow.com/a/6846158/123033)

===

# DEMOS

- [Store a name with local storage from an input form](https://front-end-materials.github.io/local-storage/local-storage-form/)  
[view code](https://github.com/front-end-materials/local-storage/tree/master/local-storage-form)
- [store multiple names in localStorage](https://front-end-materials.github.io/local-storage/local-storage-object/)  
[view code](https://github.com/front-end-materials/local-storage/tree/master/local-storage-object)

===

## CSS VARIABLES?

===

# QUESTIONNAIRE: **DO YOU…**
<!-- .slide: class="crammed smallcode smalltext" -->

one:

```js
if(condition){
  do stuff;
} else {
  do other stuff;
}
```

two:

```js
if(condition){
  do stuff;
}
else {
  do other stuff;
}
```

===

# QUESTIONS?

**please ask now…**

No crowding around the podium afterwards!

Talk to Graeme for module-related issues
