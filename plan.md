# Improvement Plan — Ways of Working repository

**Date:** 2026-07-11
**Scope:** The whole repository — the general Ways of Working collection (root `README.md` + `doc/*` articles) and the spec-driven book *Ways of Working for Digital Health & Care* (`doc/digital-health-ways-of-working/`).
**Companion file:** `tasks.md` holds the executable task list derived from this plan. An agent (e.g. Claude Opus) should read this plan first for context, then work through `tasks.md`.

---

## 1. Current state (grounded findings)

What exists and works:

- A mature 64-chapter book at `doc/digital-health-ways-of-working/` with an authoritative spec (`spec/index.md`), style guide, glossary, per-chapter template, quality gates, and a definition of done. All chapters meet the ~3,000-word floor.
- A long-standing tips collection: root `README.md` (100+ teamwork tips) plus ~55 article directories under `doc/`.
- `CITATION.cff`, `CODE_OF_CONDUCT.md`, `cspell.json` (nearly empty), `llms.txt` (a ~198 KB concatenated content dump).

Concrete defects and gaps found by inspection:

1. **`doc/digital-health-ways-of-working/INDEX.md` is empty (0 bytes)** — the spec (§2, §12) requires an A–Z concept → chapter-number index. This is the single clearest defect.
2. **No automation at all.** The spec §10 says "Automate them wherever possible" for the four quality gates (structural, link, source, consistency), but there are no scripts, no Makefile, no `.github/` directory, no CI. Every gate is currently manual.
3. **The root `README.md` does not link to the book.** The repository's largest artifact is invisible from its front door. The README's HTML comment header says "updated 2022-07-27"; its Resources list has drifted from `doc/` contents.
4. **`llms.txt` does not follow the llms.txt convention** (it should be a curated Markdown index with links, not a flat concatenation) and does not mention the book.
5. **No CONTRIBUTING.md, no per-file licence clarity in `CITATION.cff` (`license: See license file` but no obvious LICENSE file at root), no repository description of how the two halves (tips collection vs. book) relate.**
6. **No reader tooling:** no way to build the book as a single document, EPUB/PDF, or website; no prev/next navigation inside chapters; no reading paths for different roles.
7. **No tutorials or worked templates:** the book has strong in-chapter examples, but the repo offers no facilitation guides (e.g. "run a working-agreements workshop"), no fill-in templates (team charter, working agreement, decision record), and no self-assessment walkthrough that uses the maturity models.
8. **`cspell.json` lists 8 words** and no dictionary strategy for UK spelling or NHS/health terminology, so a spell-check pass would drown in false positives.

## 2. Goals

1. **Trustworthiness at scale:** every spec quality gate is machine-checked, so the 64-chapter book stays internally consistent as it grows.
2. **Readability and reach:** the book can be read as a website, a single file, an EPUB/PDF — and is discoverable from the repo front door and from `llms.txt`.
3. **Actionability:** readers can go from reading to doing via tutorials, facilitation guides, templates, and self-assessment tooling.
4. **Coherence:** the tips collection and the book are presented as one repository with a clear map.

## 3. Workstreams

### Workstream A — Validation & quality automation (capabilities)

Build a validation toolchain that mechanises the spec's four gates. Prefer a single dependency-light approach: Python 3 standard library (or Node if preferred) scripts in a new `tools/` directory, orchestrated by a `Makefile`, run in GitHub Actions on every push/PR.

