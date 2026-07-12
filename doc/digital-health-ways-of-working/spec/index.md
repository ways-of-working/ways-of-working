# Specification — *Ways of Working for Digital Health & Care*

**Status:** Authoritative source of truth. This document governs the book. Where a chapter, the README, the style guide, or any generated content disagrees with this spec, **this spec wins** — fix the artifact, or change the spec deliberately and then bring the artifacts into line.

**Purpose:** Enough here for any author or agent to (a) understand what the book is, (b) build or regenerate any single chapter to a consistent standard, and (c) verify the result against a checklist — without reading the other 72 files first.

---

## 1. Product definition

A practical handbook of best practices for leading and running digital delivery in health and social care organizations.

- **Working title:** *Ways of Working for Digital Health & Care*
- **Subtitle:** A practical handbook of best practices for delivering digital services in health and social care organizations
- **Format:** A set of Markdown files, one per chapter, stitched by `README.md` (the table of contents) plus reference matter (`GLOSSARY.md`, `INDEX.md`).
- **Premise (the book's spine):** *In health and care, **how** you work is a clinical-safety, equity, and public-trust issue — not merely an efficiency one.* Every chapter must ultimately serve this thesis.
- **Centre of gravity:** UK NHS and social care, with principles that transfer to any publicly-accountable, safety-critical, partnership-dependent health organization internationally.

### Audience
Chief executives and senior leaders; directors of digital and transformation; product, delivery, programme, and portfolio leads; clinical and care professionals moving into digital roles; and the operational managers who run services daily. Write for a busy director who wants to **act**.

---

## 2. Repository layout

| Path | Role |
|---|---|
| `README.md` | Reader-facing front door + table of contents. Must list every chapter with correct number, title, and filename. |
| `STYLE_GUIDE.md` | The prose/formatting contract every chapter author follows. Subordinate to this spec. |
| `00-preface.md` | Front matter. |
| `PP-CC-slug.md` | The 73 chapters. Filenames are **sortable zero-padded decimals** — a two-digit part number, a dash, a two-digit within-part number, then the slug (e.g. `01-00-introduction.md`, `03-10-emergency-preparedness-response.md`) — so a plain lexical sort lists chapters in reading order. See manifest, §4. |
| `GLOSSARY.md` | A–Z definitions of key terms, Wikipedia-linked, each pointing to its home chapter. |
| `INDEX.md` | A–Z concepts/frameworks → chapter numbers (numbers are **chapter numbers, not pages**). |
| `_sources/` | Raw source material used for grounding (e.g. workforce-strategy text). Not shipped as chapters. |
| `spec/index.md` | **This file** — the source of truth. |
| `spec/oxford-spelling.md` | The spelling standard (Oxford spelling, `en-GB-oxendict`) and its URL/citation-protection rules. |
| `spec/README.md` | Pointer to this file. |

---

## 3. Chapter template (canonical structure)

Every chapter uses these headings, in this order. This is the contract the maturity model, checklist, and reviews are verified against.

1. `# Chapter N — Title`
2. **In one sentence** — a single **bold** sentence stating the chapter's thesis. (No heading; it's the first line of body.)
3. `## Why this matters in health and care` — the domain-specific stakes: safety, equity, statutory duties, public money.
4. `## Core concepts` — definitions and mental models. First mention of each key named concept is hyperlinked to its English Wikipedia article.
5. `## Best practices` — **numbered**; each item a **bold lead-in** + 2–4 sentences. This is the heart of the chapter.
6. `## Questions to discuss with your team` — **exactly six** numbered, open (non-yes/no) questions, each in **bold**, each followed by a 4–8 sentence briefing that names the real tensions, concrete angles, and what an honest answer looks like. Placed **before** the worked example. Must be workshop-ready.
7. `## In practice: a health & care example` — one concrete, realistic, fictional worked scenario (e.g. an ICS rolling out a shared care record).
8. `## Sector lenses` — the same topic across four `###` subsections **in this order**: `### Startup`, `### Small business`, `### Enterprise`, `### Government`. Each 3–6 sentences, showing how the practice changes with scale, funding model, risk appetite, and accountability. **Startup** = a pre-revenue or early-stage digital-health company; **Small business** = an established small or independent provider/SME (e.g. a GP practice, a care home, a single-site provider, or a small health-tech supplier past the startup stage); **Enterprise** = a large, complex organization (NHS trust, ICS, big supplier); **Government** = a national or local public body.
9. `## Common failure modes` — anti-patterns and how to avoid them.
10. `## Maturity model` — a 5-level table with columns **Initiate / Develop / Standardize / Manage / Orchestrate** and 3–5 rows of observable characteristics. (Levels progress from ad hoc *Initiate*, through *Develop* and *Standardize*, to measured/governed *Manage* and continuously-optimizing *Orchestrate*.)
11. `## Checklist` — 6–12 actionable `- [ ]` items.
12. `## Key sources` — bulleted, real and verifiable; cite frameworks by name.
13. `## References` — a numbered list combining (a) Wikipedia articles for the key concepts named in the chapter and (b) authoritative sources. Format each: *title — publisher/author — URL*.

