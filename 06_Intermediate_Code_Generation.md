# 06. Intermediate Code Generation

---

## What is Intermediate Code Generation?

**Intermediate code generation** translates the source program into an intermediate representation (IR) that is easier to optimize and can be mapped efficiently to target machine code.

---

## Why Use Intermediate Code?

- **Portability:** IR is machine-independent, enabling retargeting to various architectures.
- **Optimization:** IR simplifies analysis and transformation.
- **Separation:** Decouples front-end syntax/semantics from back-end code generation.

---

## Types of Intermediate Representations

1. **Three-Address Code (TAC):**
    - Each statement contains at most three addresses (operands).
    - Example: `t1 = a + b; t2 = t1 * c;`

2. **Quadruples and Triples:**
    - **Quadruple:** (operator, arg1, arg2, result)
    - **Triple:** (operator, arg1, arg2), result is implicit by position.

3. **Syntax Trees and DAGs:**
    - AST: Tree representation of program structure.
    - DAG: Compact graph for common subexpression elimination.

4. **Polish Notation (Postfix, Prefix):**
    - Postfix: `ab+`
    - Used in stack-based code generation.

---

## Generating TAC

- Break complex expressions into simple steps.
- Assign temporary variables for intermediate results.

**Example:**  
    `a = b * -c + b * -c`  
TAC:  
    t1 = minus c  
    t2 = b * t1  
    t3 = b * t1  
    t4 = t2 + t3  
    a = t4

---

## Intermediate Code for Control Flow

- **Conditional Jumps:** `if a < b goto L1`
- **Unconditional Jumps:** `goto L2`
- **Labels:** Mark targets for jumps.

---

## Backpatching

- Technique for handling forward jumps before target addresses are known.
- Common in loops and if-else statements.

---

## Interview Patterns

- Generate TAC for arithmetic expressions.
- Show quadruple and triple representation.
- Use backpatching for if-else/loops.
- Build a simple syntax tree for an expression.

---

## Exercises

1. Write TAC for `a = (b + c) * (d - e)`.
2. Represent `x = y * z + w` using quadruples and triples.
3. Explain how backpatching works with an example.
4. Convert an infix expression to postfix notation.
5. Draw the DAG for `a = b + c + b + c`.

---

## Key Interview Questions

- What are the advantages of using intermediate code?
- How does TAC differ from quadruples and triples?
- What is backpatching, and why is it needed?
- How does IR help in compiler portability?

---

## References

- [Aho et al., Compilers, Ch. 6](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Intermediate Code Generation](https://www.geeksforgeeks.org/intermediate-code-generation-in-compiler-design/)
- [Wikipedia: Intermediate Representation](https://en.wikipedia.org/wiki/Intermediate_representation)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
