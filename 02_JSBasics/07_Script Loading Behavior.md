
When you include a `<script>` in an HTML page, **when the script executes depends on how and where it's included**, as well as any additional attributes (like `defer` or `async`).

### 🔹 1. **Script in the `<head>` without `defer` or `async`**

```html
<head>
  <script>
    console.log("Script in head runs immediately as it is parsed");
  </script>
</head>
```

* **Executed immediately** as the browser parses the HTML.
* This happens **before** the body is loaded or rendered.

---

### 🔹 2. **Script in the `<body>`**

```html
<body>
  <p>Hello</p>
  <script>
    console.log("Script in body runs during parsing");
  </script>
</body>
```

* Executed as the browser **parses the HTML line-by-line**.
* So it runs when the parser reaches the `<script>` tag — **not necessarily on `window.onload` or after the whole page is rendered**.

---

### 🔹 3. **Using `window.onload`**

```html
<script>
  window.onload = function() {
    console.log("This runs after all content (including images) is fully loaded");
  };
</script>
```

* Code inside `window.onload` executes **only after the entire page (HTML, images, stylesheets, etc.) is completely loaded**.

---

### 🔹 4. **Using `document.addEventListener('DOMContentLoaded', ...)`**

```html
<script>
  document.addEventListener('DOMContentLoaded', function() {
    console.log("DOM is fully parsed, but images/styles might not be loaded yet");
  });
</script>
```

* Executes **as soon as the HTML is fully parsed** — faster than `window.onload`.

---

### 🔹 5. **Using `defer` or `async` with external scripts**

```html
<script src="script.js" defer></script>
<script src="script.js" async></script>
```

* `defer`: Executes **after HTML is parsed**, just before `DOMContentLoaded`.
* `async`: Executes **as soon as it's downloaded**, which can interrupt parsing.

---

### ✅ Summary

| Placement / Method            | Execution Timing                            |
| ----------------------------- | ------------------------------------------- |
| `<script>` in `<head>`        | Immediately, during parsing                 |
| `<script>` at end of `<body>` | When parser reaches it                      |
| `window.onload`               | After everything loads (HTML, images, etc.) |
| `DOMContentLoaded`            | After HTML parsing only                     |
| `defer`                       | After HTML is parsed                        |
| `async`                       | As soon as script is ready                  |


