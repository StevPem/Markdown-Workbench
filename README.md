# Markdown Workbench

Markdown Workbench is a Markdown editor with a live preview that runs entirely in your browser. The whole app is one HTML file, [`markdown-workbench.html`](markdown-workbench.html). It needs no install, build step or server, and your documents never leave your computer.

You write Markdown on the left and see the formatted result on the right as you type. Beyond that, it has the tools you'd want for longer documents:

- an outline of your headings
- find and replace with regular expressions
- one-click table alignment and list renumbering
- clean conversion of text pasted from web pages
- export to Markdown, HTML or formatted text

## Getting started

1. Download [`markdown-workbench.html`](markdown-workbench.html) (on GitHub, open the file and click **Download raw file**).
2. Double-click the file to open it in your browser. Chrome, Edge, Firefox and Safari all work.
3. The first time, it opens a sample document that shows off the supported features. To start your own:
   - Click **New** for a blank document.
   - Click **Open** or press `Ctrl+O` to open a `.md`, `.markdown` or `.txt` file.
   - Drag a file onto the window.
   - Open an `.html` file to convert it to Markdown.

The app works offline. Fonts load from Google Fonts when you're online and fall back to system fonts otherwise. Your current document is kept in the browser and comes back the next time you open the file.

> On a Mac, use `Cmd` wherever this guide says `Ctrl`.

## Views

Use the **Edit / Split / Preview** buttons, or press `Ctrl+Shift+P` to cycle through them.

- **Edit:** the source editor only.
- **Split:** source and preview side by side. The two sides scroll together, so the preview always shows the part you are editing. On narrow screens they stack vertically.
- **Preview:** the formatted document only, for reading.

