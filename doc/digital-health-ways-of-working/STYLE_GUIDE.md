# Style guide — *Ways of Working for Digital Health & Care*

This guide is shared by every chapter author so the book reads as one coherent volume. Follow it exactly.

## Audience
Senior leaders, delivery leads, product managers, clinicians-turned-digital-leaders, and operational managers in **digital health and care organizations** — NHS bodies and trusts, integrated care systems (ICS/ICBs), social care organizations, arms-length bodies (e.g. NHS England, NHSX legacy, UKHSA), health-tech suppliers, and government digital units. Assume a UK/NHS and social-care centre of gravity, with internationally transferable principles (US HIPAA, EU/UK GDPR, HL7 FHIR context where relevant).

## Voice & tone
- Authoritative, practical, calm. Write for a busy director who wants to *act*, not admire.
- Prefer plain English. Expand every acronym on first use in each chapter.
- Second person ("you", "your organization") when giving guidance; third person when describing practice.
- No hype. Name trade-offs honestly. Evidence over assertion.

## Chapter structure (use these headings)
1. `# Chapter N — Title`
2. **In one sentence** — a single bold sentence stating the chapter's thesis.
3. `## Why this matters in health and care` — the domain-specific stakes (safety, equity, statutory duties, public money).
4. `## Core concepts` — the definitions and mental models.
5. `## Best practices` — numbered, each a bold lead-in + 2–4 sentences. This is the heart of the chapter.
6. `## Questions to discuss with your team` — exactly **three** numbered questions for peer discussion, placed BEFORE the examples. Each is an open (non-yes/no) question in **bold**, followed by a comprehensive paragraph (4–8 sentences) that: explains why the question matters in a digital health/care setting, surfaces the tensions and trade-offs to debate, points to concrete angles and examples to consider, and describes what a good, honest answer looks like. Make the questions genuinely useful in a real team workshop.
7. `## In practice: a health & care example` — a concrete worked scenario (fictional but realistic; e.g. an ICS rolling out a shared care record).
7. `## Three sector lenses` — the SAME topic applied in three different organisational contexts, as three `###` subsections in this order: `### Startup` (a small, fast, funding-constrained digital-health company), `### Enterprise` (a large, complex organisation — an NHS trust, an ICS, or a big health-tech/pharma firm), `### Government` (a national or local public body — NHS England, DHSC, a devolved government, UKHSA, a local authority). Each is 3–6 sentences, concrete and specific, showing how the chapter's practice changes with organisational scale, funding model, risk appetite, and accountability.
8. `## Common failure modes` — a short list of anti-patterns and how to avoid them.
9. `## Maturity model` — a 4-level table (Initial / Developing / Defined / Optimising) with 3–5 rows of observable characteristics.
10. `## Checklist` — 6–12 actionable checkbox items (`- [ ]`).
11. `## Key sources` — bulleted, with real, verifiable references (NHS, GOV.UK, NICE, professional bodies, recognized frameworks). Cite frameworks by name (e.g. NHS Digital Service Standard, GDS Service Manual, MSP, PRINCE2, SAFe, Kotter, ADKAR, Spotify model, Team Topologies, OKRs).
12. `## References` — a numbered list (`1.` …) of full references for the chapter, combining (a) the **Wikipedia** articles for the key concepts named in the chapter and (b) the authoritative sources. Each entry: title — publisher/author — URL. Wikipedia URLs use canonical English article titles (e.g. `https://en.wikipedia.org/wiki/Kanban_(development)`).

## Wikipedia links (required)
- On the **first mention** of a key named concept, framework, or method in `## Core concepts` (and elsewhere where natural), hyperlink the term to its English Wikipedia article: `[Cost of delay](https://en.wikipedia.org/wiki/Cost_of_delay)`.
- **Verify** each article exists before linking (a quick WebSearch/WebFetch for `site:en.wikipedia.org <term>`); never invent a slug. If no good article exists, don't force a link.
- Aim for 5–12 Wikipedia links per chapter — enough to help a reader research, not so many the prose turns blue. Every Wikipedia article you link inline must also appear in `## References`.

## Formatting rules
- Markdown only. Use tables for comparisons and maturity models.
- Keep paragraphs to 2–4 sentences.
- Bold the lead phrase of each best practice.
- Target ~2,500–3,500 words per chapter (current chapters run ~2,900–3,400). Be comprehensive but not padded.
- Use UK spelling (organisation, prioritise, programme) EXCEPT keep "program" when it means a US-style software program; use "programme" for the delivery construct (programme management, MSP). Be consistent within a chapter.
- Cross-reference sibling chapters by number and title, e.g. "(see Chapter 8.1 — Change Management)". The canonical chapter numbering lives in `spec/index.md` §4 — check it before citing a number.

## Grounding
- Ground claims in recognised frameworks and public guidance. Real, checkable sources only — do not invent citations, URLs, statistics, or quotations. If unsure of a figure, describe the pattern qualitatively instead.
- Favour these canonical bodies of knowledge where they fit: NHS Digital Service Standard & Service Manual, GOV.UK Service Manual (GDS), NICE Evidence Standards Framework for Digital Health Technologies, MHRA, DTAC (Digital Technology Assessment Criteria), Team Topologies, Spotify/agile-at-scale, SAFe, PRINCE2, MSP (Managing Successful Programmes), Management of Portfolios (MoP), Kotter's 8 steps, ADKAR (Prosci), OKRs (Doerr), Lean/Toyota, Cynefin (Snowden), double-diamond discovery (Design Council).
