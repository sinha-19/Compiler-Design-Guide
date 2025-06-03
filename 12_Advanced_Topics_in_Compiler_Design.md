# 12. Advanced Topics in Compiler Design

---

## Bootstrapping Compilers

- **Bootstrapping:** Writing a compiler in the language it compiles.
- **Self-hosting:** Compiler implemented in its own language.
- Used for new language development and porting.

---

## Just-in-Time (JIT) Compilation

- Compilation at runtime (not ahead-of-time).
- Used in Java Virtual Machine, .NET CLR, JavaScript engines.
- Balances interpretation and compilation for speed and flexibility.

---

## Cross Compilation

- Compiling code on one platform to run on another (e.g., compiling for ARM on an x86 machine).
- Used in embedded systems and OS development.

---

## Incremental Compilation

- Only recompiles changed portions of code.
- Used in large projects and interactive environments (IDEs).

---

## Linkers and Loaders

- **Linker:** Combines object files, resolves symbols, creates executable.
- **Loader:** Loads program into memory for execution.

---

## Preprocessors

- Handle macros, includes, conditional compilation (e.g., C preprocessor).

---

## Language Implementation Issues

- **Dynamic Typing:** Requires runtime type checks.
- **Reflection/Introspection:** Allows code to examine/modify itself at runtime.
- **Security:** Sandboxing, code verification.

---

## Source-to-Source Compilers (Transpilers)

- Convert code from one high-level language to another (e.g., TypeScript to JavaScript).

---

## Advanced Optimizations

- Profile-guided optimization
- Interprocedural and whole-program optimization
- Auto-vectorization

---

## Domain Specific Languages (DSLs)

- Specialized compilers for DSLs in finance, graphics, etc.

---

## Interview Patterns

- Explain how a compiler can compile itself (bootstrapping).
- Describe JIT compilation and its benefits.
- Discuss the role of the linker and loader.
- Explain cross-compilation for embedded systems.

---

## Exercises

1. Describe the steps in bootstrapping a new language.
2. Explain JIT compilation in the context of Java.
3. Outline the process of linking and loading.
4. Write a macro using the C preprocessor.
5. Discuss the advantages of incremental compilation.

---

## Key Interview Questions

- What is bootstrapping in compilers?
- How does JIT improve program performance?
- What are the differences between a linker and loader?
- Why is cross-compilation important?

---

## References

- [Aho et al., Compilers, Ch. 11](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Advanced Compiler Topics](https://www.geeksforgeeks.org/compiler-design-tutorials/)
- [Wikipedia: Self-hosting Compiler](https://en.wikipedia.org/wiki/Self-hosting_(compilers))
- [Wikipedia: Just-in-time Compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
