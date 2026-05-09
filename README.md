# Khadiza Akter — Portfolio

A single-file portfolio website. Drop the entire folder onto Vercel,
Netlify, or GitHub Pages and it will work. Or just double-click
`index.html` to preview locally.

## What's in the box

```
khadiza-portfolio/
├── index.html                       # The whole site (HTML + CSS + JS)
├── README.md                        # This file
└── assets/
    ├── portrait/khadiza.jpg         # B&W portrait used in the About section
    ├── art/01–08 …jpg               # 8 curated artworks
    ├── blog/blog-01 to blog-03.jpg  # AI illustrations for the Scrap Box
    └── cv/Khadiza-Akter-CV.docx     # Downloadable CV
```

## Section structure (8 sections)

1. **About** — bio, stats, portrait
2. **Inquiry** — three lines of intellectual focus
3. **Research** — JARVIS-I, OA-GNN-SC, DR paper, book chapters, JYESTA, IEEE SPCOM peer reviewer
4. **Papers and Chapters** — conference papers + book chapter publication status
5. **Recognition** — certificates carousel
6. **Creative** — artwork carousel with thoughts
7. **Scrap Box of Mind** — three compact blog cards. Click any card to read the full piece in a focused reader modal
8. **Contact**

## Deploying

### Netlify (drag and drop)
Go to https://app.netlify.com/drop and drag the entire folder.

### Vercel
`npx vercel` from inside the folder.

### GitHub Pages
Push to a repo, enable Pages on the main branch.

## Editing

Everything is in `index.html`. Search for the text you want to change.

- **Edit a blog scrap's prose** — search the title (e.g.,
  `The Age of Restlessness`) and find the matching entry inside
  the `const SCRAPS = [...]` array near the bottom of the script.
  The `body` field is an array of paragraphs. Edit the strings.
- **Edit a card teaser line** — the short line shown beneath the
  card image (before opening the modal) lives inside the
  `<p class="scrap-card-teaser">` of each card.
- **Replace a blog illustration** — drop a JPG into `assets/blog/`
  named `blog-01.jpg`, `blog-02.jpg`, or `blog-03.jpg`.
- **Edit a thought under an artwork** — search the artwork's title
  (e.g., `Witness`) and find the matching `art-thought` block.
- **Add an artwork** — drop into `assets/art/`, then duplicate an
  `<article class="art-card">` block in the carousel. Also add a
  matching entry to the `ARTWORKS` array near the bottom of the
  script for the lightbox.
- **Add a certificate** — duplicate any `<article class="cert-card">`
  block in the recognition carousel.
- **Edit research** — search for `<article class="work-item"`.
- **Replace your CV** — drop your new file at
  `assets/cv/Khadiza-Akter-CV.docx`. Done.

## What changed in v7

- **Drawings now reliably display.** Switched from JavaScript
  lazy-swap to direct `src` attributes with native browser
  `loading="lazy"`. Each container still has an inline base64
  thumbnail as a background-image fallback, so if the assets folder
  ever goes missing you still see a low-res preview instead of
  nothing.
- **Scrap Box is now compact** — small carousel cards just like the
  Creative and Recognition sections. Clicking a card opens a
  focused reader modal showing the illustration on the left and the
  full prose on the right (stacks vertically on mobile).
- **About section softened** — the "Rank 1st in Department" framing
  is gone. The SGPA 9.70 is kept, presented now as
  "SGPA · Diploma in CSE". The about prose drops the
  "top of department" phrasing and just states the facts.
- **Smart City book chapter** is now correctly marked "In progress"
  (was previously "Published" — only the Cardiology chapter is
  published among the three).

## Browser support

Modern browsers (Chrome, Safari, Firefox, Edge) — last 2 years.
The custom cursor only appears on devices with hover + fine pointer.
Reduced-motion preferences are respected throughout.

## Notes on the art

The artworks are signed `Andrea Piu` on some pieces and `Khadiza` on
others. The site shows everything under "Khadiza Akter" and the
Creative section's intro acknowledges the secondary signature.
