# readme-editor

A modern, browser-based Markdown editor built specifically for creating and editing professional README files. Features a split-pane interface with a code editor, live preview, document outline, and full project management — all running locally in your browser.

**Live Demo:** [readme.charlz.dev](https://readme.charlz.dev)

---

## Features

- **Split-pane editor & preview** — Resizable panels with Monaco editor (the same engine powering VS Code) on the left and a live-rendered Markdown preview on the right.
- **Multi-project management** — Create, rename, and delete multiple README projects. All data persists in your browser's local storage — nothing is ever sent to a server.
- **Rich Markdown toolbar** — Insert headings (H1–H6), bold, italic, strikethrough, links, unordered/ordered lists, blockquotes, code blocks, images, and tables with a single click.
- **Command palette (Ctrl/Cmd + K)** — Quick access to all commands: new README, open file, toggle theme, toggle outline, and more.
- **Document outline** — Automatically generates a clickable table of contents from your Markdown headings for quick navigation.
- **Dark & light themes** — Switch between light and dark mode; preference is saved locally.
- **Import & export** — Open existing `.md` files from your computer or download your work as a `.md` file.
- **Image embedding** — Paste or upload images directly into the editor as base64 data URIs (no external hosting required).
- **Zen mode** — Distraction-free fullscreen preview.
- **Undo / Redo** — Full undo/redo support within the editor.
- **Code syntax highlighting** — Fenced code blocks are highlighted using highlight.js (GitHub Dark theme).
- **Security** — Rendered HTML is sanitized with DOMPurify to prevent XSS attacks.
- **Desktop-first design** — Optimized for tablet landscape, laptop, and desktop screens due to the split-pane layout.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 19 with TypeScript |
| Build tool | Vite 7 |
| Editor | Monaco Editor (`@monaco-editor/react`) |
| Markdown parsing | Marked + marked-highlight |
| Syntax highlighting | highlight.js |
| Styling | Tailwind CSS 4 + `@tailwindcss/typography` |
| Animations | Framer Motion |
| Icons | Phosphor Icons |
| HTML sanitization | DOMPurify |
| Panels | react-resizable-panels |

---

## Getting Started

### Prerequisites

- Node.js >= 18
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/charlzx/readme-editor.git
cd readme-editor

# Install dependencies
npm install
```

### Development

```bash
npm run dev
```

Opens the app in development mode with hot module replacement (HMR). Visit `http://localhost:5173` in your browser.

### Build

```bash
npm run build
```

Compiles TypeScript and builds the production bundle to the `dist/` directory.

### Preview production build

```bash
npm run preview
```

### Lint

```bash
npm run lint
```

Runs ESLint on the codebase.

---

## Project Structure

```
readme-editor/
├── src/
│   ├── App.tsx          # Main application component
│   ├── main.tsx         # Entry point with screen guard
│   └── index.css        # Tailwind CSS + custom theme variables
├── index.html           # HTML shell
├── package.json         # Dependencies and scripts
├── vite.config.ts       # Vite configuration
├── tsconfig.json        # TypeScript configuration
└── eslint.config.js     # ESLint configuration
```

---

## Usage Guide

### Creating a README

Click **New README** on the home screen or use the command palette (`Ctrl/Cmd + K` → "New README").

### Editing

Use the Monaco editor on the left to write Markdown. The toolbar provides quick-access buttons for common formatting. The preview on the right updates in real time.

### Managing projects

All projects are listed on the home screen, sorted by most recently updated. Use the search bar to filter projects. Click the trash icon to delete a project (with confirmation dialog).

### Importing files

Click **Open file** or use the command palette to open an existing `.md` file from your computer.

### Exporting

Click the download button in the toolbar to save your README as a `.md` file.

### Keyboard shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl/Cmd + K` | Open command palette |
| `Escape` | Close command palette or exit zen mode |

### Outline panel

Toggle the document outline to see a structured overview of all headings in your document. Click any heading to jump to that section in the editor.

---

## Browser Support

The editor requires a modern browser with support for:

- Local Storage
- FileReader API
- ResizeObserver
- CSS Grid & Custom Properties

Works best on Chrome, Firefox, Safari, and Edge on desktop or tablet landscape. Mobile screens are not supported due to the split-pane layout — a friendly "Desktop Required" message is shown on small screens.

---
Built by [Charlz](https://charlz.dev)
