# 02. Phases of a Compiler

---

## Overview

The process of compilation is divided into several sequential phases, each responsible for a specific transformation or analysis of the source program.

---

## 1. Lexical Analysis (Scanner)

- Breaks source code into tokens (identifiers, keywords, literals, operators).
- Removes whitespace and comments.
- Detects lexical errors.
- Output: Sequence of tokens.

---

## 2. Syntax Analysis (Parser)

- Analyzes token sequence according to grammar rules.
- Checks for syntactical errors (structure).
- Builds **parse tree** or **syntax tree**.

---

## 3. Semantic Analysis

- Checks for semantic errors (type checking, scope, undeclared variables).
- Enforces language rules that cannot be captured by grammar alone.
- Builds and checks symbol tables.

---

## 4. Intermediate Code Generation

- Produces a machine-independent code (e.g., three-address code, abstract syntax tree).
- Eases optimization and portability.

---

## 5. Code Optimization

- Improves intermediate code without changing output.
- **Local Optimization:** Within a basic block (e.g., constant folding).
- **Global Optimization:** Across basic blocks (e.g., loop unrolling, dead code elimination).

---

## 6. Code Generation

- Converts optimized intermediate code to target machine code or assembly.
- Allocates registers, handles instruction selection and addressing.

---

## 7. Error Handling

- Reports, recovers, and tracks errors at each phase.
- Provides meaningful diagnostics to users.

---

## Passes in a Compiler

- **Pass:** Traversal of the source program (single-pass, multi-pass).
- **Single Pass:** Fast but limited analysis/optimization.
- **Multi Pass:** More complex, enables better optimization.

---

## Symbol Table

- Data structure to store information about identifiers (name, type, scope, etc.).
- Built and used throughout various phases.

---

## Intermediate Representations

- **Syntax Tree:** Abstract representation of code structure.
- **Three-Address Code (TAC):** Each instruction has at most three addresses.
- **Quadruples, Triples:** Variants of TAC for code generation.

---

## Error Recovery Techniques

- **Panic Mode:** Skip tokens until a synchronizing token is found.
- **Phrase-Level Recovery:** Correct the error locally and continue.
- **Error Productions:** Special grammar rules for common errors.
- **Global Correction:** Tries to find the minimal changes for correction (rare in practice).

---

## Interview Patterns

- Describe the role of each compiler phase.
- Explain how errors are handled and reported.
- Discuss the use of symbol tables in compilation.
- Differentiate between single pass and multi pass compilers.

---

## Exercises

1. Draw a block diagram showing all phases of a compiler.
2. Explain how intermediate code improves portability.
3. What are the advantages of multi-pass compilation?
4. How does a compiler recover from errors?
5. Describe the use of TAC and quadruples.

---

## Key Interview Questions

- Why is intermediate code generation important?
- How does semantic analysis differ from syntax analysis?
- What is the role of the symbol table?
- What are common error recovery strategies?

---

## References

- [Aho et al., Compilers – Principles, Techniques, & Tools, Ch. 1-2](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Phases of a Compiler](https://www.geeksforgeeks.org/phases-of-a-compiler/)
- [Wikipedia: Compiler](https://en.wikipedia.org/wiki/Compiler#Phases)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
