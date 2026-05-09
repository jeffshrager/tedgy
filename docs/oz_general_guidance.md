# Oz General Guidance

This document captures standing guidance for how TedGy should format and structure daily sheets. It applies to all projects unless overridden by a project-specific note. Update it as decisions get made.

---

## Page structure

Every daily sheet follows this order, top to bottom:

1. **Header line** — project name (bold, large) and day number, on one line
2. **Project sentence** — one sentence describing the project; identical every day; in italics below the header
3. **Today paragraph** — short, plain-English paragraph in Ted's voice describing what the team is doing today; not a bullet list
4. **Widgets** — the day's fill-in sections (tables, blanks, checkboxes); each preceded by a brief instruction
5. **Footer** — "Hand this in at the end of class." on the last page of the packet; omit on the final day of the project

Multi-page packets: all pages for one team on one day scan together as a unit. Each page after the first should carry a smaller header (project name + day + "page N of M") so pages don't get mixed up.

---

## Fonts

*To be decided. Placeholder defaults below — update once confirmed.*

| Element | Font | Size | Style |
|---------|------|------|-------|
| Header (project + day) | TBD | 18pt | Bold |
| Project sentence | TBD | 11pt | Italic |
| Today paragraph | TBD | 12pt | Regular |
| Section labels | TBD | 12pt | Bold |
| Widget instructions | TBD | 11pt | Regular |
| Fill-in labels | TBD | 11pt | Regular |
| Footer | TBD | 10pt | Regular |

General preference: clean, readable sans-serif. Avoid decorative fonts. Kids will read this in a classroom, not on a screen.

---

## Boxes and fill-in lines

- **Boxes must be large enough to write in by hand.** Minimum height: ~0.75 inch (about 2 cm) per row in a table; more for open-ended response boxes.
- Fill-in lines should be actual printed lines (underscores or ruled lines), not just whitespace.
- Checkboxes should be printed squares (at least 0.25 inch), not dashes or bullets.
- Don't pack widgets too tightly. White space is a feature — it signals "write here."

*Note: box sizing is the main known layout issue as of 2026-05-09. Current markdown mocks use underscore lines as placeholders; the PDF pass needs to replace these with properly spaced ruled lines.*

---

## Widget design rules

- Widgets should constrain input structurally: labeled blanks, fixed-column tables, checkboxes. Avoid asking for free-form diagrams or drawings — these are hard for TedGy to parse from a scan.
- Every widget should have a one-line instruction immediately above it explaining what to put there.
- If a table has optional rows (e.g., "use as many as you need"), say so explicitly in the instruction.
- Triage-type widgets (e.g., "is this a problem? yes / no / maybe") are useful — they make team judgment visible to TedGy, not just raw observations.

---

## Tone and voice

- Ted's voice throughout: warm, direct, not condescending. Talks to kids like they're capable of making real decisions.
- The "today paragraph" should feel like Ted is speaking, not like a worksheet prompt.
- Instructions near widgets can be more terse — kids are reading them while working, not as an introduction.
- Avoid jargon. "Scene map" is fine; "narrative branching structure" is not.

---

## Scanning

- Target: flatbed or document-feeder scanner, grayscale, 200–300 DPI.
- Consistent orientation matters. Portrait, always.
- Wizard handles occasional mis-reads manually — no need to over-engineer.
- Filename convention: `days/N/<team>/scan.png` for single-page; `scan_p1.png`, `scan_p2.png`, etc. for multi-page packets.

---

## Things not yet decided

- Exact fonts
- Whether to include a small team-name box on each page (useful if pages get separated)
- Whether page headers on pages 2+ are auto-generated or manually specified
