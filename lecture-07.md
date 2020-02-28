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

# REFACTORING

new tesla/kitten code

===

# STORING DATA *01*

There a few ways to store data for browsing sessions:

- cookies (server)
- databases (server)
- **browser storage** (client):
  - `sessionStorage`
  - `localStorage`
  - `IndexedDB`

All **client-side storage** can hold **far more data** (varies but around 5mb) than cookies

(If you see mention of *WebSQL*, it's old and dying)

---

# STORING DATA *02*

the front-end (client) methods are:

- `sessionStorage`: per-page/tab, deleted on close
- `localStorage`: per-site, stored permanently as a string
- `IndexedDB`: structured data, including files/blobs

In all these, data are stored as ‘NoSQL’ key-value pairs

Resources:

- [HTML5 Web Storage (W3Schools)](https://www.w3schools.com/html/html5_webstorage.asp)
- [IndexedDB (JavaSctip.info)](https://javascript.info/indexeddb)

---

# STORING DATA *03*

This is an evloving technology with varying browser support and [storage limits](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API/Browser_storage_limits_and_eviction_criteria#Storage_limits)

- `localStorage`: 
- `IndexedDB`: domain-specific [same-origin policy](https://www.w3.org/Security/wiki/Same_Origin_Policy): websites *can’t access* databases *on other sites*

Storage can be cleared by the user, or (if limits are reached) by the browser.

In production, some browser storage requires a site to run under `https` with an SSL certificate )[LetsEncrypt](https://letsencrypt.org/) is free and can be set up on a server to auto-renew)

---

# STORING DATA *04*

checking limits (rough estimate):

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

# STORING DATA *05*

checking limits (complete readout):

```js
async function showEstimatedQuota(est) {
  return await navigator.storage && navigator.storage.estimate ?
    navigator.storage.estimate() :
    undefined;
}
console.log(showEstimatedQuota());
```

DEMO: js-storage-check

---

# STORING DATA *06*

> IndexedDB is a “best-effort” database that can be erased in situations of low disk space on a device. The browser may delete your database without notifying the user … to free up space for other website’s data … used more recently than yours.
>
> Actually, this is a good thing … as the end-users may not want everything … stored forever on each site they visit. But if IndexedDB is critical for your application…

…this browser-behavior needs managing, although `StorageManager` is still experimental:

- [How To Use the StorageManager API](https://dexie.org/docs/StorageManager)
- [StorageManager (MDN)](https://developer.mozilla.org/en-US/docs/Web/API/StorageManager) 

---

# STORING DATA *06*

localStorage clashes

===

# LOCAL STORAGE: **1**
<!-- .slide: class="crammed" -->

Browsers have **their own storage**, similar to cookies.

In this module, we're using one of the storage functions: `localStorage`

- it’s for **small amounts** of data (5Mb)
- it stores data in **key value** pairs

`localStorage` is **insecure** (so not good for ~~sensitive data~~ - see [Please Stop Using Local Storage](https://dev.to/rdegges/please-stop-using-local-storage-1i04)).  
However, it’s still **good for non-critical data**.

---

# LOCAL STORAGE: **2**
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

# LOCAL STORAGE: **3**
<!-- .slide: class="crammed" -->

Instead of *cookies*, many websites now use **local storage** to keep small amounts of **data between visits**. It can:

- **store user preferences** 
- **personalise each visit**

You can **see what a website stores** in your own browser:

- open the **web inspector**
- select the **"Application" tab**…

---

![local storage in the browser Application tab](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/localstorage//local-storage-application-tab.png)

---

**Facebook** uses `localStorage` for several settings:

![Facebook local storage](https://raw.githubusercontent.com/DaveEveritt/TECH3015/master/imgs/localstorage/local-storage-facebook.png)

You can see stored **objects** (`{…}`) and **arrays** (`[…]`)  
We don’t know what most of those are!

---

# LOCAL STORAGE: **4**
<!-- .slide: class="crammed" -->

Example: set a localStorage item from a **field value**:

```javascript
const theName = document.getElementById("name-field");

localStorage.setItem("name", theName.value);

myElement.innerText = localStorage.getItem("name");
```

---

# LOCAL STORAGE: **5**
<!-- .slide: class="crammed" -->

You can **remove** an item from `localStorage` or **clear all**:

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

- [Store a name with local storage from an input form](https://front-end-materials.github.io/local-storage/js-local-storage-form/)  
[view code](https://github.com/front-end-materials/local-storage/tree/master/js-local-storage-form)
- [store multiple names in localStorage](https://front-end-materials.github.io/local-storage/local-storage-object/)  
[view code](https://github.com/front-end-materials/local-storage/tree/master/local-storage-object)

===

# QUESTIONS?

**please ask now…**

No crowding around the podium afterwards!

Talk to Graeme for module-related issues
