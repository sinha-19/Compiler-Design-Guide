# 07. Code Optimization

---

## What is Code Optimization?

**Code optimization** improves the intermediate code to make the final program run faster, occupy less memory, or use fewer resources, without changing its semantics.

---

## Types of Code Optimization

### 1. Local Optimization

- Applied within a basic block (straight-line code, no jumps).
- Examples: Constant folding, algebraic simplification, dead code elimination.

### 2. Global Optimization

- Applied across basic blocks, possibly the whole function or module.
- Examples: Loop unrolling, code motion, induction variable elimination, common subexpression elimination.

---

## Common Optimization Techniques

- **Constant Folding:** Evaluate constant expressions at compile time.
- **Constant Propagation:** Replace variables known to have constant values.
- **Dead Code Elimination:** Remove code that never executes or whose result is not used.
- **Copy Propagation:** Replace variables with their values when possible.
- **Strength Reduction:** Replace expensive operations with cheaper ones (e.g., multiplication by 2 with a shift).
- **Loop Invariant Code Motion:** Move calculations outside of loops if possible.

---

## Peephole Optimization

- Examines and replaces small sets of instructions (peepholes) with more efficient ones (e.g., sequence of moves, redundant loads/stores).

---

## Data Flow Analysis

- Tracks values and control flow to optimize across blocks.
- **Use-Def Chains:** Track where variables are defined and used.

---

## Register Allocation

- Assigns variables to CPU registers to minimize memory access.

---

## Control Flow Graph (CFG)

- Graph where nodes are basic blocks, edges represent control flow.
- Used for global optimizations.

---

## Loop Optimization

- **Unrolling:** Repeat loop body multiple times, reduce overhead.
- **Invariant Code Motion:** Move computations outside the loop.
- **Strength Reduction:** Use simpler operations in loops.

---

## Advanced Optimizations

- **Inlining:** Replace function calls with function body.
- **Tail Call Optimization:** Optimize recursive calls to prevent stack growth.
- **Vectorization:** Use SIMD instructions for data parallelism.

---

## Interview Patterns

- Identify optimization opportunities in code.
- Draw the control flow graph for a program.
- Apply constant folding and dead code elimination to TAC.
- Explain register allocation algorithms.

---

## Exercises

1. Optimize the code:  
   `for (int i=0; i<100; i++) { x = 3*4; y = x + i; }`
2. Perform constant propagation on a given TAC sequence.
3. Draw the CFG for a small function with if-else and loop.
4. Explain dead code elimination with an example.
5. Apply loop unrolling to a simple loop.

---

## Key Interview Questions

- What is the difference between local and global optimization?
- Explain how data flow analysis aids optimization.
- What is peephole optimization?
- How does register allocation work?

---

## References

- [Aho et al., Compilers, Ch. 8](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Code Optimization](https://www.geeksforgeeks.org/code-optimization-in-compiler-design/)
- [Wikipedia: Compiler Optimization](https://en.wikipedia.org/wiki/Optimizing_compiler)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
