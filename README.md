# markdown-editor

A modern, browser-based Markdown editor built specifically for creating, editing, and previewing professional Markdown structures. Features a split-pane interface with a code editor, live rendering preview, document outline tracker, and full project management — all running locally in your browser.

**Live Demo:** [markdown.charlz.dev](https://markdown.charlz.dev)

---

## Key Features

- **Split-Pane Workspace:** Monaco editor (powering VS Code) on the left, with real-time responsive split-pane rendering on the right.
- **Dynamic Preview Outline:** Clicking headers in the automatically generated table of contents scrolls the editor directly to that section.
- **Rich Format Toolbar:** One-click shortcuts for inserting headings, styling (bold, italics, strikethrough), tables, lists, quotes, and links.
- **Asset Upload & Embedding:** Drag-and-drop or paste local images and videos directly into the editor for instant cloud uploading or base64 local embedding.
- **Local Sandbox Storage:** Multi-project manager persisting files 100% locally in your browser profile's localStorage.
- **Zen Mode & Command Palette:** Enter fullscreen Zen Mode to write distraction-free, or trigger commands instantly via `Ctrl/Cmd + K`.
- **HTML Sanitization & Highlighting:** Pre-renders clean, DOMPurify-sanitized HTML outputs with highlight.js syntax styling.

---

## Tech Stack

- **Framework:** React 19 + TypeScript + Vite 7
- **Editor:** Monaco Editor (`@monaco-editor/react`)
- **Markdown Parsing:** Marked + marked-highlight
- **Syntax Highlighting:** highlight.js
- **HTML Sanitization:** DOMPurify
- **Styling & Layout:** Tailwind CSS 4 + `@tailwindcss/typography` + `react-resizable-panels`

---

## Getting Started

### Prerequisites

- Node.js >= 18
- pnpm (recommended)

### Setup

```bash
# Clone the repository
git clone https://github.com/charlzx/markdown-editor.git
cd markdown-editor

# Install dependencies
pnpm install

# Start local dev server
pnpm dev

# Build production assets
pnpm build
```

---

Built by [Charlz](https://charlz.dev)