The **Outline** panel (`Ctrl+\`) lists your headings. Click one to jump to that section. The section you're currently reading is highlighted.

## Writing

### The editor

- Syntax is colored as you type, so headings, emphasis, links, code, list markers and quotes are easy to tell apart.
- The current line is highlighted, and the status bar shows the line and column, word and character counts, reading time, and how many words are selected.

### Formatting buttons and shortcuts

| Action | Button | Shortcut |
|---|---|---|
| Bold / italic / strikethrough | **B** / *I* / ~~S~~ | `Ctrl+B` / `Ctrl+I` / `Ctrl+Shift+X` |
| Inline code | `<>` | `Ctrl+E` |
| Heading 1–6 / normal text | **H** | `Ctrl+Alt+1`…`6` / `Ctrl+Alt+0` |
| Link / image | link / image icons | `Ctrl+K` |
| Bulleted / numbered / task list | list icons | `Ctrl+Shift+8` / `Ctrl+Shift+7` / `Ctrl+Shift+9` |
| Quote | quote icon | `Ctrl+Shift+.` |
| Table | table icon | (choose rows and columns) |
| Code block | code-block icon | `Ctrl+Shift+K` |
| Divider | line icon | |

Pressing a formatting shortcut again on the same text removes the formatting.

### Smart editing

- **Lists continue automatically.** Pressing `Enter` in a list starts the next item, numbering it or adding an empty checkbox as needed. Pressing `Enter` on an empty item ends the list. Quotes continue the same way.
- **Nesting:** `Tab` and `Shift+Tab` indent and outdent list items (or any selected lines). Nested items line up under the parent's text.
- **Wrapping a selection:** with text selected, typing `*`, `_`, `` ` ``, `~`, `=`, `"`, `[` or `(` wraps the selection instead of replacing it.
- **Moving and duplicating:** `Alt+↑` / `Alt+↓` move lines up and down, and `Ctrl+Shift+D` duplicates them.
- **Linking:** paste a URL while text is selected to turn the text into a link.
- **Pasting from the web:** formatted text copied from web pages or Google Docs is converted to clean Markdown, keeping headings, bold, italics, links, lists, tables and code. `Ctrl+Shift+V` pastes plain text instead. You can turn conversion off in **Tools → Settings**.
- **Undo and redo:** `Ctrl+Z` / `Ctrl+Y` cover every edit, including toolbar actions and tools.

### Find and replace

Press `Ctrl+F` or click the search icon. All matches are highlighted in the editor, with a count.

- `Enter` and `Shift+Enter` move between matches.
- **Aa** matches case, **W** matches whole words, and **.\*** uses regular expressions. With regular expressions, the replacement can use `$1`, `$2` and so on.
- **Replace** changes the current match and **All** replaces every match in one step, which a single undo reverses.

## The preview

- **Jump to the source:** double-click any paragraph, heading, list item or table row in the preview to jump to that line in the editor.
- **Tick tasks:** checkboxes in the preview can be ticked, and doing so updates `- [ ]` / `- [x]` in your source.
- **Copy code:** code blocks have a **Copy** button that appears on hover.
- **Links:** heading `#` links and footnote links jump within the document. External links open in a new tab.
- **Copy formatted:** copies the rendered document as rich text for pasting into email, Google Docs or Word.
- **Export HTML:** downloads the document as a standalone, styled web page that supports light and dark mode.

### Supported Markdown

The app supports CommonMark plus the GitHub extensions people use most:

- Headings (`#` style and underlined style), paragraphs, line breaks, emphasis, strong, ~~strikethrough~~ and `==highlight==`
- Bulleted, numbered and nested lists, plus task lists `- [ ]` / `- [x]`
- Block quotes and GitHub alerts: `> [!NOTE]`, `[!TIP]`, `[!IMPORTANT]`, `[!WARNING]`, `[!CAUTION]`
- Tables with left, center and right column alignment
- Fenced and indented code blocks, with syntax highlighting for JavaScript/TypeScript, Python, shell, Go, Rust, C/C++/C#/Java/Kotlin/Swift/PHP, Ruby, SQL, JSON, YAML, HTML/XML, CSS and diff
- Inline links, reference links, images, autolinks and bare URLs
- Footnotes `[^1]`
- YAML front matter, shown as a small table at the top of the preview
- Emoji shortcodes such as `:tada:` and `:rocket:`
- Raw HTML such as `<details>`, `<kbd>` and `<sup>`. Scripts, event handlers and unsafe links are removed before anything is shown.

## Tools menu

| Tool | What it does |
|---|---|
| Align table columns | Pads every table so its columns line up in the source, keeping column alignment |
| Renumber ordered lists | Fixes numbering in every numbered list (`1. 2. 3.`) |
| Tidy whitespace | Removes trailing spaces (keeping two-space line breaks), collapses extra blank lines and ends the file with a newline |
| Promote / Demote headings | Moves every heading (or those in the selection) up or down one level |
| Insert table of contents | Inserts a linked, nested list of your headings at the cursor |
| Save Markdown / Export HTML page | Saves the document as `.md` or as a styled `.html` page |
| Copy HTML source / Copy formatted text | Copies the rendered HTML code, or rich text for pasting elsewhere |
| Download this app | Saves a fresh copy of the app itself |
| Settings | Toggles for synced scrolling, rendering raw HTML, treating single line breaks as `<br>`, converting pasted web pages, and spell check, plus larger and smaller text (`Ctrl+=` / `Ctrl+-`) |

## Saving

- `Ctrl+S` saves the document as Markdown. In Chrome and Edge it writes straight back to the file you opened; in other browsers it downloads a copy.
- Click the file name in the toolbar to rename the file.
- The status bar shows **Saved** or **Unsaved changes**, and a dot appears next to the file name while there are unsaved changes.
- Your document is also kept in the browser's local storage as a backup. Private windows and cleared site data lose it, so save important work to a file.

## Keyboard shortcuts

Press `Ctrl+/` in the app to see these.

| Shortcut | Action |
|---|---|
| `Ctrl+O` / `Ctrl+S` | Open / save |
| `Ctrl+Z` / `Ctrl+Y` | Undo / redo |
| `Ctrl+F` | Find and replace |
| `Ctrl+Shift+P` | Cycle Edit, Split and Preview |
| `Ctrl+\` | Toggle outline |
| `Ctrl+=` / `Ctrl+-` | Larger / smaller text |
| `Ctrl+B` / `Ctrl+I` / `Ctrl+E` / `Ctrl+K` | Bold / italic / code / link |
| `Ctrl+Shift+X` | Strikethrough |
| `Ctrl+Alt+1`…`6`, `Ctrl+Alt+0` | Heading level, normal text |
| `Ctrl+Shift+7` / `8` / `9` | Numbered / bulleted / task list |
| `Ctrl+Shift+.` | Quote |
| `Ctrl+Shift+K` | Code block |
| `Tab` / `Shift+Tab` | Indent / outdent |
| `Alt+↑` / `Alt+↓` | Move lines |
| `Ctrl+Shift+D` | Duplicate lines |

## Limitations

- Opening from and saving back to the same file needs a Chromium-based browser (Chrome, Edge, Opera). Other browsers download a copy instead.
- Documents over about 150 KB switch off source highlighting to stay responsive, and the preview takes longer to update.
- Math (LaTeX) and Mermaid diagrams are shown as code blocks rather than rendered.
