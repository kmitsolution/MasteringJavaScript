In JavaScript, **control structures** like conditional statements are used to make decisions in code. Here's a clear explanation of each with examples:

---

## ✅ 1. `if` Statement

Executes a block of code **only if the condition is true**.

### 🔹 Syntax:

```javascript
if (condition) {
  // code to execute if condition is true
}
```

### 🔹 Example:

```javascript
let age = 18;

if (age >= 18) {
  console.log("You are eligible to vote.");
}
```

---

## ✅ 2. `if...else` Statement

Executes one block if the condition is true, another block if false.

### 🔹 Syntax:

```javascript
if (condition) {
  // code if condition is true
} else {
  // code if condition is false
}
```

### 🔹 Example:

```javascript
let isRaining = false;

if (isRaining) {
  console.log("Take an umbrella.");
} else {
  console.log("Enjoy the sunshine!");
}
```

---

## ✅ 3. `if...else if...else` Statement

Used to check **multiple conditions** in sequence.

### 🔹 Syntax:

```javascript
if (condition1) {
  // code for condition1
} else if (condition2) {
  // code for condition2
} else {
  // code if none of the above conditions are true
}
```

### 🔹 Example:

```javascript
let marks = 75;

if (marks >= 90) {
  console.log("Grade: A");
} else if (marks >= 75) {
  console.log("Grade: B");
} else if (marks >= 60) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}
```

---

## ✅ 4. `switch` Statement

Used to **select one of many code blocks to execute**, based on a value.

### 🔹 Syntax:

```javascript
switch(expression) {
  case value1:
    // code block
    break;
  case value2:
    // code block
    break;
  default:
    // default code block
}
```

### 🔹 Example:

```javascript
let day = 3;

switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  case 3:
    console.log("Wednesday");
    break;
  default:
    console.log("Invalid day");
}
```

> 🔸 **`break`** stops the execution once a case matches. Without it, JavaScript continues to the next case ("fall-through").

---

Would you like a printable summary or interactive code you can test?
