# JavaScript Scope and Execution Context

## Introduction
This document provides an overview of JavaScript's execution context, scope, and lexical scoping principles. Understanding these concepts is crucial for mastering JavaScript and writing efficient, error-free code.

## Execution Context
The **execution context** defines the environment in which JavaScript code is executed. Each function execution creates a new execution context.

- Functions like `findMyName()`, `printName()`, and `sayMyName()` operate within their execution contexts.
- Functions can access variables from their own scope and parent scopes through the **scope chain**.

## Lexical Environment
The **lexical environment** determines variable accessibility based on where a function is written, not where it is called.

- JavaScript uses **lexical (static) scoping**, meaning:
  - Functions have access to variables defined in their parent environments.
  - The JavaScript compiler determines variable scope before execution.

## Scope Chain
The **scope chain** links functions to their parent environments.

- A function first searches its own scope for a variable.
- If the variable is not found, it moves up the scope chain to its parent environment.
- This continues until the global scope is reached.

Example:
```javascript
const a = 'Global';

function sayMyName() {
  const b = 'Parent';

  function findMyName() {
    const c = 'Child';
    console.log(a); // Accessible
    console.log(b); // Accessible
    console.log(c); // Accessible
  }
  findMyName();
}

sayMyName();
```

### Key Observations:
- `findMyName()` has access to variables `a`, `b`, and `c`.
- `sayMyName()` has access to `a` and `b`, but not `c`.
- The scope chain ensures functions can access parent scope variables.

## Global and Local Scope
### Global Scope
- Variables declared outside any function belong to the **global scope**.
- They are accessible from any function within the program.

### Local Scope
- Variables declared inside a function belong to the **local scope**.
- These variables are not accessible outside the function.

## Common Errors
### Undefined vs. Reference Error
- **Undefined**: A declared variable exists but has no assigned value.
- **Reference Error**: A variable is completely undeclared and inaccessible.

Example:
```javascript
console.log(x); // ReferenceError: x is not defined
let y;
console.log(y); // Undefined
```

## Avoiding Scope Issues
- Avoid using `eval()` and `with`, as they modify the scope chain and hinder performance optimizations.
- Always declare variables using `let` or `const` to prevent unintended global scope pollution.

## Conclusion
Scope in JavaScript determines the accessibility of variables and functions. By understanding lexical scoping, scope chains, and execution contexts, developers can write cleaner and more predictable code.
