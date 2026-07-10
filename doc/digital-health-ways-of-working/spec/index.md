# Specification — *Ways of Working for Digital Health & Care*

**Status:** Authoritative source of truth. This document governs the book. Where a chapter, the README, the style guide, or any generated content disagrees with this spec, **this spec wins** — fix the artifact, or change the spec deliberately and then bring the artifacts into line.

**Purpose:** Enough here for any author or agent to (a) understand what the book is, (b) build or regenerate any single chapter to a consistent standard, and (c) verify the result against a checklist — without reading the other 47 files first.

---

## 1. Product definition

A practical handbook of best practices for leading and running digital delivery in health and social care organisations.

- **Working title:** *Ways of Working for Digital Health & Care*
- **Subtitle:** A practical handbook of best practices for delivering digital services in health and social care organisations
- **Format:** A set of Markdown files, one per chapter, stitched by `README.md` (the table of contents) plus reference matter (`GLOSSARY.md`, `INDEX.md`).
- **Premise (the book's spine):** *In health and care, **how** you work is a clinical-safety, equity, and public-trust issue — not merely an efficiency one.* Every chapter must ultimately serve this thesis.
- **Centre of gravity:** UK NHS and social care, with principles that transfer to any publicly-accountable, safety-critical, partnership-dependent health organisation internationally.

### Audience
Chief executives and senior leaders; directors of digital and transformation; product, delivery, programme, and portfolio leads; clinical and care professionals moving into digital roles; and the operational managers who run services daily. Write for a busy director who wants to **act**.

---

## 2. Repository layout

| Path | Role |
|---|---|
| `README.md` | Reader-facing front door + table of contents. Must list every chapter with correct number, title, and filename. |
| `STYLE_GUIDE.md` | The prose/formatting contract every chapter author follows. Subordinate to this spec. |
| `00-preface.md` | Front matter. |
| `NN-slug.md` | The 48 chapters (see manifest, §4). |
| `GLOSSARY.md` | A–Z definitions of key terms, Wikipedia-linked, each pointing to its home chapter. |
| `INDEX.md` | A–Z concepts/frameworks → chapter numbers (numbers are **chapter numbers, not pages**). |
| `_sources/` | Raw source material used for grounding (e.g. workforce-strategy text). Not shipped as chapters. |
| `spec/index.md` | **This file** — the source of truth. |
| `spec/README.md` | Pointer to this file. |

---

## 3. Chapter template (canonical structure)

Every chapter uses these headings, in this order. This is the contract the maturity model, checklist, and reviews are verified against.

1. `# Chapter N — Title`
2. **In one sentence** — a single **bold** sentence stating the chapter's thesis. (No heading; it's the first line of body.)
3. `## Why this matters in health and care` — the domain-specific stakes: safety, equity, statutory duties, public money.
4. `## Core concepts` — definitions and mental models. First mention of each key named concept is hyperlinked to its English Wikipedia article.
5. `## Best practices` — **numbered**; each item a **bold lead-in** + 2–4 sentences. This is the heart of the chapter.
6. `## Questions to discuss with your team` — **exactly three** numbered, open (non-yes/no) questions, each in **bold**, each followed by a 4–8 sentence briefing that names the real tensions, concrete angles, and what an honest answer looks like. Placed **before** the worked example. Must be workshop-ready.
7. `## In practice: a health & care example` — one concrete, realistic, fictional worked scenario (e.g. an ICS rolling out a shared care record).
8. `## Three sector lenses` — the same topic across three `###` subsections **in this order**: `### Startup`, `### Enterprise`, `### Government`. Each 3–6 sentences, showing how the practice changes with scale, funding model, risk appetite, and accountability.
9. `## Common failure modes` — anti-patterns and how to avoid them.
10. `## Maturity model` — a 4-level table with columns **Initial / Developing / Defined / Optimizing** and 3–5 rows of observable characteristics.
11. `## Checklist` — 6–12 actionable `- [ ]` items.
12. `## Key sources` — bulleted, real and verifiable; cite frameworks by name.
13. `## References` — a numbered list combining (a) Wikipedia articles for the key concepts named in the chapter and (b) authoritative sources. Format each: *title — publisher/author — URL*.

