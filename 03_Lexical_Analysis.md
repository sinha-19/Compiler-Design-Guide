# 03. Lexical Analysis

---

## What is Lexical Analysis?

**Lexical analysis** is the first phase of a compiler. It converts a sequence of characters in source code into a sequence of tokens, which are atomic units such as keywords, identifiers, operators, and literals.

---

## Functions of Lexical Analyzer

- Removes whitespace and comments.
- Identifies tokens.
- Reports lexical errors (illegal characters, malformed numbers, etc.).
- Provides input to the syntax analyzer (parser).

---

## Tokens, Patterns, and Lexemes

- **Token:** Symbolic name representing a pattern (e.g., identifier, number).
- **Pattern:** Rule describing the set of lexemes for a token.
- **Lexeme:** Actual substring in the source code matched to a token.

---

## Regular Expressions in Lexical Analysis

- Used to specify token patterns.
- Example:  
    - Identifier: `[a-zA-Z_][a-zA-Z0-9_]*`
    - Integer: `[0-9]+`

---

## Finite Automata

- **Deterministic Finite Automaton (DFA):** Efficient for recognizing regular languages (token patterns).
- **Nondeterministic Finite Automaton (NFA):** Easier to construct from regex, converted to DFA for implementation.

---

## Lexical Error Handling

- Skip error character and continue scanning.
- Report error with line/column info.

---

## Symbol Table Interaction

- Lexical analyzer enters new identifiers into the symbol table.

---

## Tools for Lexical Analysis

- **Lex/Flex:** Tools for generating lexical analyzers from regex specifications.

---

## Example: Lexical Analysis Process

Source code: `int sum = a + b;`

| Lexeme | Token         |
|--------|--------------|
| int    | KEYWORD      |
| sum    | IDENTIFIER   |
| =      | ASSIGN_OP    |
| a      | IDENTIFIER   |
| +      | PLUS_OP      |
| b      | IDENTIFIER   |
| ;      | SEMICOLON    |

---

## Challenges

- Overlapping patterns (greedy matching).
- Handling literals, escape sequences, comments.
- Unicode and multi-byte characters.

---

## Interview Patterns

- Write regex for identifiers, numbers, comments.
- Construct DFA for a token pattern.
- Explain how lexical errors are handled.
- Design a simple lexical analyzer for a subset of a language.

---

## Exercises

1. Write regular expressions for:
   - Floating point numbers
   - C-style comments
2. Draw a DFA for recognizing valid identifiers.
3. Use Lex/Flex to tokenize arithmetic expressions.
4. Describe how the lexical analyzer interacts with the symbol table.
5. Explain greedy vs. non-greedy matching.

---

## Key Interview Questions

- What is the role of the lexical analyzer?
- How are regular expressions used in lexical analysis?
- What is the difference between a token, pattern, and lexeme?
- How does a DFA differ from an NFA in lexical analysis?

---

## References

- [Aho et al., Compilers, Ch. 3](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Lexical Analysis](https://www.geeksforgeeks.org/lexical-analysis-in-compiler-design/)
- [Wikipedia: Lexical Analysis](https://en.wikipedia.org/wiki/Lexical_analysis)
- [Flex (Fast Lexical Analyzer)](https://westes.github.io/flex/manual.html)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
