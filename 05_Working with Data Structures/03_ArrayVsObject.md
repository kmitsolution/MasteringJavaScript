 **Array vs Object** use cases in JavaScript to help you decide when to use which.

---

## 🔄 Arrays vs Objects: When to Use What?

| Feature               | Array                                                                                              | Object                                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Purpose**           | Ordered list of items                                                                              | Collection of key-value pairs                                                                           |
| **Access**            | By **index** (numeric, zero-based)                                                                 | By **key** (string or symbol)                                                                           |
| **Use case examples** | Lists, sequences, stacks, queues, collections of similar items                                     | Dictionaries, records, configuration settings, entities with named properties                           |
| **Iteration**         | Typically with loops (`for`, `for...of`, `forEach`)                                                | Usually with `for...in`, `Object.keys()`, or `Object.entries()`                                         |
| **Methods**           | Rich built-in methods for list operations like `push()`, `pop()`, `map()`, `filter()`              | Methods related to properties and prototype chain                                                       |
| **Ordering**          | Maintains order of elements                                                                        | Order is not guaranteed (ES6+ maintains insertion order for string keys but not always reliable)        |
| **Length/Size**       | Has `.length` property                                                                             | No built-in length; use `Object.keys(obj).length`                                                       |
| **Use for**           | - Storing multiple values of the same type <br> - Maintaining order <br> - Iterating over elements | - Storing structured data with named attributes <br> - Lookup by key <br> - Grouping heterogeneous data |

---

## 📝 Examples

### Use Array for:

* List of students: `["Alice", "Bob", "Charlie"]`
* Collection of numbers: `[10, 20, 30, 40]`
* Stack or queue operations

### Use Object for:

* Storing a user profile:

```javascript
let user = {
  name: "Amit",
  age: 28,
  email: "amit@example.com"
};
```

* Configuration settings:

```javascript
let config = {
  theme: "dark",
  language: "en",
  showNotifications: true
};
```

---

## ⚡ Summary

| Scenario                              | Use Array | Use Object            |
| ------------------------------------- | --------- | --------------------- |
| When you need ordered data            | ✅         | ❌ (not guaranteed)    |
| When you need fast key lookup         | ❌         | ✅ (direct key access) |
| When items are similar and indexed    | ✅         | ❌                     |
| When items are named or heterogeneous | ❌         | ✅                     |

---

how to **convert between Arrays and Objects**, and how you can combine them effectively.

---

## 1️⃣ Convert Object to Array

### Using `Object.keys()`, `Object.values()`, or `Object.entries()`

```javascript
const user = {
  name: "Amit",
  age: 28,
  email: "amit@example.com"
};

// Get array of keys
const keys = Object.keys(user);
console.log(keys);  
// Output: ["name", "age", "email"]

// Get array of values
const values = Object.values(user);
console.log(values);  
// Output: ["Amit", 28, "amit@example.com"]

// Get array of [key, value] pairs
const entries = Object.entries(user);
console.log(entries);  
/* Output:
[
  ["name", "Amit"],
  ["age", 28],
  ["email", "amit@example.com"]
]
*/
```

---

## 2️⃣ Convert Array to Object

### Using `Object.fromEntries()`

```javascript
const entries = [
  ["name", "Amit"],
  ["age", 28],
  ["email", "amit@example.com"]
];

const userObj = Object.fromEntries(entries);
console.log(userObj);
/* Output:
{
  name: "Amit",
  age: 28,
  email: "amit@example.com"
}
*/
```

---

## 3️⃣ Combining Arrays and Objects

You can have **arrays inside objects** or **objects inside arrays** for flexible data structures.

### Example: Array of Objects

```javascript
const students = [
  { name: "Alice", age: 20 },
  { name: "Bob", age: 22 },
  { name: "Charlie", age: 21 }
];

console.log(students[1].name);  // Output: Bob
```

### Example: Object with Array Property

```javascript
const classroom = {
  roomNumber: 101,
  students: ["Alice", "Bob", "Charlie"]
};

console.log(classroom.students[2]);  // Output: Charlie
```

---

## Bonus: Iterate over Array of Objects

```javascript
students.forEach(function(student) {
  console.log(student.name + " is " + student.age + " years old.");
});

/* Output:
Alice is 20 years old.
Bob is 22 years old.
Charlie is 21 years old.
*/
```

---