---

## 4. Chapter manifest

48 chapters in 10 parts, plus front and reference matter. Numbers, titles, and filenames are canonical — `README.md` must match exactly.

**Part I — Foundations**
1. Ways of Working in Digital Health & Care — `01-introduction.md`
2. The Operating Model — `02-operating-model.md`
3. Digital Strategy & Roadmapping — `03-digital-strategy-roadmapping.md`
4. Evidence-Driven Decisions — `04-evidence-driven-decisions.md`
5. Clinical Safety & Risk Management — `05-clinical-safety.md`
6. Information Governance, Data Protection & Cyber Security — `06-information-governance-cyber.md`
7. Data Ethics, Consent & Public Trust — `07-data-ethics-consent-trust.md`
8. Digital Inclusion & Accessibility — `08-digital-inclusion-accessibility.md`
9. Safeguarding in Digital Services — `09-safeguarding-digital-services.md`

**Part II — Managing the Flow of Work**
10. Work Intake — `10-work-intake.md`
11. Work Triage — `11-work-triage.md`
12. Work Prioritisation — `12-work-prioritisation.md`

**Part III — The Delivery Lifecycle**
13. User Research & Service Design — `13-user-research-service-design.md`
14. Patient & Citizen-Facing Digital Services — `14-patient-citizen-facing-services.md`
15. Discovery Phases — `15-discovery-phases.md`
16. Delivery Lifecycles — `16-delivery-lifecycles.md`
17. Testing & Quality Assurance — `17-testing-quality-assurance.md`
18. Service Management & Live Operations — `18-service-management-operations.md`
19. Business Continuity & Disaster Recovery — `19-business-continuity-disaster-recovery.md`

**Part IV — Technology, Architecture & Data**
20. Technical Architecture, Cloud & Legacy — `20-technical-architecture-cloud-legacy.md`
21. Interoperability & Data Standards — `21-interoperability-data-standards.md`
22. Data, Analytics & Population Health Management — `22-data-analytics-population-health.md`

**Part V — Modes of Delivery**
23. Product-Led Work — `23-product-led-work.md`
24. Project-Led Work — `24-project-led-work.md`
25. Programme-Led Work — `25-programme-led-work.md`
26. Enterprise Project Portfolio Management (EPPM) — `26-eppm.md`
27. Enterprise Resource Planning (ERP) — `27-erp.md`

**Part VI — Money, Value & Governance**
28. Financial Management & Business Cases — `28-financial-management-business-cases.md`
29. Health Economics — `29-health-economics.md`
30. Procurement & Commercial — `30-procurement-commercial.md`
31. Governance & Assurance — `31-governance-assurance.md`

**Part VII — People, Teams & Workforce**
32. Team Structures, Roles & Responsibilities — `32-team-structures-roles.md`
33. Workforce Planning — `33-workforce-planning.md`
34. Workforce Strategy — `34-workforce-strategy.md`
35. People & Organisational Development — `35-people-org-development.md`
36. Workforce Equality, Diversity & Inclusion — `36-workforce-edi.md`

**Part VIII — Change & Innovation**
37. Phasing in Innovation — `37-phasing-innovation.md`
38. Change Management — `38-change-management.md`
39. Communications & Engagement — `39-communications-engagement.md`
40. AI & Emerging Technology Governance — `40-ai-emerging-technology.md`
41. Sustainability & Net Zero — `41-sustainability-net-zero.md`
42. Research & Real-World Evaluation — `42-research-real-world-evaluation.md`

**Part IX — Partnerships & Government**
43. Collaborating with Partner Organisations — `43-collaborating-partner-organizations.md`
44. Working with Local & National Governments — `44-working-with-governments.md`

