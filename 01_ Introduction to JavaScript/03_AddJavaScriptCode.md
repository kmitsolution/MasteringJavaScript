 **How to add JavaScript to HTML** using **Inline**, **Internal**, and **External** methods—with syntax, examples, and best practices.

---

## 🧠 1. **Inline JavaScript**

JavaScript code is written **directly within an HTML element's attribute**, usually the `onclick`, `onmouseover`, etc.

### ✅ Example:

```html
<button onclick="alert('Button clicked!')">Click Me</button>
```

### ⚠️ Best for:

* Very short, simple actions.

### ❌ Avoid when:

* Code becomes long or complex—makes HTML messy and harder to maintain.

---

## 🧠 2. **Internal JavaScript**

JavaScript is added **within a `<script>` tag** directly inside the HTML file.

### ✅ Example:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Internal JS</title>
</head>
<body>
  <h1>Hello World</h1>

  <script>
    document.body.style.backgroundColor = "lightyellow";
    console.log("Internal JavaScript is working!");
  </script>
</body>
</html>
```

### 📌 Notes:

* The `<script>` tag can be placed in the `<head>` or just before `</body>`.
* If placed in the `<head>`, use `window.onload` or `DOMContentLoaded` to delay execution.

---

## 🧠 3. **External JavaScript**

JavaScript is written in a **separate `.js` file** and linked to the HTML file via the `src` attribute in the `<script>` tag.

### ✅ Example:

#### 📄 `main.js`:

```javascript
function showMessage() {
  alert("Hello from external JS!");
}
```

#### 📄 `index.html`:

```html
<!DOCTYPE html>
<html>
<head>
  <title>External JS</title>
  <script src="main.js" defer></script>
</head>
<body>
  <button onclick="showMessage()">Click Me</button>
</body>
</html>
```

### 📌 Advantages:

* Cleaner, maintainable code
* Reusable across multiple HTML files
* Easier to debug and organize

---

## 🔍 Comparison Table

| Method   | Use Case                   | Pros                          | Cons                     |
| -------- | -------------------------- | ----------------------------- | ------------------------ |
| Inline   | Quick, simple actions      | Fast, no external file needed | Messy, not scalable      |
| Internal | Small scripts in one file  | Keeps code together           | Still clutters HTML      |
| External | Real projects, reusability | Clean, maintainable, reusable | Needs extra HTTP request |

---

## ✅ Best Practices

* Prefer **external JavaScript** for real-world projects.
* Avoid inline JavaScript for anything beyond quick demos.
* Use `defer` or `async` in the `<script>` tag to control load order:

  ```html
  <script src="main.js" defer></script>
  ```

---


