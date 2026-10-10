# Docx Desk

**Live demo: https://lowriskbtc.github.io/docx-desk/**

A Word (.docx) editor that runs in your browser. Open a .docx, edit it, sign it, and save it back as .docx **with its original formatting untouched**. Nothing gets uploaded: the whole thing runs on your own machine.

## Features

- Open a .docx with the Open button or by dragging it onto the page
- **Edits your file in place.** Only the text you change is touched. Fonts, colors, spacing, lists, tables, images, headers, footers, margins and every paragraph you didn't edit stay exactly as they were. Saving without edits returns your original file unchanged.
- New text takes the formatting of the text next to it
- Add images, and paste as plain text
- A blank page (New) has a full formatting toolbar: styles, bold, italic, underline, lists, alignment, links and tables
- Find and replace (Ctrl+F)
- **Sign:** draw your signature or type it in a handwriting font, with an optional printed name and date. You can save it in your browser and reuse it.
- Save as .docx (Ctrl+S). Your current draft is kept in the browser between visits.

## Run it

Open `index.html` in any modern browser. There's no build step. To host it, turn on GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch).

## Limits

On an opened Word file the formatting buttons (bold, italic, styles, lists and so on) are switched off, because changing a file's formatting is exactly what this mode avoids. Edit text, add images and sign. Merged table cells, text boxes and similar layout objects show in simplified form on the page, but they are saved back untouched.

A drawn or typed signature is fine for everyday agreements. It has no audit trail or tamper seal, though, so if a contract needs a verified e-signature, use a signing service.

## Built with

- [JSZip](https://github.com/Stuk/jszip) for reading and writing the .docx package
- [docx](https://github.com/dolanmiu/docx) for building new documents from the blank page
