# Aurora CV Builder

A CV builder that runs in your browser as a single HTML file. Write your CV, pick a design, check how well it reads in applicant tracking systems (ATS), and save it as a PDF with real, selectable text.

![Alternative Text](https://raw.githubusercontent.com/DLazzzar/Aurora-CV-Builder/refs/heads/main/Preview%20Image.png)

There is no account, no server and no upload. Your CV stays in your own browser.

**Live page:** https://dlazzzar.github.io/Aurora-CV-Builder/

---

## Features

- **8 templates.** Aurora, Aurora Sidebar, Aurora Spotlight, Glass, Classic, Garamond Banner, Details and Simple ATS. The Templates tab previews each one with your content.
- **Rich text editing.** Bold, italic, underline, strikethrough, alignment, bullet and numbered lists, links, text colour and highlight.
- **Flexible sections.** 18 section types, including experience, education, skills, languages, projects, certifications, courses, volunteering, awards, publications, hobbies and references. Sections can be reordered by drag and drop, hidden or renamed, and given one of 115 icons.
- **Contacts and links.** Email, phone, location, LinkedIn, GitHub and website become clickable links automatically. Custom details such as nationality or a driving licence can be added too.
- **Design controls.** 21 fonts (including Inter, Calibri, Garamond, Arial, Times New Roman, Roboto and Source Sans) with weights from 100 to 900. You also set sizes, colours and a background gradient with any number of colour glows. Each template keeps its own settings.
- **Layout controls.** Photo size, shape and position, spacing, margins, column widths, icons, and which sections sit in a side column.
- **ATS check.** A live score from 15 checks, keyword matching against a pasted job ad, and the plain text a parser would read.
- **Import.** Reads an existing PDF or Word (.docx) CV and fills in the fields, including links, bold text and the photo where possible.
- **ATS-ready PDF export.** Uses Chrome's "Save as PDF" with embedded TrueType fonts, so the text stays real and selectable.
- **Save and open.** Your CV downloads as a small `.json` file you can open again on any computer.
- **Light and dark editor**, a guided tour on first visit, and a layout that works on phones.

---

## Getting started

### Online
Open the live page in **Chrome** or **Edge**.

### Offline
1. Download `index.html` from this repository.
2. Open it in Chrome or Edge.

An internet connection is needed the first time fonts load. The PDF import tools also load from the internet when you first use Import.

---

## How to use it

| Step | Where | What to do |
|---|---|---|
| 1 | **Templates** tab | Pick a design. Previews show example content until you add your own. |
| 2 | **Content** tab | Fill in your profile, contacts and sections. Click the arrow on a section to edit it. |
| 3 | **Design** / **Layout** tabs | Choose fonts, colours, gradient, spacing and photo settings. |
| 4 | **ATS check** tab | Review your score and paste a job ad to compare keywords. |
| 5 | **Save** | Download your CV as a `.json` file to keep a copy. |
| 6 | **Export PDF** | Follow the print settings below. |

Click **?** in the top bar to reopen the guided tour at any time.

---

## Exporting an ATS-ready PDF

Click **Export PDF**. A checklist appears, then Chrome's print window opens. Use these settings:

| Setting | Value |
|---|---|
| Destination | **Save as PDF** (not "Microsoft Print to PDF") |
| Pages | All |
| Pages per sheet | 1 |
| Margins | None (use **Default** if your CV runs to 2 pages) |
| Paper size | A4 (under *More settings*) |
| Scale | Default (100) |
| Background graphics | On or off; colours print either way |

The resulting PDF has real text with embedded fonts, a correct reading order and clickable links.

---

## Your data and privacy

- Everything you type is saved in **your browser's local storage** on your own device. Nothing is sent anywhere.
- Clearing browser data deletes the copy saved there, so use **Save** to keep a `.json` backup.
- **New CV** clears the current CV. It offers to save a copy first.
- Each browser keeps its own CV. Anyone you share this page with sees an empty builder, never your CV.

> Never commit your own `.json` CV file or exported PDFs to this repository. They contain your personal details and photo.

---

## Browser support

| Browser | Status |
|---|---|
| Chrome / Edge (Windows, macOS, Linux) | Recommended |
| Firefox / Safari | Editing works; PDF export may differ |

The **San Francisco** font only shows on Apple devices; other systems use Inter instead. For the safest PDF, use Inter or another listed font.

---

## Project structure

```
index.html   The whole app: markup, styles and script in one file
LICENSE      MIT licence
README.md    This file
```

External resources loaded at runtime:
- Static fonts from [Fontsource](https://fontsource.org) via jsDelivr
- [pdf.js](https://mozilla.github.io/pdf.js/) and [mammoth.js](https://github.com/mwilliamson/mammoth.js) for importing PDF and Word CVs (loaded only when you use Import)
- Icons from [Lucide](https://lucide.dev), built into the file

---

## Disclaimer

This project is provided **as is, without warranty of any kind**. The ATS score and keyword match are estimates based on general parsing rules. They do not guarantee how any specific applicant tracking system will read your CV, or the outcome of any application. Always review your exported PDF before sending it.

---

## Licence

Released under the [MIT License](LICENSE).

---

## Third-party notices

This project uses the following open-source work. Their licences apply to those parts.

**Lucide icons** (built into `index.html`), ISC License

```
ISC License

Copyright (c) for portions of Lucide are held by Cole Bemis 2013-2022 as part of Feather (MIT). All other copyright (c) for Lucide are held by Lucide Contributors 2022.

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```

**Fonts** (loaded at runtime from [Fontsource](https://fontsource.org) via jsDelivr, not stored in this repository)
- SIL Open Font License 1.1: Inter, Carlito, Source Sans 3, Lato, Open Sans, IBM Plex Sans, DM Sans, Manrope, Figtree, Nunito Sans, EB Garamond, Noto Serif, Source Serif 4, Merriweather, Libre Baskerville, Crimson Pro, PT Serif
- Apache License 2.0: Arimo, Tinos, Roboto

Font names belong to their respective owners. Calibri, Arial, Times New Roman and San Francisco are trademarks of their owners; this project only refers to them by name and uses open, metric-compatible alternatives or the fonts already installed on the user's system.

**Libraries loaded only when importing a CV**
- [pdf.js](https://github.com/mozilla/pdf.js) by Mozilla, Apache License 2.0
- [mammoth.js](https://github.com/mwilliamson/mammoth.js) by Michael Williamson, BSD 2-Clause License
