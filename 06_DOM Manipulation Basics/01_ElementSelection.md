 **DOM selection methods** in JavaScript — including `getElementById`, `querySelector`, `getElementsByName`, `getElementsByClassName`, and more.

---

# 🕸️ DOM Element Selection Methods

The **DOM (Document Object Model)** lets you access and manipulate HTML elements with JavaScript. To do that, you first need to **select elements** using various methods.

---

## 1️⃣ `document.getElementById(id)`

* Selects **one element** by its unique `id`.
* Returns the element or `null` if not found.

### Example:

```html
<div id="header">Welcome!</div>
```

```javascript
const header = document.getElementById("header");
console.log(header.textContent);  // Output: Welcome!
```

---

## 2️⃣ `document.getElementsByClassName(className)`

* Selects **all elements** with the given class name.
* Returns a **live HTMLCollection** (array-like but not an array).

### Example:

```html
<p class="note">Note 1</p>
<p class="note">Note 2</p>
```

```javascript
const notes = document.getElementsByClassName("note");
console.log(notes.length);  // Output: 2
console.log(notes[0].textContent);  // Output: Note 1
```

---

## 3️⃣ `document.getElementsByTagName(tagName)`

* Selects all elements with the given tag name (e.g., `"div"`, `"p"`).
* Returns a live HTMLCollection.

### Example:

```javascript
const paragraphs = document.getElementsByTagName("p");
console.log(paragraphs.length); // Number of `<p>` tags on the page
```

---

## 4️⃣ `document.getElementsByName(name)`

* Selects all elements with a given `name` attribute.
* Returns a NodeList (array-like).

### Example:

```html
<input type="radio" name="gender" value="male">
<input type="radio" name="gender" value="female">
```

```javascript
const radios = document.getElementsByName("gender");
console.log(radios.length);  // Output: 2
```

---

## 5️⃣ `document.querySelector(selector)`

* Returns the **first element** that matches a CSS selector.
* Very flexible — supports any valid CSS selector.

### Example:

```html
<div class="content">Hello</div>
<p class="content">World</p>
```

```javascript
const firstContent = document.querySelector(".content");
console.log(firstContent.textContent);  // Output: Hello
```

---

## 6️⃣ `document.querySelectorAll(selector)`

* Returns **all elements** that match a CSS selector.
* Returns a **static NodeList** (not live).

### Example:

```javascript
const allContents = document.querySelectorAll(".content");
console.log(allContents.length);  // Output: 2
allContents.forEach(el => console.log(el.textContent));
```

---

## Summary Table

| Method                              | Returns                | Selects                            | Notes                      |
| ----------------------------------- | ---------------------- | ---------------------------------- | -------------------------- |
| `getElementById(id)`                | Single element or null | Element with given ID              | Fastest method, unique ID  |
| `getElementsByClassName(className)` | HTMLCollection         | All elements with a class          | Live collection            |
| `getElementsByTagName(tagName)`     | HTMLCollection         | All elements with a tag name       | Live collection            |
| `getElementsByName(name)`           | NodeList               | All elements with a name attribute | Often used for form inputs |
| `querySelector(selector)`           | Single element or null | First matching CSS selector        | Very flexible              |
| `querySelectorAll(selector)`        | NodeList               | All matching CSS selectors         | Static collection          |

---


