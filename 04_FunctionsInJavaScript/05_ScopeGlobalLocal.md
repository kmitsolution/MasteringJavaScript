 **Function Scope** in JavaScript — specifically the difference between **Global Scope** and **Local Scope** 

---

## 🔍 What is Scope?

**Scope** refers to the part of a program where a variable is accessible.

---

## ✅ 1. Global Scope

* A variable declared **outside any function** has **global scope**.
* It can be accessed **anywhere** in the code (inside or outside functions).

### Example:

```javascript
let globalVar = "I am global";

function showGlobal() {
  console.log(globalVar); // Accessible here
}

showGlobal();  // Output: I am global
console.log(globalVar);  // Output: I am global
```

---

## ✅ 2. Local Scope (Function Scope)

* A variable declared **inside a function** has **local scope**.
* It is **only accessible within that function**.

### Example:

```javascript
function showLocal() {
  let localVar = "I am local";
  console.log(localVar);  // Accessible here
}

showLocal();  // Output: I am local
console.log(localVar);  // ❌ Error: localVar is not defined
```

> Variables defined with `let`, `const`, or `var` inside a function are **not accessible outside** that function.

---

## ✅ Mixing Global and Local

If both global and local variables have the same name, the **local one takes precedence inside the function**.

### Example:

```javascript
let name = "Global Name";

function printName() {
  let name = "Local Name";
  console.log(name);  // Output: Local Name
}

printName();
console.log(name);  // Output: Global Name
```

---

## ✅ Summary Table

| Scope Type   | Declared Where        | Accessible Where          |
| ------------ | --------------------- | ------------------------- |
| Global Scope | Outside all functions | Anywhere in the code      |
| Local Scope  | Inside a function     | Only within that function |

---

## ✅ Tip:

Variables declared with `var` are function-scoped,
but `let` and `const` are **block-scoped** (also work in loops and conditionals).


