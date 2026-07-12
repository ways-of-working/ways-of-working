# Chapter 1.1 — The Operating Model

**In one sentence:** A target operating model (TOM) is the deliberate design of how your organization's strategy flows through value streams, capabilities, teams, governance, technology, data, and suppliers to deliver digital health and care outcomes — and getting its shape right determines whether everything downstream is fast and safe or slow and brittle.

## Why this matters in health and care

Most digital health organizations do not fail for lack of talent or technology; they fail because their operating model fights them. Funding is tied to time-limited projects, decision rights are ambiguous, and every team rebuilds the same login, integration, and audit plumbing. The result is duplicated cost on public money, inconsistent clinical safety, and services that cannot share data across an integrated care system (ICS).

An operating model is distinctive in this domain because it must reconcile competing goods. It has to be **federated enough** to respect the autonomy of sovereign organizations — trusts, local authorities, GP practices — yet **coherent enough** to give a patient one safe experience across them. It must balance **run** (keeping clinical systems safely available) against **change** (improving them), when downtime can affect care. And it must spend proportionately: assurance heavy enough for public accountability and clinical safety, light enough not to strangle iteration. The TOM is where those trade-offs are made explicit rather than left to accident.

## Core concepts

**The layers of an [operating model](https://en.wikipedia.org/wiki/Operating_model).** A useful TOM is a stack, each layer serving the one above:

- **Strategy and outcomes** — the measurable population and service outcomes you exist to improve (often expressed as [OKRs](https://en.wikipedia.org/wiki/Objectives_and_key_results); see Chapter 1.3 — Evidence-Driven Decisions).
- **[Value streams](https://en.wikipedia.org/wiki/Value_stream)** — the end-to-end flows that deliver value to a user, e.g. "refer, triage, and treat a patient" — organized around the citizen's journey, not the org chart.
- **Capabilities** — the things you must be able to do (identity, appointment booking, clinical documentation, analytics). Capabilities are stable even as solutions change.
- **Teams** — the people organized to deliver capabilities and value streams (see Team Topologies below).
- **Governance and decision rights** — who decides what, and how assurance is applied.
- **Technology and data** — the platforms, standards, and data architecture the teams build on.
- **Suppliers** — the market you buy from and how you manage it.

Designing top-down (strategy → value streams → capabilities) keeps teams and technology aligned to outcomes rather than to legacy structures.

**Centralized vs federated vs platform models.** A **centralized** model concentrates delivery in one team or arms-length body: consistent and cheap to standardize, but a bottleneck and often remote from local need. A **federated** model devolves delivery to trusts and places: responsive and locally owned, but prone to duplication and divergence. A **platform** model is the reconciling pattern: a central team provides shared, reusable capabilities (identity, interoperability, hosting, design system) as a *platform*, and federated teams build on top at speed. Most mature health systems converge on "platform plus federation."

**Team Topologies.** This framework names four team types — stream-aligned (owning a value stream), platform (providing self-service capabilities), enabling (coaching others up a capability), and complicated-subsystem (deep specialist work such as an algorithm) — and stresses low-friction interaction between them. It maps cleanly onto the platform model: platform teams reduce the cognitive load on stream-aligned teams so they can focus on user and clinical value.

**Run vs change.** *Run* is keeping live services safe and available; *change* is improving or building them. Product teams that both build and run a service ("you build it, you run it") close the feedback loop and improve safety, but the balance must be funded honestly — starving run to fund change is how clinical systems degrade.

**The thinnest viable platform (TVP).** From Team Topologies: a platform should be the *smallest* set of shared services that genuinely reduces friction for stream teams — no more. An over-built platform becomes its own bottleneck and its own legacy. Start with the few capabilities every team truly needs (authentication, an interoperability layer, hosting, a design system) and grow only on evidenced demand.

## Best practices

1. **Design the model from outcomes down, not the org chart up.** Begin with the population and service outcomes you must move, derive the value streams that deliver them, and only then design teams and technology. A TOM anchored in the existing hierarchy just automates the current silos.

2. **Adopt a platform-plus-federation shape.** Provide shared capabilities centrally as a self-service platform, and let stream-aligned teams in trusts and places build on top. This gives you national consistency on safety and interoperability with local speed and ownership — the reconciliation the domain demands.

3. **Fund products, not projects.** Move money from time-boxed projects to persistently funded product teams aligned to value streams. Project funding forces teams to disband at exactly the point they have learned the domain; product funding sustains the safety knowledge and iteration that health services need (see Chapter 5.0 — Product-Led Work).

4. **Make spend control proportionate and staged.** Use staged funding tied to evidence — release money at discovery, alpha, beta, and live gates rather than approving a whole programme up front. [GDS](https://en.wikipedia.org/wiki/Government_Digital_Service)-style spend controls and the NHS assurance route exist to prevent large sunk costs on unproven ideas; apply them as thresholds scaled to risk and value, not blanket bureaucracy.

5. **Make decision rights explicit with a RACI or RAPID map.** Ambiguous authority is the commonest cause of stalled delivery. Name, for each significant decision type, who is Responsible/Accountable/Consulted/Informed ([RACI](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix)) or who Recommends, Agrees, Performs, has Input, and Decides (RAPID). Publish it so teams stop escalating decisions they are empowered to make.

6. **Keep the platform thin and demand-led.** Build shared capabilities only when two or more teams demonstrably need the same thing, and treat the platform as a product with its own users (the internal teams). Resist the urge to pre-build a grand platform; the thinnest viable platform earns its scope through adoption.

7. **Manage suppliers as part of the model, not outside it.** Decide deliberately which capabilities are strategic (build/own) and which are commodity (buy), avoid single-supplier [lock-in](https://en.wikipedia.org/wiki/Vendor_lock-in) on core clinical data, and require open standards and exit rights in contracts. Your suppliers are a layer of your operating model, and their ways of working must be compatible with yours.

8. **Make decision rights explicit.** An operating model only works if people know who decides what — which choices sit with a product team, which with a clinical-safety authority, and which must reach a board. Map decision rights and push each decision to the lowest level that can safely hold it, so delivery is not throttled by needless escalation. Ambiguous authority is one of the most common causes of slow, defensive delivery.

9. **Treat the operating model as a product you evolve.** A target operating model is not set once and framed on a wall; inspect it as demand, technology and partnerships change, and adapt it on evidence. Watch a few signals — flow of work, time-to-decision, rework, and team health — and change structures when they are demonstrably getting in the way, not in response to reorganization fashion.

## Questions to discuss with your team

1. **Is our operating model designed from outcomes and value streams down, or has it simply automated our existing org chart and its silos?**
   This question goes to the chapter's central warning that a TOM anchored in the current hierarchy just entrenches the silos you already have, so it is worth putting on the table before any reorganization. It matters in a health and care setting because value streams follow the citizen's journey — refer, triage, treat — across sovereign organizations, while org charts follow institutional boundaries, and a model built on the latter will keep producing fragmented, non-interoperable services on public money. The tension to debate honestly is that designing top-down from outcomes is genuinely disruptive: it cuts across departmental ownership, budgets, and reporting lines that senior people have built careers around, so there is real political cost to doing it properly. Test yourselves concretely by naming your top three outcomes and tracing whether your actual team boundaries and funding lines follow those value streams or the departments; if teams map cleanly to departments, that is your answer. A good, honest response admits where the model is org-chart-shaped, identifies at least one value stream that is currently split across silos to its detriment, and is realistic about which structural boundaries the organization is willing to redraw.

2. **What belongs in our thinnest viable platform, and how will we stop it from either being over-built into a bottleneck or under-built so every team rebuilds the same plumbing?**
   The platform-plus-federation shape only works if the platform stays thin and demand-led, and this question makes the team confront both failure modes the chapter names — the grand platform that becomes its own legacy bottleneck, and the absence that forces every team to rebuild login, integration, and audit. It matters because in an ICS the platform is effectively shared infrastructure (identity, a FHIR interoperability layer, hosting with safety baselines, a design system) and getting its scope wrong multiplies either cost or friction across every stream team. The trade-off to debate is timing and evidence: build too early and you guess wrong and create a bottleneck; build too late and duplication has already calcified — so the "two or more teams demonstrably need the same thing" test is the crux, and the team should stress-test whether they actually apply it or just build what seems obviously central. Look at what you currently treat as platform versus what teams rebuild, and ask whether the platform is run as a product with its own internal users and SLAs or as a queue everyone waits behind. An honest answer names the specific capabilities that pass the two-team test today, resists the temptation to pre-build the rest, and commits to treating the platform team's internal users as real customers with real service levels.

3. **Where are our decision rights genuinely ambiguous, and what are teams escalating today that they should be empowered to decide themselves?**
   Ambiguous authority is called out as the commonest cause of stalled delivery, so this question surfaces the everyday friction that a published RACI or RAPID map is meant to remove. It matters acutely in a federated health system where place teams, an ICS digital board, clinical safety, and information governance all have legitimate claims on a decision, and unclear boundaries mean either everything escalates or, worse, no one owns a call until it goes wrong. The tension worth exploring is that devolving decisions requires trusting teams within guardrails, which senior leaders and boards often resist precisely where clinical safety or public money is involved — yet withholding that trust is what creates the escalation gridlock in the first place. Make it concrete by listing the last five decisions that escalated and asking, for each, who should have decided and what guardrail would have let them; the pattern usually reveals a small number of recurring ambiguous decision types. A good answer produces a specific, publishable statement of who decides what — distinguishing platform standards, service design, and clinical-safety sign-off — and is honest about which decisions the organization is genuinely willing to devolve versus which it will keep central and why.

4. **Are we funding run and change honestly, or are we quietly starving live-service operations to pay for new features?**
   The chapter is blunt that starving run to fund change is how clinical systems degrade, and this question forces the balance into the open before an outage or a safety incident makes it for you. It matters in health and care because "run" is not back-office overhead — it is the availability of systems clinicians depend on at the point of care, so a degraded run budget shows up as downtime that can affect patients, not merely inconvenienced users. The trade-off is uncomfortable because change is visible and celebrated while run is invisible until it fails, so boards and roadmaps naturally bias toward the new; a "you build it, you run it" model helps by keeping the feedback loop closed, but only if the team's run time is genuinely protected rather than notionally allocated and then raided. Make it concrete by looking at what proportion of each product team's capacity actually went to keeping services safe and available last quarter versus what was planned, and whether run work is tracked and valued or treated as interruption. An honest answer names where run is being under-funded today, protects a realistic run allocation as a first charge rather than a residual, and is candid about which live services are carrying accumulated operational risk.

5. **Which capabilities are we deliberately choosing to build and own versus buy, and are we accepting lock-in on our core clinical data without meaning to?**
   Best practice here is to decide build versus buy deliberately, avoid single-supplier lock-in on core clinical data, and treat suppliers as a layer of the operating model rather than something outside it — this question tests whether those choices are actually being made or defaulting. It matters because in digital health the most consequential lock-in is around the clinical record and its data, where a proprietary store with no realistic exit can trap a whole system for a decade and dictate what every downstream service can do. The tension is speed versus optionality: buying is faster and often cheaper today, especially for a stretched team, but each convenient buy without open standards or exit rights quietly narrows tomorrow's choices, and the cost only becomes visible when you try to leave. Make it concrete by listing your core capabilities, marking each as strategic (build/own) or commodity (buy), and checking whether the contracts behind the commodity ones actually require open standards (HL7 FHIR, SNOMED CT) and enforceable exit rights. A good answer distinguishes the few genuinely strategic capabilities from the many that are safely bought, is honest about where the organization is already locked in on clinical data, and commits to open standards and exit rights in the contracts that matter most.

6. **How will we know when our operating model needs to change, and what signals would tell us — rather than reorganizing on fashion or on a new leader's arrival?**
   The chapter frames the operating model as a product you evolve on evidence, not a diagram framed on a wall, so this question asks the team to define in advance what evidence would justify reshaping it. It matters in health and care because reorganization is disruptive and expensive — it disbands hard-won domain and clinical-safety knowledge — yet the sector is prone to structural churn driven by policy cycles and new appointments rather than by whether the current model is actually getting in the way. The tension is between stability and adaptation: change the model too readily and you never let teams settle or accrue safety expertise, change it too rarely and calcified structures throttle flow long after they stopped fitting the work. Make it concrete by choosing a small set of signals to watch — flow of work, time-to-decision, rework, and team health — and agreeing what movement in them would trigger a deliberate redesign versus a smaller adjustment. An honest answer commits to a few leading indicators, distinguishes evidence-led change from reorganization theatre, and is clear about who is accountable for inspecting the model and acting when the signals say it is impeding delivery.

## In practice: a health & care example

An ICS covering five places has each trust building its own patient-facing appointment tools. Costs duplicate, experiences diverge, and none share data cleanly. The ICS redesigns its operating model.

It defines three outcomes (reduce did-not-attends, cut avoidable admissions, improve access equity) and the value streams behind them. It stands up a small **platform team** owning four thinnest-viable capabilities: a shared identity/login, a [FHIR](https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources)-based interoperability layer, common hosting with security and clinical-safety baselines, and a design system. Each place keeps a **stream-aligned team** but now builds on the platform instead of from scratch.

Funding shifts from annual project bids to standing product budgets for each stream, released through discovery/alpha/beta gates. A published RAPID map makes clear that place teams *decide* their own service design within platform and clinical-safety guardrails, while the ICS digital board *decides* platform standards. Within a year, three places share one booking capability, the design and safety baseline is consistent, and new features that once took a project cycle ship in weeks — because the platform absorbed the undifferentiated heavy lifting.

## Sector lenses

An operating model is sized to the organization it serves; the same layers — value streams, capabilities, teams, governance, platform, suppliers — are drawn very differently by a startup, an enterprise, and a government body.

### Startup

In a small digital-health company the operating model is mostly implicit and that is fine: one or two stream-aligned teams, a founder holding most decision rights, and no platform team because there is nothing yet to platform. The discipline is to make the few real decisions explicit early — build versus buy for the clinical data store, which open standards to commit to — so today's shortcut does not become tomorrow's lock-in. Run and change sit in the same hands, so the risk is that keeping the lights on for early customers starves the roadmap; a simple, honest split of engineering time is the lightweight equivalent of a protected run budget. Suppliers are chosen for speed, but a startup should still refuse core-clinical-data lock-in, because its future NHS buyers will demand exit rights.

### Small business

An established small provider — a GP practice, a community pharmacy, a care home or domiciliary-care provider, a single-site clinic, or a small health-tech supplier past the pre-revenue stage — has real patients and ongoing operations but no platform team, no dedicated digital or IT capability, and little slack in cash or staff. Here the operating model is largely a set of bought capabilities stitched together, so the decisive choices are supplier ones: insisting on open standards and exit rights in the clinical systems you procure, because you carry the same interoperability and clinical-safety duties as a large trust without its buying power or in-house expertise. Run and change collapse onto the same handful of people who also deliver care, so the honest discipline is protecting a little time to keep systems safe and up to date rather than only firefighting. Decision rights are simple — usually a partner or owner-manager decides — but that makes it easy to defer digital decisions indefinitely, so the value is naming the few that matter (which clinical record, which shared regional platform to join) and making them deliberately. Where an ICS or national body offers a shared identity, interoperability, or design platform, the small business's best move is often to build on it rather than reinvent, borrowing the capability it cannot staff itself.

### Enterprise

An NHS trust or ICS is where the platform-plus-federation shape earns its keep: sovereign organizations that must feel like one service to a patient. The hard problems are political as much as technical — moving money from time-limited project bids to standing product budgets, and publishing a RACI/RAPID map so place teams stop escalating decisions they own. A large health-tech or pharma enterprise has the platform engineering muscle but risks over-building a grand internal platform that becomes its own bottleneck; the thinnest-viable-platform test — two or more teams demonstrably need the same thing — is the brake. At this scale, decision rights and funding flow are the operating model; the technology usually is not the constraint.

### Government

A national or local public body designs operating models that other organizations must inhabit, so its choices about standards and platforms are effectively national infrastructure. NHS England or DHSC providing a shared identity layer, an interoperability spine, or a design system is the platform pattern applied at population scale, and its spend controls and staged assurance gates are how public money is held to account. The failure mode is a centralized model that becomes a remote bottleneck, mandating one solution for every local context; the corrective is to platform the truly common capabilities and federate the rest to trusts and local authorities. Accountability to Parliament also means build/buy and supplier management are matters of public record, so open standards and exit rights are not merely prudent but expected.

## Common failure modes

- **Automating the org chart.** Designing teams around existing departments rather than value streams, so the TOM entrenches silos. Antidote: design from outcomes and value streams down.
- **The platform that becomes a bottleneck.** An over-scoped central platform team every request must queue behind. Antidote: thinnest viable platform, treated as a product with SLAs.
- **Project funding for product work.** Money that expires forces disband-and-rebuild churn. Antidote: persistent product funding with staged gates.
- **Run starved to feed change.** Under-funding live-service operations until clinical systems degrade. Antidote: fund run and change explicitly and protect the run budget.
- **Unowned decisions.** No one knows who decides, so everything escalates. Antidote: a published RACI/RAPID.
- **Lock-in by default.** Core clinical data trapped in a proprietary supplier system with no exit. Antidote: open standards and exit rights in every strategic contract.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| Structure | Org-chart-driven, siloed | Some value-stream alignment | Platform-plus-federation established | Boundaries governed and reviewed against flow metrics | Continuously reshaped around outcomes |
| Funding | Annual projects | Mixed project/product | Product funding with staged gates | Spend and delivery tracked against KPIs, gates assured | Outcome-based, evidence-released funding |
| Decision rights | Ambiguous, everything escalates | Partly documented | RACI/RAPID published and used | Decision latency and escalations measured and managed | Devolved within clear guardrails, rarely escalated |
| Platform | None; every team rebuilds | Ad hoc shared bits | Thinnest viable platform, demand-led | Platform SLAs, adoption and reliability tracked against targets | Platform as a mature internal product |
| Suppliers | Lock-in, tactical buys | Some standards required | Build/buy decided deliberately | Supplier performance and standards compliance assured | Open standards, exit rights, healthy market |

## Checklist

- [ ] The operating model is designed from outcomes and value streams, not the existing hierarchy.
- [ ] Shared capabilities are provided as a thinnest-viable platform, with stream teams building on top.
- [ ] Product teams are persistently funded and aligned to value streams.
- [ ] Spend control is staged (discovery/alpha/beta/live gates) and proportionate to risk and value.
- [ ] Decision rights are documented (RACI or RAPID) and published.
- [ ] Run and change are funded explicitly, with the run budget protected.
- [ ] Team types (stream-aligned, platform, enabling, complicated-subsystem) are understood and used.
- [ ] Build/buy is a deliberate choice per capability; core clinical data avoids lock-in.
- [ ] Contracts require open standards (e.g. HL7 FHIR, [SNOMED CT](https://en.wikipedia.org/wiki/SNOMED_CT)) and exit rights.

## Key sources

- Matthew Skelton & Manuel Pais — *Team Topologies* (stream-aligned, platform, enabling, complicated-subsystem teams; thinnest viable platform).
- GOV.UK Service Manual — *spend controls* and staged assurance (discovery/alpha/beta/live); Government Digital Service.
- NHS digital service manual — *NHS service standard* (service-manual.nhs.uk).
- AXELOS — *Management of Portfolios (MoP)* and *Managing Successful Programmes (MSP)* for portfolio and programme governance.
- Bain & Company — *RAPID* decision-rights framework; and the RACI responsibility-assignment model.
- John Doerr — *Measure What Matters* (OKRs) for outcome definition.

## References

1. Operating model — Wikipedia — https://en.wikipedia.org/wiki/Operating_model
2. Value stream — Wikipedia — https://en.wikipedia.org/wiki/Value_stream
3. Objectives and key results (OKRs) — Wikipedia — https://en.wikipedia.org/wiki/Objectives_and_key_results
4. Responsibility assignment matrix (RACI) — Wikipedia — https://en.wikipedia.org/wiki/Responsibility_assignment_matrix
5. Vendor lock-in — Wikipedia — https://en.wikipedia.org/wiki/Vendor_lock-in
6. Government Digital Service — Wikipedia — https://en.wikipedia.org/wiki/Government_Digital_Service
7. Fast Healthcare Interoperability Resources (HL7 FHIR) — Wikipedia — https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources
8. SNOMED CT — Wikipedia — https://en.wikipedia.org/wiki/SNOMED_CT
9. *Team Topologies: Organizing Business and Technology Teams for Fast Flow* — Matthew Skelton & Manuel Pais, IT Revolution — https://teamtopologies.com/book
10. Spend controls and staged assurance (discovery/alpha/beta/live) — GOV.UK Service Manual, Government Digital Service — https://www.gov.uk/service-manual/agile-delivery
11. NHS service standard — NHS digital service manual, NHS England — https://service-manual.nhs.uk/standards-and-technology/service-standard
12. *Managing Successful Programmes (MSP)* and *Management of Portfolios (MoP)* — AXELOS/PeopleCert — https://www.axelos.com/
13. *Measure What Matters* (OKRs) — John Doerr — https://www.whatmatters.com/the-book