---

## 4. Chapter manifest

73 chapters in 10 parts, numbered by part and within-part (section.chapter, e.g. `1.0`, `1.1`), plus front and reference matter. Filenames are **sortable zero-padded decimals** of the form `PP-CC-slug.md` (two-digit part, dash, two-digit within-part, dash, slug), so files sort in reading order; the heading and table of contents use the natural form (`Chapter 1.0`, `Chapter 3.10`). Numbers, titles, and filenames are canonical — `README.md` must match exactly.

**Part 1 — Foundations**
1.0. Ways of Working in Digital Health & Care — `01-00-introduction.md`
1.1. The Operating Model — `01-01-operating-model.md`
1.2. Digital Strategy & Roadmapping — `01-02-digital-strategy-roadmapping.md`
1.3. Evidence-Driven Decisions — `01-03-evidence-driven-decisions.md`
1.4. Hazard Ratios — `01-04-hazard-ratios.md`
1.5. Regulation & Compliance Landscape — `01-05-regulation-compliance.md`
1.6. Clinical Safety & Risk Management — `01-06-clinical-safety.md`
1.7. Information Governance, Data Protection & Cyber Security — `01-07-information-governance-cyber.md`
1.8. Data Ethics, Consent & Public Trust — `01-08-data-ethics-consent-trust.md`
1.9. Digital Inclusion & Accessibility — `01-09-digital-inclusion-accessibility.md`
1.10. Safeguarding in Digital Services — `01-10-safeguarding-digital-services.md`

**Part 2 — Managing the Flow of Work**
2.0. Work Intake — `02-00-work-intake.md`
2.1. Work Triage — `02-01-work-triage.md`
2.2. Work Prioritization — `02-02-work-prioritization.md`

**Part 3 — The Delivery Lifecycle**
3.0. User Research & Service Design — `03-00-user-research-service-design.md`
3.1. Content Design & Health Literacy — `03-01-content-design-health-literacy.md`
3.2. Design Systems & Prototyping — `03-02-design-systems-prototyping.md`
3.3. Patient & Citizen-Facing Digital Services — `03-03-patient-citizen-facing-services.md`
3.4. Discovery Phases — `03-04-discovery-phases.md`
3.5. Delivery Lifecycles — `03-05-delivery-lifecycles.md`
3.6. DevOps & Engineering Excellence — `03-06-devops-engineering-excellence.md`
3.7. Testing & Quality Assurance — `03-07-testing-quality-assurance.md`
3.8. Service Management & Live Operations — `03-08-service-management-operations.md`
3.9. Business Continuity & Disaster Recovery — `03-09-business-continuity-disaster-recovery.md`
3.10. Emergency Preparedness, Resilience & Response — `03-10-emergency-preparedness-response.md`
3.11. Telehealth, Remote Consultation & Virtual Wards — `03-11-telehealth-virtual-wards.md`

