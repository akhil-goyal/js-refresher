# Understanding Lexical Environment in JavaScript

The **lexical environment** in JavaScript refers to where code is written and how the JavaScript engine reads it during compilation. It's closely related to **lexical scope** and **lexical analysis**, which determine how variables and functions are accessed based on where they are written.

Each time an **execution context** is created (e.g., when a function runs), a new **lexical environment** is formed, like a new "universe" in which the function operates. The **global execution context** serves as the first lexical environment, where globally declared functions and variables exist.

## Key Takeaways
- **Lexical environment** refers to where code is written at compile time.
- **Lexical scope** determines which variables/functions are accessible based on their location in the code.
- **Execution context** tells us which lexical environment is currently running.
- The **first lexical environment** is the **global lexical environment**, where all top-level code exists.

Understanding lexical environments helps us grasp how JavaScript organizes and executes code, especially when dealing with scope and variable accessibility.
