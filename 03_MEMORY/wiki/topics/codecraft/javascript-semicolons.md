# JavaScript Semicolon Usage

**Summary**: Guidance on the use of semicolons in Node.js/JavaScript, explaining Automatic Semicolon Insertion (ASI) and best practices for safety and consistency.

**Sources**: (source: javascript_conventions_and_IDE_config.md)

**Last updated**: 2026-06-14.

---

In Node.js and JavaScript, semicolons are used to separate statements. While the language provides a feature called **Automatic Semicolon Insertion (ASI)**, which allows many lines to omit semicolons, explicit usage is generally recommended for safety.

## Automatic Semicolon Insertion (ASI)

ASI automatically inserts semicolons where the interpreter deems them necessary during execution. Most line breaks are treated as semicolons.

### Mandatory Semicolons

Semicolons are strictly required if the subsequent line begins with any of the following characters:

- `[` (Left bracket)
- `(` (Left parenthesis)
- `` ` `` (Template literal backtick)

### Common ASI Pitfalls

1. **Line Merging**: If a line starts with a parenthesis or bracket, JavaScript may merge it with the previous line, leading to runtime errors or unexpected behavior.
2. **Return Statement Trap**: Placing a return value on a new line after the `return` keyword will result in `undefined` being returned, as ASI inserts a semicolon immediately after `return`.

## Best Practices

- **Explicit Usage**: It is generally safer to always use semicolons to eliminate the risk of ASI-related bugs and ensure clearer intent.
- **Consistency**: Use tooling such as **ESLint** or **Prettier** to enforce a consistent style across the project.
- **Standardization**: Explicit semicolons align JavaScript with other C-style languages (C++, Java, C#).

## Related pages

- [[topics/operations/markdownlint/index]]
- [[topics/codecraft/index]]
