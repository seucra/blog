---
layout: page
title: Blog Formatting Guide
permalink: /help/
---

Welcome to your blog reference and formatting guide! This page serves as a quick-reference cheat sheet for writing posts and page content using Markdown and the specific styling syntax supported by your Jekyll (Chirpy) theme.

---

## 1. Post Front Matter (Jekyll Metadata)
Every blog post file (placed in `_posts/` folder with the name format `YYYY-MM-DD-title-slug.md`) needs a header block called **Front Matter**:

```yaml
---
title: "My Awesome Blog Post"
date: 2026-07-21 17:00:00 +0530
categories: [Cybersecurity, DevOps]
tags: [cloudflare, serverless, guide]
# pin: true # (Optional) Set to true to pin this post to the top of the home page
# image: /assets/img/my-hero.png # (Optional) Add a cover image for the post card
---
```

---

## 2. Text Formatting Styles

| Style | Syntax | Output |
| :--- | :--- | :--- |
| **Bold** | `**Bold Text**` | **Bold Text** |
| *Italic* | `*Italic Text*` | *Italic Text* |
| ~~Strikethrough~~ | `~~Strikethrough Text~~` | ~~Strikethrough Text~~ |
| `Inline Code` | `` `Inline Code` `` | `Inline Code` |
| Link | `[Anchor Text](URL)` | [Anchor Text](https://seucra.tech) |

---

## 3. Custom Alerts / Callout Prompts
Your theme supports specialized styling classes for notes, tips, warnings, and error messages. Apply these directly under your blockquotes:

### Tip
> This is a tip prompt. Use it for suggestions and best practices.
{: .prompt-tip }

### Info
> This is an informational prompt. Use it to highlight key facts.
{: .prompt-info }

### Warning
> This is a warning prompt. Use it to prevent common mistakes.
{: .prompt-warning }

### Danger / Error
> This is a danger prompt. Use it to warn about high-risk actions.
{: .prompt-danger }

---

## 4. Code Blocks and File Paths

### Highlighting Code
Specify the language next to the triple backticks for syntax highlighting:

```rust
fn main() {
    let matrix = Matrix::new(3, 3);
    println!("Matrix created: {:?}", matrix);
}
```

### Specifying File Paths
You can add a `.filepath` class inline under a blockquote to style a folder path:

> Create the configuration file inside `hosted/seucra-api/wrangler.jsonc`{: .filepath } to configure settings.

---

## 5. Media & Layouts

### Embed Image
```markdown
![Alternative Text](/path/to/image.png)
```

### Keyboard Keys (KBD)
You can represent keystrokes using HTML `<kbd>` tags:
Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to exit the server.

### Checklists
- [x] Create the GitHub Page deployment workflows
- [x] Configure DNS CNAME mapping
- [ ] Implement Yjs peer-to-peer collaboration in Super Sudoku

---

## 6. Table Layouts
Create clean grids by dividing headers with hyphens (`-`) and columns with pipes (`|`):

| Subdomain | App Name | Status Monitor |
| :--- | :--- | :--- |
| `chef.seucra.tech` | CyberChef | Live 🟢 |
| `2048.seucra.tech` | 2048 Game | Live 🟢 |
| `sudoku.seucra.tech` | Super Sudoku | Live 🟢 |

---

## What is Quartz?
**Quartz** is an open-source static site generator specifically optimized for rendering Obsidian vaults or standard Markdown notes as a fast, clean website. 

### Why is it useful?
1. **Digital Garden**: Unlike a chronological blog, Quartz creates an interlinked wiki-like digital garden or second brain.
2. **Interactive Local Graph**: Renders interactive graphs showing connections between notes.
3. **Internal Backlinks**: Displays backlinks pointing to the current note, similar to Obsidian.
4. **Fast Global Search**: Includes instant full-text search across all notes.
5. **Obsidian Integration**: Directly supports obsidian double-bracket links `[[Note Name]]`, callouts, and canvas structures.
