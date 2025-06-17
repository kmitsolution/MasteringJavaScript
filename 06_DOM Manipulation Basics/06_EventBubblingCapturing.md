Great! Let's dive into **advanced JavaScript event concepts** — namely:

---

## 🔸 Event Bubbling and Capturing

When an event occurs (like a click), it doesn’t just trigger on the element you clicked — it can **bubble up** or **capture down** through the DOM tree.

### 🔹 1. **Event Bubbling** (Default Behavior)

* Events start at the **target element** and **bubble up** to its ancestors.

**Example:**

```html
<div id="parent">
  <button id="child">Click Me</button>
</div>

<script>
  document.getElementById("parent").addEventListener("click", () => {
    console.log("Parent clicked");
  });

  document.getElementById("child").addEventListener("click", () => {
    console.log("Child clicked");
  });
</script>
```

**Click Output (in Console):**

```
Child clicked
Parent clicked
```

---

### 🔹 2. **Event Capturing** (Optional)

* Events are first captured by the outermost element and then move inward.

To use capturing, pass `true` as the third argument in `addEventListener`.

```javascript
document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked (capturing)");
}, true);
```

---

## 🔸 Event Delegation

Instead of adding event listeners to many child elements, add **one listener to a common parent** and detect which child was clicked.

### ✅ Why Use Event Delegation?

* Better performance for large lists or dynamic elements.
* Cleaner and more maintainable code.

### 🔹 Example:

```html
<ul id="menu">
  <li>Home</li>
  <li>About</li>
  <li>Contact</li>
</ul>

<script>
  document.getElementById("menu").addEventListener("click", function(e) {
    if (e.target.tagName === "LI") {
      console.log("Clicked on:", e.target.textContent);
    }
  });
</script>
```

Even if you add new `<li>` elements later with JavaScript, the listener still works! 🎯

---

## 🔸 Bonus: `event.stopPropagation()` and `event.preventDefault()`

* `event.stopPropagation()` – Stops the event from bubbling up.
* `event.preventDefault()` – Prevents the default browser action (e.g., submitting a form or following a link).

**Example:**

```javascript
btn.addEventListener("click", function(event) {
  event.stopPropagation(); // Stops bubbling
  event.preventDefault();  // Prevents default action
});
```

---


