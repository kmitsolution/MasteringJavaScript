**Function Expressions** and **Anonymous Functions** in JavaScript 

---

## ✅ Function Expressions

A **Function Expression** is when you assign a function to a variable. The function can be **named** or **anonymous**, and it is created when the script reaches that line.

### Syntax:

```javascript
const variableName = function(parameters) {
  // code to execute
};
```

### Example:

```javascript
const sayHello = function(name) {
  console.log("Hello, " + name);
};

sayHello("Ankit");  // Output: Hello, Ankit
```

> The function is not hoisted like a function declaration. You **must define it before calling it**.

---

## ✅ Anonymous Functions

An **Anonymous Function** is a function **without a name**. It is often used in function expressions, callbacks, or as arguments to other functions.

### Example:

```javascript
const greet = function(name) {
  return "Welcome, " + name;
};

console.log(greet("Riya"));  // Output: Welcome, Riya
```

Here, `function(name) { ... }` is an anonymous function assigned to the variable `greet`.

---

### ✅ Anonymous Function in a Callback

```javascript
setTimeout(function() {
  console.log("This message appears after 2 seconds.");
}, 2000);
```

> Anonymous functions are frequently used in asynchronous code, array methods, and event handling.

---

## 🔁 Function Declaration vs Function Expression

| Feature          | Function Declaration                 | Function Expression                  |
| ---------------- | ------------------------------------ | ------------------------------------ |
| Syntax           | `function name() {}`                 | `const name = function() {}`         |
| Hoisted          | Yes (can be used before declaration) | No (must be defined first)           |
| Can be anonymous | No                                   | Yes                                  |
| Use case         | General use                          | Callbacks, conditionals, assignments |

---

## ✅ Summary

* **Function Expression**: A function assigned to a variable.
* **Anonymous Function**: A function without a name, usually used in expressions or callbacks.
* Used for **flexibility**, **inline logic**, and **asynchronous operations**.

---


