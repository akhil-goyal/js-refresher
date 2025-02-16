# Creating a Memory Leak in JavaScript

## How to Create a Memory Leak

A simple way to create a memory leak is by using an **infinite loop** that keeps adding data to an array.

Example:

```
let array = [];

for (let i=5; i>1; i++) {
    array.push(i-1)
}
```

Since memory is finite, this eventually **crashes the browser**.

This happens because the **garbage collector** cannot free up memory while the loop keeps adding data.

## What is a Memory Leak?

A **memory leak** occurs when memory that is no longer needed is not returned to the pool of available memory.

### Common Causes of Memory Leaks

1. **Global Variables**

   - Declaring too many global variables (`var a = 1;`) keeps them in memory.
   - If deeply nested objects are created, memory usage increases further.

2. **Event Listeners**

   - Not removing event listeners (e.g., `element.addEventListener("click", onClick)`) causes them to persist.
   - In **Single Page Applications (SPAs)**, failing to remove event listeners when navigating between pages leads to excessive memory usage.

3. **setInterval() Usage**
   - `setInterval()` continues running indefinitely unless explicitly cleared.
   - Objects referenced within it stay in memory, leading to leaks.

## Real-World Example: SoundCloud

- **SoundCloud’s JavaScript-based app** on a gaming console had a memory leak.
- Users kept the app running in the background for **hours**, causing memory usage to grow indefinitely.
- Since the app was not frequently restarted like a web page, the leak became a **critical issue**.

## Managing Memory Efficiently

- **Avoid unnecessary global variables**.
- **Remove event listeners** when they are no longer needed.
- **Clear intervals (`clearInterval()`)** when they are no longer required.
- **Monitor memory usage** to prevent crashes.

### Final Thoughts

Memory is **limited**, and JavaScript stores it in the **call stack** and **memory heap**. Writing efficient code means **avoiding memory leaks** and managing memory carefully.

Take a break, grab a coffee or tea, and see you in the next lesson!
