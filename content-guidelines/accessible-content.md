# Accessible Content

The guidelines gathered here are based on global guidelines such as **WCAG**, as well as conversations with people with disability and their personal experiences.

---

## Reading Level and Readability

Our content must reach as many people as possible and provide the opportunity for all of these people to understand the guidelines, explanations and actions to be taken.

To meet such criteria, we must take into account the level of reading and readability of the texts. A standard established by **UNESCO** puts simple and clear language as a way to meet the world's basic educational level of people.

### Good Practices

- If the sentence is long, try to break it into two smaller sentences.  
- Avoid repeating words and redundant words.  
- Use conversational language and with references to the spoken language.  
- Avoid technical and far-fetched terms whenever possible.  
- Test your content whenever you can.  

---

## Jargon, Memes, Local Expressions, Foreign Words and Abbreviations

The use of jargon, memes, local expressions, foreign words and abbreviations can make reading difficult via assistive technology, such as screen readers, but also creates barriers of understanding for people with functional illiteracy, ASD (Autistic Spectrum Disorder), ADHD (Attention Deficit Hyperactivity Disorder), elderly people, people with Tourette Syndrome, Dyslexia and others. Therefore, we recommend using **plain language** on all content approaches for any experience.

### Good Practices

- When writing acronyms, always provide the meaning in parentheses right at the front, for example:  
  `ASD (Autistic Spectrum Disorder)`.
- Whenever possible, replace words in other languages with the native language of the user.

**Exception:** words in other languages that have already become popular and whose meanings are easily understood by people.  
_Examples: shopping, motoboy, selfie, show, site._

Memes, slang and local expressions should be avoided because they can make a lot of sense to some people but can bring up questions and make many confused. At Nubank, our content must be accessible to everyone. Some expressions are widely used in specific regions of the country but are unknown to others. Therefore, **objectivity and simplicity** should always be our starting point.

---

## Visual Cues

For users who are colorblind, other design elements can help express the same amount of information. Because colorblindness takes different forms (including red-green, blue-yellow, and monochromatic), multiple visual cues help communicate important states. Elements such as strokes, indicators, patterns, texture, or text can describe actions and content.

### Good Practices

- Don't just rely on using colors to identify status or feedback; use other mechanisms to indicate this information, for example using iconography or illustrations.  
- Also ensure correct semantic usage. Color foundations are designed to also guarantee the minimum contrast for applications over other colors.

---

## Imagery

### Decorative Images

According to <https://www.w3.org/WAI/tutorials/images/decorative>, decorative images don't add important information to the content of a page, that is, they are merely complementary to the main content, but do not communicate information individually.

### Informative Images

According to <https://www.w3.org/WAI/tutorials/images/informative>, informative images convey a concept in a short, digestible manner. Informative images:

- Relay accurate information that is relevant to the adjacent text.  
- Have to meet the [accessibility requirements for essential items](https://nuds.nu.com.br/46f3733aa/v/0/p/31d6f8-accessibility-v2/t/754f7f).

### Charts

Users who have low vision or colorblindness need additional visual cues that don't rely solely on color to distinguish the data points on a complex graph. Consider additional cues to link data points to their corresponding legend text and make sure you are applying the [color foundations](https://nuds.nu.com.br/46f3733aa/v/0/p/02872e-colors/t/69c3d9) properly to guarantee contrast between colors.

---

## Accessibility: Examples of Do's and Don'ts

| Area / Topic | Do | Don't | Example |
|--------------|----|-------|---------|
| **Component naming & position** | Use default names for interaction components. | Don't rely on terms that point only to direction or placement rules. | **Do:** "Clique no botão **Salvar**."  **Don't:** "Clique no botão **ali embaixo à direita**." |
| **Component naming & color** | Use default names for interaction components and describe their function. | Don't specify colors or value attributes of an element as the only way to identify it. | **Do:** "Use o botão **Continuar** no fim da página."  **Don't:** "Use o botão **roxo** no fim da página." |
| **Sensory language** | Use terms or synonyms that do not depend on a sensory action. | Don't use purely sensory verbs for links or buttons (e.g. "veja", "ouça", "sinta") when the action is more specific. | **Do:** "Selecione **Ver detalhes da fatura**."  **Don't:** "**Veja aqui**." |
| **Icons** | For visual representation using symbols, use the official iconography library. | Don't use special characters or random Unicode symbols in place of icons. | **Do:** usar `icon-info` do design system.  **Don't:** usar `★`, `►`, `➤` como se fossem ícones funcionais. |
| **Emojis** | Use emojis apenas quando forem essenciais para a experiência e coloque-os no **final** da frase. | Don't use emoji as a word replacement or repeat emojis; one is enough. | **Do:** "Pagamento concluído com sucesso! ✅"  **Don't:** "✅ Pagamento ✅ concluído" ou "Seu limite está ok 💳✨✨✨". |
| **Language choice** | Prefer native words (in the language you are writing). | Avoid technical terms or terms from another language when há opção nativa clara. | **Do (pt-BR):** "Acesso **pelo navegador**."  **Don't:** "Acesse **pela web**." |
| **Text in images** | When an image contains phrases or words, describe that text claramente no conteúdo adjacente **ou** use only decorative images without text relevante. | Don't use images containing phrases or texts without any way of contextualizing or reproducing that content em texto. | **Do:** imagem com frase "Pague tudo em um só lugar" + mesmo texto no título ao lado.  **Don't:** card com texto importante embutido na imagem e nenhum texto equivalente na tela. |
| **Charts & graphs** | Always use graphics accompanied by a clear legend (key). | Even when using Data Visualization colors, don't rely on non-contrasting colors or color alone to differentiate data. | **Do:** barras com rótulo de texto + legenda com nome e padrão visual.  **Don't:** duas linhas em tons muito parecidos de verde sem legenda textual. |

---

_Source: <https://nuds.nu.com.br/46f3733aa/p/598527-accessibility>_
