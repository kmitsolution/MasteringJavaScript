In JavaScript, **event listeners** and **events** (like `onclick`, `onmouseover`, etc.) are used to make web pages interactive by responding to user actions such as clicks, key presses, mouse movements, and more.

---

### 🔹 What Is an Event?

An **event** is an action or occurrence that happens in the browser, such as:

* Clicking a button (`click`)
* Hovering over an element (`mouseover`)
* Pressing a key (`keydown`)
* Submitting a form (`submit`)
* Loading a page (`load`)

---

### 🔹 Ways to Handle Events in JavaScript

#### ✅ 1. Using HTML Event Attributes (Not Recommended)

```html
<button onclick="sayHello()">Click Me</button>

<script>
  function sayHello() {
    alert("Hello!");
  }
</script>
```

*🟡 This mixes HTML and JavaScript, which is discouraged in modern development.*

---

#### ✅ 2. Using `element.onclick` in JavaScript

```html
<button id="myBtn">Click Me</button>

<script>
  const btn = document.getElementById("myBtn");
  btn.onclick = function () {
    alert("Button clicked!");
  };
</script>
```

*🟢 Better than inline HTML, but still limited to one handler per event.*

---

#### ✅ 3. Using `addEventListener` (Recommended)

```html
<button id="myBtn">Click Me</button>

<script>
  const btn = document.getElementById("myBtn");
  btn.addEventListener("click", function () {
    alert("Button clicked using addEventListener!");
  });
</script>
```

**Advantages:**

* Allows multiple event listeners for the same event.
* Better separation of concerns (HTML and JavaScript are separate).
* Supports event capturing and bubbling (advanced features).

---

### 🔹 Common Event Types

| Event       | Description                         |
| ----------- | ----------------------------------- |
| `click`     | Mouse click                         |
| `mouseover` | Mouse over an element               |
| `mouseout`  | Mouse leaves an element             |
| `keydown`   | Key is pressed                      |
| `keyup`     | Key is released                     |
| `submit`    | Form is submitted                   |
| `load`      | Page or resource finishes loading   |
| `change`    | Value of form element changes       |
| `input`     | Value of an input field is modified |

---

### 🔹 Example: Multiple Listeners

```html
<button id="multiBtn">Click Me</button>

<script>
  const btn = document.getElementById("multiBtn");

  btn.addEventListener("click", () => {
    console.log("Listener 1");
  });

  btn.addEventListener("click", () => {
    console.log("Listener 2");
  });
</script>
```

✔️ Both listeners will run when the button is clicked.

---


