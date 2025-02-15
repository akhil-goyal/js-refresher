# Introduction to JavaScript

## JavaScript Engine

A JavaScript engine is a program that interprets and executes JavaScript code. Since computers only understand binary (1s and 0s), they can’t directly process JavaScript. The engine acts as a translator, converting JavaScript into machine code that the computer can execute.

### How It Works
You write JavaScript code

Example: ```const whatsUp = Sky;```

This is human-readable, but the computer doesn’t understand it yet.

- The JavaScript engine reads the code
- The engine takes the JavaScript file and parses it, breaking it into smaller parts for understanding.
- Conversion to machine code

The engine compiles the code into low-level instructions that the CPU can process efficiently.

### Execution

The computer executes the machine code, allowing your browser or server to perform the desired action.

### Popular JavaScript Engines

There isn’t just one JavaScript engine - there are multiple, each developed by different organizations:

- V8 (by Google) – Used in Chrome and Node.js
- SpiderMonkey (by Mozilla) – Used in Firefox
- Chakra (by Microsoft) – Used in older versions of Edge

### Why JavaScript Engines Matter
JavaScript engines have improved significantly over time. Before 2008, JavaScript execution was slow. Google revolutionized the industry with V8, making JavaScript faster by introducing Just-In-Time (JIT) compilation, which compiles code at runtime instead of interpreting it line by line.

### How JavaScript Engine works

- Lexical Analysis – The engine breaks the JavaScript code into smaller pieces called tokens, identifying key elements like variables and keywords.
- Abstract Syntax Tree (AST) – These tokens are structured into a tree-like representation of the program, allowing the engine to understand the code's logic.
- Interpreter & Compiler – The engine processes the AST through an interpreter and compiler to generate optimized machine code.

### Takeaway

JavaScript engines are the reason why JavaScript can run efficiently on browsers and servers. They constantly evolve to optimize performance, ensuring JavaScript applications - like Google Maps run smoothly.

