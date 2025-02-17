# How JavaScript Runs Code

In JavaScript, code runs inside an **execution context**. The **JavaScript engine** creates an execution context every time a function is called. 

## 1. Global Execution Context  
- When JavaScript runs, it first creates a **global execution context**.  
- This includes the **global object** (like `window` in browsers or `global` in Node.js) and the `this` keyword.

## 2. Function Execution Contexts  
- When a function is called, a new **execution context** is created and added to the **call stack**.  
- Each function creates its own execution context, which is pushed onto the stack and later popped off when the function completes.

## 3. Execution Phases  
- **Creation Phase**: The JavaScript engine sets up the environment (global execution context, variables, and functions).  
- **Execution Phase**: The code runs, executing functions and managing the call stack.

## 4. Global Object & `this`  
- Even in an empty JavaScript file, the `this` keyword and the global object (`window` in browsers) are already available.  
- Example: Declaring `var a = "Apples";` adds `a` to the global object (`window.a === "Apples"`).

Whenever JavaScript runs code, it always does so within an execution context—either global or function-specific.
