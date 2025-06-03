# 04. Syntax Analysis (Parsing)

---

## What is Syntax Analysis?

**Syntax analysis** (parsing) is the second phase of compilation. It checks the sequence of tokens for grammatical structure according to the language’s context-free grammar (CFG).

---

## Functions of the Parser

- Builds parse tree or abstract syntax tree (AST).
- Reports syntax errors (e.g., missing semicolon, unmatched parenthesis).
- Guides semantic analysis.

---

## Context-Free Grammar (CFG)

- Set of production rules describing valid phrase structure.
- Example:  
    ```
    E → E + T | T  
    T → T * F | F  
    F → (E) | id
    ```

---

## Types of Parsers

### Top-Down Parsing

- **Recursive Descent:** Manual or automated, uses recursive procedures for non-terminals.
- **Predictive Parsing (LL Parsers):** Uses lookahead, no backtracking.
- **FIRST and FOLLOW sets:** Used in table construction.

### Bottom-Up Parsing

- **Shift-Reduce Parsing:** Builds parse tree from leaves up.
- **LR Parsers (LR(0), SLR, LALR, Canonical LR):** Most powerful, used in practice.
- **Operator Precedence Parsing:** For expressions.

---

## Parse Tree vs. Abstract Syntax Tree (AST)

- **Parse Tree:** Complete syntactic structure.
- **AST:** Simplified tree, omits some grammar details, used for semantic analysis and code generation.

---

## Error Recovery in Parsing

- **Panic Mode:** Discards tokens until a synchronizing token is found.
- **Phrase-Level Recovery:** Makes local corrections.
- **Error Productions:** Adds rules for common errors.

---

## Left Recursion and Left Factoring

- **Left Recursion:**  
    - Problematic for top-down parsers.
    - Remove by rewriting grammar.
- **Left Factoring:**  
    - Used to handle common prefixes in productions.

---

## Parser Generators

- **Yacc/Bison:** Tools for generating LALR parsers from grammar specifications.

---

## Interview Patterns

- Eliminate left recursion from a grammar.
- Construct FIRST and FOLLOW sets.
- Build LL(1) parse tables.
- Trace shift-reduce parsing steps.
- Explain difference between parse tree and AST.

---

## Exercises

1. Convert a left-recursive grammar to right-recursive.
2. Write FIRST and FOLLOW sets for a given grammar.
3. Simulate shift-reduce parsing for a simple expression.
4. Use Yacc/Bison to parse arithmetic expressions.
5. Draw the parse tree for `a + b * c`.

---

## Key Interview Questions

- What is the difference between top-down and bottom-up parsing?
- Why is left recursion a problem in recursive descent parsers?
- How are syntax errors handled in parsing?
- What is the role of the AST?

---

## References

- [Aho et al., Compilers, Ch. 4](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Syntax Analysis](https://www.geeksforgeeks.org/syntax-analysis-compiler/)
- [Wikipedia: Syntax Analysis](https://en.wikipedia.org/wiki/Syntax_analysis)
- [Bison Manual](https://www.gnu.org/software/bison/manual/bison.html)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