**Part 4 — Technology, Architecture & Data**
4.0. Technical Architecture, Cloud & Legacy — `04-00-technical-architecture-cloud-legacy.md`
4.1. Platforms & Shared Services — `04-01-platforms-shared-services.md`
4.2. Identity & Access Management — `04-02-identity-access-management.md`
4.3. Interoperability & Data Standards — `04-03-interoperability-data-standards.md`
4.4. Connected Devices, IoT & Clinical Engineering — `04-04-connected-devices-iot.md`
4.5. Data, Analytics & Population Health Management — `04-05-data-analytics-population-health.md`
4.6. Electronic Patient Records & Clinical Systems — `04-06-electronic-patient-records.md`
4.7. Clinical Decision Support & Clinical Informatics — `04-07-clinical-decision-support.md`
4.8. Electronic Prescribing & Medicines Management — `04-08-electronic-prescribing-medicines.md`
4.9. Data Quality & Master Data Management — `04-09-data-quality-mdm.md`
4.10. Secure Data Environments & Research Data Access — `04-10-secure-data-environments.md`
4.11. Genomics & Precision-Medicine Data — `04-11-genomics-precision-medicine.md`

**Part 5 — Modes of Delivery**
5.0. Product-Led Work — `05-00-product-led-work.md`
5.1. Project-Led Work — `05-01-project-led-work.md`
5.2. Programme-Led Work — `05-02-programme-led-work.md`
5.3. Enterprise Project Portfolio Management (EPPM) — `05-03-eppm.md`
5.4. Enterprise Resource Planning (ERP) — `05-04-erp.md`

**Part 6 — Money, Value & Governance**
6.0. Financial Management & Business Cases — `06-00-financial-management-business-cases.md`
6.1. Health Economics — `06-01-health-economics.md`
6.2. Benefits Realization & Value Management — `06-02-benefits-realization-value.md`
6.3. Procurement & Commercial — `06-03-procurement-commercial.md`
6.4. Governance & Assurance — `06-04-governance-assurance.md`
6.5. Technology Cost Management & Cloud FinOps — `06-05-technology-cost-finops.md`
6.6. Vendor & Service Integration Management (SIAM) — `06-06-vendor-siam.md`

**Part 7 — People, Teams & Workforce**
7.0. Team Structures, Roles & Responsibilities — `07-00-team-structures-roles.md`
7.1. Agile Delivery Practices & Team Health — `07-01-agile-delivery-team-health.md`
7.2. Workforce Planning — `07-02-workforce-planning.md`
7.3. Workforce Strategy — `07-03-workforce-strategy.md`
7.4. Digital Skills & Capability Building — `07-04-digital-skills-capability.md`
7.5. People & Organizational Development — `07-05-people-org-development.md`
7.6. Workforce Equality, Diversity & Inclusion — `07-06-workforce-edi.md`

**Part 8 — Change & Innovation**
8.0. Phasing in Innovation — `08-00-phasing-innovation.md`
8.1. Change Management — `08-01-change-management.md`
8.2. Communications & Engagement — `08-02-communications-engagement.md`
8.3. Behavioural Science & Adoption — `08-03-behavioural-science-adoption.md`
8.4. AI & Emerging Technology Governance — `08-04-ai-emerging-technology.md`
8.5. Sustainability & Net Zero — `08-05-sustainability-net-zero.md`
8.6. Research & Real-World Evaluation — `08-06-research-real-world-evaluation.md`

**Part 9 — Partnerships & Government**
9.0. Collaborating with Partner Organizations — `09-00-collaborating-partner-organizations.md`
9.1. Working with Local & National Governments — `09-01-working-with-governments.md`
9.2. Global & International Digital Health — `09-02-global-international-digital-health.md`
9.3. Digital in Adult Social Care — `09-03-digital-adult-social-care.md`

**Part 10 — Measurement, Improvement, Knowledge & Leadership**
10.0. Objectives & Key Results (OKRs) — `10-00-okrs.md`
10.1. Key Performance Indicators (KPIs) — `10-01-kpis.md`
10.2. Quality Improvement & Improvement Science — `10-02-quality-improvement.md`
10.3. Knowledge Management & Documentation — `10-03-knowledge-management.md`
10.4. Visibility for the CEO & Senior Leaders — `10-04-leadership-visibility.md`

**Front matter:** Preface — `00-preface.md`
**Reference:** Glossary — `GLOSSARY.md` · Index — `INDEX.md`

## 5. Voice, style & formatting rules

