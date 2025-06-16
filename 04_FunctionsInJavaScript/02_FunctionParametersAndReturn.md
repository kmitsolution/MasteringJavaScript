**Function Parameters and Return** in JavaScript

---

## ✅ Function Parameters

Parameters are **placeholders for values** that you pass to a function when you call it.

### Example with Parameters:

```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("Amit");  // Output: Hello, Amit!
```

In this example, `name` is a **parameter**, and `"Amit"` is an **argument** passed to the function.

---

## ✅ Multiple Parameters

You can pass multiple values to a function.

### Example:

```javascript
function add(a, b) {
  console.log("Sum:", a + b);
}

add(5, 3);  // Output: Sum: 8
```

---

## ✅ Default Parameters

You can give parameters default values if no argument is passed.

### Example:

```javascript
function welcome(user = "Guest") {
  console.log("Welcome, " + user);
}

welcome();        // Output: Welcome, Guest
welcome("Neha");  // Output: Welcome, Neha
```

---

## ✅ Function Return

A function can **return** a value using the `return` statement.

### Syntax:

```javascript
function functionName(parameters) {
  return value;
}
```

### Example:

```javascript
function multiply(x, y) {
  return x * y;
}

let result = multiply(4, 5);
console.log("Result:", result);  // Output: Result: 20
```

> Once `return` is executed, the function stops and returns the value.

---

## ✅ Returning Without Parameters

Functions can return a value even if they don't take parameters.

### Example:

```javascript
function getMessage() {
  return "This is a message from the function.";
}

console.log(getMessage());
```

---

## ✅ Summary

| Concept            | Description                                |
| ------------------ | ------------------------------------------ |
| Parameters         | Variables listed in function declaration   |
| Arguments          | Actual values passed to the function       |
| Default Parameters | Fallback values if no argument is provided |
| return             | Sends a value back to the caller           |

---


