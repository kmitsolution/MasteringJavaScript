**Modify element content and styles** after selecting elements in the DOM.

---

## ✍️ Modify Element Content

### 1. Change Text Content

```javascript
const header = document.getElementById("header");
header.textContent = "New Header Text!";
```

* `.textContent` sets or gets the **text inside** an element (without HTML).

---

### 2. Change HTML Content

```javascript
const container = document.querySelector(".container");
container.innerHTML = "<strong>Bold Text</strong> and normal text.";
```

* `.innerHTML` lets you set or get **HTML markup** inside an element.

---

## 🎨 Modify Element Styles

You can change CSS styles directly via the `.style` property.

```javascript
const box = document.querySelector(".box");
box.style.backgroundColor = "lightblue";
box.style.border = "2px solid black";
box.style.padding = "10px";
```

---

## 🛠️ Modify Attributes

You can add, change, or remove attributes:

```javascript
const link = document.querySelector("a");

// Change href attribute
link.setAttribute("href", "https://example.com");

// Get href attribute
console.log(link.getAttribute("href"));

// Remove an attribute
link.removeAttribute("title");
```

---

## Example: Changing Button Text and Color on Click

```html
<button id="myBtn">Click Me</button>
```

```javascript
const btn = document.getElementById("myBtn");

btn.addEventListener("click", function() {
  btn.textContent = "Clicked!";
  btn.style.backgroundColor = "green";
  btn.style.color = "white";
});
```

---

## Summary

| What to Modify | How to Access/Change                                       |
| -------------- | ---------------------------------------------------------- |
| Text content   | `.textContent`                                             |
| HTML content   | `.innerHTML`                                               |
| CSS styles     | `.style.propertyName = "value"`                            |
| Attributes     | `.setAttribute()`, `.getAttribute()`, `.removeAttribute()` |

---


