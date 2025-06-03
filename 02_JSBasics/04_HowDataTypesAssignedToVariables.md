 In **JavaScript**, data types are assigned **automatically** — it is a **dynamically typed** language. This means:

> You do **not** declare the data type explicitly — JavaScript figures it out at runtime based on the value assigned.

---

## ✅ 1. **Automatic Type Assignment (Dynamic Typing)**

```js
let x = 42;         // x is a Number
let name = "John";  // name is a String
let isOn = true;    // isOn is a Boolean
```

> The type of a variable is based on the **value** you assign to it, and it can change:

```js
let something = 10;     // Number
something = "hello";    // Now it's a String
```

---

## ❌ You **can't** do this in JavaScript:

```js
// This will NOT work in JavaScript (but is valid in TypeScript or Java)
int x = 10;   // ❌ Error
```

---

## ✅ 2. Checking the Data Type

You can use `typeof` to find out the type of a variable:

```js
let value = 123;
console.log(typeof value); // "number"

value = "hello";
console.log(typeof value); // "string"
```

---

## ✅ 3. Explicit Typing in JavaScript?

JavaScript does **not** support type declarations directly.

### But if you want **explicit typing**, use **TypeScript**, a superset of JavaScript.

### Example in TypeScript:

```ts
let age: number = 25;
let name: string = "Alice";
let isStudent: boolean = true;
```

To use TypeScript, you need to compile it into JavaScript using the TypeScript compiler (`tsc`), since browsers only understand JavaScript.

---

## ✅ Summary

| Feature          | JavaScript                  |
| ---------------- | --------------------------- |
| Type declaration | ❌ Not required              |
| Type checking    | ✅ Use `typeof`              |
| Dynamic typing   | ✅ Yes                       |
| Static typing    | ❌ No (✅ Only in TypeScript) |

---


