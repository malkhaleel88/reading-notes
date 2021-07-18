# **Local Storage**

## **HTML Web Storage**

*With web storage, web applications can store data locally within the user's browser.*

*Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.*

*Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.*

*Web storage is per origin (per domain and protocol). All pages, from one origin, can store and access the same data.*

**HTML web storage provides two objects for storing data on the client:**

* `window.localStorage` - *stores data with no expiration date.*
* `window.sessionStorage` - *stores data for one session (data is lost when the browser tab is closed).*

## **Local Storage**

*The localStorage and sessionStorage properties allow to save key/value pairs in a web browser.*

*The localStorage object stores data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.*

*The localStorage property is read-only.*

**Syntax**

`window.localStorage`

**Syntax for SAVING data to localStorage:**

`localStorage.setItem("key", "value");`

**Syntax for READING data from localStorage:**

`var lastname = localStorage.getItem("key");`

**Syntax for REMOVING data from localStorage:**

`localStorage.removeItem("key");`


[HOME](https://malkhaleel88.github.io/reading-notes)