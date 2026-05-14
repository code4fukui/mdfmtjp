# mdfmtjp

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

An opinionated Markdown formatter for Japanese documents.

## Features

`mdfmtjp` automatically formats all `.md` files in the current directory.

- **Character Normalization:** Standardizes punctuation and spacing common in Japanese text.
  - `．` → `.`
  - `,` → `、`
  - `｡` → `。`
  - `　` → ` ` (full-width space to half-width)
  - `＃` → `#`
  - `･` → `・`
- **Numbered List Normalization:** Ensures a period and a single space follow the number in ordered lists (e.g., `1.item` is corrected to `1. item`).

## Requirements

- [Deno](https://deno.land/) runtime

## Installation

```bash
deno install --allow-read --allow-write https://code4fukui.github.io/mdfmtjp/mdfmtjp.js
```

## Usage

Navigate to the directory containing your Markdown files and run:

```bash
mdfmtjp
```

The script will find all `.md` files in the current directory, apply formatting, and overwrite the files in place. It will print the names of any modified files to the console.

### Example

**Before:**
```markdown
＃＃＃＃ 1.あいう
2.いい
```

**After:**
```markdown
#### 1. あいう
2. いい
```

## Uninstall

```bash
rm $(which mdfmtjp)
```

## License

MIT