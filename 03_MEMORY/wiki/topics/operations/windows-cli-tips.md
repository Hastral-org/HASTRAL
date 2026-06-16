# Windows CLI Tips

**Summary**: Useful commands and flags for the Windows command line (CMD and PowerShell) to improve productivity and automation.

**Sources**: (source: Get-GitHubTree.md)

**Last updated**: 2026-06-15

---

## File Structure Generation

### Generating ASCII Trees

To generate a compatible file structure for GitHub issues on Windows 10, use the `tree` command.

**Recommended Command**:
`tree /F /A | clip`

**Flag Breakdown**:

- `/F`: Displays the names of the files in each folder.
- `/A`: Uses text characters instead of graphic characters to ensure compatibility across all platforms (ASCII).
- `| clip`: Pipes the output directly to the Windows clipboard.

**Unicode Alternative**:
Omitting the `/A` flag will produce a visually "prettier" tree using Unicode characters, which is supported by most modern browsers.

## Related pages

- [[topics/codecraft/github-markdown-formatting]]
- [[topics/operations/index]]
