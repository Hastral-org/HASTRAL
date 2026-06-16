# GitHub Markdown Formatting for File Structures

**Summary**: Best practices for displaying project file structures in GitHub issues and documentation using monospace fonts and ASCII trees.

**Sources**: (source: Get-GitHubTree.md)

**Last updated**: 2026-06-15

---

To ensure that file structures are rendered correctly in GitHub issues, the use of monospace fonts is mandatory.

## Formatting Techniques

### Fenced Code Blocks

The primary method for forcing monospace display is wrapping the structure in triple backticks.

\`\`\`text
project/
├── src/
│   └── index.js
└── package.json
\`\`\`

### Best Practices

- **Language Modifiers**: Use `text` or `plaintext` after the first set of backticks to prevent automatic syntax highlighting from interfering with the visual structure.
- **Visual Clarity**: Use standard ASCII/Unicode symbols (`├──`, `└──`, `│`) to maintain a clean and readable tree.
- **Managing Length**: For extensive file structures, wrap the code block in HTML `<details>` tags to prevent the issue from becoming overly long.

Example:

```markdown
<details>
<summary>Click to view full project structure</summary>

```text
...
</details>
```

## Related pages

- [[topics/codecraft/index]]
- [[topics/operations/windows-cli-tips]]
