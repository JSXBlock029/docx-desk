# Docx Desk

[![Live demo](https://img.shields.io/badge/live_demo-open-22d3ee)](https://lowriskbtc.github.io/docx-desk/) ![No build step](https://img.shields.io/badge/build-none_needed-0f172a) [![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)

A Word (.docx) and PDF editor that runs in your browser. Open a .docx, edit it, sign it, and save it back **with its original formatting untouched**. Open a PDF to sign it, fill in its form fields, and type on it. Nothing gets uploaded: the whole thing runs on your own machine.

## Features

- Open a .docx with the Open button or by dragging it onto the page
- **Edits your file in place.** Only the text you change is touched. Fonts, colors, spacing, lists, tables, images, headers, footers, margins and every paragraph you didn't edit stay exactly as they were. Saving without edits returns your original file unchanged.
- New text takes the formatting of the text next to it
- Add images, and paste as plain text
- A blank page (New) has a full formatting toolbar: styles, bold, italic, underline, lists, alignment, links and tables
- Find and replace (Ctrl+F)
- **Sign:** draw your signature (pen and eraser, each with adjustable size) or type it in a handwriting font, with an optional printed name and date. You can save it in your browser and reuse it.
- Save as .docx (Ctrl+S). Your current draft is kept in the browser between visits.

## PDFs

Open a PDF with the Open button or by dragging it onto the page.

- **Sign:** draw or type a signature, then click the page where it should go. Drag to move it and pull the corner to resize.
- **Erase:** paint white over anything on the page, with an adjustable brush size and undo. It covers the page visually; the original content is still in the file underneath, so it isn't a secure redaction.
- **Text and Date:** click a line on the page and type. The text sits just above the spot you click. Choose the text size in the toolbar.
- **Checkmark and X:** click a box to mark it.
- **Form fields:** fillable fields (text, multi-line, checkboxes, radio buttons, dropdowns) are highlighted in yellow. Fill them in directly.
- **Save .pdf:** what you added is drawn onto the original pages. The pages themselves are never rewritten, and saving with nothing added returns your original file unchanged.

PDF text can't be edited in place, and password-protected PDFs need the password removed first. Digital-signature fields aren't supported.

## Run it

Open `index.html` in any modern browser. There's no build step. To host it, turn on GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch).

## Limits

On an opened Word file the formatting buttons (bold, italic, styles, lists and so on) are switched off, because changing a file's formatting is exactly what this mode avoids. Edit text, add images and sign. Merged table cells, text boxes and similar layout objects show in simplified form on the page, but they are saved back untouched.

A drawn or typed signature is fine for everyday agreements. It has no audit trail or tamper seal, though, so if a contract needs a verified e-signature, use a signing service.

## Built with

- [JSZip](https://github.com/Stuk/jszip) for reading and writing the .docx package
- [PDF.js](https://github.com/mozilla/pdf.js) for showing PDF pages
- [pdf-lib](https://github.com/Hopding/pdf-lib) for writing your changes into a PDF
- [docx](https://github.com/dolanmiu/docx) for building new documents from the blank page
