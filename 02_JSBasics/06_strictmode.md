In JavaScript, `"use strict"` is a **directive** that enables **Strict Mode**, a way to opt in to a restricted variant of JavaScript. This helps you write cleaner, safer code by catching common mistakes and unsafe actions.

---

### ✅ **How to Use It**

Place `"use strict"` at the **top of your script or function**:

```js
"use strict";
let x = 3.14;
```

Or inside a function:

```js
function myFunction() {
  "use strict";
  // Strict mode is active here
}
```

---

### 🔍 **What Strict Mode Does**

#### 1. **Prevents the use of undeclared variables**

```js
"use strict";
x = 10;  // ❌ ReferenceError: x is not defined
```

#### 2. **Throws error on assigning to read-only properties**

```js
"use strict";
const obj = {};
Object.defineProperty(obj, "prop", { value: 1, writable: false });
obj.prop = 2;  // ❌ TypeError
```

#### 3. **Eliminates silent errors**

Without strict mode, some errors fail silently. With strict mode, they throw exceptions.

#### 4. **Disallows duplicate parameter names**

```js
"use strict";
function sum(a, a) {}  // ❌ SyntaxError
```

#### 5. **Disallows `this` defaulting to `window` in functions**

```js
"use strict";
function test() {
  console.log(this);  // undefined instead of window
}
```

#### 6. **Disallows `with` statements**

```js
"use strict";
with (Math) { x = cos(2); }  // ❌ SyntaxError
```

---

### ⚠️ When Not to Use

* Avoid in older JavaScript environments (e.g., very old browsers).
* Be careful in 3rd-party code if you didn’t write it.

---

### 📝 Summary

**"use strict"** helps:

* Prevent hard-to-debug errors
* Make your code more secure and robust
* Prepare your code for future versions of JavaScript


