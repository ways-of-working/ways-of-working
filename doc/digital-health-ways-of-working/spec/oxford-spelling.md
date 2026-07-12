# Spelling standard — Oxford spelling (`en-GB-oxendict`)

**Status:** Authoritative for the whole book. Every chapter and every reference file follows the spelling rules on this page. Where any artifact disagrees, this page and [`spec/index.md`](index.md) win.

This book is written in **Oxford spelling** — British English that uses the `-ize`/`-ization` endings for the relevant Greek‑derived words, while keeping every other British convention. It is also called *Oxford English Dictionary spelling* or *Oxford style*, and it is the spelling implied by the IETF language tag **`en-GB-oxendict`**. It reflects that the `-ize` ending "corresponds more closely to the Greek etymon, ‑ίζω (‑ízō)."

## Why Oxford spelling

Oxford spelling is the official or de facto standard in the style guides of the international organizations of the United Nations System — including the **World Health Organization**, the **International Telecommunication Union**, the **International Labour Organization**, the **World Food Programme**, the **International Court of Justice**, and **UNESCO** — and of all UN treaties and declarations, such as the Universal Declaration of Human Rights.

Other international bodies that adhere to it include the **International Organization for Standardization (ISO)**, the **International Electrotechnical Commission (IEC)**, the **World Trade Organization (WTO)**, the **North Atlantic Treaty Organization (NATO)**, the **International Atomic Energy Agency (IAEA)**, **Interpol**, the **International Committee of the Red Cross (ICRC)**, the **World Wide Fund for Nature (WWF)**, **Amnesty International**, the **World Economic Forum (WEF)**, and the **Global Biodiversity Information Facility (GBIF)**. It is also the house style of academic publishers and journals including *Nature*, the *Philosophical Transactions of the Royal Society*, Oxford University Press, and Cambridge University Press.

For a book whose centre of gravity is the UK NHS and social care but whose principles are internationally transferable — and which cites WHO, ISO/IEC and UN‑system sources throughout — Oxford spelling is the natural register: unmistakably British, yet aligned with the global standards bodies the book leans on.

## The rule

- **Use `-ize` / `-ization` / `-izable`** for the Greek‑derived family: *organize, organization, prioritize, prioritization, standardize, standardization, realize, realization, recognize, recognizable, optimize, digitize, maximize, minimize, categorize, characterize, summarize, emphasize, utilize, harmonize, normalize, rationalize, anonymize, pseudonymize, randomize, authorize, centralize, specialize, industrialize, operationalize, incentivize, marginalize, scrutinize, criticize* and the like (roughly 200 verbs and their derivatives).

## Exceptions that keep `-ise` / `-yse`

Oxford spelling is **not** a blanket "‑ise → ‑ize". These words keep `-ise`/`-yse` because they are **not** formed from the Greek `-izo` suffix — the ending is part of the root, or the word derives from another stem (e.g. Greek *lysis*):

> **‑yse (from *lysis*):** analyse, analysed, analysing, analyser; paralyse; catalyse; dialyse.
>
> **‑ise as part of the root:** advertise, advise, apprise, arise, chastise, circumcise, comprise, compromise, demise, despise, devise, disguise, enterprise, excise, exercise, franchise (and disenfranchise), improvise, incise, merchandise, premise, prise, promise, raise, revise, rise, supervise, surprise, televise, wise.

When in doubt, check whether the root drops cleanly to a Greek `‑iz` verb (organ‑ize ✓) or whether the `‑ise` is inseparable from the stem (comprom‑ise → not *‑ize*).

## British features that are KEPT (Oxford spelling is not American)

Oxford spelling changes **only** the `‑ize` family above. Everything else stays British:

| Feature | Keep (Oxford = British) | Not this (American) |
|---|---|---|
| `-our` | colour, behaviour, favour, labour, honour, rigour, neighbour | color, behavior … |
| `-re` | centre, theatre, metre, litre, fibre, calibre | center, theater … |
| `-yse` | analyse, paralyse, catalyse | analyze … |
| Doubled `l` | modelling, modelled, labelled, travelling, cancelled, counselling, signalling, levelling | modeling, labeled … |
| Noun/verb `-ce`/`-se` | licence (noun) / license (verb); defence; offence; practise (verb) / practice (noun) | license, defense, practice (all) |
| `programme` | programme (initiative/broadcast); *program* only for a computer program | program (all) |
| `-ae`/`-oe` | paediatric, haematology, anaesthetic, foetal, manoeuvre, encyclopaedia | pediatric, hematology … |
| Misc | catalogue, dialogue, ageing, judgement, acknowledgement, enrolment, fulfilment, skilful | catalog, aging, judgment … |

## Applying it to this repository (non‑negotiable mechanics)

When converting or authoring, change spelling **only** in body prose and the book's own headings, titles and internal cross‑reference text. **Never** alter the following — they are copied verbatim:

1. **URLs and link targets.** Wikipedia article slugs and other URLs may contain British `‑isation` spellings (e.g. `…/wiki/Benefits_realisation_management`). Changing them **breaks the link**. Protect every `http(s)://…` and every `](…)` target.
2. **Formal titles, journal‑article titles and reference citations.** Leave the `## References` and `## Key sources` sections, and any cited document/report/programme title, exactly as published — e.g. the NHS **"Digitising Social Care"** programme keeps its spelling; the Wikipedia display text of an inline link keeps the article's own spelling.
3. **Inline code and file paths.** Anything in `` `backticks` `` — including chapter filenames such as `03-10-emergency-preparedness-response.md` — is left unchanged during prose conversion. When a filename genuinely needs to change (see below), rename the file and update every pointer in the same change.

**Filenames follow Oxford spelling too.** Chapter slugs use the same `‑ize`/`‑ization` forms as the prose — e.g. `02-02-work-prioritization.md` and `06-02-benefits-realization-value.md`, not the British `‑isation`. Renaming a slug is a structural change: rename the file (with `git mv`) and update every pointer — the `README.md` table of contents, the manifest in `spec/index.md` (§4) and `spec/README.md`, and any inbound links — in the same commit, then re‑run the consistency gate. The slug still need not letter‑match the chapter title (the book lets `03-10-…` differ from "Chapter 3.10"); Oxford spelling only governs the spelling of the words that do appear in the slug.

## Definition of done (spelling)

- [ ] No convertible Greek‑family `‑ise`/`‑isation` word remains in body prose (organize/prioritize/standardize/realize/optimize/… all `‑ize`).
- [ ] Every `‑yse` word (analyse, paralyse) and every root `‑ise` word (exercise, comprise, enterprise, promise, premise, surprise …) is untouched.
- [ ] All British `‑our`/`‑re`/doubled‑`l`/`programme`/`licence`/`‑ae‑oe` spellings are intact.
- [ ] Every URL and link target is byte‑for‑byte identical to before conversion.
- [ ] `## References` and `## Key sources` sections and cited titles are unchanged.