- **Voice:** authoritative, practical, calm. No hype. Name trade-offs honestly; evidence over assertion.
- **Person:** second person ("you", "your organization") for guidance; third person when describing practice.
- **Acronyms:** expand every acronym on first use **in each chapter**.
- **Spelling:** **Oxford spelling** (`en-GB-oxendict`) — British English with `-ize`/`-ization` endings for the Greek-derived family (organize, prioritize, standardize, realize, optimize, digitize, recognize). Keep every other British form: `-our` (behaviour, colour), `-re` (centre, theatre), `-yse` (analyse, paralyse — **not** analyze), doubled `l` (modelling, labelled), `licence`/`defence` nouns, `programme` (use "program" only for a computer program), and `-ae/-oe` (paediatric). The full rules, exceptions, and the URL/citation-protection mechanics live in **[`spec/oxford-spelling.md`](oxford-spelling.md)** — follow it exactly. Be consistent within a chapter.
- **Paragraphs:** 2–4 sentences. Markdown only. Use tables for comparisons and maturity models.
- **Length:** target **~3,000–3,500 words of substantive prose per chapter** (most run ~3,000–4,000 words including tables and references). Deepen rather than pad; never invent filler. No chapter should fall below ~3,000 words.
- **Cross-references:** reference sibling chapters by number and title — e.g. "(see Chapter 8.1 — Change Management)". Always include the title, not just the number, so references survive renumbering.

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
- [ ] Exactly **six** open discussion questions, each with a 4–8 sentence briefing, placed before the worked example.
- [ ] Four sector lenses in order: Startup, Small business, Enterprise, Government.
- [ ] Maturity model is a 5-level table (Initiate / Develop / Standardize / Manage / Orchestrate).
- [ ] Checklist has 6–12 `- [ ]` items.
- [ ] 5–12 verified Wikipedia links; every inline link also in `## References`.
- [ ] Every citation is real and checkable; no invented facts, URLs, or numbers.
- [ ] UK spelling; acronyms expanded on first use; ~2,500–3,500 words.
- [ ] `README.md`, `GLOSSARY.md`, and `INDEX.md` updated for any new terms/structure (§7).

---

## 9. How to author or regenerate a chapter

A chapter can be written from scratch, regenerated, or deepened by a human or an agent using only this spec plus the chapter's manifest entry. The workflow:

1. **Fix the scope.** Read the manifest (§4) entry — number, title, filename, part — and the neighbouring chapters so you know where the boundaries lie and what to cross-reference rather than repeat. A chapter earns its place by covering what no other chapter owns; if it overlaps a sibling, narrow it or deepen the sibling instead (§13).
2. **Research and verify sources first.** Gather real, current sources and **verify every Wikipedia article exists** before you link it (a quick check per slug). Never link a guessed slug; if no good article exists, name the concept in plain text and cite an authoritative source in `## References` instead.
3. **Draft to the template.** Follow §3 exactly — all thirteen sections, in order, with the correct headings. Open with the bold one-sentence thesis; make `## Best practices` the substantive heart; write exactly six workshop-ready questions before the worked example; give the four sector lenses in the fixed order.
4. **Hit the length by depth.** Reach the §5 length target by adding real substance — more best practices, richer core concepts, a fuller worked example — never filler. If a chapter is short, add practices and concepts a practitioner would actually use.
5. **Self-check against the definition of done (§8)** and update the reference matter (§7) for any new terms or structure.

**Authoring at scale.** When many chapters are created or renumbered at once, one writer per chapter — each editing a *distinct* file — is safe and fast; never let two writers touch the same file concurrently. Give every writer the full final manifest so cross-references resolve to the right numbers, and **complete any renumbering before writing new chapters** so numbers are final when authors cite them. Transient failures happen: check what actually reached disk and re-run only what is genuinely missing, rather than blindly repeating work.

## 10. Review & quality gates

Before a chapter or a change is considered complete, it passes four gates. Automate them wherever possible; a failure in any gate blocks "done".

