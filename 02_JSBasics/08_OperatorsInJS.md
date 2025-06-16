In JavaScript, **operators** are special symbols or keywords used to perform operations on values and variables. Here’s a categorized breakdown of the main types of operators:

---

### 🔢 1. **Arithmetic Operators**

Used for mathematical calculations.

| Operator | Description         | Example                |
| -------- | ------------------- | ---------------------- |
| `+`      | Addition            | `5 + 3` → `8`          |
| `-`      | Subtraction         | `5 - 3` → `2`          |
| `*`      | Multiplication      | `5 * 3` → `15`         |
| `/`      | Division            | `6 / 2` → `3`          |
| `%`      | Modulus (remainder) | `5 % 2` → `1`          |
| `**`     | Exponentiation      | `2 ** 3` → `8`         |
| `++`     | Increment           | `let x = 1; x++` → `2` |
| `--`     | Decrement           | `let x = 1; x--` → `0` |

---

### 🧮 2. **Assignment Operators**

Used to assign values to variables.

| Operator | Example   | Equivalent To     |
| -------- | --------- | ----------------- |
| `=`      | `x = y`   | Assign `y` to `x` |
| `+=`     | `x += y`  | `x = x + y`       |
| `-=`     | `x -= y`  | `x = x - y`       |
| `*=`     | `x *= y`  | `x = x * y`       |
| `/=`     | `x /= y`  | `x = x / y`       |
| `%=`     | `x %= y`  | `x = x % y`       |
| `**=`    | `x **= y` | `x = x ** y`      |

---

### 🧭 3. **Comparison Operators**

Used to compare two values.

| Operator | Description                | Example     | Result  |
| -------- | -------------------------- | ----------- | ------- |
| `==`     | Equal to (type-converting) | `5 == '5'`  | `true`  |
| `===`    | Strict equal (no convert)  | `5 === '5'` | `false` |
| `!=`     | Not equal                  | `5 != '5'`  | `false` |
| `!==`    | Strict not equal           | `5 !== '5'` | `true`  |
| `>`      | Greater than               | `5 > 3`     | `true`  |
| `<`      | Less than                  | `5 < 3`     | `false` |
| `>=`     | Greater than or equal to   | `5 >= 5`    | `true`  |
| `<=`     | Less than or equal to      | `5 <= 3`    | `false` |

---

### 🔀 4. **Logical Operators**

Used to combine boolean values.

| Operator | Description | Example         | Result     |        |   |         |        |
| -------- | ----------- | --------------- | ---------- | ------ | - | ------- | ------ |
| `&&`     | Logical AND | `true && false` | `false`    |        |   |         |        |
| \`       |             | \`              | Logical OR | \`true |   | false\` | `true` |
| `!`      | Logical NOT | `!true`         | `false`    |        |   |         |        |

---

### 🔧 5. **Bitwise Operators**

Operate on binary representations.

| Operator | Description           | Example         |     |         |
| -------- | --------------------- | --------------- | --- | ------- |
| `&`      | AND                   | `5 & 1` → `1`   |     |         |
| \`       | \`                    | OR              | \`5 | 1`→`5\` |
| `^`      | XOR                   | `5 ^ 1` → `4`   |     |         |
| `~`      | NOT                   | `~5`    → `-6`  |     |         |
| `<<`     | Left shift            | `5 << 1` → `10` |     |         |
| `>>`     | Right shift           | `5 >> 1` → `2`  |     |         |
| `>>>`    | Zero-fill right shift | `5 >>> 1` → `2` |     |         |

---

### 🧠 6. **Type Operators**

Used to check or convert types.

| Operator     | Description     | Example                         |
| ------------ | --------------- | ------------------------------- |
| `typeof`     | Returns type    | `typeof "hi"` → `"string"`      |
| `instanceof` | Checks instance | `arr instanceof Array` → `true` |

---

### 🧵 7. **String Operators**

Mostly just `+` for concatenation.

```js
"Hello" + " World"  // "Hello World"
```

---

### ❓ 8. **Ternary Operator**

A shorthand for `if...else`.

```js
condition ? expr1 : expr2
// Example:
let age = 18;
let vote = age >= 18 ? "Yes" : "No";  // "Yes"
```

---

