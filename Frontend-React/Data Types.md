# Data Types in JavaScript

JavaScript is a **dynamically typed language**, meaning variables can hold values of any data type, and the type of value can change during execution. It supports **primitive** and **non-primitive** (**reference**) data types.


## 1. Primitive Data Types

Primitive data types are immutable and stored by value. These types include:

### 1.1. Number
- Used to represent numerical values (both integers and floating-point numbers).
- Follows the IEEE-754 standard for 64-bit floating-point numbers.
- Includes special numeric values:
   - `Infinity`: Result of dividing by 0 or a value too large to represent.
   - `-Infinity`: Result of negative values divided by 0 or a very large negative number.
   - `NaN` (Not-a-Number): Indicates an invalid mathematical operation.
 
**Example**
```javascript
let integer = 42;         // Integer
let float = 3.14;         // Floating-point number
let inf = 1 / 0;          // Infinity
let invalid = "a" / 2;    // NaN
```

**Functions**:
- `isNaN(value)`: Checks if a value is NaN.
- `Number.isInteger(value)`: Checks if a value is an integer.
- `parseFloat(value)` and `parseInt(value)`: Converts strings to numbers.


---

### 1.2. String
- Represents a sequence of characters.
- Enclosed in single (`'`), double (`"`), or backticks (``).
- Strings are immutable; once created, they cannot be changed (but you can assign a new string to the variable).

**Example**:
```javascript
let singleQuote = 'Hello';
let doubleQuote = "World";
let template = `The result is ${42}`; // Template literals
```

**Common Methods**:
- `length`: Returns the string's length.
- `toUpperCase()`, `toLowerCase()`: Converts case.
- `substring(start, end)`, `slice(start, end)`: Extracts parts of a string.
- `trim()`: Removes whitespace.
- `split(delimiter)`: Splits a string into an array.


---


### 1.3. Boolean
- Represents logical values: `true` or `false`.
- Often used in conditions.


**Example**
```javascript
let isTrue = true;
let isFalse = false;
```
**Example in Conditional Statement**:

```javascript
if (isTrue) {
    console.log("This is true!");
}
```

---

### 1.4. Undefined
- A variable declared but not assigned a value has the value `undefined`.
- The type of undefined is `"undefined"`.


**Example**:
```javascript
let x;
console.log(x); // undefined
```

---

### 1.5. Null
- Represents the intentional absence of any object value.
- The type of `null` is `"object"` (a historical bug in JavaScript).


**Example**:
```javascript
let y = null;
console.log(y); // null
```

---

### 1.6. Symbol (ES6)
- A unique and immutable primitive value.
- Used as unique property keys in objects.


**Example**:
```javascript
let sym = Symbol("unique");
console.log(sym); // Symbol(unique)
```

---

### 1.7. BigInt (ES11)
- Represents integers larger than the maximum safe integer in JavaScript (`2^53 - 1`).
- Created by appending n to the end of the number.


**Example**:
```javascript
let big = 123456789012345678901234567890n;
console.log(big + 1n); // Works with BigInt
```

---

# 2. Non-Primitive (Reference) Data Types
Non-primitive types are objects stored by reference.


### 2.1. Object
- A collection of key-value pairs.
- Keys can be strings or symbols; values can be any data type.


**Example**:
```javascript
let person = {
    name: "John",
    age: 30,
    greet: function() {
        return "Hello!";
    }
};
console.log(person.name); // "John"
```

---

### 2.2. Array
- Special type of object for storing ordered collections.
- Indexed starting at 0.


**Example**:
```javascript
let fruits = ["apple", "banana", "cherry"];
console.log(fruits[1]); // "banana"
```

---


### 2.3. Function
- Functions are callable objects that can execute a block of code.
- First-class citizens: They can be assigned to variables, passed as arguments, and returned from other functions.


**Example**:
```javascript
function add(a, b) {
    return a + b;
}
console.log(add(5, 3)); // 8
```

---


### 2.4. Date
- Used to work with dates and times.


**Example**:
```javascript
let now = new Date();
console.log(now); // Current date and time
```

---

### 2.5. RegExp
- Represents regular expressions for pattern matching in strings.


**Example**:
```javascript
let pattern = /hello/i; // Case-insensitive pattern
console.log(pattern.test("Hello")); // true
```

---

# 3. Type Conversion
## Implicit Type Conversion (Type Coercion):
JavaScript converts values between types automatically.

**Example**:
```javascript
console.log("5" + 2); // "52" (string concatenation)
console.log("5" - 2); // 3 (number subtraction)
```

### Explicit Type Conversion:
You can convert values using methods like `String()`, `Number()`, `Boolean()`.

**Example**:
```javascript
console.log(Number("42"));   // 42
console.log(String(42));     // "42"
console.log(Boolean(1));     // true
```

---

### 4. Checking Data Types
To check the type of a value, use the `typeof` operator.

**Example**:

```javascript
console.log(typeof 42);        // "number"
console.log(typeof "hello");   // "string"
console.log(typeof true);      // "boolean"
console.log(typeof undefined); // "undefined"
console.log(typeof null);      // "object" (quirk in JavaScript)
console.log(typeof Symbol());  // "symbol"
console.log(typeof {});        // "object"
console.log(typeof []);        // "object"
console.log(typeof function(){}); // "function"
```
