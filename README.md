# Docx Desk

A Word (.docx) editor that runs in your browser. Open a .docx, edit it, sign it, and save it back as .docx. Nothing gets uploaded: the whole thing runs on your own machine.

## Features

- Open a .docx with the Open button or by dragging it onto the page
- Paragraph styles (Normal, Heading 1–3, Quote), bold, italic, underline, strikethrough
- Bulleted and numbered lists with indenting, text alignment, links, images and tables
- Find and replace (Ctrl+F)
- **Sign:** draw your signature or type it in a handwriting font, with an optional printed name and date. You can save it in your browser and reuse it.
- Save as .docx (Ctrl+S). Your current draft is kept in the browser between visits.

## Run it

Open `index.html` in any modern browser. There's no build step. To host it, turn on GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch).

## Limits

Docx Desk edits a document's text and structure, but not its full Word layout. Custom fonts, text colors, headers and footers, comments, tracked changes and page settings are lost when you open and save a file.

A drawn or typed signature is fine for everyday agreements. It has no audit trail or tamper seal, though, so if a contract needs a verified e-signature, use a signing service.

## Built with

- [mammoth.js](https://github.com/mwilliamson/mammoth.js) for reading .docx files
- [docx](https://github.com/dolanmiu/docx) for writing .docx files
