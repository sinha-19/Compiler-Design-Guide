# 05. Semantic Analysis

---

## What is Semantic Analysis?

**Semantic analysis** is the phase in compilation that checks for semantic errors and ensures that the program’s meaning is consistent with the language definition.

---

## Functions of Semantic Analyzer

- Type checking (e.g., int + float)
- Scope resolution (detects undeclared variables)
- Enforces language-specific rules (e.g., return type matches function type)
- Populates and checks symbol tables
- Annotates syntax tree with semantic information

---

## Type Checking

- **Static Typing:** Checked at compile time (C, Java).
- **Dynamic Typing:** Checked at runtime (Python, JavaScript).
- **Type Compatibility:** Ensures correct operations (e.g., cannot add int and string).
- **Type Conversion (Coercion):** Implicit conversion between types if allowed.

---

## Scope and Binding

- **Scope:** Region where a variable/function is visible.
    - **Block/Local Scope**
    - **Global Scope**
- **Binding:** Association of names with entities (variables, functions).
    - **Static Binding:** At compile time.
    - **Dynamic Binding:** At run time.

---

## Symbol Table

- Stores information about identifiers (type, scope, memory location).
- Built during lexical/syntax analysis, used in semantic analysis.

---

## Attribute Grammars

- Extend context-free grammars with attributes (values, types).
- **Synthesized attributes:** Computed from children (bottom-up).
- **Inherited attributes:** Passed from parent/siblings (top-down).

---

## Semantic Error Examples

- Undeclared variable usage
- Type mismatch in assignment
- Invalid function call (wrong parameters)
- Array index out of bounds (compile time)
- Multiple declarations in the same scope

---

## Static vs. Dynamic Semantics

- **Static:** Checked at compile time (types, scopes).
- **Dynamic:** Checked at runtime (array bounds, dynamic type checks).

---

## Interview Patterns

- Detect undeclared variable errors in code snippet.
- Perform type checking for expressions.
- Build and update symbol table for a code segment.
- Annotate a parse tree with types.

---

## Exercises

1. Check if the following assignment is semantically valid: `int a; float b; a = b + 2.0;`
2. Build a symbol table for a sample C function.
3. Identify semantic errors in a code snippet.
4. Explain synthesized and inherited attributes with an example.
5. Write rules for type checking arithmetic expressions.

---

## Key Interview Questions

- What is the purpose of semantic analysis?
- How does a compiler detect type errors?
- What is a symbol table, and how is it used?
- What are attribute grammars?

---

## References

- [Aho et al., Compilers, Ch. 5](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Semantic Analysis](https://www.geeksforgeeks.org/semantic-analysis-in-compiler-design/)
- [Wikipedia: Semantic Analysis (Compilers)](https://en.wikipedia.org/wiki/Semantic_analysis_(compilers))
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
