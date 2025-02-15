# Interpreters & Compilers

Interpreters and compilers are two main ways programming languages, including JavaScript, translate code into machine-readable instructions.

- Interpreters allow code to run immediately without a compilation step, making them great for languages like JavaScript, which need fast execution in browsers. However, they can be slow when running the same code repeatedly, as they translate the same instructions each time.

- Compilers, on the other hand, take longer initially but generate optimized machine code that runs faster by avoiding redundant translations. This makes compiled code more efficient, especially for repeated operations.

To get the best of both worlds, modern browsers use Just-In-Time (JIT) compilers, like Google's V8 engine. JIT compilers start by interpreting the code (via Ignition in V8), then analyze it using a profiler to identify frequently executed code. This code is then optimized and compiled on the fly by the Turbofan compiler, improving performance over time.

Understanding this process helps developers write more efficient JavaScript and avoid patterns that might lead to de-optimizations, which slow down execution.