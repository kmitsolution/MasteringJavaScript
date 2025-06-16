---

## 🧩 What is an Object?

An **object** is a collection of **key-value pairs** (properties). The keys are strings (or symbols), and the values can be anything — including functions!

---

## ✅ 1. Properties

Properties are values associated with an object.

### Creating an object with properties:

```javascript
let person = {
  name: "Amit",
  age: 30,
  city: "Delhi"
};

console.log(person.name);  // Output: Amit
console.log(person["age"]); // Output: 30
```

> You can access properties using **dot notation** (`person.name`) or **bracket notation** (`person["age"]`).

---

## ✅ 2. Methods

Methods are **functions attached to objects**.

### Adding a method to an object:

```javascript
let person = {
  name: "Amit",
  greet: function() {
    console.log("Hello, my name is " + this.name);
  }
};

person.greet();  // Output: Hello, my name is Amit
```

> The keyword `this` inside the method refers to the object (`person`).

---

## ✅ 3. Nesting Objects

Objects can contain other objects or arrays as properties.

### Example of nested objects:

```javascript
let student = {
  name: "Neha",
  age: 22,
  address: {
    street: "MG Road",
    city: "Mumbai",
    postalCode: 400001
  },
  subjects: ["Math", "Physics", "Chemistry"]
};

console.log(student.address.city);       // Output: Mumbai
console.log(student.subjects[1]);        // Output: Physics
```

---

## ✅ Summary Table

| Concept  | Description                      | Example                       |
| -------- | -------------------------------- | ----------------------------- |
| Property | Key-value pair inside object     | `name: "Amit"`                |
| Method   | Function as a property           | `greet: function() {}`        |
| Nesting  | Object or array inside an object | `address: { city: "Mumbai" }` |

---

**adding/deleting properties dynamically** and **looping through objects** in JavaScript.

---

## 1️⃣ Adding and Deleting Properties Dynamically

### Adding Properties

You can add properties to an existing object anytime:

```javascript
let car = {
  brand: "Toyota"
};

// Add new property
car.model = "Camry";
car["year"] = 2023;

console.log(car);
// Output: { brand: 'Toyota', model: 'Camry', year: 2023 }
```

---

### Deleting Properties

Use the `delete` keyword to remove a property:

```javascript
delete car.year;

console.log(car);
// Output: { brand: 'Toyota', model: 'Camry' }
```

---

## 2️⃣ Looping Through Objects

### Using `for...in` Loop

Iterate over **all enumerable properties** of an object:

```javascript
let person = {
  name: "Riya",
  age: 25,
  city: "Delhi"
};

for (let key in person) {
  console.log(key + ": " + person[key]);
}
/* Output:
name: Riya
age: 25
city: Delhi
*/
```

---

### Using `Object.keys()` and `forEach()`

Get all keys as an array, then loop through them:

```javascript
Object.keys(person).forEach(function(key) {
  console.log(key + ": " + person[key]);
});
```

---

### Using `Object.entries()` (ES6)

Get an array of `[key, value]` pairs and loop with `for...of`:

```javascript
for (let [key, value] of Object.entries(person)) {
  console.log(key + ": " + value);
}
```

---

## Summary

| Action                       | How to do it                           |
| ---------------------------- | -------------------------------------- |
| Add property                 | `obj.newProp = value;`                 |
| Delete property              | `delete obj.propName;`                 |
| Loop with `for...in`         | Iterates keys directly                 |
| Loop with `Object.keys()`    | Get keys array, then iterate           |
| Loop with `Object.entries()` | Get `[key, value]` pairs, then iterate |

---


 Let’s explore how to **check if a property exists** in an object and how to **clone/copy objects** in JavaScript.

---

## 1️⃣ Check if a Property Exists

### Using the `in` Operator

```javascript
let person = {
  name: "Riya",
  age: 25
};

console.log("name" in person);   // true
console.log("city" in person);   // false
```

---

### Using `hasOwnProperty()` Method

This checks if the property exists **directly on the object** (not inherited).

```javascript
console.log(person.hasOwnProperty("age"));   // true
console.log(person.hasOwnProperty("toString")); // false (inherited)
```

---

## 2️⃣ Cloning / Copying Objects

---

### a) Shallow Copy with `Object.assign()`

Copies all enumerable own properties into a new object.

```javascript
let original = { name: "Amit", age: 30 };
let copy = Object.assign({}, original);

console.log(copy);  // { name: "Amit", age: 30 }
```

> **Note:** This is a **shallow copy**; nested objects are still referenced.

---

### b) Shallow Copy with Spread Operator (`...`)

```javascript
let copy2 = { ...original };
console.log(copy2);  // { name: "Amit", age: 30 }
```

---

### c) Deep Copy (for simple objects) using `JSON.parse` and `JSON.stringify`

```javascript
let nested = {
  name: "Neha",
  address: { city: "Delhi", postalCode: 110001 }
};

let deepCopy = JSON.parse(JSON.stringify(nested));
deepCopy.address.city = "Mumbai";

console.log(nested.address.city);  // Output: Delhi
console.log(deepCopy.address.city); // Output: Mumbai
```

> **Note:** This method does **not** copy functions or handle special types like `Date`, `undefined`, or `RegExp`.

---

## Summary Table

| Task                     | How to do it                                     |
| ------------------------ | ------------------------------------------------ |
| Check property existence | `"prop" in obj` or `obj.hasOwnProperty("prop")`  |
| Shallow copy object      | `Object.assign({}, obj)` or `{ ...obj }`         |
| Deep copy object         | `JSON.parse(JSON.stringify(obj))` (simple cases) |

---



