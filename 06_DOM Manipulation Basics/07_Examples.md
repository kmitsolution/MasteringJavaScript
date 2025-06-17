
* Event bubbling
* Event capturing
* Event delegation
* stopPropagation
* preventDefault

---

### ✅ Copy & paste this into an `.html` file and open it in your browser:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript Event Playground</title>
  <style>
    #parent {
      padding: 20px;
      background-color: #d1e7dd;
    }
    #child {
      padding: 10px;
      background-color: #f8d7da;
      margin-top: 10px;
    }
    ul {
      background-color: #cfe2ff;
      padding: 10px;
    }
    li {
      margin: 5px;
      cursor: pointer;
    }
    a {
      display: inline-block;
      margin-top: 20px;
      color: blue;
    }
  </style>
</head>
<body>

  <h2>Event Playground</h2>

  <!-- Bubbling & Capturing -->
  <div id="parent">
    Parent Div
    <div id="child">Child Div (Click Me)</div>
  </div>

  <!-- Event Delegation -->
  <ul id="menu">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
  </ul>

  <!-- Prevent Default -->
  <a href="https://www.google.com" id="link">Click me (Google)</a>

  <script>
    // Bubbling (default)
    document.getElementById("parent").addEventListener("click", () => {
      console.log("Parent clicked (bubbling)");
    });

    // Capturing
    document.getElementById("parent").addEventListener("click", () => {
      console.log("Parent clicked (capturing)");
    }, true);

    // Child with stopPropagation
    document.getElementById("child").addEventListener("click", (e) => {
      console.log("Child clicked - stopPropagation active");
      e.stopPropagation();
    });

    // Event Delegation on <ul>
    document.getElementById("menu").addEventListener("click", function (e) {
      if (e.target.tagName === "LI") {
        console.log("Delegated click on:", e.target.textContent);
      }
    });

    // Prevent Default on link
    document.getElementById("link").addEventListener("click", function (e) {
      e.preventDefault();
      alert("Default action prevented (no navigation)");
    });
  </script>

</body>
</html>
```

---

### 🔍 Try This:

1. **Click on the child div** — watch the console to see bubbling and capturing.
2. **Click a list item** — see how event delegation works.
3. **Click the link** — see `preventDefault` in action.
4. Open your browser’s **Console (F12)** to view the event logs.

---


