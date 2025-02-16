# Garbage Collection in JavaScript: What You Need to Know  

JavaScript is a **garbage-collected language**, meaning it **automatically** allocates and frees up memory when objects are no longer needed. This prevents memory from being unnecessarily occupied, ensuring efficient memory usage.  

However, **garbage collection isn't perfect**. Many developers assume they don’t need to worry about memory management, but mistakes can still lead to **memory leaks**—when unused memory remains allocated, gradually consuming resources.  

## How Garbage Collection Works  
JavaScript uses the **Mark and Sweep algorithm**:  
1. **Mark** – Identifies objects still in use.  
2. **Sweep** – Removes objects no longer referenced.  

For example, if an object in memory is no longer linked to a variable, the garbage collector removes it to free up space.  

## Comparing JavaScript to Low-Level Languages  
In languages like **C**, developers manually manage memory, which can be risky but allows for highly optimized performance. JavaScript automates this, making coding safer but sometimes leading to inefficiencies.  

## Why This Matters  
Understanding garbage collection helps **prevent memory leaks** and optimize performance. Now that we know how it works, we can dive into common **memory leak issues** in JavaScript.  
