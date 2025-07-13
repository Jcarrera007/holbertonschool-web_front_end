# JavaScript Warm-up - Holberton School Web Front-End

![JavaScript Logo](https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png)

## 📋 Project Overview

This project is part of the Holberton School Web Front-End curriculum, designed to introduce fundamental JavaScript concepts and programming techniques. Through practical exercises, you'll learn the core principles that make JavaScript one of the most popular programming languages in the world.

## 🚀 Why JavaScript Programming is Amazing

JavaScript is incredible for many reasons:

### **Versatility**
- **Frontend Development**: Create interactive web pages and user interfaces
- **Backend Development**: Build server-side applications with Node.js
- **Mobile Apps**: Develop cross-platform mobile applications
- **Desktop Applications**: Create desktop software with Electron

### **Accessibility**
- **Easy to Learn**: Simple syntax and forgiving nature for beginners
- **Immediate Results**: Run code instantly in any web browser
- **Huge Community**: Extensive resources, libraries, and frameworks

### **Modern Features**
- **Event-Driven**: Handle user interactions and asynchronous operations
- **Dynamic Typing**: Flexible variable types that adapt at runtime
- **Functional Programming**: Support for higher-order functions and closures
- **Object-Oriented**: Classes, inheritance, and encapsulation

## 💻 How to Run a JavaScript Script

### **Method 1: Using Node.js (Recommended)**
```bash
# Install Node.js first, then run:
node script_name.js
```

### **Method 2: In a Web Browser**
```html
<!DOCTYPE html>
<html>
<head>
    <title>JavaScript Test</title>
</head>
<body>
    <script src="script_name.js"></script>
</body>
</html>
```

### **Method 3: Browser Console**
```javascript
// Open browser Developer Tools (F12)
// Go to Console tab
// Type your JavaScript code directly
console.log("Hello, World!");
```

## 🔧 Variables and Constants

### **Creating Variables and Constants**
```javascript
// Constants (cannot be reassigned)
const PI = 3.14159;
const name = "John";

// Variables (can be reassigned)
let age = 25;
let isStudent = true;

// Old way (not recommended)
var oldVariable = "avoid using var";
```

### **Differences Between var, const, and let**

| Feature | `var` | `let` | `const` |
|---------|-------|-------|---------|
| **Scope** | Function/Global | Block | Block |
| **Reassignment** | ✅ Yes | ✅ Yes | ❌ No |
| **Redeclaration** | ✅ Yes | ❌ No | ❌ No |
| **Hoisting** | ✅ Yes (undefined) | ❌ No (TDZ) | ❌ No (TDZ) |
| **Best Practice** | ❌ Avoid | ✅ Use for variables | ✅ Use for constants |

```javascript
// var issues
function varExample() {
    if (true) {
        var x = 1;  // Function-scoped
    }
    console.log(x);  // 1 (accessible outside block)
}

// let and const fix this
function letExample() {
    if (true) {
        let y = 1;     // Block-scoped
        const z = 2;   // Block-scoped
    }
    // console.log(y);  // ReferenceError
    // console.log(z);  // ReferenceError
}
```

## 📊 Data Types in JavaScript

### **Primitive Types**
```javascript
// String
const message = "Hello, World!";
const template = `My name is ${name}`;

// Number
const integer = 42;
const float = 3.14;
const negative = -10;

// Boolean
const isTrue = true;
const isFalse = false;

// Undefined
let notDefined;
console.log(notDefined);  // undefined

// Null
const empty = null;

// Symbol (ES6+)
const sym = Symbol('identifier');

// BigInt (ES2020+)
const bigNumber = 123456789012345678901234567890n;
```

### **Non-Primitive Types**
```javascript
// Object
const person = {
    name: "Alice",
    age: 30,
    isEmployed: true
};

// Array
const numbers = [1, 2, 3, 4, 5];
const mixed = [1, "hello", true, null];

// Function
function greet(name) {
    return `Hello, ${name}!`;
}

// Date
const now = new Date();
```

## 🔀 Conditional Statements