- **Structural gate checker:** for each `PP-CC-*.md`, verify the 13 template sections exist in order with exact headings; bold one-sentence thesis; numbered best practices with bold lead-ins; exactly three discussion questions before the worked example; sector lenses in Startup/Enterprise/Government order; 4-column maturity table; 6–12 `- [ ]` checklist items.
- **Consistency gate checker:** filename ↔ `# Chapter N — Title` heading ↔ spec §4 manifest ↔ `README.md` ToC all agree; every `Chapter N — Title` cross-reference in prose names the chapter that actually holds that number; word-count floor (~3,000 substantive words) enforced with a report, not a hard fail.
- **Link gate checker:** extract all Wikipedia links; verify each inline link also appears in `## References`; count 5–12 per chapter; optionally verify slugs resolve via HTTP (behind a flag, cached, so CI stays fast/offline-safe).
- **Reference-matter checker:** every GLOSSARY entry's "See Chapter N" points at a real chapter; INDEX entries map to real chapter numbers; alphabetical ordering holds.
- **Repo-wide link check:** relative links in root `README.md` and `doc/*/index.md` resolve to real paths (this will catch the existing broken `how-to-send-progress-updates` link style drift).
- **Spelling:** grow `cspell.json` with UK-English config and a project dictionary (NHS, DTAC, Caldicott, interoperability vocab, proper nouns); wire into CI as a warning first, gate later.
- **CI:** `.github/workflows/ci.yml` running `make check` (all of the above). Badge in root README.

### Workstream B — Publishing & reader functionality

- **Single-file build:** `make book` concatenates preface + chapters in manifest order into `dist/ways-of-working-for-digital-health-and-care.md` (gitignored), with a generated title page and ToC.
- **EPUB/PDF:** optional `make epub` / `make pdf` via pandoc if available; degrade gracefully with a clear message if not installed.
- **Website:** publish the book (and ideally the whole repo) with mdBook or MkDocs Material to GitHub Pages. Generate `SUMMARY.md`/`mkdocs.yml` nav from the spec manifest so the site can never drift from the book. (Decision for executor: pick mdBook for zero-Python or MkDocS Material for better search/themes; either is acceptable — document the choice.)
- **In-chapter navigation:** add a small, script-generated prev/next footer line to every chapter (`◀ Chapter 1.3 … | Contents | Chapter 1.5 … ▶`), maintained by a `make nav` target so it never rots.
- **Regenerate `llms.txt`** to follow the llms.txt convention: short project summary, then curated links (book README, spec, each part, glossary, key articles). Optionally emit `llms-full.txt` for the full-content variant.

### Workstream C — Book content completion & deepening

- **Rebuild `INDEX.md`** (the empty file): A–Z concepts/frameworks → ascending, de-duplicated chapter numbers, per spec §12. Generate a first pass by scanning chapter headings, bold lead-ins, and Wikipedia-linked terms; then curate.
- **Glossary audit:** every chapter's key named concepts have a GLOSSARY entry pointing at the right home chapter; entries alphabetical within letter sections.
- **Cross-reference densification:** each chapter should point to its natural siblings ("see Chapter 8.1 — Change Management"); audit for chapters with zero inbound or outbound references and add where genuinely useful.
- **Preface expansion:** `00-preface.md` is 577 words vs. 3,000+ for chapters — deliberate, but it should at least explain the book's origin, how it was produced (spec-driven), reading paths (see Workstream E), and how to contribute.
- **New reference matter:** an `ABBREVIATIONS.md` (the sector is acronym-dense) and a `READING-PATHS.md` (role-based: CEO, digital director, delivery lead, clinician-in-digital, social-care lead).
- **Currency pass:** spec-favoured frameworks evolve (NHS bodies reorganise, DTAC versions change); one chapter-by-chapter pass confirming named organisations/standards are current as of 2026, adjusting qualitatively (never inventing figures).

### Workstream D — Repository-wide documentation

