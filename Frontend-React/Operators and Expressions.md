# Operators and Expressions


JavaScript is a programming language that allows developers to perform various operations using `operators` within `expressions`. Operators are symbols or keywords that perform operations on values (operands). An `expression` is any valid combination of values, variables, operators, and functions that JavaScript evaluates to produce a result.

---

## 1. Types of Operators
### 1.1. Arithmetic Operators
Used to perform mathematical operations.

|Operator|Description|Example|Result|
|--------|-----------|-------|------|
|+|Addition|`5 + 3`|`8`|
|-|Substraction|`5 -3`|`2`|
|*|Multiplication|`5 * 3`|`15`|
|/|Division|`5 / 2`|`2.5`|
|%|Modulus (remainder)|`5 % 2`|`1`|
|**|Exponentiation|`5 ** 2`|`25`|

**Example**:
```javascript
let a = 10, b = 3;
console.log(a + b);  // 13
console.log(a % b);  // 1
```

**Example**
```javascript
let a = 10, b = 3;
console.log(a + b);  // 13
console.log(a % b);  // 1
```

---

## 1.2. Assignment Operators
Used to assign values to variables.

|Operator|Description|Example|Equivalent To|
|--------|-----------|-------|-------------|
|`=`|Assignment|`x = 5`|`x = 5`|
|`+=`|Add and assign|`x += 3`|`x = x + 3`|
|`_=`|Subtract and assign|`x -= 3`|`x = x - 3`|
|`*=`|Multiply and assign|`x *= 3`|`x = x * 3`|
|`/=`|Divide and assign|`x /= 3`|`x = x / 3`|
|`%=`|Modulus and assign|`x %= 3`|`x = x % 3`|
|`**=`|Exponentiation and assign|`x **= 3`|`x = x ** 3`|

**Example**
```javascript
let x = 10;
x += 5; // x = x + 5
console.log(x); // 15
```

---

## 1.3. Comparison Operators
Used to compare two values and return a boolean (`true` or `false`).

|Operator|Description|Example|Result|
|--------|-----------|-------|------|
|`==`|Equal to|`5 == "5"`|`true`|
|`===`|Strict equal to|`5 === "5"`|`false`|
|`!=`|Not equal to|`5 != "6"`|`true`|
|`!==`|Strict not equal to|`5 !== "5"`|`true`|
|`>`|Greater than|`5 > 3`|`true`|
|`<`|Less than|`5 < 3`|`false`|
|`>=`|Greater than or equal to|`5 >= 5`|`true`|
|`<=`|Less than or equal to|`5 <= 3`|`false`|


**Example**:
```javascript
console.log(5 == "5");  // true
console.log(5 === "5"); // false
```

---

















