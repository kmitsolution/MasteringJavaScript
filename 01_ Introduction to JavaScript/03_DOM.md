 **DOM(Document Object Model) in JavaScript** — what it is, how it works, and then visualize it with a diagram.

---

## 🧠 What is the DOM?

**DOM** stands for **Document Object Model**.

It is a **programming interface** (an API) provided by the browser that lets JavaScript **interact with and manipulate** HTML and CSS of a web page.

Think of it like a **tree structure** representing the web page — where **each HTML tag becomes an object** in a hierarchy.

---

## 🧩 JavaScript and the DOM

* When a web page loads, the **browser** parses the HTML and builds the **DOM tree**.
* JavaScript can **read or modify** this DOM — change text, styles, structure, or even remove/add elements.

### Example:

```html
<!-- HTML -->
<p id="demo">Hello!</p>

<!-- JavaScript -->
<script>
  document.getElementById("demo").innerText = "Hi from JavaScript!";
</script>
```

🔍 This JavaScript accesses the `p` tag using the DOM and changes its text.

---

## 🌳 DOM Tree Hierarchy

Now let’s draw a **conceptual diagram** of the DOM starting from `window`, then `document`, down to elements.

```
                   ┌────────────┐
                   │  window    │  ← Browser window (global)
                   └────┬───────┘
                        │
                        ▼
                   ┌────────────┐
                   │ document   │  ← Represents the HTML page
                   └────┬───────┘
                        │
                        ▼
               ┌────────────────┐
               │ <html> element │
               └────┬─────┬─────┘
                    │     │
         ┌──────────┘     └────────────┐
         ▼                             ▼
   ┌────────────┐              ┌────────────┐
   │  <head>    │              │  <body>    │
   └────┬───────┘              └────┬───────┘
        │                            │
        ▼                            ▼
 ┌────────────┐              ┌────────────┐
 │ <title>    │              │ <h1>       │
 └────────────┘              │ <p>        │
                             │ <div>      │
                             └────────────┘
```

---

### 🔑 Key DOM Objects in JavaScript

| DOM Object                      | Description                               |
| ------------------------------- | ----------------------------------------- |
| `window`                        | Global object representing browser window |
| `document`                      | The web page loaded in that window        |
| `document.body`                 | The `<body>` of the page                  |
| `document.getElementById("id")` | Finds an element by ID                    |
| `element.innerText`             | Gets or sets the text content             |
| `element.style`                 | Access or change CSS styles               |

---

## ✅ Summary:

* The **DOM** is a tree structure of HTML elements.
* **JavaScript uses the DOM API** to dynamically update content and styles.
* **`window`** is the global object; **`document`** is its child that represents the web page.
* Each HTML tag is a **node** (object) in this tree.

---

