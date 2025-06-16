**Create, Insert, and Remove DOM elements dynamically** using JavaScript.

---

## 1️⃣ Creating New Elements

Use `document.createElement(tagName)` to create a new element.

```javascript
const newDiv = document.createElement("div");
newDiv.textContent = "I am a new div!";
newDiv.style.color = "blue";
```

---

## 2️⃣ Inserting Elements into the DOM

### a) Append as last child

```javascript
const container = document.getElementById("container");
container.appendChild(newDiv);
```

---

### b) Insert before a specific element

```javascript
const referenceNode = document.querySelector(".reference");
container.insertBefore(newDiv, referenceNode);
```

---

### c) Using `insertAdjacentHTML` or `insertAdjacentElement`

```javascript
const container = document.getElementById("container");

// Insert HTML string before end of container
container.insertAdjacentHTML("beforeend", "<p>Inserted paragraph!</p>");

// Or insert an element before the container
container.insertAdjacentElement("beforebegin", newDiv);
```

---

## 3️⃣ Removing Elements

### a) Remove a child element

```javascript
const child = document.querySelector(".child");
child.parentNode.removeChild(child);
```

---

### b) Using `.remove()` method (modern browsers)

```javascript
const child = document.querySelector(".child");
child.remove();
```

---

## 4️⃣ Example: Dynamically Add and Remove List Items

```html
<ul id="myList">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
<button id="addBtn">Add Item</button>
<button id="removeBtn">Remove Last Item</button>
```

```javascript
const list = document.getElementById("myList");
const addBtn = document.getElementById("addBtn");
const removeBtn = document.getElementById("removeBtn");

addBtn.addEventListener("click", function() {
  const newItem = document.createElement("li");
  newItem.textContent = "New Item";
  list.appendChild(newItem);
});

removeBtn.addEventListener("click", function() {
  if (list.lastElementChild) {
    list.lastElementChild.remove();
  }
});
```

---

## Summary Table

| Action                | Method/Property                              |
| --------------------- | -------------------------------------------- |
| Create element        | `document.createElement("tagName")`          |
| Add as last child     | `parent.appendChild(child)`                  |
| Insert before element | `parent.insertBefore(newElem, refElem)`      |
| Insert adjacent HTML  | `element.insertAdjacentHTML(position, html)` |
| Remove element (old)  | `parent.removeChild(child)`                  |
| Remove element (new)  | `element.remove()`                           |

---


