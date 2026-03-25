# Review Log — Public Payroll: Refinanciamento GTM Comms

**Date:** 2026-03-24
**Product:** Public Payroll (Consignado)
**Context:** Go-to-market communications for the Refinanciamento feature launch
**Source document:** [Google Docs — Refinanciamento GTM Comms](https://docs.google.com/document/d/1rqQfGcD9x1kKWMo9U3kigIpn9kqkUDIaxpQsi6FN2Y4/edit?tab=t.0)

---

## Original content (pre-review)

### Push
- **Title:** Novidade no seu consignado
- **Message:** Refinancie seu contrato e receba um valor extra na conta em até 3 horas. Saiba mais.

### App Screen
- **Title:** Refinanciamento de consignado
- **Paragraph:** Refinanciar seu consignado permite que você atualize os termos do seu contrato atual para que ele se adeque melhor à sua vida financeira atual. Ao decidir pelo refinanciamento, você tem a liberdade de reorganizar os valores e prazos do seu contrato em um único fluxo.
- **Benefit 1:** Acesso à mais crédito — Escolha o valor adicional que você precisa para realizar seus objetivos.
- **Benefit 2:** Prazo sob medida — Defina a quantidade de parcelas que melhor se encaixa no seu planejamento.
- **Benefit 3:** Parcela ideal — Escolha o valor da parcela mensal que cabe no seu orçamento.
- **CTA:** Simule agora

### Announcement Screen
- **Title:** Refinancie seu consignado com o Nubank
- **Paragraph:** Agora você pode refinanciar seu consignado com as condições que melhor atendem às suas necessidades.
- **Benefit 1:** Valor extra desejado — Escolha o valor que você precisa para realizar seus objetivos.
- **Benefit 2:** Prazo sob medida — Defina a quantidade de parcelas que melhor se encaixa no seu planejamento.
- **Benefit 3:** Parcela ideal — Escolha o valor da parcela mensal que cabe no seu orçamento.
- **CTA:** Simule agora

### Email — Marinha & Aeronáutica
- **Subject:** Oportunidade no consignado
- **Preview:** Refinancie seu contrato direto pelo app, sem intermediários.
- **Header:** Seu consignado do seu jeito
- **Body:** Oi, {{preferred_name}}. O seu consignado do Nubank agora conta com a flexibilidade do refinanciamento, uma novidade que permite que você adapte o seu contrato ativo ao seu momento atual. Ao refinanciar seu contrato, você pode ajustar o valor das parcelas e os prazos, além de liberar um valor extra na conta para dar mais fôlego aos seus planos.
- **CTA 1:** Simular refinanciamento
- **Steps:** Inicie a simulação → Personalize seu contrato → Confirme a contratação
- **Step detail (Personalize):** Defina as novas condições e avance no botão roxo no canto inferior da tela.
- **Step detail (Confirme):** Leia o resumo das condições do empréstimo e confirme o refinanciamento utilizando sua senha de 4 dígitos.
- **CTA 2:** Simule agora

### Email — Apenas Exército
- **Subject:** Oportunidade no consignado
- **Preview:** Refinancie seu contrato direto pelo app, sem intermediários.
- **Header:** Seu consignado do seu jeito
- **Body:** Oi, {{preferred_name}}. O seu consignado do Nubank agora conta com a flexibilidade do refinanciamento, uma novidade que te permite  adaptar o seu contrato ativo ao seu momento atual. Ao refinanciar seu contrato, você pode ajustar o valor das parcelas e os prazos, além de liberar um valor extra na conta para dar mais fôlego aos seus planos.
- **CTA 1:** Simular refinanciamento
- **Steps:** Inicie a simulação → Personalize seu contrato → Validação no eConsig → Confirme a contratação
- **Step detail (Personalize):** Defina as novas condições e avance no botão roxo no canto inferior da tela.
- **Step detail (eConsig):** Na tela de validação, toque em "Gerar código no eConsig". No app eConsig, acesse a aba "Serviços", copie seu "Código Único" e cole-o no aplicativo do Nubank.
- **Step detail (Confirme):** Leia o resumo das condições do empréstimo e confirme o refinanciamento utilizando sua senha de 4 dígitos.
- **CTA 2:** Simule agora

### Highlight
- **Message:** ** Novidade:** refinanciamento de consignado. Saiba mais.

---

## What was reviewed

| # | Comms type | Target audience |
|---|---|---|
| 1 | Push Notification | All Public Payroll users |
| 2 | App Screen | All Public Payroll users |
| 3 | Announcement Screen | All Public Payroll users |
| 4 | Email | Marinha & Aeronáutica |
| 5 | Email | Apenas Exército |
| 6 | Highlight | All Public Payroll users |

---

## Key decisions and reasoning

### "botão roxo no canto inferior da tela" flagged as accessibility issue
Both emails instructed users to "avance no botão roxo no canto inferior da tela". This was flagged based on two accessibility guidelines: (1) Don't specify colors as the only way to identify an element, and (2) Don't rely on direction/placement terms alone. The accessible-content.md explicitly lists "Use o botão roxo no fim da página" as a Don't example. Suggested using the button's name instead.

### "Acesso à mais crédito" flagged as grammar error
The crase in "à mais crédito" is incorrect in Portuguese. Crase requires a feminine definite article meeting the preposition "a". "Mais crédito" does not satisfy this condition. This is a grammar issue, not a guideline-specific one, but the content-heuristics checklist includes "Correct — Have all spelling, grammar, capitalization been checked?"

### "reorganizar os valores e prazos" flagged as glossary conflict
In the Public Payroll glossary, "Reorganizar" is defined as renegotiating overdue debt — a different concept from refinancing. Using "reorganizar" in a refinanciamento context could confuse users who know the term from collections/renegotiation flows. Suggested "ajustar" or "redefinir" as alternatives.

### "valor extra" vs "Troco" flagged as ⚠️ (not ❌)
The glossary lists "Troco" as validated with users for top-up loan value. However, these are marketing comms (not in-product), and "valor extra" may be clearer for a broader audience. Flagged as ⚠️ for the team to decide, rather than ❌.

### Step-by-step without numbered lists flagged in emails
The NUDs content guidelines state: "Whenever you need to describe a step by step or a process that has an order, use numbered lists, not bullet points." The emails present 3–4 ordered steps using title formatting instead of numbers.

### CTA inconsistency flagged in emails
The first CTA uses infinitive ("Simular refinanciamento") while the second uses imperative ("Simule agora"). This inconsistency was flagged under the UX Writing heuristic "Consistent — Do text elements of the same type use parallel patterns?"

### "eConsig" without explanation flagged as ⚠️
The accessible-content.md says acronyms should have meaning in parentheses on first use. However, eConsig is a known app for the Exército audience, so this was flagged as ⚠️ rather than ❌.

---

## Summary of results

| Comms type | ✅ | ❌ | ⚠️ |
|---|---|---|---|
| Push | 12 | 0 | 1 |
| App Screen | 8 | 4 | 0 |
| Announcement Screen | 11 | 0 | 1 |
| Email Marinha & Aeronáutica | 11 | 4 | 0 |
| Email Exército | 10 | 5 | 1 |
| Highlight | 8 | 1 | 0 |
| **Total** | **60** | **14** | **3** |

---

## Open questions

- **"Troco" vs "valor extra"** — should marketing comms align with the in-product glossary term, or is "valor extra" acceptable for GTM?
- **Consistency guide** — a dedicated guide for checking consistency across comms (verb tense in CTAs, structure in step-by-steps, etc.) is still pending.
- **eConsig context** — should we always explain "eConsig" even for military audiences who use it daily?
