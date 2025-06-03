# 08. Code Generation

---

## What is Code Generation?

**Code generation** is the phase in which the intermediate representation is transformed into the target language, typically machine code or assembly.

---

## Goals of Code Generation

- Correctness: Generated code must preserve the semantics of the source program.
- Efficiency: Use minimal instructions, registers, and memory accesses.
- Conformity: Follow the target architecture’s conventions (calling, alignment, etc.).

---

## Steps in Code Generation

1. **Instruction Selection:** Map IR operations to machine instructions.
2. **Register Allocation and Assignment:** Assign variables/temporaries to CPU registers.
3. **Instruction Scheduling:** Order instructions to minimize stalls and hazards.
4. **Address Calculation:** Compute addresses for variables, arrays, and pointers.
5. **Handling Calling Conventions:** Set up stack frames, parameter passing, return values.

---

## Register Allocation

- Assign variables to registers where possible.
- Use heuristics or graph coloring to minimize spills to memory.

---

## Example: Code Generation for TAC

TAC:  
    t1 = a + b  
    t2 = t1 * c  
    d = t2

Machine code (x86-like):  
    MOV R1, a  
    ADD R1, b  
    MUL R1, c  
    MOV d, R1

---

## Addressing Modes

- Immediate, direct, indirect, indexed, register—all must be supported as needed by the code generator.

---

## Instruction Scheduling

- Order instructions to avoid pipeline hazards, optimize for parallel execution (superscalar).

---

## Handling Control Flow

- Translate conditional and unconditional jumps.
- Generate labels for targets.
- Handle function calls, returns, prologues/epilogues.

---

## Stack Management

- Allocate/deallocate stack frames for local variables.
- Save/restore registers as per calling convention.

---

## Interview Patterns

- Generate assembly code for a given TAC or high-level code.
- Show register allocation and instruction selection for an expression.
- Discuss calling conventions for function calls.
- Explain stack frame structure.

---

## Exercises

1. Generate machine code for `a = b + c * d`.
2. Show register allocation for a function with multiple variables.
3. Translate an if-else statement to assembly.
4. Explain how parameters are passed in C on x86.
5. Draw a stack frame for a recursive function.

---

## Key Interview Questions

- What are the goals of code generation?
- How is register allocation performed?
- What are calling conventions, and why are they important?
- How is code for control flow (branches, loops) generated?

---

## References

- [Aho et al., Compilers, Ch. 9](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Code Generation](https://www.geeksforgeeks.org/code-generation-in-compiler-design/)
- [Wikipedia: Code Generation (Compiler)](https://en.wikipedia.org/wiki/Code_generation_(compiler))
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