- **Structural gate.** Thirteen sections present and correctly named; a bold one-sentence thesis; numbered best practices with bold lead-ins; exactly six discussion questions before the example; four sector lenses in the order Startup, Small business, Enterprise, Government; a five-column maturity table (Initiate / Develop / Standardize / Manage / Orchestrate); a checklist of 6–12 `- [ ]` items.
- **Link gate.** Every inline Wikipedia link resolves to a real article and also appears in `## References`; no invented or guessed slugs; 5–12 links per chapter.
- **Source gate.** No invented citations, URLs, statistics, or quotations. Figures are either real and checkable or described qualitatively.
- **Consistency gate.** The `# Chapter N — Title` heading matches the filename and the manifest; every `Chapter N — Title` cross-reference names the chapter that actually holds that number; UK spelling; acronyms expanded on first use.

## 11. Structural change & renumbering procedure

Adding, removing, splitting, merging, or reordering chapters is the highest-risk change in the book, because chapter numbers appear in filenames, headings, cross-references, the index, and the glossary. Follow this order every time:

1. **Decide the final manifest first** — the complete target list of numbers, titles, and filenames — before touching any file.
2. **Back up.** Untracked files are not protected by git; copy the directory somewhere safe before renumbering.
3. **Remap in one pass.** Rewrite in-prose chapter references by mapping each chapter label through a single lookup applied once, so a shorter label can never partially match a longer one. Rename files two-phase (to a temporary name, then to the final name) to avoid collisions when numbers shift.
4. **Remap the reference matter.** Update the chapter-number lists in `INDEX.md` and the "See Chapter N" pointers in `GLOSSARY.md` through the same map.
5. **Rebuild** `README.md` and this manifest (§4) to match, then re-run the consistency gate (§10). Fix any reference whose title no longer matches its number, including pre-existing ones the renumber exposes.

## 12. Reference-matter conventions

- **`GLOSSARY.md`** — one **bold term**, a plain-English definition, an optional *verified* Wikipedia link, and a "See Chapter N" pointer to the term's home chapter. Entries are alphabetical within `## A … ## Z` letter sections. When a term gains a dedicated home chapter, repoint it there.
- **`INDEX.md`** — entries of the form `**Concept** — n, m, …` where the numbers are **chapter numbers, not pages**, listed ascending and de-duplicated. Include the concept's home chapter plus every chapter that materially covers it. Keep both files in step with the manifest in the same change (§7).

## 13. Book-level anti-patterns to avoid

- **Inventing sources or figures** to hit a target or sound authoritative — describe the pattern qualitatively instead.
- **Drifting from the template** "because this topic is different" — the template is the contract that makes the book navigable and self-assessable.
- **Number-only cross-references** that rot the moment chapters are renumbered — always carry the title.
- **Silent overlap** — a new chapter that largely repeats an existing one. Prefer deepening the existing chapter (adding best practices or a subsection) over adding a thin new chapter.
- **Half-renumbering** — changing numbers without updating `README.md`, `GLOSSARY.md`, and `INDEX.md` in the same change, leaving the book internally inconsistent.

## 14. Versioning & change control

Treat structural changes — chapters added, removed, split, merged, renumbered, or reorganized into new parts — as versioned events. Make each such change as a single, self-contained commit that updates **every** artifact in §7 together, so the repository is never left half-renumbered between commits. Where the repository and this manifest disagree, the manifest expresses the intended structure and the repository must be corrected to match it, not the other way around. Keep this spec current in the same change: it is only a source of truth if it describes the book as it actually is.


## 15. Non-goals & scope boundaries

To keep the book coherent, some things are deliberately out of scope:

- **Not a clinical guideline or a product manual.** The book describes *how to work* — the operating disciplines of digital delivery — not clinical protocols, condition-specific pathways, or step-by-step instructions for a particular product or platform.
- **Not vendor or tool documentation.** Name frameworks and standards, but do not become a how-to for a specific commercial product; those date quickly and belong elsewhere.
- **Not a legal or regulatory authority.** The book explains the terrain (see Chapter 1.5 — Regulation & Compliance Landscape) and points to primary sources, but readers must consult current statute, regulator guidance, and their own governance for binding decisions.
- **UK-centred, not UK-only.** The centre of gravity is the NHS and UK social care; internationally-transferable principles are welcome (and Chapter 9.2 makes the global case), but the book does not attempt to document every jurisdiction.

When a proposed addition falls into a non-goal, prefer a short signpost and an authoritative external reference over new chapters, so the book stays focused on ways of working.