### **if and if...else Statements**
```javascript
// Basic if statement
const age = 18;
if (age >= 18) {
    console.log("You are an adult");
}

// if...else statement
const temperature = 25;
if (temperature > 30) {
    console.log("It's hot outside");
} else {
    console.log("It's not too hot");
}

// if...else if...else statement
const grade = 85;
if (grade >= 90) {
    console.log("Grade: A");
} else if (grade >= 80) {
    console.log("Grade: B");
} else if (grade >= 70) {
    console.log("Grade: C");
} else {
    console.log("Grade: F");
}

// Ternary operator
const status = age >= 18 ? "adult" : "minor";
```

## 💬 Comments

```javascript
// Single-line comment
console.log("This line runs");

/*
Multi-line comment
This is useful for longer explanations
or temporarily disabling code blocks
*/

/**
 * JSDoc comment for documentation
 * @param {string} name - The person's name
 * @returns {string} A greeting message
 */
function greet(name) {
    return `Hello, ${name}!`;
}
```

## 📝 Assigning Values to Variables

```javascript
// Direct assignment
let x = 5;
let y = 10;

// Multiple assignment
let a = 1, b = 2, c = 3;

// Assignment from expressions
let sum = x + y;
let isGreater = x > y;

// Assignment from function calls
let result = Math.max(x, y);

// Destructuring assignment
const [first, second] = [1, 2];
const {name, age} = {name: "John", age: 25};

// Assignment operators
x += 5;  // x = x + 5
y -= 3;  // y = y - 3
x *= 2;  // x = x * 2
y /= 2;  // y = y / 2
```

## 🔄 Loops

### **while Loop**
```javascript
let count = 0;
while (count < 5) {
    console.log(`Count: ${count}`);
    count++;
}

// do...while loop
let i = 0;
do {
    console.log(`i is ${i}`);
    i++;
} while (i < 3);
```

### **for Loop**
```javascript
// Traditional for loop
for (let i = 0; i < 5; i++) {
    console.log(`Iteration ${i}`);
}

// for...in loop (for objects)
const person = {name: "Alice", age: 30, job: "Developer"};
for (const key in person) {
    console.log(`${key}: ${person[key]}`);
}

// for...of loop (for arrays)
const fruits = ["apple", "banana", "orange"];
for (const fruit of fruits) {
    console.log(fruit);
}
```

### **break and continue Statements**
```javascript
// break statement
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break;  // Exit the loop
    }
    console.log(i);  // Prints 0, 1, 2, 3, 4
}

// continue statement
for (let i = 0; i < 5; i++) {
    if (i === 2) {
        continue;  // Skip this iteration
    }
    console.log(i);  // Prints 0, 1, 3, 4
}
```

## 🔧 Functions

### **Function Declaration**
```javascript
// Function declaration
function greet(name) {
    return `Hello, ${name}!`;
}

// Function expression
const multiply = function(a, b) {
    return a * b;
};

// Arrow function (ES6+)
const divide = (a, b) => a / b;
const square = x => x * x;
```

### **Function Return Values**
```javascript
// Function with return statement
function add(a, b) {
    return a + b;
}

// Function without return statement
function logMessage(message) {
    console.log(message);
    // Returns undefined automatically
}

console.log(add(5, 3));        // 8
console.log(logMessage("Hi")); // undefined
```

## 🌍 Variable Scope

```javascript
// Global scope
const globalVar = "I'm global";

function outerFunction() {
    // Function scope
    const outerVar = "I'm in outer function";
    
    if (true) {
        // Block scope
        const blockVar = "I'm in block";
        let blockLet = "Me too";
        
        console.log(globalVar);  // Accessible
        console.log(outerVar);   // Accessible
        console.log(blockVar);   // Accessible
    }
    
    // console.log(blockVar);  // ReferenceError
    
    function innerFunction() {
        console.log(globalVar);  // Accessible
        console.log(outerVar);   // Accessible
        // console.log(blockVar);  // ReferenceError
    }
}
```

## 🧮 Arithmetic Operators

