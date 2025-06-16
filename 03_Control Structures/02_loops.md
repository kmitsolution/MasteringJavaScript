# Loops in JavaScript

---

## 🔁 JavaScript Loops Summary with Examples

---

### ✅ 1. `for` Loop

Used when you know how many times you want to repeat a block.

#### 🔹 Syntax:

```javascript
for (initialization; condition; increment) {
  // code to execute
}
```

#### 🔹 Example:

```javascript
console.log(" for loop:");

for (let i = 1; i <= 5; i++) {
  console.log("Count: " + i);
}
```

---

### ✅ 2. `while` Loop

Repeats a block **as long as** the condition is true. The condition is checked **before** each iteration.

#### 🔹 Syntax:

```javascript
while (condition) {
  // code to execute
}
```

#### 🔹 Example:

```javascript
console.log(" while loop:");

let j = 1;
while (j <= 3) {
  console.log("Number: " + j);
  j++;
}
```

---

### ✅ 3. `do...while` Loop

Like `while`, but the block is executed **at least once** before checking the condition.

#### 🔹 Syntax:

```javascript
do {
  // code to execute
} while (condition);
```

#### 🔹 Example:

```javascript
console.log(" do...while loop:");

let k = 1;
do {
  console.log("Value: " + k);
  k++;
} while (k <= 2);
```

---

### ✅ 4. `for...of` Loop

Used to iterate **over iterable objects** like arrays, strings, etc.

#### 🔹 Syntax:

```javascript
for (let element of iterable) {
  // code to execute
}
```

#### 🔹 Example:

```javascript
console.log(" for...of loop:");

let fruits = ["Apple", "Banana", "Mango"];
for (let fruit of fruits) {
  console.log("Fruit: " + fruit);
}
```

---

### ✅ 5. `for...in` Loop

Used to iterate **over the keys (properties)** of an object.

#### 🔹 Syntax:

```javascript
for (let key in object) {
  // code to execute
}
```

#### 🔹 Example:

```javascript
console.log(" for...in loop:");

let student = {
  name: "Amit",
  age: 20,
  course: "B.Tech"
};

for (let key in student) {
  console.log(key + ": " + student[key]);
}
```

---

## 🧠 Summary Table

| Loop Type    | Best For                      | Iterates Over                  |
| ------------ | ----------------------------- | ------------------------------ |
| `for`        | Known number of iterations    | Any loop                       |
| `while`      | Unknown number, pre-condition | Any loop                       |
| `do...while` | At least once execution       | Any loop                       |
| `for...of`   | Values in arrays, strings     | Iterable (Array, String, etc.) |
| `for...in`   | Properties of objects         | Object keys                    |

---


