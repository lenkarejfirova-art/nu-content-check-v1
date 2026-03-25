---
name: nu-content-check
description: >-
  Review Portuguese (pt-BR) product copy against Nubank content guidelines,
  accessibility rules, UX writing heuristics, and lending glossaries.
  Use when the user asks to "check content", "content check", "revisar conteúdo",
  "checar texto", or any request to validate screen copy for Nubank Brazil products.
---

# Nu Content Check

## What this skill does

Audits product copy (pt-BR) against Nubank's official content guidelines, returning a checklist of what passes and what needs revision.

## How to trigger

The user will ask manually, e.g.:
- "faça o content check"
- "check this content"
- "revisar conteúdo"
- "checar texto"

The user will provide the copy to review — either as pasted text or by describing the screen context.

## Step 1 — Read the guidelines

Before every review, read all reference files to ensure accuracy:

1. `content-guidelines/nuds-content-guidelines.md`
2. `content-guidelines/accessible-content.md`
3. `content-guidelines/content-heuristics.md`

If the copy is related to a lending product, also read the relevant glossary:

- `lending-glossary/private-payroll.md`
- `lending-glossary/fgts.md`
- `lending-glossary/pj-personal-loans.md`
- `lending-glossary/pf-personal-loans.md`
- `lending-glossary/public-payroll.md`

## Step 2 — Ask for context (if needed)

If the user hasn't specified, ask:
- What **product** is this for? (to pick the right glossary)
- What **component type** is this? (title, subtitle, button, error message, push notification, tooltip, modal, etc.)

## Step 3 — Run the content check

Evaluate the copy against each category below. For each item, mark:
- ✅ = passes
- ❌ = fails (include what's wrong and a suggested fix)
- ⚠️ = needs attention / ambiguous

### Checklist categories

**Tone of Voice**
- [ ] Objective — direct, short, no unnecessary words
- [ ] Attentive — empathetic, human, not overly intimate
- [ ] Spirited — appropriate use of humor (if any), not childish
- [ ] Up to date — culturally relevant without overdoing memes/emojis

**Content Patterns**
- [ ] Punctuation — periods, no periods in titles/buttons/lists
- [ ] Date format — correct for context (running text vs technical)
- [ ] Time format — 24h system, correct use of `h` vs `:`
- [ ] Numbers — numerals used, not spelled out
- [ ] Money — `R$` with space, correct decimal format
- [ ] Fees — `%` with no space, comma for decimals
- [ ] Line breaks — currency symbol and amount stay together
- [ ] Lists — numbered for steps, bullets for unordered
- [ ] Links — descriptive text or clear context
- [ ] Error messages — problem + solution + CTA formula
- [ ] Terms & Conditions — scannable, simple language, progressive disclosure
- [ ] Emoticons — not used (accessibility)
- [ ] Emojis — end of sentence only, max 1 per paragraph, no pejorative emojis

**Accessibility**
- [ ] Reading level — simple, clear, short sentences
- [ ] No jargon/memes/local expressions without explanation
- [ ] Acronyms — meaning provided in parentheses on first use
- [ ] Foreign words — replaced with native equivalent when possible
- [ ] No reliance on color/position/sensory cues alone
- [ ] No text embedded in images without text alternative

**UX Writing Best Practices**
- [ ] Readable — conversational, ~6th grade level
- [ ] Concise — no repetition or redundancy
- [ ] Consistent — same patterns for same component types
- [ ] Guiding — next action is clear
- [ ] User-focused — benefits over product/company goals
- [ ] Prioritized — information hierarchy is clear

**Glossary check** (if lending product)
- [ ] Terms match the official Nubank terminology
- [ ] Capitalization follows glossary rules
- [ ] No competitor or informal terms used where official term exists

## Step 4 — Present the results

**Always review piece by piece.** When the user sends multiple pieces of content (e.g. push, email, app screen, highlight), present a **separate, complete content check for each piece** before moving to the next. Each piece starts when the user indicates a new "Comms type", screen, or component.

This allows the person reviewing to adjust in real time, one piece at a time.

Output format **per piece**:

```
## Content Check — [Comms type / Screen name]

**[List the content fields: Title, Message, CTA, etc.]**

### Tom de Voz
- ✅ / ❌ / ⚠️ per item

### Content Patterns
- ✅ / ❌ / ⚠️ per item

### Acessibilidade
- ✅ / ❌ / ⚠️ per item

### UX Writing
- ✅ / ❌ / ⚠️ per item

### Glossário (if applicable)
- ✅ / ❌ / ⚠️ per item

### Resultado: ✅ X | ❌ X | ⚠️ X
```

After all pieces are reviewed, add a **summary table**:

```
## Resumo Geral

| Comms type | ✅ | ❌ | ⚠️ |
|---|---|---|---|
| [type] | X | X | X |
| **Total** | **X** | **X** | **X** |
```

## Step 5 — Generate a review log

After every content check, create a short Markdown file inside `review-logs/` documenting the review. Use the naming format: `YYYY-MM-DD-[product]-[comms-description].md`.

The file should contain:
- **Date**, **product/context**, and **source document link** (if provided)
- **Original content (pre-review)** — full copy as received, organized by comms type
- **What was reviewed** (list of comms types)
- **Key decisions** — why certain items were flagged, what guideline backed each decision
- **Summary of results** (pass/fail/attention counts per comms type)
- **Open questions** — anything ambiguous or not covered by current guidelines

This log serves as a reference for future reviews and for tracking how decisions were made.

---

## Important rules

- Always check against the **latest version** of the guideline files (re-read them each time).
- Do NOT take liberties — if something is not covered by the guidelines, flag it as ⚠️ rather than inventing a rule.
- Write feedback in the **same language as the copy being reviewed** (Portuguese for pt-BR copy).
- Be specific: quote the exact text that has an issue and provide a corrected version.
- When the copy is for a lending product, the glossary check is mandatory.
