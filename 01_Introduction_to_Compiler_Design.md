# 01. Introduction to Compiler Design

---

## What is Compiler Design?

A **compiler** is a special program that translates high-level programming language source code into machine language, intermediate code, or another programming language. Compiler design is a core subject in computer science, underlying how all software is executed across platforms.

---

## Why Study Compiler Design?

- **Deepens understanding** of how programming languages are implemented.
- **Optimizes code:** Compilers improve program efficiency and performance.
- **Essential for language design:** Enables creation of new languages and language features.
- **Interview importance:** Questions on parsing, optimization, and code generation are common in interviews.

---

## Types of Translators

- **Compiler:** Translates high-level code to machine code.
- **Interpreter:** Translates and executes code line by line.
- **Assembler:** Converts assembly code to machine code.
- **Preprocessor:** Handles directives before compilation.

---

## Compilation vs. Interpretation

| Feature        | Compiler                | Interpreter             |
| -------------- | ----------------------- | ----------------------- |
| Translation    | Whole program at once   | One statement at a time |
| Output         | Generates object code   | No object code          |
| Execution      | Fast (after compiling)  | Slower                  |
| Debugging      | Harder                  | Easier                  |

---

## Structure of a Compiler

High-level phases (see [Phases of a Compiler](02_Phases_of_a_Compiler.md)):

1. Lexical Analysis
2. Syntax Analysis
3. Semantic Analysis
4. Intermediate Code Generation
5. Code Optimization
6. Code Generation
7. Error Handling

---

## Front End vs. Back End

- **Front End:** Analyzes source code (lexical, syntax, semantic analysis).
- **Back End:** Optimizes and generates target code.

---

## Single Pass vs. Multi Pass Compilers

- **Single Pass:** Reads source code once (fast, but less analysis/optimization).
- **Multi Pass:** Multiple scans (allows complex analysis and optimizations).

---

## Cross Compiler

Generates code for a platform different from the one on which the compiler is running.

---

## Just-in-Time (JIT) Compilation

Compiles code during execution (run time), e.g., Java Virtual Machine, .NET CLR.

---

## Applications

- Programming language implementation
- Static analysis tools
- IDEs (syntax highlighting, code completion)
- Embedded systems

---

## Interview Patterns

- Compare compiler and interpreter.
- Explain why multi-pass compilation is used.
- Discuss real-world examples of JIT compilation.
- Explain the significance of cross compilers.

---

## Exercises

1. List all phases of a compiler and describe each briefly.
2. Explain the role of an assembler.
3. Why are interpreters preferred in scripting languages?
4. What is the difference between static and dynamic compilation?
5. Give examples of compiled and interpreted languages.

---

## Key Interview Questions

- What is the difference between a compiler and an interpreter?
- Why are multiple passes needed in some compilers?
- What is JIT compilation?
- What are the front end and back end of a compiler?

---

## References

- [Alfred V. Aho, Monica S. Lam, Ravi Sethi, Jeffrey D. Ullman: Compilers – Principles, Techniques, & Tools ("Dragon Book")](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Introduction to Compiler Design](https://www.geeksforgeeks.org/compiler-design-tutorials/)
- [NPTEL - Compiler Design](https://nptel.ac.in/courses/106/105/106105190/)
- [Wikipedia: Compiler](https://en.wikipedia.org/wiki/Compiler)
- [Stanford CS143: Compilers](https://web.stanford.edu/class/cs143/)

---
