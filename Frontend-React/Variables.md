# Variables in JavaScript

In JavaScript, variables are used to store and manipulate data. They act as containers for data that can be referenced and updated throughout a program.

---

## Declaring Variables
JavaScript provides three keywords for declaring variables:

   - `var` (legacy, avoid in modern code)
   - `let` (block-scoped, introduced in ES6)
   - `const` (block-scoped, for constants, introduced in ES6)

---


## 1. `var`

**Characteristics**:

1. Function Scope:
- Variables declared with `var` are scoped to the function in which they are declared.
- If declared outside a function, they are globally scoped.


2. Hoisting:
- Variables declared with `var` are hoisted to the top of their scope but are not initialized. They are `undefined` until the declaration is encountered.


3. Re-declaration:
- Variables declared with `var` can be re-declared in the same scope.

**Syntax**
```javascript
var name = "John"; // Declare and initialize
name = "Doe";      // Reassign value
var name = "Jane"; // Re-declare variable
```

**Example**
```javascript
function testVar() {
    console.log(x); // undefined (hoisting)
    var x = 10;
    console.log(x); // 10
}
testVar();
```


---


## 2. `let`
**Characteristics**

1. Block Scope:
- Variables declared with `let` are scoped to the block, statement, or expression in which they are defined.


2. Hoisting:
- Variables declared with `let` are hoisted but are not initialized. Accessing them before their declaration results in a `ReferenceError`.


3. Re-declaration:
- Variables declared with `let` cannot be re-declared in the same scope.

**Syntax**
```javascript
let age = 25; // Declare and initialize
age = 30;     // Reassign value
// let age = 40; // Error: Cannot re-declare
```

**Example**
```javascript
if (true) {
    let y = 20;
    console.log(y); // 20
}
// console.log(y); // Error: y is not defined (block-scoped)
```

---

## 3. `const`

**Characteristics**:

1. Block Scope:
- Similar to let, variables declared with const are block-scoped.

2. Hoisting:
- Variables declared with const are hoisted but not initialized, resulting in a ReferenceError if accessed before declaration.


3. Constant Value:
- Once assigned, the value of a const variable cannot be changed (immutable binding).


4. Re-declaration:
- Variables declared with const cannot be re-declared in the same scope.

**Syntax**
```javascript
const PI = 3.14; // Declare and initialize
// PI = 3.1415; // Error: Assignment to constant variable
```

**Example**
```javascript
if (true) {
    const z = 50;
    console.log(z); // 50
}
// console.log(z); // Error: z is not defined (block-scoped)
```

---

## Key Differences Between `var`, `let`, and `const`

|Feature| `var` | `let` | `const` |
|-------|-------|-------|---------|
|Scope|Function|Block|Block|
|Hoisting|Yes (initiazed to `undefined`)|Yes (uninitialized, `ReferenceError`)|Yes (uninitialized, `ReferenceError`)|
|Re-declaration|Allowed|Not allowed|Not allowed|
|Reassignment|Allowed|Allowed|Not allowed|
|Default Usage|Avoid|Use for variables that change|Use for constants|

---


### Best Practices
1. **Avoid var**: Use `let` or `const` in modern JavaScript for clarity and better scope management.


2. **Use** `const` **by Default**:
- Use const unless you know the variable's value will change.
- This ensures immutability and prevents accidental reassignments.


3. **Switch to** `let` **Only When Necessary**:
- Use let if you anticipate reassigning a variable, such as in loops.


---

## Advanced Topics Related to Variables


1. **Temporal Dead Zone (TDZ)**:

- The time between the hoisting of a `let` or `const` variable and its initialization is known as the Temporal Dead Zone.

- Accessing the variable during this phase throws a `ReferenceError`.

**Example**
```javascript
console.log(a); // ReferenceError
let a = 10;
```

2. **Global Object** (`window` or `globalThis`):

- Variables declared with `var` in the global scope become properties of the global object.
- `let` and `const` do not attach to the global object.

**Example**:

```javascript
var x = 10;
let y = 20;
console.log(window.x); // 10
console.log(window.y); // undefined
```


3. **Block Scope in Loops**:

- Each iteration of a loop creates a new block scope with `let` or `const`.


**Example**:

```javascript
for (let i = 0; i < 3; i++) {
    console.log(i); // 0, 1, 2
}
// console.log(i); // ReferenceError
```