- **Rewrite root `README.md`:** lead with a map of the repo's two halves — (1) the Ways of Working tips collection, (2) the Digital Health & Care book — then the existing tips content, reorganised. Fix drifted/broken links (e.g. `how-to-send-progress-updates-by-slava-akhmechet` missing the `doc/` prefix). Refresh the stale metadata comment. Add CI badge and site link once A/B land.
- **`CONTRIBUTING.md`:** how to propose a tip, how to author/regenerate a book chapter (point at spec §9), how to run `make check`.
- **LICENSE clarity:** `CITATION.cff` says "See license file" but there is no LICENSE at root — add one (owner's choice; default suggestion: content under CC-BY-SA-4.0 or the repository's historical licence if one exists in another repo of the author's set) and update `CITATION.cff` (also update its `abstract` to a real description, and consider `type: dataset`→ keep `software` or change to `document`).
- **Article index page:** generate `doc/README.md` listing every article directory with a one-line description, so `doc/` is navigable without the root README.

### Workstream E — Tutorials (new)

A new `tutorials/` directory (or `doc/tutorials/`), each tutorial a step-by-step guide with time-boxes, prerequisites, and expected outputs:

1. **Run a working-agreements workshop** — 90-minute agenda using the repo's tips + Esther Derby/Jane Haskell articles; produces a signed team working agreement.
2. **Self-assess with the maturity models** — how a team scores itself against a chapter's 4-level maturity table, picks one "Developing → Defined" move, and re-assesses in 90 days.
3. **Adopt the book in an organisation** — a 6-week rollout: pick reading paths per role, run chapter-based discussion sessions using the "Questions to discuss with your team" (they are already workshop-ready by spec §3.6), track via the checklists.
4. **Facilitate a chapter discussion session** — a repeatable 60-minute format built on any chapter's three questions.
5. **Author or regenerate a chapter with an AI agent** — a practical walk-through of spec §9 (fix scope → verify sources → draft to template → hit length by depth → self-check), including how to run the Workstream A validators.

### Workstream F — Examples & templates (new)

A new `templates/` directory of fill-in Markdown artifacts, each paired with one completed fictional example:

1. **Team working agreement** (template + a completed example for a fictional NHS-adjacent product team).
2. **Team charter / "people & projects" documents** (formalising what root README's orientation section describes).
3. **Decision record** (lightweight ADR-style, matched to the book's evidence-driven-decisions chapter).
4. **Maturity self-assessment scorecard** (a table covering all 64 chapters at one row each; teams mark Initial/Developing/Defined/Optimising and a next action).
5. **Working-agreement retrospective agenda** (feeds Tutorial 1).
6. **Chapter checklist extraction:** `make checklists` generates a single `dist/checklists.md` compiling all 64 chapter checklists — instantly useful as an operational audit document.

### Workstream G — Maintenance & hygiene

- `.gitignore` for `dist/`; `.editorconfig`; consistent heading style in older `doc/*` articles (defer heavy edits — content is historical/quoted material and should not be rewritten, only navigation-fixed).
- Fix `cspell.json` as per Workstream A.
- Decide and document a versioning scheme for the book (the spec §14 calls structural changes "versioned events" but defines no version identifier — add `VERSION` or a `## Changelog` in the spec).

## 4. Priorities & phasing

| Phase | Contents | Rationale |
|---|---|---|
| **1 — Fix defects** | C1 (INDEX.md), D1 (root README links to book), B5 (llms.txt), D3 (LICENSE/CITATION) | Visible defects; cheap; unblock nothing else but embarrass the repo now |
| **2 — Automation** | All of A, G | Everything after this is protected by CI; do before mass content edits |
| **3 — Publishing** | B1–B4 | Depends on A's manifest-parsing code |
| **4 — Content** | C2–C6, D2, D4 | Safe once validators run in CI |
| **5 — Tutorials & templates** | All of E, F | New value; independent, can parallelise |

Dependencies: A before C's mass edits (validators catch regressions); A's manifest parser is reused by B's build and nav generation; F4 and F6 depend on A's chapter parser.

## 5. Success criteria

- `make check` passes clean in CI on `main`; any spec-gate violation fails a PR.
- `INDEX.md` is populated and machine-verified against chapters.
- The book is readable as a website and a single file; root README front-doors both halves of the repo.
- At least 5 tutorials and 6 templates exist, each self-contained and immediately usable by a team.
- `llms.txt` conforms to the convention and covers the whole repo.

## 6. Non-goals (for this plan)

- Rewriting the historical/quoted articles under `doc/*` (they are source material; fix only navigation and typos).
- Renumbering or restructuring the book's 64-chapter manifest (spec §11 makes this high-risk; nothing found requires it).
- Translations, print typesetting, or paid distribution.
