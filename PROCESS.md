# nu-content-check-v1 — Process Documentation

## What is this project?

A scalable content review tool for Nubank designers and other functions. Instead of relying solely on peer reviews, this tool lets anyone check their screen copy against official content guidelines — making reviews faster, more thorough, and accessible to everyone.

**Initial scope:** Portuguese-written copies for Nubank Brazil products.

---

## How we're building the guidelines base

### Step 1 — Extract guidelines to plain text
Using Glean to convert Nubank's internal content documents into clean plain text.

### Step 2 — Convert to Markdown
Glean transforms the plain text into structured Markdown format.

### Step 3 — Repeat for all relevant sources
The same process (Steps 1–2) will be applied to every guideline document we consider relevant:

- [x] Nubank Content Guidelines → `content-guidelines/nuds-content-guidelines.md`
- [x] Content Heuristics → `content-guidelines/content-heuristics.md`
- [x] Accessibility / WCAG Guides for Content → `content-guidelines/accessible-content.md`
- [x] Lending Glossary → `lending-glossary/` (one .md per product)
  > **Disclaimer:** The Lending Glossary is sourced from a Google Sheets document. Whenever that sheet is updated, the corresponding `.md` file must be manually updated as well (by adding a new SVG file). These updates are infrequent.
- [ ] Legal / Product Ops content check _(under review — may become `legal-content-check.md`)_

### Step 4 — Consolidate into the content-guidelines folder
Once all guides are collected in Markdown, they are placed in the `content-guidelines/` folder. These become the reference base for all future content checks.

### Step 5 — Create the Content Check skill
A Cursor skill (`nu-content-check`) was created to automate content reviews against the guidelines. The skill reads all guideline files and the relevant lending glossary, then outputs a structured checklist per piece of content.

### Step 6 — Test the skill with real content
The skill was tested with real go-to-market communications (Public Payroll — Refinanciamento), including: Push, App Screen, Announcement Screen, Email (Marinha & Aeronáutica), Email (Exército), and Highlight. The test validated the skill's ability to catch issues across tone of voice, content patterns, accessibility, UX writing best practices, and glossary compliance. Results are returned **separated per comms type** for easier review and real-time adjustments.

### Pending improvements

- [ ] **Consistency check guide** — A guide for checking consistency across comms is still missing (e.g. step-by-step lists: should they use numbered lists, same verb tense, same structure?). This will be elaborated and added as a new guideline file to strengthen the content check.

---

## Project structure

```
nu-content-check-v1/
├── README.md                          # Project overview
├── PROCESS.md                         # This file — documents how we built it
├── content-guidelines/
│   ├── nuds-content-guidelines.md     # Nubank Content Guidelines (tone of voice, patterns)
│   ├── accessible-content.md          # Accessibility guidelines (WCAG, readability, visual cues, imagery)
│   └── content-heuristics.md          # UX Writing Best Practices Checklist
├── lending-glossary/                  # Lending product glossaries (one .md per product)
│   ├── private-payroll.md
│   ├── fgts.md
│   ├── pj-personal-loans.md
│   ├── pf-personal-loans.md
│   └── public-payroll.md
├── review-logs/                       # Review documentation (one .md per content check session)
│   └── 2026-03-24-public-payroll-refinanciamento-gtm.md
└── .cursor/skills/nu-content-check/   # Content check skill (shared via repo)
    └── SKILL.md
```

---

## Log

| Date       | Action                                      |
|------------|---------------------------------------------|
| 2026-03-24 | Project created, repo initialized on GitHub  |
| 2026-03-24 | Created style-guide folder and PROCESS.md    |
| 2026-03-24 | Added content-guidelines.md to style-guide    |
| 2026-03-24 | Added accessible-content.md to content-guidelines |
| 2026-03-24 | Extracted content-heuristics.md from nuds-content-guidelines |
| 2026-03-24 | Added lending-glossary with 5 products: private-payroll, fgts, pj-personal-loans, pf-personal-loans, public-payroll |
| 2026-03-24 | Created nu-content-check skill (personal) |
| 2026-03-24 | First test: Public Payroll Refinanciamento go-to-market comms (push, app screen, announcement, emails, highlight) |
