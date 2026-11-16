# PDF Editor

Edit the text in a PDF right in your browser, then download the edited copy.

Made by [PVS Prasanth](https://github.com/pvsp2003).

**Live:** https://pvsp2003.github.io/pdf-editor/

Nothing is uploaded. The PDF is opened, edited and saved entirely on your own device.

## Features

- **Edit existing text.** Click any text on the page and type.
- **Keeps the original font.** Edited text is drawn with the font embedded in the PDF, so it matches the rest of the document.
- **Keeps the original colour.** Each piece of text's colour and background are detected and preserved.
- **Add text.** Place new text anywhere on a page.
- **Duplicate.** Copy existing text with its exact font, size and colour (Ctrl+D).
- **Move and align.** Drag text to a new position. It snaps to the edges and baselines of nearby text, with guide lines.
- **Whole lines.** In Move mode, double-click a piece to select its whole line, or Shift+click to pick several. Then move them together, align their left or right edges, put them on the same line, or join them into one editable piece.
- **Find & replace.** Ctrl+F to find text across the document and replace one match or all of them.
- **Zoom.** The − / + buttons, Ctrl+scroll or Ctrl + / −. Pages re-render sharply at every zoom level.
- **Page tools.** Hover over a page to move it up or down, rotate it or delete it.
- **Images and signatures.** Insert a PNG or JPG (or drag one onto the page), or draw a signature. Drag it into place and resize it from the corner.
- **Annotate.** Highlight, underline or strike through text (click a piece of text, or drag across it and the mark fits the text), and draw boxes, lines, arrows, ticks and crosses. Pick the colour and thickness, and change them later on any mark. Highlights use a highlighter-style blend so the text stays readable.
- **Redact.** Black out anything by dragging over it. Redacted pages are turned into images on download, so the hidden text is really removed, not just covered.
- **Style controls.** Change size, bold and colour, or delete text.
- **Undo / redo.** Ctrl+Z and Ctrl+Y (or Ctrl+Shift+Z).
- **Protected PDFs.** Many PDFs (payslips, bank statements) are encrypted but open without a password. They are unlocked automatically so the edited file opens everywhere.

## How to use

1. Open the site and choose a PDF, or drag one onto the window.
2. Pick a mode in the toolbar:
   - **Edit**: click text to change it.
   - **Add text**: click on a page to add new text.
   - **Move**: drag text into place. Hold Shift to move in one direction only, hold Alt to turn off snapping. Arrow keys nudge by 1px (Shift for 10px). Double-click selects a whole line; Shift+click selects several pieces.
   - **Annotate**: pick a tool in the bar at the bottom. Click or drag across text to highlight, underline or strike it through; drag to draw a box, line or arrow (Shift keeps lines straight); click to place a tick or cross.
   - **Redact**: drag over anything to black it out.
   - **Image** / **Signature**: insert a picture or draw a signature, then drag it into place.
3. Click **Download PDF** to save `yourfile-edited.pdf`.

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| Ctrl+Z | Undo |
| Ctrl+Y / Ctrl+Shift+Z | Redo |
| Ctrl+D | Duplicate selected text, image or mark |
| Ctrl+F | Find & replace |
| Ctrl + / Ctrl − / Ctrl 0 | Zoom in / out / reset |
| Delete | Remove the selected image, mark, redaction or (in Move mode) text |
| Esc | Stop editing the current text |
| Arrow keys | Nudge selected text (Move mode) or image |

## Limitations

- **Existing graphics stay put.** Images, lines and shapes already in the PDF can't be moved or edited (you can cover them with a redaction or place new images on top).
- **Missing characters.** PDFs usually embed only the characters they use. If you type a character the embedded font doesn't have, that character is drawn in a similar standard font.
- **How edits are applied.** Edited text is covered with a patch in the background colour and redrawn on top. On gradient or image backgrounds the patch may be visible.
- **Find works piece by piece.** A phrase split across separate pieces of text isn't found. Join the pieces first.
- **Redacted pages become images.** Their text can no longer be selected or searched.
- **Rotated pages are view-only** in the editor until you rotate them back.
- **Unsupported files.** Scanned PDFs have no editable text, though you can still add text. Rotated text can't be edited. PDFs that need a password to open, or that use AES-256 protection, can be viewed but not saved.

## Running locally

It's a single `index.html` file. Download it and open it in Chrome, Edge or Firefox. An internet connection is needed the first time to load the libraries and fonts from their CDNs.

## Built with

- [PDF.js](https://mozilla.github.io/pdf.js/) for rendering pages and reading text
- [pdf-lib](https://pdf-lib.js.org/) for writing the edited PDF
- No build step, no server, no framework
