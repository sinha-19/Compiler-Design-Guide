# 09. Error Handling and Recovery

---

## Why is Error Handling Important?

Compilers must detect, report, and recover from errors to provide meaningful feedback and continue processing as much of the source as possible.

---

## Types of Errors

1. **Lexical Errors:** Illegal characters or malformed tokens.
2. **Syntax Errors:** Grammar violations (e.g., missing parenthesis).
3. **Semantic Errors:** Type mismatches, undeclared variables.
4. **Logical Errors:** Not detected by compiler (wrong algorithm).

---

## Error Detection

- Each phase detects its own errors and passes them forward.
- Early detection leads to better error messages and easier recovery.

---

## Error Reporting

- Should be clear, informative, and point to the source location.
- Include suggestions when possible.

---

## Error Recovery Strategies

### 1. Panic Mode

- Skip input until a synchronizing token is found.
- Simple, avoids cascading errors.

### 2. Phrase-Level Recovery

- Make local corrections (insert, delete, replace tokens).
- Continue parsing with minimal disruption.

### 3. Error Productions

- Add grammar rules to recognize common errors.

### 4. Global Correction

- Attempt to make minimal changes to fix all errors.
- Rarely practical.

---

## Examples

- Misspelling a keyword (`whlie` instead of `while`)
- Missing semicolon or parenthesis
- Using undeclared variable

---

## Error Recovery in Each Phase

- **Lexical:** Remove or replace invalid character.
- **Syntax:** Insert/delete tokens, synchronize at statement boundaries.
- **Semantic:** Use default types, ignore erroneous statements.

---

## Reporting Multiple Errors

- Compilers aim to report as many errors as possible in a single pass.
- Avoid stopping at first error (fail-fast).

---

## Interview Patterns

- Implement error recovery for a parser.
- Recognize and correct common syntax errors.
- Suggest improvements for compiler error messages.

---

## Exercises

1. Write error productions for common syntax errors in C.
2. Simulate panic mode recovery for a code snippet with errors.
3. Propose an error message for an undeclared variable.
4. Explain how a compiler avoids cascading errors.
5. Suggest ways to improve compiler diagnostics.

---

## Key Interview Questions

- What are the main types of errors in compilation?
- How does panic mode recovery work?
- What are error productions?
- How can error messages be improved for users?

---

## References

- [Aho et al., Compilers, Ch. 2.3, 4.4](https://www.pearson.com/en-us/subject-catalog/p/compilers-principles-techniques-and-tools-global-edition/P200000001288/9781292100555)
- [GeeksforGeeks - Error Handling](https://www.geeksforgeeks.org/error-handling-in-compiler-design/)
- [Wikipedia: Compiler Error Handling](https://en.wikipedia.org/wiki/Compiler#Error_handling)
- [NPTEL - Compiler Design Lectures](https://nptel.ac.in/courses/106/105/106105190/)

---
