## Call Stack and Memory Heap  

In JavaScript, understanding how the **Call Stack** and **Memory Heap** work is essential for writing efficient and error-free code. These two components handle the storage and execution of code within the JavaScript engine.  

---

## Memory Heap: Storing and Managing Data  
The **Memory Heap** is a large region in memory where JavaScript stores variables, objects, and other data. It allows the engine to allocate, use, and release memory dynamically.  

- Memory is allocated when variables, objects, or functions are declared.  
- Data is stored without any strict order, and variables point to specific memory locations.  
- Garbage collection automatically frees up memory when data is no longer needed.  

### Example: Storing Variables in Memory Heap  
```js
const number = 610;  
const string = "Some text";  
const human = { firstName: "Andre", lastName: "Nagwa" };  
```
- The number `610` and string `"Some text"` are stored in memory.  
- The `human` object is allocated memory, and its properties (`firstName` and `lastName`) are stored as well.  

---

## Call Stack: Managing Code Execution  
The **Call Stack** is responsible for keeping track of function calls and executing them in a **first in, last out (FILO)** order.  

- Each time a function is called, it is added to the top of the stack.  
- When a function completes execution, it is removed (popped) from the stack.  
- The stack ensures that functions run in the correct sequence.  

### Example: How Call Stack Works  
```js
function calculate() {  
    const sumTotal = 4 + 5;  
    return sumTotal;  
}  

calculate();
```
- The `calculate` function is added to the stack when called.  
- After execution, it returns `9` and is removed from the stack.  

---

## Nested Function Calls in the Call Stack  
When one function calls another, multiple functions are stacked on top of each other.  

### Example: Function Calls and the Call Stack  
```js
function subtractTwo(num) {  
    return num - 2;  
}  

function calculate() {  
    const sumTotal = 4 + 5;  
    return subtractTwo(sumTotal);  
}  

calculate();
```
- **Step 1:** `calculate()` is called and added to the stack.  
- **Step 2:** Inside `calculate`, `subtractTwo(sumTotal)` is called, pushing `subtractTwo` onto the stack.  
- **Step 3:** `subtractTwo` executes and returns `7`.  
- **Step 4:** The stack removes `subtractTwo`, then `calculate`, and finally returns the value `7`.  

---

## Tracking Execution in Developer Tools  
JavaScript’s developer console allows us to visualize how the call stack works in real-time.  

- In Chrome DevTools:  
  - Open **Sources** > **Snippets**.  
  - Add a new snippet and paste the code.  
  - Use the **Debugger** statement to pause execution at key points.  
  - Observe how functions are pushed and popped from the stack.  

---

## Understanding Global Execution Context  
- Before running any code, JavaScript creates a **Global Execution Context** (GEC).  
- This GEC is always the **first item** in the call stack.  
- When the script starts, the GEC is added to the stack.  
- As functions execute, they get added and removed from the stack.  

---

## Call Stack Behavior with Multiple Function Calls  
If a function is called multiple times, the stack keeps track of each instance.  

### Example: Running a Function Twice  
```js
calculate();  
calculate();
```
- The function `calculate()` runs once and is removed from the stack.  
- Then, it runs again, following the same process.  

---

## Stack Overflow: When the Call Stack Overflows  
A **Stack Overflow** occurs when functions keep calling themselves indefinitely, causing the stack to run out of space.  

### Example of Stack Overflow  
```js
function infiniteLoop() {  
    infiniteLoop();  
}  

infiniteLoop();  
```
- Since `infiniteLoop()` never stops calling itself, the stack keeps growing until it crashes.  

---

## Key Takeaways  
1. **Memory Heap** stores variables, objects, and functions in an unordered fashion.  
2. **Call Stack** follows a **first in, last out (FILO)** order for function execution.  
3. Functions are **pushed** onto the stack when called and **popped** when they return a value.  
4. **Nested function calls** temporarily store multiple functions in the stack.  
5. **Stack Overflow** happens when functions recurse infinitely.  
6. JavaScript uses **Garbage Collection** to free unused memory in the heap.  

Understanding the **Call Stack** and **Memory Heap** is fundamental for debugging, optimizing performance, and writing efficient JavaScript code.
