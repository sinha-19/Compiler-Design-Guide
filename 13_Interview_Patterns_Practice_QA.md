# 13. Interview Patterns, Practice, and Q&A

---

## 1. Lexical Analysis

- **Pattern:** Write regex for identifiers, numbers, comments.
- **Practice:**  
  - DFA for valid identifier.
  - Use Lex/Flex for arithmetic expressions.

---

## 2. Syntax Analysis

- **Pattern:** Eliminate left recursion, build parse tables, simulate parsing.
- **Practice:**  
  - Convert grammar, build FIRST/FOLLOW.
  - Trace shift-reduce parse.

---

## 3. Semantic Analysis

- **Pattern:** Type checking, symbol table management.
- **Practice:**  
  - Build symbol table for a code snippet.
  - Check semantic errors.

---

## 4. Intermediate Code Generation

- **Pattern:** Generate TAC, quadruples, triples.
- **Practice:**  
  - TAC for arithmetic and control flow.
  - Backpatching.

---

## 5. Code Optimization

- **Pattern:** Spot and apply optimizations (constant folding, DCE).
- **Practice:**  
  - Optimize code segment.
  - Draw CFG and apply global optimization.

---

## 6. Code Generation

- **Pattern:** Generate assembly, explain register allocation.
- **Practice:**  
  - Assembly for expressions, if-else, loops.
  - Draw stack frame.

---

## 7. Error Handling

- **Pattern:** Simulate panic mode, design error productions.
- **Practice:**  
  - Error message for undeclared variable.
  - Recovery for missing semicolon.

---

## Sample Interview Questions

- What is the difference between compiler and interpreter?
- How do you remove left recursion from a grammar?
- What is the purpose of intermediate code?
- Explain different types of code optimization.
- How does register allocation work in code generation?
- Describe error recovery in parsing.
- What is bootstrapping in compilers?
- How does a compiler manage scopes and symbol tables?

---

## Exercises

1. Write regex for floating point numbers and comments.
2. Build a parse tree for an expression.
3. Generate TAC for a control flow statement.
4. Optimize a loop using code motion.
5. Draw the activation record for a recursive function call.

---

## Resources for Practice

- [GeeksforGeeks - Compiler Design Interview Questions](https://www.geeksforgeeks.org/compiler-design-interview-questions/)
- [Brilliant - Compiler Construction](https://brilliant.org/wiki/compiler-construction/)
- [Stanford CS143: Compilers](https://web.stanford.edu/class/cs143/)
- [NPTEL - Compiler Design](https://nptel.ac.in/courses/106/105/106105190/)
- [Lex and Yacc for Beginners](https://epaperpress.com/lexandyacc/)

---

## Summary

Compiler Design questions test your understanding of theory, language processing, and systems. Practice each phase, focus on common patterns, and be ready to explain your reasoning and choices.

---
