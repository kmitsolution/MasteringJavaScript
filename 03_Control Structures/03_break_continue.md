Let's explore the **`break`** and **`continue`** statements in JavaScript — essential tools for controlling loop flow.

---

## 🔚 `break` Statement

Stops the **loop immediately**, even if the condition is still true.

### 🔹 Example:

```javascript
console.log("👉 break statement example:");

for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    console.log("Stopping loop at i = " + i);
    break;
  }
  console.log("i = " + i);
}
```

### 🔍 Output:

```
i = 1
i = 2
Stopping loop at i = 3
```

> 🟡 Use `break` when you want to **exit** a loop early based on a condition.

---

## ⏭️ `continue` Statement

**Skips** the current iteration and goes to the next one.

### 🔹 Example:

```javascript
console.log("👉 continue statement example:");

for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    console.log("Skipping i = " + i);
    continue;
  }
  console.log("i = " + i);
}
```

### 🔍 Output:

```
i = 1
i = 2
Skipping i = 3
i = 4
i = 5
```

> 🟡 Use `continue` when you want to **skip** specific iterations without stopping the whole loop.

---

## 🔁 Use with `while` or `do...while`:

### Example with `while` and `break`:

```javascript
let x = 1;
while (x <= 10) {
  if (x === 6) break;
  console.log("x = " + x);
  x++;
}
```

### Example with `do...while` and `continue`:

```javascript
let y = 0;
do {
  y++;
  if (y === 4) continue;
  console.log("y = " + y);
} while (y < 6);
```

---

## 🧠 Summary

| Statement  | What It Does                       | Use Case                          |
| ---------- | ---------------------------------- | --------------------------------- |
| `break`    | Exits the loop immediately         | Stop loop when a condition is met |
| `continue` | Skips current iteration, continues | Skip unwanted values in a loop    |

---