```javascript
let a = 10;
let b = 3;

// Basic arithmetic
console.log(a + b);  // 13 (Addition)
console.log(a - b);  // 7  (Subtraction)
console.log(a * b);  // 30 (Multiplication)
console.log(a / b);  // 3.333... (Division)
console.log(a % b);  // 1  (Modulus/Remainder)
console.log(a ** b); // 1000 (Exponentiation)

// Increment and decrement
let x = 5;
console.log(x++);  // 5 (post-increment)
console.log(++x);  // 7 (pre-increment)
console.log(x--);  // 7 (post-decrement)
console.log(--x);  // 5 (pre-decrement)

// Comparison operators
console.log(a > b);   // true
console.log(a < b);   // false
console.log(a >= b);  // true
console.log(a <= b);  // false
console.log(a == b);  // false
console.log(a === b); // false (strict equality)
console.log(a != b);  // true
console.log(a !== b); // true (strict inequality)
```

## 📚 Working with Objects (Dictionaries)

```javascript
// Creating objects
const person = {
    name: "John",
    age: 30,
    email: "john@example.com"
};

// Accessing properties
console.log(person.name);        // "John"
console.log(person["age"]);      // 30

// Adding properties
person.phone = "123-456-7890";
person["address"] = "123 Main St";

// Modifying properties
person.age = 31;
person["email"] = "john.doe@example.com";

// Deleting properties
delete person.phone;

// Checking if property exists
console.log("name" in person);          // true
console.log(person.hasOwnProperty("age")); // true

// Getting all keys and values
const keys = Object.keys(person);
const values = Object.values(person);
const entries = Object.entries(person);

// Iterating over objects
for (const key in person) {
    console.log(`${key}: ${person[key]}`);
}

// Modern object methods
const newPerson = Object.assign({}, person, {city: "New York"});
const cloned = {...person}; // Spread operator
```

## 📥 Importing Files

### **CommonJS (Node.js)**
```javascript
// math.js
function add(a, b) {
    return a + b;
}

function subtract(a, b) {
    return a - b;
}

module.exports = {add, subtract};

// main.js
const {add, subtract} = require('./math.js');
console.log(add(5, 3));      // 8
console.log(subtract(5, 3)); // 2
```

### **ES6 Modules (Modern JavaScript)**
```javascript
// math.js
export function add(a, b) {
    return a + b;
}

export function subtract(a, b) {
    return a - b;
}

export default function multiply(a, b) {
    return a * b;
}

// main.js
import multiply, {add, subtract} from './math.js';
console.log(add(5, 3));      // 8
console.log(multiply(5, 3)); // 15
```

## 📁 Project Structure

```
javascript-warm_up/
├── 0-javascript_is_amazing.js
├── 1-multi_languages.js
├── 2-arguments.js
├── 3-value_argument.js
├── 4-concat.js
├── 5-to_integer.js
├── 6-multi_languages_loop.js
├── 7-multi_c.js
├── 8-square.js
├── 9-add.js
├── 10-factorial.js
├── 11-second_biggest.js
├── 12-object.js
├── 13-add.js
└── README.md
```

## 🎯 Learning Objectives

By completing this project, you will be able to:

- ✅ Understand why JavaScript is an amazing programming language
- ✅ Execute JavaScript scripts in different environments
- ✅ Create and manipulate variables and constants
- ✅ Differentiate between var, let, and const
- ✅ Work with all JavaScript data types
- ✅ Use conditional statements effectively
- ✅ Write clear and meaningful comments
- ✅ Assign values to variables using various methods
- ✅ Implement loops and control flow
- ✅ Create and use functions
- ✅ Understand variable scope and closures
- ✅ Perform arithmetic operations
- ✅ Manipulate objects and their properties
- ✅ Import and export modules

## 🚀 Getting Started

1. **Install Node.js** on your system
2. **Clone the repository** to your local machine
3. **Navigate** to the javascript-warm_up directory
4. **Run scripts** using `node filename.js`

## 📚 Resources

- [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript.info](https://javascript.info/)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [ECMAScript 6 Features](http://es6-features.org/)

## 🏆 Best Practices

- Use `const` by default, `let` when you need to reassign
- Avoid `var` in modern JavaScript
- Use meaningful variable names
- Write clear, concise comments
- Handle errors appropriately
- Follow consistent coding style
- Test your code thoroughly

---

**Happy coding! 🎉**