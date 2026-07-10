# Chapter 1.0 — Ways of Working in Digital Health & Care

**In one sentence:** *Ways of working* are the deliberate, shared habits — how you organise teams, make decisions, manage risk, and deliver value — that let a health and care organisation turn intent into safe, equitable, evidence-based outcomes for patients and citizens.

## Why this matters in health and care

Every organisation has ways of working, whether chosen or inherited. In digital health and care, the ones you inherit are usually wrong for the job: they were built for construction-style projects with fixed scope, not for adaptive services that touch clinical safety, statutory duty, and public money. Getting them right is not a back-office nicety; it is the difference between a shared care record that clinicians trust and one that sits unused.

Health and care is distinctive in ways that shape every practice in this book. **Safety** is non-negotiable — a defect in a digital service can harm a patient, so clinical risk management (see Chapter 1.6 — Clinical Safety & Risk Management) is woven through delivery, not bolted on. **Equity** matters because a service that works only for the digitally confident widens [health inequalities](https://en.wikipedia.org/wiki/Health_equity); the Core20PLUS5 populations and people with limited digital access must be designed for, not designed out. **Statutory duties** — the NHS commitment to comprehensive care, data-protection law, the duty of confidentiality — constrain what you may do with data and how you must consult. **Public money** demands proportionate spend control and demonstrable value. And almost nothing is delivered by one body alone: **partnership** across integrated care systems (ICS), local authorities, social care providers, and suppliers is the default operating condition.

These four pressures — safety, equity, duty, money — are why you cannot simply copy a consumer-tech playbook. You need ways of working that are agile *and* accountable, fast *and* safe, user-centred *and* population-fair.

## Core concepts

**Ways of working** operate at three levels. At the **team** level they are the daily practices: stand-ups, user research, iterative delivery, pairing. At the **organisational** level they are the operating model — how strategy becomes value streams, capabilities, funding, and decision rights (see Chapter 1.1 — The Operating Model). At the **system** level they are how independent organisations align: shared standards, interoperability, and common governance across an ICS. This book moves deliberately across all three.

**[User-centred design](https://en.wikipedia.org/wiki/User-centered_design)** means starting from the needs of the people who use a service — patients, carers, clinicians, administrators — rather than from an assumed solution. The UK [Government Digital Service](https://en.wikipedia.org/wiki/Government_Digital_Service) (GDS) and the NHS codified this in service standards: understand users and their needs before you build, and keep testing with real users throughout.

**[Agile, iterative delivery](https://en.wikipedia.org/wiki/Agile_software_development)** means getting a working service in front of real users early, learning, and adapting — rather than specifying everything up front. The NHS digital service manual is explicit that agile, user-centred ways of working reduce the risk of building the wrong thing. Agile here is a risk-management strategy as much as a delivery method.

**[Multidisciplinary teams (MDTs)](https://en.wikipedia.org/wiki/Interdisciplinarity)** bring together, in one empowered team, the mix of skills a service needs: product and delivery management, user research and design, engineering, clinical and information-governance expertise, and operational knowledge. The NHS service standard requires teams that include multidisciplinary skills and perspectives — including access to specialist clinical, legal, or policy input. The MDT is the atom of digital delivery; most failures trace back to a missing discipline at the table.

**Product over project.** A project has a start, an end, and a hand-off; a [product](https://en.wikipedia.org/wiki/Product_management) is funded and stewarded for its whole life. The shift from project to product thinking (see Chapter 1.1 and Chapter 5.0 — Product-Led Work) changes funding, teams, and accountability, and it fits health services — which are long-lived and continuously evolving — far better than one-off projects do.

## Best practices

1. **Start from user needs, evidenced by research.** Before committing to a build, understand who the users are, what they are trying to do, and where the current service fails them. Fund a discovery (see Chapter 3.4 — Discovery Phases) and treat "we assumed" as a red flag. User needs, not internal preferences, are the anchor for every later decision.

2. **Build multidisciplinary, empowered, and stable teams.** Assemble the full mix of skills — including clinical safety and information governance — and give the team authority to decide within clear guardrails. Keep teams together around a service rather than disbanding them at each project boundary; stable teams accumulate the domain and safety knowledge that health services demand.

3. **Work in the open and [iterate in small steps](https://en.wikipedia.org/wiki/Iterative_and_incremental_development).** Ship thin slices, measure, and adjust. Small, frequent releases are safer than big-bang launches because problems surface while they are still small, and they let clinical-safety and information-governance review keep pace with change rather than becoming a gate at the end.

4. **Make safety and equity first-class from day one.** Run clinical risk management (DCB0129/DCB0160) and equality/health-inequalities analysis alongside delivery, not as end-stage sign-offs. Ask early who could be excluded or harmed, and design for the hardest cases — assisted digital routes, accessibility ([WCAG](https://en.wikipedia.org/wiki/Web_Content_Accessibility_Guidelines)), and offline fallbacks.

5. **Decide with evidence, and record the decision.** Distinguish clinical evidence (does it work and is it safe?) from delivery evidence (are we building it well and being used?), and keep a lightweight decision log so the reasoning survives staff turnover (see Chapter 1.3 — Evidence-Driven Decisions). Evidence beats the highest-paid person's opinion.

6. **Design for interoperability and reuse.** Health and care data must flow safely between organisations; build to open standards ([HL7 FHIR](https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources), [SNOMED CT](https://en.wikipedia.org/wiki/SNOMED_CT)) and reuse platforms rather than re-inventing them (see Chapter 1.1's "thinnest viable platform" and Chapter 4.3 — Interoperability & Data Standards). A service that cannot share data is a silo waiting to become a risk.

7. **Govern proportionately.** Match the weight of assurance to the level of risk. High-risk clinical changes deserve deep scrutiny; low-risk content changes should not wait weeks for a board. Proportionate governance keeps you both safe and fast.

8. **Work in the open.** Share plans, decisions, roadmaps and — where safe — code, so partners, clinicians and the public can see how and why choices are made. Openness builds trust, cuts duplication across a fragmented system, and invites challenge before mistakes harden into live services. In health and care, being transparent about what a service does with data, and why, is itself a trust and safety practice.

9. **Design for the long term and for handover.** Digital services in health outlive the teams and contracts that build them, so capture decisions, avoid undocumented "hero" knowledge, and design for the people who will run and change the service for years (see Chapter 10.3 — Knowledge Management & Documentation). Treat sustainability — of the team, the technology and the funding model — as a first-class constraint, not an afterthought.

## Questions to discuss with your team

1. **Where are our current ways of working inherited rather than chosen, and which inherited habit is costing us the most in safety, equity, or wasted spend?**
   This question forces an honest audit of the practices no one decided but everyone follows — fixed-scope programme funding, disband-and-rebuild project teams, governance consulted only at go-live. It matters because inherited habits are usually invisible until named, and in health and care they carry real cost: a shared record clinicians do not trust, a service that excludes Core20PLUS5 populations, or a rebuild of the same login plumbing on public money. The tension to debate is that inherited ways often feel safe precisely because they are familiar and auditable, so retiring them looks like taking on risk rather than removing it. Ground the discussion in concrete artefacts — look at your last three business cases, your team turnover between projects, and when clinical safety was first engaged — rather than trading opinions. A good answer names one or two specific habits with evidence of their cost, distinguishes the ones worth keeping from the ones actively harming outcomes, and commits to a change that a senior leader will be accountable for.

2. **Do our teams genuinely have the full multidisciplinary skill mix — including clinical safety and information governance — sitting inside the team, or are those disciplines still bolted on as end-stage gates?**
   The chapter argues the MDT is the atom of digital delivery and that most failures trace to a missing discipline at the table, so this question tests whether that principle is real in your organisation or merely aspirational. It matters because a clinical safety officer or Caldicott Guardian engaged only at go-live forces either rework or unsafe shortcuts, whereas one embedded from week one keeps a live hazard log that paces delivery. The trade-off worth surfacing is cost and scarcity: specialist clinical, legal, and IG time is genuinely limited, so "embed everyone in every team" collides with real resourcing constraints, and the team must decide where fractional or shared roles are acceptable and where they are not. Look at a current service and map who is actually in the standing team versus who is consulted as an external sign-off, and check whether the team has authority to decide within guardrails or must escalate constantly. An honest, good answer is specific about which disciplines are missing or borrowed, acknowledges the resourcing tension frankly, and proposes a concrete model — full-time, fractional, or on-call — for closing the gap without pretending scarcity away.

3. **When have we treated a digital service as a project with a hand-off rather than a product stewarded for its whole life, and what did that cost us in lost domain and safety knowledge?**
   Product-over-project is one of the chapter's load-bearing shifts, and this question makes the team confront where they still fund and staff for closure rather than continuity. It matters because health services are long-lived and continuously evolving; a team disbanded at the project boundary takes with it exactly the accumulated clinical and operational knowledge that keeps a service safe, and "pilot purgatory" is the recurring symptom. The real tension is financial and structural: product funding requires standing budgets and challenges the annual-bid, time-boxed model that finance and governance are built around, so this is as much a conversation about money and accountability as about delivery. Consider a specific service that went through a hand-off — trace what happened to its hazard log, its user research, and its team — and weigh that against the discipline product funding demands. A good answer identifies a concrete case, quantifies or at least characterises the knowledge lost, and is candid about which organisational barriers (funding cycles, resourcing rules, governance structures) would have to move for persistent product teams to become the norm.

## In practice: a health & care example

An integrated care system wants to give clinicians across three acute trusts, community services, and local authority social care a **shared care record**. The old way would commission a fixed-scope programme, specify every screen up front, and integrate late.

Instead the ICS forms a multidisciplinary team: a product manager, delivery manager, user researcher, interaction designer, two engineers, a clinical safety officer, and an information governance lead, with access to a caldicott guardian and a social-care practitioner. They run an eight-week discovery, observing how a district nurse, an A&E consultant, and a social worker actually try to find information today. They discover the real pain is not "no data" but "data they cannot trust the currency of."

The team ships a narrow alpha: read-only access to allergies, medications, and current care-plan status for one clinical pathway, with a visible "last updated" stamp. Clinical safety runs in parallel; a hazard log is maintained from week one. They measure whether clinicians stop phoning other teams to confirm information. Only once that thin slice proves valuable and safe do they widen the record — funded as a continuing product, not a closed project.

## Three sector lenses

The same four pressures — safety, equity, duty, money — bear on every organisation, but the ways of working that answer them shift with scale, funding, and accountability.

### Startup

A small digital-health company lives or dies by focus, so its ways of working are lean by necessity: one multidisciplinary team, flat decision-making, and daily contact with users. The constraint is runway, not headcount rules, so discovery is measured in weeks and evidence is gathered cheaply — a handful of clinical interviews, a clickable prototype, an honest hazard log kept by a fractional clinical safety officer. The danger is skipping safety and information-governance rigour to hit an investor milestone; the discipline that survives scrutiny is treating DCB0129 and a data-protection impact assessment as entry criteria for a pilot, not paperwork deferred until a trust asks. Interoperability from day one (FHIR, SNOMED CT) is also a commercial asset, because a startup that cannot exchange data will never clear NHS procurement.

### Enterprise

An NHS trust or ICS has the opposite problem: abundant process and fragmented ownership. Ways of working here are as much about *unlearning* — retiring fixed-scope programme habits, standing down disband-and-rebuild project teams — as about adopting new practices. Accountability is formal and personal (a senior responsible owner, a Caldicott Guardian, board-level clinical safety sign-off), so the win is embedding those roles inside the delivery team rather than bolting them on as gates. A large health-tech or pharma supplier faces the mirror image: strong engineering maturity but distance from frontline clinical reality, which multidisciplinary teams with real clinician time exist to close.

### Government

A national or local public body — NHS England, DHSC, UKHSA, a local authority — sets the standards everyone else works to, so its ways of working ripple outward. Its accountability is to Parliament and the public, which raises the bar on transparency, spend control, and equity: a service standard, a published assurance route, and Core20PLUS5 duties are instruments of that accountability, not optional extras. The risk at this scale is designing centrally for an average citizen who does not exist and mandating a solution before understanding local need. The corrective is the same user-centred, iterative discipline as everywhere else, applied with a bias to setting open standards and reusable platforms that federated organisations can build on — governing the system, not just delivering a service.

## Common failure modes

- **Solution-first delivery.** Committing to a named product before understanding the need. Antidote: fund discovery and make user needs the entry criterion for build.
- **Governance as a late gate.** Clinical safety and information governance consulted only at go-live, forcing rework or unsafe shortcuts. Antidote: embed both in the team from day one.
- **Project churn.** Standing teams up and tearing them down, losing hard-won domain and safety knowledge. Antidote: product funding and persistent teams.
- **Pilot purgatory.** Endless pilots that never scale because adoption, training, and business change were never resourced (see Chapter 8.1 — Change Management). Antidote: plan the path to scale before the pilot.
- **Equity as an afterthought.** Designing for the confident majority and excluding the people who need care most. Antidote: design for the hardest cases first.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Teams | Roles borrowed ad hoc per project | Some MDTs, unstable membership | Standing MDTs with full skill mix incl. clinical safety | Empowered product teams, low turnover, deep domain knowledge |
| Delivery | Big-bang, fixed scope | Occasional iteration, mostly waterfall | Iterative delivery against user needs | Continuous delivery with safety keeping pace |
| Evidence | Decisions by seniority | Some data gathered, rarely used | Clinical and delivery evidence routinely inform decisions | Decisions logged, evaluated, and revisited |
| Safety & equity | Bolted on at go-live | Assessed once, late | Clinical risk and equity analysis run in parallel | Continuous hazard and inequalities monitoring |
| Governance | Heavy, one-size-fits-all | Inconsistent | Proportionate to risk | Adaptive, fast for low risk, rigorous for high |

## Checklist

- [ ] Every service has a named, stable multidisciplinary team with clinical-safety and information-governance skills.
- [ ] No build starts without evidenced user needs from discovery.
- [ ] Clinical risk management (DCB0129/DCB0160) runs from day one, with a live hazard log.
- [ ] An equity / health-inequalities analysis has been done, and assisted-digital routes exist.
- [ ] Delivery proceeds in small, frequent, measurable slices.
- [ ] Decisions are recorded, distinguishing clinical from delivery evidence.
- [ ] Services are built to open interoperability standards and reuse shared platforms.
- [ ] Governance weight is matched to risk, and known to the team.
- [ ] There is a funded path from pilot to scale, including training and change.

## Key sources

- NHS digital service manual — *NHS service standard* and its points, including "Use agile ways of working" and "Create a team that includes multidisciplinary skills and perspectives" (service-manual.nhs.uk).
- GOV.UK Service Manual and the *Government Service Standard* — Government Digital Service (gov.uk/service-manual).
- NHS England / NHSX — *Digital Technology Assessment Criteria (DTAC)*.
- Clinical safety standards *DCB0129* and *DCB0160* (NHS England / former NHS Digital).
- NICE — *Evidence Standards Framework for digital health technologies* (nice.org.uk).
- NHS England — *Core20PLUS5* approach to reducing health inequalities.

## References

1. User-centered design — Wikipedia — https://en.wikipedia.org/wiki/User-centered_design
2. Government Digital Service — Wikipedia — https://en.wikipedia.org/wiki/Government_Digital_Service
3. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
4. Iterative and incremental development — Wikipedia — https://en.wikipedia.org/wiki/Iterative_and_incremental_development
5. Interdisciplinarity — Wikipedia — https://en.wikipedia.org/wiki/Interdisciplinarity
6. Product management — Wikipedia — https://en.wikipedia.org/wiki/Product_management
7. Health equity — Wikipedia — https://en.wikipedia.org/wiki/Health_equity
8. Web Content Accessibility Guidelines — Wikipedia — https://en.wikipedia.org/wiki/Web_Content_Accessibility_Guidelines
9. Fast Healthcare Interoperability Resources (HL7 FHIR) — Wikipedia — https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources
10. SNOMED CT — Wikipedia — https://en.wikipedia.org/wiki/SNOMED_CT
11. NHS service standard — NHS digital service manual, NHS England — https://service-manual.nhs.uk/standards-and-technology/service-standard
12. Government Service Standard — Government Digital Service, GOV.UK — https://www.gov.uk/service-manual/service-standard
13. Digital Technology Assessment Criteria (DTAC) — NHS England — https://www.nhs.uk/digital-technology-assessment-criteria-dtac/
14. Clinical Risk Management: DCB0129 and DCB0160 — NHS England — https://digital.nhs.uk/services/clinical-safety
15. Evidence Standards Framework for digital health technologies — NICE — https://www.nice.org.uk/about/what-we-do/digital-health
16. Core20PLUS5 — NHS England — https://www.england.nhs.uk/about/equality/equality-hub/national-healthcare-inequalities-improvement-programme/core20plus5/
