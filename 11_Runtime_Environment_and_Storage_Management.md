# 11. Runtime Environment and Storage Management

---

## What is the Runtime Environment?

The **runtime environment** is the infrastructure provided by the compiler and language runtime to support program execution, including memory organization and management.

---

## Memory Organization

- **Code Segment:** Contains executable instructions.
- **Data Segment:** Global/static variables.
- **Heap:** Dynamically allocated memory.
- **Stack:** Function calls, parameters, return addresses, local variables.

---

## Activation Record (Stack Frame)

- Stores information for a function call.
- **Fields:**
    - Return address
    - Parameters
    - Local variables
    - Saved registers
    - Control link (pointer to previous frame)
    - Access link (for non-local variables in nested functions)

---

## Calling Sequence

- Set up activation record.
- Pass parameters.
- Save caller/callee registers.
- Transfer control to callee.

---

## Heap Management

- For dynamic memory allocation (`malloc`, `new`).
- Uses free lists, garbage collection, or reference counting.

---

## Parameter Passing Mechanisms

- **Call by Value:** Copy of actual parameter.
- **Call by Reference:** Address of actual parameter.
- **Call by Name/Result:** Rare; deferred evaluation or copy out.

---

## Static vs. Dynamic Allocation

- **Static:** At compile time (globals, statics).
- **Dynamic:** At runtime (heap, stack frames).

---

## Storage Classes

- **Automatic (local variables):** Stack.
- **Static:** Data segment.
- **Dynamic:** Heap.

---

## Garbage Collection

- Automatic memory reclamation (Java, Python).
- Techniques: Reference counting, mark-and-sweep, generational GC.

---

## Interview Patterns

- Draw stack and heap layout for a function call.
- Explain activation record structure.
- Describe parameter passing in C/C++/Java.
- Discuss how garbage collection works.

---

## Exercises

1. Draw the activation record for a recursive function.
2. Explain the difference between stack and heap allocation.
3. Compare call by value and call by reference.
4. Illustrate heap fragmentation and memory leaks.
5. Describe mark-and-sweep garbage collection.

---

## Key Interview Questions

- What is an activation record?
- How does the compiler manage function calls and returns?
- What is the role of the stack and heap?
- How is memory managed in languages with garbage collection?

---

## References

- [Aho et al., Compilers, Ch. 7](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Runtime Environment](https://www.geeksforgeeks.org/runtime-environment-in-compiler-design/)
- [Wikipedia: Runtime System](https://en.wikipedia.org/wiki/Runtime_system)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
