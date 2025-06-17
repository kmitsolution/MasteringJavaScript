
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


 Here's an upgraded version of the playground with a button that **dynamically adds new `<li>` items**, so you can see how **event delegation** still works even for elements added *after* the event listener is attached.

---

### ✅ Copy & paste this into an `.html` file and open in a browser:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Event Delegation Playground</title>
  <style>
    body {
      font-family: sans-serif;
    }
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
    button {
      margin-top: 10px;
      padding: 5px 10px;
    }
    a {
      display: inline-block;
      margin-top: 20px;
      color: blue;
    }
  </style>
</head>
<body>

  <h2>Event Playground (with Dynamic Items)</h2>

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
  <button id="addItem">Add Menu Item</button>

  <!-- Prevent Default -->
  <a href="https://www.google.com" id="link">Click me (Google)</a>

  <script>
    // Bubbling
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

    // Dynamically add new <li> items
    const menu = document.getElementById("menu");
    let count = 1;

    document.getElementById("addItem").addEventListener("click", () => {
      const li = document.createElement("li");
      li.textContent = "New Item " + count++;
      menu.appendChild(li);
    });
  </script>

</body>
</html>
```

---

### 🔍 Try This:

* Click **existing or new `<li>` items** – they all work with the **same listener**.
* Click **"Add Menu Item"** to create new list items.
* Check the console for logs when clicking anywhere.

---


Perfect! Let’s now expand into **form and input handling using event delegation**, and optionally introduce **custom events** if you want more advanced behavior (like building reusable components).

---

## ✅ Example: Event Delegation for Dynamic Form Fields

This version shows:

* Adding/removing dynamic form inputs
* Handling all changes with a **single delegated listener**
* Submitting the form and capturing all input values

---

### 🧪 Try This Dynamic Form Playground

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Form Event Delegation</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 20px;
    }
    .field {
      margin-bottom: 10px;
    }
    button {
      margin-right: 10px;
    }
  </style>
</head>
<body>

  <h2>Dynamic Form with Event Delegation</h2>

  <form id="myForm">
    <div id="fieldContainer">
      <div class="field">
        <input type="text" name="input1" placeholder="Enter something" />
        <button type="button" class="removeBtn">Remove</button>
      </div>
    </div>
    <button type="button" id="addField">Add Input Field</button>
    <button type="submit">Submit Form</button>
  </form>

  <script>
    const fieldContainer = document.getElementById("fieldContainer");

    // Delegate input and button events to the container
    fieldContainer.addEventListener("click", function (e) {
      if (e.target.classList.contains("removeBtn")) {
        const fieldDiv = e.target.closest(".field");
        fieldDiv.remove();
        console.log("Field removed.");
      }
    });

    // Optional: Log input changes
    fieldContainer.addEventListener("input", function (e) {
      if (e.target.tagName === "INPUT") {
        console.log("Input changed:", e.target.value);
      }
    });

    // Add new input field
    let inputCount = 2;
    document.getElementById("addField").addEventListener("click", () => {
      const div = document.createElement("div");
      div.className = "field";
      div.innerHTML = `
        <input type="text" name="input${inputCount}" placeholder="Enter something" />
        <button type="button" class="removeBtn">Remove</button>
      `;
      fieldContainer.appendChild(div);
      inputCount++;
    });

    // Handle form submit
    document.getElementById("myForm").addEventListener("submit", function (e) {
      e.preventDefault();

      const data = {};
      const inputs = fieldContainer.querySelectorAll("input");
      inputs.forEach((input, index) => {
        data[input.name || `field${index}`] = input.value;
      });

      console.log("Form submitted with values:", data);
      alert(JSON.stringify(data, null, 2));
    });
  </script>

</body>
</html>
```

---

### ✅ Features in This Example

* You can dynamically add/remove fields.
* All `input` and `click` events are handled by **delegation** on a single parent.
* When submitting, the values are collected into an object and shown via `alert()` and logged to the console.

---

### ✅ Want More?

If you’d like, I can also show:

* How to create and dispatch **custom events** between components.
* An example with **dropdowns**, **checkboxes**, or **radio buttons**.
* Integration with **local storage**, **fetch**, or **server-side code**.

Let me know your goal — form builder, app prototype, reusable widget — and I’ll tailor it.
