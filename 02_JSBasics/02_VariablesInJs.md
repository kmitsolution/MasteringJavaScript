**JavaScript variables**, **data types**, and **object-oriented features**, then tie it all into an enhanced example.

---

## 🧠 1. JavaScript Variables — In Detail

### ✅ `var`

* **Scope**: Function-level
* **Hoisting**: Yes (moved to top of its scope but undefined)
* **Re-declaration**: Allowed
* **Use case**: Old code or for function-scoped variables

```js
function testVar() {
  console.log(x); // undefined (hoisted)
  var x = 10;
  console.log(x); // 10
}
```

### ✅ `let`

* **Scope**: Block-level
* **Hoisting**: Yes, but not accessible before declaration (TDZ - Temporal Dead Zone)
* **Re-declaration**: Not allowed in same block

```js
function testLet() {
  // console.log(y); // ReferenceError
  let y = 20;
  console.log(y); // 20
}
```

### ✅ `const`

* **Scope**: Block-level
* **Constant binding**: Cannot be reassigned
* **Note**: Objects declared with `const` **can still be modified**

```js
const z = 30;
// z = 40; // Error

const user = { name: "Alice" };
user.name = "Bob"; // Valid
```

---

## 🎨 2. JavaScript Data Types — Explained

### 🔹 Primitive Types (Immutable)

| Type      | Example                 |
| --------- | ----------------------- |
| String    | `"hello"`               |
| Number    | `123`, `3.14`           |
| Boolean   | `true`, `false`         |
| Null      | `null`                  |
| Undefined | `undefined`             |
| Symbol    | `Symbol('id')`          |
| BigInt    | `12345678901234567890n` |

### 🔹 Reference Types (Mutable)

* Object `{ key: value }`
* Array `[1, 2, 3]`
* Function `function() { }`
* Date `new Date()`
* Class Instances

---

## 🧱 3. Object-Oriented Programming (OOP) in JavaScript

### JavaScript OOP uses:

* **Objects**
* **Constructor functions**
* **Prototypes**
* **Classes** (introduced in ES6)

---

### 🏗️ Object Example

```js
let student = {
  name: "Sara",
  age: 22,
  greet: function() {
    return "Hello " + this.name;
  }
};

console.log(student.greet());
```

---

### 🏗️ Class Example (Modern JavaScript)

```js
class Animal {
  constructor(type, sound) {
    this.type = type;
    this.sound = sound;
  }

  makeSound() {
    return `${this.type} says ${this.sound}`;
  }
}

let dog = new Animal("Dog", "Woof");
console.log(dog.makeSound()); // Dog says Woof
```

---

## 🌐 Enhanced Complete HTML Page

Great idea! Moving JavaScript to an external file is a **best practice** for clean, maintainable code. Let me guide you through restructuring your example into:

---

### ✅ Folder Structure

```
project-folder/
│
├── index.html
└── js/
    └── script.js
```

---

## 📄 1. **HTML (`index.html`)**

```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Variables and OOP</title>
</head>
<body>
  <h1>Check the Console for Output</h1>

  <!-- Link to the external JS file -->
  <script src="js/script.js"></script>
</body>
</html>
```

---

## 📁 2. **JavaScript (`js/script.js`)**

```js
// === Primitive Types ===
function showPrimitiveTypes() {
  var city = "New York";
  let temperature = 28.5;
  const isRaining = false;

  console.log("City:", city);
  console.log("Temperature:", temperature);
  console.log("Is Raining:", isRaining);
}

// === Reference Types ===
function showReferenceTypes() {
  const user = {
    name: "John",
    age: 35
  };

  const hobbies = ["reading", "gaming", "cycling"];

  console.log("User Object:", user);
  console.log("Hobbies Array:", hobbies);

  console.log(greetUser(user));
}

// === Function with template literal ===
function greetUser(u) {
  return `Hello, ${u.name}`;
}

// === Object-Oriented Programming Example ===
function showVehicleInfo() {
  class Vehicle {
    constructor(brand, model) {
      this.brand = brand;
      this.model = model;
    }

    getFullName() {
      return `${this.brand} ${this.model}`;
    }
  }

  let myVehicle = new Vehicle("Tesla", "Model S");
  console.log("Vehicle:", myVehicle.getFullName());
}

// === Scope Example ===
function scopeExample() {
  if (true) {
    let scopedLet = "I'm block-scoped";
    var scopedVar = "I'm function-scoped";
    console.log(scopedLet);
  }
  // console.log(scopedLet); // Uncommenting this will throw ReferenceError
  console.log(scopedVar);
}

// === Call all functions ===
showPrimitiveTypes();
showReferenceTypes();
showVehicleInfo();
scopeExample();
```

---

## ✅ What You Achieved

* ✅ Clean separation of HTML and JavaScript
* ✅ Organized code using functions
* ✅ Reusable and modular structure
* ✅ Easy to maintain and scale

---



---

### ✅ Summary

| Feature       | `var`    | `let`     | `const`      |
| ------------- | -------- | --------- | ------------ |
| Scope         | Function | Block     | Block        |
| Hoisted       | Yes      | Yes (TDZ) | Yes (TDZ)    |
| Re-declarable | Yes      | No        | No           |
| Mutable       | Yes      | Yes       | No (binding) |


