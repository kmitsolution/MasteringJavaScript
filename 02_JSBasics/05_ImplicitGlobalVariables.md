An **implicit global variable** is a variable that is **created without being declared** using `let`, `const`, or `var`.

#### 🔴 Example (Bad Practice — No Declaration)

```js
function sayHello() {
  message = "Hello, world!"; // ← Implicit global!
}
sayHello();
console.log(message); // Outputs: Hello, world!
```

In this code:

* `message` is assigned a value **without being declared**, so JavaScript creates it as a **global variable**, even though it was written inside a function.
* This behavior can lead to bugs, especially in large codebases.

---

### ✅ How to Prevent Implicit Globals with `"use strict"`

Strict mode **disallows** creating variables without a declaration. If you try to create an implicit global, it will **throw an error**.

#### ✅ Example Using `"use strict"`:

```js
"use strict";

function sayHello() {
  message = "Hello, world!"; // ❌ ReferenceError: message is not defined
}
sayHello();
```

Here:

* JavaScript stops you from accidentally creating `message` as a global.
* To fix it, you'd explicitly declare the variable:

```js
"use strict";

function sayHello() {
  let message = "Hello, world!"; // ✅ Safe
  console.log(message);
}
sayHello();
```

---

### ⚠️ Why Implicit Globals Are Problematic

* They **pollute the global scope**
* Increase the risk of **name collisions**
* Make code **harder to debug**
* Behave unpredictably across different environments (e.g., browser vs. Node.js)

---

### ✅ Best Practice

Always use `let`, `const`, or `var` to declare variables, and start files or functions with `"use strict"` to help enforce that rule.


