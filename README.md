# PDF Editor

Edit the text in a PDF right in your browser, then download the edited copy.

**Live:** https://pvsp2003.github.io/pdf-editor/

Nothing is uploaded. The PDF is opened, edited and saved entirely on your own device.

## Features

- **Edit existing text.** Click any text on the page and type.
- **Keeps the original font.** Edited text is drawn with the font embedded in the PDF, so it matches the rest of the document.
- **Keeps the original colour.** Each piece of text's colour and background are detected and preserved.
- **Add text.** Place new text anywhere on a page.
- **Duplicate.** Copy existing text with its exact font, size and colour (Ctrl+D).
- **Move and align.** Drag text to a new position. It snaps to the edges and baselines of nearby text, with guide lines.
- **Style controls.** Change size, bold and colour, or delete text.
- **Undo / redo.** Ctrl+Z and Ctrl+Y (or Ctrl+Shift+Z).
- **Protected PDFs.** Many PDFs (payslips, bank statements) are encrypted but open without a password. They are unlocked automatically so the edited file opens everywhere.

## How to use

1. Open the site and choose a PDF, or drag one onto the window.
2. Pick a mode in the toolbar:
   - **Edit**: click text to change it.
   - **Add text**: click on a page to add new text.
   - **Move**: drag text into place. Hold Shift to move in one direction only, hold Alt to turn off snapping. Arrow keys nudge by 1px (Shift for 10px).
3. Click **Download PDF** to save `yourfile-edited.pdf`.

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| Ctrl+Z | Undo |
| Ctrl+Y / Ctrl+Shift+Z | Redo |
| Ctrl+D | Duplicate selected text |
| Esc | Stop editing the current text |
| Arrow keys (Move mode) | Nudge selected text |

## Limitations

- **Text only.** Images, lines and shapes are part of the page and can't be moved or edited.
- **Missing characters.** PDFs usually embed only the characters they use. If you type a character the embedded font doesn't have, that character is drawn in a similar standard font.
- **How edits are applied.** Edited text is covered with a patch in the background colour and redrawn on top. On gradient or image backgrounds the patch may be visible.
- **Unsupported files.** Scanned PDFs have no editable text, though you can still add text. Rotated text can't be edited. PDFs that need a password to open, or that use AES-256 protection, can be viewed but not saved.

## Running locally

It's a single `index.html` file. Download it and open it in Chrome, Edge or Firefox. An internet connection is needed the first time to load the libraries and fonts from their CDNs.

## Built with

- [PDF.js](https://mozilla.github.io/pdf.js/) for rendering pages and reading text
- [pdf-lib](https://pdf-lib.js.org/) for writing the edited PDF
- No build step, no server, no framework
