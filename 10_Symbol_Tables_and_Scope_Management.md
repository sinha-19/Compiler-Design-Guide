# 10. Symbol Tables and Scope Management

---

## What is a Symbol Table?

A **symbol table** is a data structure used by the compiler to store information about identifiers (variables, functions, types) in the source program.

---

## Functions of Symbol Table

- Stores identifier names, types, scopes, addresses, and attributes.
- Supports fast lookup, insertion, and deletion.
- Used throughout compilation (lexical to code generation).

---

## Operations on Symbol Table

- **Insert:** Add a new identifier.
- **Lookup:** Find properties of an identifier.
- **Delete:** Remove identifier (on scope exit).
- **Update:** Change attributes (e.g., type).

---

## Scope Management

- **Scope:** Region where an identifier is visible/accessible.
    - **Global Scope:** Visible throughout the program.
    - **Local Scope:** Visible only within a block or function.
- **Block Structure:** Nested scopes (C, Java, etc.)

---

## Implementation Techniques

- **Linear List:** Simple, slow for large tables.
- **Hash Table:** Fast average lookup (most common).
- **Tree-Based:** For ordered traversal, scoping.

---

## Handling Nested Scopes

- Stack of symbol tables (one per block/scope).
- On entering a new scope, push a new table; on exit, pop it.

---

## Attributes Stored

- Name
- Type
- Scope level
- Storage location (offset, register)
- Array dimensions, parameter lists (for functions)
- Access modifiers (private, public, etc.)

---

## Symbol Table in Semantic Analysis

- Type checking, scope resolution, duplicate definition detection.

---

## Symbol Table in Code Generation

- Provides memory locations or register assignments for variables.

---

## Interview Patterns

- Implement a symbol table using hashing.
- Manage nested scopes with a stack of tables.
- Explain operations performed on symbol tables during compilation.

---

## Exercises

1. Design a symbol table for a C function with local variables and parameters.
2. Implement insert and lookup in a hash-based symbol table.
3. Simulate scope entry and exit in a nested block.
4. Compare linear list and hash table implementations.
5. List all attributes tracked for a function symbol.

---

## Key Interview Questions

- What is the purpose of the symbol table?
- How do compilers manage nested scopes?
- What information is stored in the symbol table?
- Why are hash tables preferred for symbol tables?

---

## References

- [Aho et al., Compilers, Ch. 7](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Symbol Table](https://www.geeksforgeeks.org/symbol-table-in-compiler-design/)
- [Wikipedia: Symbol Table](https://en.wikipedia.org/wiki/Symbol_table)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