**Part X — Measurement, Improvement, Knowledge & Leadership**
45. OKRs & KPIs — `45-okrs-kpis.md`
46. Quality Improvement & Improvement Science — `46-quality-improvement.md`
47. Knowledge Management & Documentation — `47-knowledge-management.md`
48. Visibility for the CEO & Senior Leaders — `48-leadership-visibility.md`

**Front matter:** Preface — `00-preface.md`
**Reference:** Glossary — `GLOSSARY.md` · Index — `INDEX.md`

---

## 5. Voice, style & formatting rules

- **Voice:** authoritative, practical, calm. No hype. Name trade-offs honestly; evidence over assertion.
- **Person:** second person ("you", "your organisation") for guidance; third person when describing practice.
- **Acronyms:** expand every acronym on first use **in each chapter**.
- **Spelling:** UK spelling (organis*e*, prioritis*e*, programme). Exception: keep "program" only for a US-style software program; use "programme" for the delivery construct (programme management, MSP). Be consistent within a chapter.
- **Paragraphs:** 2–4 sentences. Markdown only. Use tables for comparisons and maturity models.
- **Length:** target **~2,500–3,500 words per chapter** (current chapters run ~2,900–3,400). Comprehensive, not padded.
- **Cross-references:** reference sibling chapters by number and title — e.g. "(see Chapter 19 — Change Management)".

---

## 6. Grounding & citation rules (non-negotiable)

- **Real, checkable sources only.** Never invent citations, URLs, statistics, or quotations. If unsure of a figure, describe the pattern qualitatively.
- **Wikipedia linking:** on first mention of a key named concept/framework/method, hyperlink it to its canonical English Wikipedia article, e.g. `[Cost of delay](https://en.wikipedia.org/wiki/Cost_of_delay)`. **Verify each article exists** before linking; never invent a slug. Aim for **5–12** Wikipedia links per chapter. Every inline Wikipedia link must also appear in `## References`.
- **Favoured bodies of knowledge** (use where they fit): NHS Digital Service Standard & Service Manual; GOV.UK Service Manual (GDS); NICE Evidence Standards Framework for Digital Health Technologies; MHRA; DTAC; HM Treasury Green Book / Five Case Model; Team Topologies; SAFe; PRINCE2; MSP; Management of Portfolios (MoP); Kotter's 8 steps; ADKAR (Prosci); OKRs (Doerr); Lean/Toyota; Cynefin (Snowden); Double Diamond (Design Council); Topol Review; Caldicott principles; clinical safety standards DCB0129/0160.

---

## 7. Cross-artifact consistency rules

When a chapter is added, renamed, renumbered, or its concepts change, update **all** of these in the same change so the book stays coherent:

1. `README.md` table of contents (number, title, filename, part).
2. This manifest (§4) if structure changed.
3. `GLOSSARY.md` — every newly-introduced key term gets an entry pointing to its home chapter.
4. `INDEX.md` — every key concept maps to the chapter numbers that cover it.
5. Inbound/outbound cross-references in sibling chapters.

---

## 8. Definition of done (per chapter)

A chapter is complete when all are true:

- [ ] Filename and `# Chapter N — Title` match the manifest (§4) exactly.
- [ ] All 13 template sections (§3) present, correctly ordered and named.
- [ ] Opens with a single **bold** one-sentence thesis.
- [ ] `## Best practices` is numbered with bold lead-ins.
- [ ] Exactly **three** open discussion questions, each with a 4–8 sentence briefing, placed before the worked example.
- [ ] Three sector lenses in order: Startup, Enterprise, Government.
- [ ] Maturity model is a 4-level table (Initial / Developing / Defined / Optimizing).
- [ ] Checklist has 6–12 `- [ ]` items.
- [ ] 5–12 verified Wikipedia links; every inline link also in `## References`.
- [ ] Every citation is real and checkable; no invented facts, URLs, or numbers.
- [ ] UK spelling; acronyms expanded on first use; ~2,500–3,500 words.
- [ ] `README.md`, `GLOSSARY.md`, and `INDEX.md` updated for any new terms/structure (§7).
