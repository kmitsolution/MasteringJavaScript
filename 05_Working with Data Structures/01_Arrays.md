## 📚 Arrays in JavaScript

An **array** is a list-like object used to store multiple values in a single variable.

---

## ✅ 1. Declaring Arrays

### Using square brackets `[]`:

```javascript
let fruits = ["Apple", "Banana", "Mango"];
console.log(fruits);  // Output: ["Apple", "Banana", "Mango"]
```

### Using the `Array` constructor:

```javascript
let numbers = new Array(1, 2, 3, 4);
console.log(numbers);  // Output: [1, 2, 3, 4]
```

---

## ✅ 2. Common Array Methods

---

### `push()`

**Adds one or more elements to the end** of an array.

```javascript
fruits.push("Orange");
console.log(fruits);  // Output: ["Apple", "Banana", "Mango", "Orange"]
```

---

### `pop()`

**Removes the last element** from an array and returns it.

```javascript
let lastFruit = fruits.pop();
console.log(lastFruit); // Output: Orange
console.log(fruits);    // Output: ["Apple", "Banana", "Mango"]
```

---

### `map()`

**Creates a new array** by applying a function to every element of the original array.

```javascript
let numbers = [1, 2, 3, 4];
let squares = numbers.map(function(num) {
  return num * num;
});
console.log(squares);  // Output: [1, 4, 9, 16]
```

---

### `filter()`

**Creates a new array with elements that pass a test** (a condition).

```javascript
let numbers = [1, 2, 3, 4, 5];
let evens = numbers.filter(function(num) {
  return num % 2 === 0;
});
console.log(evens);  // Output: [2, 4]
```

---

### `shift()`

Removes the **first element** from an array.

```javascript
let firstFruit = fruits.shift();
console.log(firstFruit); // Output: Apple
console.log(fruits);     // Output: ["Banana", "Mango"]
```

---

### `unshift()`

Adds **one or more elements** to the **beginning** of an array.

```javascript
fruits.unshift("Strawberry");
console.log(fruits); // Output: ["Strawberry", "Banana", "Mango"]
```

---

### `forEach()`

Executes a provided function once for each array element (no returned array).

```javascript
fruits.forEach(function(fruit) {
  console.log("I like " + fruit);
});
```

---

### `includes()`

Checks if an array **contains** a certain element; returns `true` or `false`.

```javascript
console.log(fruits.includes("Mango")); // Output: true
console.log(fruits.includes("Apple")); // Output: false
```

---

## ✅ Summary Table of Common Array Methods

| Method       | Description                        | Returns         |
| ------------ | ---------------------------------- | --------------- |
| `push()`     | Add element(s) at the end          | New length      |
| `pop()`      | Remove last element                | Removed element |
| `shift()`    | Remove first element               | Removed element |
| `unshift()`  | Add element(s) at the beginning    | New length      |
| `map()`      | Transform each element             | New array       |
| `filter()`   | Filter elements based on condition | New array       |
| `forEach()`  | Execute function on each element   | `undefined`     |
| `includes()` | Check if array contains a value    | Boolean         |

---

Awesome! Here are some more useful **array methods** with examples, plus how to manipulate arrays using loops.

---

## 📌 Additional Array Methods

---

### 1. `find()`

Returns the **first element** that satisfies a condition.

```javascript
let numbers = [5, 12, 8, 130, 44];
let found = numbers.find(function(num) {
  return num > 10;
});
console.log(found);  // Output: 12
```

---

### 2. `findIndex()`

Returns the **index** of the first element that satisfies a condition, or `-1` if none.

```javascript
let index = numbers.findIndex(function(num) {
  return num > 10;
});
console.log(index);  // Output: 1
```

---

### 3. `slice()`

Returns a **shallow copy** of a portion of an array into a new array.

```javascript
let animals = ["Cat", "Dog", "Elephant", "Fox"];
let someAnimals = animals.slice(1, 3);
console.log(someAnimals);  // Output: ["Dog", "Elephant"]
```

---

### 4. `splice()`

Changes the contents of an array by removing or replacing existing elements and/or adding new ones.

```javascript
let months = ["Jan", "March", "April", "June"];
months.splice(1, 1, "Feb"); // At index 1, remove 1 item, add "Feb"
console.log(months);        // Output: ["Jan", "Feb", "April", "June"]
```

---

### 5. `concat()`

Combines two or more arrays.

```javascript
let arr1 = [1, 2];
let arr2 = [3, 4];
let combined = arr1.concat(arr2);
console.log(combined);  // Output: [1, 2, 3, 4]
```

---

## 📋 Manipulating Arrays Using Loops

---

### Using `for` loop

```javascript
let numbers = [10, 20, 30, 40];
for (let i = 0; i < numbers.length; i++) {
  console.log("Number at index " + i + " is " + numbers[i]);
}
```

---

### Using `for...of` loop

```javascript
for (let num of numbers) {
  console.log("Number: " + num);
}
```

---

### Using `forEach()` method

```javascript
numbers.forEach(function(num, index) {
  console.log("Index: " + index + ", Number: " + num);
});
```

---



