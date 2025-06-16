**Declaring and Calling functions** in JavaScript

---

## **1. Function Declaration**

This is the standard way to define a named function.

### Syntax:

```javascript
function functionName(parameters) {
  // code to execute
}
```

### Example:

```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}
```

### Calling the Function:

```javascript
greet("Rahul");
```

**Output:**

```
Hello, Rahul!
```

---

## **2. Function Expression**

You can assign a function to a variable. This is called an anonymous function expression.

### Example:

```javascript
const add = function(a, b) {
  return a + b;
};

console.log(add(5, 3));  // Output: 8
```

---

## **3. Arrow Function (ES6)**

A modern way to write functions using the `=>` syntax.

### Example:

```javascript
const multiply = (x, y) => {
  return x * y;
};

console.log(multiply(4, 6));  // Output: 24
```

You can also write it in one line if there's only one expression:

```javascript
const square = n => n * n;

console.log(square(5));  // Output: 25
```

---

## **4. Function with Default Parameters**

You can assign default values to parameters.

### Example:

```javascript
function greetUser(name = "Guest") {
  console.log("Welcome, " + name);
}

greetUser();         // Output: Welcome, Guest
greetUser("Anjali"); // Output: Welcome, Anjali
```

---

## Summary Table

| Method               | Description                           |
| -------------------- | ------------------------------------- |
| Function Declaration | Traditional named function            |
| Function Expression  | Anonymous function stored in variable |
| Arrow Function       | Concise syntax introduced in ES6      |
| Default Parameters   | Parameters with fallback values       |

---


