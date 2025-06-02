## 🔹 More JavaScript Output & Interaction Functions

### 1. `alert()`

* ✅ Shows a simple message in a popup.

```javascript
alert("This is an alert message.");
```

---

### 2. `confirm()`

* ✅ Shows a dialog with **OK** and **Cancel** buttons.
* Returns `true` if the user clicks OK, `false` if Cancel.

```javascript
let isConfirmed = confirm("Do you want to continue?");
console.log("User clicked:", isConfirmed);
```

---

### 3. `prompt()`

* ✅ Shows a dialog asking the user to enter text.
* Returns the entered string or `null` if canceled.

```javascript
let name = prompt("What is your name?");
console.log("User's name is:", name);
```

---

### 4. `console.error()`, `console.warn()`, `console.info()`

* ✅ Used for different levels of logging in the console.

```javascript
console.error("This is an error message!");
console.warn("This is a warning!");
console.info("This is just some info.");
```

---

### 5. `innerHTML` (Modify page content dynamically)

* ✅ Used to write content into HTML elements.

```html
<p id="output"></p>

<script>
  document.getElementById("output").innerHTML = "Hello from innerHTML!";
</script>
```

---

## ✅ Full HTML Example Using All These Functions

```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Output Examples</title>
</head>
<body>
  <h2>JavaScript Output & Dialogs</h2>
  <p id="output"></p>

  <script>
    // 1. console.log
    console.log("Hello from console.log()");

    // 2. alert
    alert("This is an alert popup!");

    // 3. confirm
    let userConfirmed = confirm("Do you agree?");
    console.log("Confirm result:", userConfirmed);

    // 4. prompt
    let userName = prompt("Enter your name:");
    console.log("User entered name:", userName);

    // 5. document.write (avoid in production)
    document.write("<strong>Using document.write</strong><br>");

    // 6. innerHTML (preferred way to write to page)
    document.getElementById("output").innerHTML = "Hello, " + (userName || "Guest") + "!";

    // 7. console methods
    console.warn("This is a warning");
    console.error("This is an error");
    console.info("Some informational message");
  </script>
</body>
</html>
```

---

### 🔁 Summary Table

| Method             | Purpose                | Visible To User? | Best For             |
| ------------------ | ---------------------- | ---------------- | -------------------- |
| `alert()`          | Show simple popup      | ✅                | Notifications        |
| `confirm()`        | Ask Yes/No question    | ✅                | User decisions       |
| `prompt()`         | Get input from user    | ✅                | Simple input forms   |
| `console.log()`    | Log info to console    | ❌                | Debugging            |
| `console.warn()`   | Warning messages       | ❌                | Debugging            |
| `console.error()`  | Error messages         | ❌                | Debugging            |
| `document.write()` | Write directly to page | ✅                | Demos only           |
| `innerHTML`        | Modify page content    | ✅                | Dynamic page updates |


