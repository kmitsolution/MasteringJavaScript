 **Event Listeners** in JavaScript — how to listen for user actions like clicks, mouse movements, key presses, and more.

---

## 🎯 What is an Event Listener?

An **event listener** is a function that waits for an event (like a click or key press) on a DOM element and runs when the event occurs.

---

## 🔥 Adding Event Listeners

Use `element.addEventListener(eventType, callbackFunction)` to attach an event listener.

---

## Common Events and Examples

### 1️⃣ Click Event

```html
<button id="btn">Click Me</button>
```

```javascript
const btn = document.getElementById("btn");

btn.addEventListener("click", function() {
  alert("Button was clicked!");
});
```

---

### 2️⃣ Mouseover and Mouseout Events

```html
<div id="hoverBox" style="width:100px; height:100px; background:lightgray;">Hover me</div>
```

```javascript
const box = document.getElementById("hoverBox");

box.addEventListener("mouseover", function() {
  box.style.backgroundColor = "lightblue";
});

box.addEventListener("mouseout", function() {
  box.style.backgroundColor = "lightgray";
});
```

---

### 3️⃣ Keydown Event (Detect keyboard key press)

```html
<input type="text" id="inputBox" placeholder="Type something...">
```

```javascript
const input = document.getElementById("inputBox");

input.addEventListener("keydown", function(event) {
  console.log("Key pressed: " + event.key);
});
```

---

### 4️⃣ Other Useful Events

| Event Type | Description                |
| ---------- | -------------------------- |
| `dblclick` | Double-click event         |
| `submit`   | Form submission            |
| `change`   | Input value changes        |
| `focus`    | Element gains focus        |
| `blur`     | Element loses focus        |
| `scroll`   | When a user scrolls        |
| `resize`   | When the window is resized |

---

## Removing Event Listeners

You can remove an event listener using `removeEventListener`, but you need a **named function**:

```javascript
function onClick() {
  alert("Clicked!");
}

btn.addEventListener("click", onClick);

// Later, remove the listener
btn.removeEventListener("click", onClick);
```

---

## Summary

| Method                | Usage                                      |
| --------------------- | ------------------------------------------ |
| Add event listener    | `element.addEventListener("event", fn)`    |
| Remove event listener | `element.removeEventListener("event", fn)` |

---


