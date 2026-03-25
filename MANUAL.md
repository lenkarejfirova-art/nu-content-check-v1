# Nu Content Check — User Manual

A tool that reviews your product copy against Nubank's official content guidelines. It checks tone of voice, content patterns, accessibility, UX writing best practices, and lending glossary compliance.

**Scope:** Portuguese (pt-BR) copies for Nubank Brazil products.

---

## Getting started

### What you need

- [Cursor](https://cursor.sh/) installed on your Mac
- Access to this repository

### Setup (one time only)

1. Open your terminal and clone the repository:
   ```
   git clone https://github.com/lenkarejfirova-art/nu-content-check-v1.git
   ```
2. Open the folder `nu-content-check-v1` in Cursor
3. Done! The skill is already included in the repo and will be available automatically

---

## How to use

### Step 1 — Open a chat in Cursor

In Cursor, open the Agent chat (Cmd + L or click the chat icon).

### Step 2 — Ask for a content check

Type one of these (or similar):

- `faça o content check`
- `check this content`
- `revisar conteúdo`
- `checar texto`

### Step 3 — Provide your content

Paste the copy you want to review. You can send:

- A single screen (title, body, CTA, etc.)
- Multiple pieces at once (push, email, app screen, etc.) — just label each one with its **Comms type**

**Example format:**

```
Comms type: Push
Title: Novidade no seu consignado
Message: Refinancie seu contrato e receba um valor extra na conta.

Comms type: Email
Subject: Oportunidade no consignado
Header: Seu consignado do seu jeito
Body: Oi, {{preferred_name}}. O seu consignado...
CTA: Simule agora
```

### Step 4 — Tell the agent which product it's for

If your content is for a lending product, let the agent know which one so it can check the glossary:

- Private Payroll (Consignado do Trabalhador)
- Public Payroll (Consignado público)
- FGTS (Antecipação do Saque-Aniversário)
- PF Personal Loans (Empréstimo Pessoal PF)
- PJ Personal Loans (Capital de Giro)

If it's not a lending product, the agent will skip the glossary check.

### Step 5 — Review the results

The agent will return a checklist for **each piece of content separately**, covering:

| Category | What it checks |
|---|---|
| **Tom de Voz** | Objective, attentive, spirited, up to date |
| **Content Patterns** | Punctuation, dates, time, numbers, money, fees, lists, links, errors, emojis |
| **Acessibilidade** | Reading level, jargon, acronyms, color/position references |
| **UX Writing** | Readability, conciseness, consistency, guidance, hierarchy |
| **Glossário** | Correct terms, capitalization, no informal/competitor terms |

Each item is marked:
- ✅ Passes
- ❌ Fails (with explanation and suggested fix)
- ⚠️ Needs attention (ambiguous or not covered by guidelines)

At the end, you get a **summary table** with totals per piece.

### Step 6 — A review log is saved automatically

After each review, the agent creates a log file in the `review-logs/` folder with:
- The original content (pre-review)
- Source document link (if provided)
- Key decisions and reasoning
- Summary of results
- Open questions

This way anyone can come back later and understand what was reviewed and why.

---

## What's inside the repo

```
nu-content-check-v1/
├── README.md                        # Project overview
├── MANUAL.md                        # This file
├── PROCESS.md                       # How the tool was built
├── content-guidelines/              # The rules the agent checks against
│   ├── nuds-content-guidelines.md   # Tone of voice, content patterns
│   ├── accessible-content.md        # Accessibility (WCAG-based)
│   └── content-heuristics.md        # UX Writing best practices checklist
├── lending-glossary/                # Official terms per lending product
│   ├── private-payroll.md
│   ├── fgts.md
│   ├── pj-personal-loans.md
│   ├── pf-personal-loans.md
│   └── public-payroll.md
├── review-logs/                     # Logs from past reviews
└── .cursor/skills/nu-content-check/ # The skill that powers the tool
    └── SKILL.md
```

---

## Tips

- **Send the source document link** when asking for a review — the agent will include it in the log for reference.
- **Label each piece** with "Comms type" when sending multiple pieces — this helps the agent separate the checks.
- **Be specific about the component** (title, button, subtitle, error message, etc.) — punctuation rules differ by component type.
- **You can ask follow-up questions** after the review, like "can you suggest a rewrite for the app screen?" or "what would be a better CTA?"

---

## Keeping the tool updated

### Guidelines or glossary changed?

If Nubank updates a content guideline or a glossary term is added/changed:

1. Open the relevant `.md` file in the `content-guidelines/` or `lending-glossary/` folder
2. Make the edit
3. Commit and push to keep everyone in sync:
   ```
   git add .
   git commit -m "Update [file name] with [what changed]"
   git push
   ```

### Pulling the latest version

Before using the tool, make sure you have the latest version:

```
cd nu-content-check-v1
git pull
```

---

## Questions?

Reach out to Lenka Rejfirova (Content Design, Lending) for questions about the tool or the guidelines.
