# Chapter 12 — Delivery Lifecycles

**In one sentence:** A [delivery lifecycle](https://en.wikipedia.org/wiki/Systems_development_life_cycle) is the sequence of phases and decision gates — Discovery, Alpha, Beta, Live, and eventual retirement — through which a digital service moves, with clinical safety, information governance, and assurance woven into every phase rather than bolted on at the end.

## Why this matters in health and care

A lifecycle is how an organisation converts an idea into a safe, live service and, eventually, retires it responsibly. In health and care, each transition carries statutory and clinical weight: you cannot deploy a system that touches patient care without a clinical safety case, and you cannot process confidential patient data without a lawful basis and a completed [data protection impact assessment](https://en.wikipedia.org/wiki/Privacy_impact_assessment) (DPIA). A lifecycle that treats these as end-of-project paperwork produces services that are late, unsafe, or both.

The stakes are asymmetric. A consumer app that ships a bug annoys users; a shared care record that ships a bug can show a clinician the wrong patient's allergies. This is why the NHS embeds the GOV.UK phase model *and* the clinical risk-management standards DCB0129 and DCB0160 into the same lifecycle. Getting the lifecycle right is not a governance nicety — it is the mechanism by which safety, equity, and value for public money are actually delivered rather than merely promised.

Leaders also need the lifecycle because it makes progress *legible*. Named phases and gates let a board see where a service is, what evidence exists, and what decision is due — replacing the fog of "it's nearly done" with a defensible, staged commitment of public money.

## Core concepts

**The phase model: Discovery → Alpha → Beta → Live.** The NHS and GOV.UK service standards define four phases. **Discovery** (see Chapter 11 — Discovery Phases) understands the problem. **Alpha** builds [throwaway prototypes](https://en.wikipedia.org/wiki/Software_prototyping) to test whether a solution *could* work and to burn down the riskiest assumptions. **Beta** builds the real, private-then-public service on production infrastructure, iterating with real users at growing scale. **Live** runs the service in continuous operation, still iterating, until it is retired. The phases are a risk-reduction ramp: each commits more money and exposes more users, justified by evidence from the last.

**Continuous iteration, not a conveyor belt.** The phases are not a one-way waterfall. A service in beta may loop back to alpha for a hard feature; a live service iterates continuously. The value of the model is its *gates*, not a promise that work flows in one direction.

**Agile, waterfall, and hybrid.** *[Waterfall](https://en.wikipedia.org/wiki/Waterfall_model)* fixes scope up front and proceeds in sequence — suitable only where requirements are genuinely stable and knowable (a data-centre migration, a mandated regulatory change). *[Agile](https://en.wikipedia.org/wiki/Agile_software_development)* delivers in small increments, inspecting and adapting — suited to the uncertainty of user-facing services. *Hybrid* is the honest reality of most large health programmes: agile product teams operating inside a milestone-and-funding wrapper the organisation and its regulators require. Match the method to the uncertainty, not to fashion.

**Service assessments and standards gates.** At the transitions between phases — especially alpha-to-beta and before public launch — NHS and GOV.UK services face a **service assessment**: an independent panel testing the work against the Service Standard's points (user need, accessibility, security, reliability, team, technology choices). Passing is the gate to spend more and expose more users. The assessment is evidence-based peer review, not a rubber stamp.

**Clinical safety and information governance as lifecycle threads.** DCB0129 (for the manufacturer/supplier) and DCB0160 (for the deploying health or care organisation) require a clinical risk management system, a **hazard log**, and a **clinical safety case report** signed off by a named, trained Clinical Safety Officer (CSO). Information governance requires a lawful basis, a DPIA, and adherence to the Caldicott principles. Both are *threads* that run through discovery, alpha, beta, and live — not gates at the end.

**Decommissioning.** A lifecycle has an end. Retiring a service safely — migrating or archiving data under retention law, redirecting users, notifying clinicians, and preserving records — is a phase in its own right, and one of the most neglected.

## Best practices

1. **Use the phases as risk-reduction gates, not calendar milestones.** Let each phase's decision be "is there enough evidence to justify committing the next tranche of money and users?" A phase that ends because the date arrived, rather than because the evidence is in, has skipped the point of the gate.

2. **Weave clinical safety in from alpha, not before Live.** Appoint a Clinical Safety Officer and open the hazard log as soon as a solution shape exists. Hazards identified in alpha are cheap to design out; hazards found at go-live are a launch-blocking crisis. The safety case matures alongside the service, so DCB0129/0160 sign-off is a summary of work already done, not a scramble.

3. **Start the DPIA and IG work in discovery and keep it live.** Data flows, lawful basis, and Caldicott considerations shape architecture, so surface them while the architecture is still soft. A DPIA written after build is a documentation exercise; one written alongside design actually reduces risk and prevents rework.

4. **Automate the path to production with [CI/CD](https://en.wikipedia.org/wiki/CI/CD) and [DevOps](https://en.wikipedia.org/wiki/DevOps).** [Continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) and [continuous delivery](https://en.wikipedia.org/wiki/Continuous_delivery) — automated build, test, and deployment pipelines — let a team ship small, reversible changes safely and often. In a safety-critical domain, the ability to deploy a fix in minutes and roll back cleanly is itself a safety control. Pair it with monitoring, alerting, and [infrastructure-as-code](https://en.wikipedia.org/wiki/Infrastructure_as_code) so the live service is [observable](https://en.wikipedia.org/wiki/Observability_(software)) and reproducible.

5. **Match the method to the uncertainty.** Use agile where user needs are uncertain and discovery is still teaching you things; accept waterfall-like sequencing only where requirements are genuinely fixed and the risk of change is low. Be explicit about running a hybrid — agile teams inside a programme wrapper — rather than pretending one method governs everything, which fools no one and frustrates everyone.

6. **Treat the service assessment as a design tool, not an exam.** Bring assurance, clinical safety, security, and accessibility reviewers in *early* and often, so the formal assessment confirms a service already built to standard. Teams that first meet the standard the week before assessment fail slowly and expensively; teams that internalise it pass as a by-product.

7. **Keep iterating in Live — and resource it.** A service does not stop needing a team when it goes live. Live is where real usage exposes the last inequities, the rare-but-serious clinical edge cases, and the accessibility gaps. Fund a standing product team for the service's operational life (see Chapter 15 — Product-Led Work); a live service with no team is technical debt accruing clinical risk.

8. **Plan decommissioning before you need it.** Decide, while building, how the service will eventually be retired: data retention and migration under records-management law, user redirection, clinician notification, and archival of the clinical safety case and audit trail. An unplanned retirement strands data and users; a planned one is a controlled, auditable phase.

## Questions to discuss with your team

1. **Are our phase gates genuinely governed by evidence, or have they quietly become dates on a plan?**
   The entire value of the Discovery–Alpha–Beta–Live model is that each transition commits more money and exposes more users only when the evidence from the previous phase justifies it; the moment a gate fires because the quarter ended rather than because the evidence is in, the ramp stops reducing risk and becomes "waterfall in agile costume". This question asks a team to look honestly at its last few transitions and ask what would have happened if the evidence had said "not yet" — was there room to hold, loop a beta back to alpha for a hard feature, or was the go-live date politically immovable? The tension to debate is between the organisation's need for legible, board-scheduled milestones and the reality that safe services move at the pace of evidence, and hybrid delivery lives precisely in that friction. Concrete angles include naming the specific decision and evidence due at the next gate, checking whether "sprints" actually change scope or merely track a fixed plan, and asking who is empowered to delay a gate without career risk. A good answer can point to a real instance where evidence changed the plan, and can articulate what evidence would justify — or block — the next commitment of public money and users.

2. **Are clinical safety and information governance living threads through every phase, or paperwork we intend to finish before Live?**
   In health and care the DPIA and the DCB0129/0160 clinical risk work are not end-of-project sign-offs but threads that must shape architecture and design from alpha onward, because a hazard designed out early is cheap while one discovered at go-live is a launch-blocking crisis — or worse, a pressure to wave the safety case through. This question surfaces whether a named, trained Clinical Safety Officer and an open hazard log exist as soon as a solution shape appears, and whether the DPIA and lawful-basis analysis began in discovery while the data flows were still soft enough to change. The trade-off worth debating is the felt drag of doing this continuously versus the far larger cost and clinical risk of a retrofit, especially for smaller teams or startups where no regulator is yet watching but the DCB0129 obligation attaches to the manufacturer regardless. Consider concrete evidence: does the hazard log show hazards found and mitigated in alpha, does the safety case read as a summary of work already done, and does the DPIA trace to real design decisions? An honest answer distinguishes a team maturing its safety case alongside the service from one heading for a documentation scramble the month before launch.

3. **How will this service be run in Live and eventually retired — and who is funded to do it?**
   Lifecycles have a long tail that organisations routinely underfund: Live is where real usage exposes the last inequities, rare-but-serious clinical edge cases, and accessibility gaps, and it needs a standing product team, monitoring, and fast, reversible deployment rather than a team that disbands at go-live leaving the service to rot and accrue clinical risk silently. Equally neglected is decommissioning — retiring a service under records-retention law, migrating or archiving data, redirecting users, notifying clinicians, and preserving the hazard log and audit trail — which for a national system is a major programme in its own right, not an afterthought when the replacement arrives. The tension to debate is annual funding cycles and the pressure to declare a project "finished" at launch versus the whole-life ownership a safe service actually requires. Useful angles include whether a CI/CD pipeline with monitoring and quick rollback is treated as a live safety control, whether an on-call and iteration budget survives the go-live celebration, and whether an exit plan was written while building rather than improvised in a panic. A good answer names who owns the service for its operational life and describes a controlled, auditable retirement rather than a hope that someone will handle it later.

## In practice: a health & care example

A community NHS trust is replacing a legacy paper-and-spreadsheet system for district-nurse visit scheduling. Coming out of discovery (Chapter 11), the team enters **alpha** and builds two throwaway prototypes to test the riskiest assumptions: that nurses will use a phone in patients' homes, and that the schedule can integrate with the electronic patient record. A Clinical Safety Officer is appointed on day one of alpha and opens a hazard log; an early hazard — a stale schedule showing a visit already completed by a colleague — drives a design decision to show real-time sync status. The DPIA, begun in discovery, flags that location data on lone workers needs a defined lawful basis and retention limit.

At the **alpha-to-beta service assessment**, an independent panel probes accessibility (nurses with visual impairments), security, and the team's reasoning. The service passes with actions. In **private beta**, ten nurses use the real system on production infrastructure; a CI/CD pipeline lets the team ship daily and roll back a bad release in under ten minutes. Usage reveals an equity issue — agency staff without trust devices — leading to a browser-based fallback. **Public beta** scales to three localities; the clinical safety case report is completed and signed off under DCB0160 before wider rollout.

The service goes **Live** with a standing product team, monitoring dashboards, and an on-call rota. Eighteen months later, when the trust adopts a regional platform, the schedule is **decommissioned** to plan: data migrated under the retention schedule, nurses retrained and redirected, and the hazard log and safety case archived for audit. Every transition was a decision backed by evidence, not a date on a Gantt chart.

## Three sector lenses

### Startup

A startup's lifecycle is compressed and largely self-governed: there is no independent service assessment panel, so the discipline of the Alpha–Beta–Live gates must be self-imposed or it collapses into "ship continuously and hope". The advantage is that a small team can run genuine CI/CD from day one and iterate faster than any large body. The danger is quietly dropping the clinical-safety and DPIA threads because no regulator is yet watching — a fatal mistake in health, where DCB0129 obligations attach to the manufacturer regardless of company size, and one unmanaged hazard can end both the product and the company. Startups should adopt the phase model's intent — evidence before exposure — even without the ceremony, appointing a Clinical Safety Officer (often fractional) as soon as a solution shape exists.

### Enterprise

An NHS trust or major supplier runs the lifecycle in its fullest, most assured form: formal service assessments, a named Clinical Safety Officer, DCB0160 deployment sign-off, change advisory boards, and an annual funding cycle the agile work must fit inside. The characteristic challenge is the hybrid — agile delivery teams operating within a programme-and-milestone wrapper the organisation and its auditors require — and the classic failure is "waterfall in agile costume", where gates quietly become calendar dates. Enterprises have the resources to do CI/CD, observability, and standing product teams properly, yet organisational inertia and legacy integration often slow deployment to a crawl. The accountability is broad and the blast radius large, so the phased ramp from private beta to live is not optional prudence but essential risk control.

### Government

A national body delivers under the full Service Standard, published service assessments, spend controls, and parliamentary scrutiny, so every phase gate is also a point of public accountability. Lifecycles here are long and the exposure vast — a live NHS-wide service may touch millions — which raises the stakes on the phased ramp, clinical safety assurance, and the decommissioning of the legacy systems being replaced. Procurement rules and multi-year funding settlements shape what "agile" can mean in practice, and retiring a national system (with its decades of records and statutory retention duties) is a major programme in its own right. The trade-off is assurance versus speed: government delivery is heavily gated, which protects safety and public money but demands deliberate effort to keep teams iterating rather than reverting to big-design-up-front.

## Common failure modes

- **Waterfall in agile costume.** The team runs "sprints" but scope, dates, and design were all fixed up front; iteration is theatre. Antidote: let evidence at each gate genuinely change the plan.
- **Safety and IG bolted on at the end.** The clinical safety case and DPIA are written the month before go-live, blocking launch or, worse, waved through under pressure. Antidote: open the hazard log and DPIA in alpha and mature them continuously.
- **The big-bang launch.** The service skips private/public beta and goes straight to full rollout, exposing every user to unproven software. Antidote: use the phased ramp; grow exposure with evidence.
- **The abandoned Live service.** The delivery team disbands at go-live; the service rots, and clinical risk accrues silently. Antidote: fund a standing product team for the operational life.
- **Assessment cramming.** Standards are ignored until the assessment looms, then met superficially. Antidote: engage assurance and clinical reviewers continuously.
- **No exit plan.** The service is retired in a panic when its replacement arrives, stranding data and users. Antidote: plan decommissioning as a first-class phase.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Phase discipline | Ad-hoc; phases skipped or renamed | Phases named but gates are calendar-driven | Evidence-based gates govern spend and exposure | Portfolio-wide staged funding; weak services stopped early |
| Method fit | One method forced onto all work | Agile used, but inside rigid fixed scope | Method matched to uncertainty; hybrid made explicit | Teams flex method continuously as uncertainty changes |
| Clinical safety & IG | Addressed after build, if at all | Raised late; CSO/DPIA a launch scramble | Hazard log, safety case, DPIA maintained from alpha | Safety and IG evidence shapes design; sign-off is routine |
| CI/CD & operations | Manual, infrequent, risky deployments | Some automation; slow, feared releases | Automated pipeline, monitoring, fast rollback | Continuous delivery as a safety control; strong observability |
| Live & retirement | No standing team; no exit plan | Team retained ad-hoc; retirement improvised | Funded product team; decommissioning planned | Whole-life ownership; retirements controlled and audited |

## Checklist

- [ ] The service has an explicit current phase (Discovery / Alpha / Beta / Live) and a named next decision.
- [ ] Phase transitions are gated on evidence, not on dates.
- [ ] A Clinical Safety Officer is appointed and a hazard log is open (DCB0129/0160) from alpha onward.
- [ ] A DPIA and lawful-basis assessment (Caldicott, UK GDPR) began in discovery and is kept current.
- [ ] The delivery method is matched to the level of uncertainty, and any hybrid arrangement is explicit.
- [ ] Service assessments are planned, and assurance/security/accessibility reviewers are engaged early.
- [ ] A CI/CD pipeline with monitoring and fast rollback is in place before public beta.
- [ ] The service is exposed to users in a phased ramp (private beta → public beta → live), not big-bang.
- [ ] A standing product team is funded for the service's operational life (see Chapter 15).
- [ ] A decommissioning plan covers data retention/migration, user redirection, and archival of safety and audit records.

## Key sources

- GOV.UK Service Manual — the phases of an agile project (Discovery, Alpha, Beta, Live) and the Government Service Standard.
- NHS England — NHS Service Standard and NHS Digital Service Manual; NHS service assessments.
- NHS England Digital — DCB0129 (Clinical Risk Management: its Application in the Manufacture of Health IT Systems) and DCB0160 (its Application in the Deployment and Use of Health IT Systems).
- NHS England — Digital clinical safety assurance; the Clinical Safety Officer role, hazard log, and clinical safety case report.
- NHS England — Digital Technology Assessment Criteria (DTAC).
- UK Caldicott Principles; Data Protection Act 2018 / UK GDPR and data protection impact assessments.
- NICE — Evidence Standards Framework for Digital Health Technologies.
- DevOps and continuous delivery practice (e.g. the DORA capabilities: continuous integration, deployment automation, monitoring); GOV.UK Service Manual guidance on continuous delivery and operating a service.

## References

1. Systems development life cycle — Wikipedia — https://en.wikipedia.org/wiki/Systems_development_life_cycle
2. Waterfall model — Wikipedia — https://en.wikipedia.org/wiki/Waterfall_model
3. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
4. Software prototyping — Wikipedia — https://en.wikipedia.org/wiki/Software_prototyping
5. CI/CD — Wikipedia — https://en.wikipedia.org/wiki/CI/CD
6. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
7. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
8. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
9. Infrastructure as Code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
10. Observability (software) — Wikipedia — https://en.wikipedia.org/wiki/Observability_(software)
11. Privacy impact assessment (data protection impact assessment) — Wikipedia — https://en.wikipedia.org/wiki/Privacy_impact_assessment
12. Agile delivery: the phases of an agile project — Government Digital Service, GOV.UK Service Manual — https://www.gov.uk/service-manual/agile-delivery
13. NHS service standard and NHS digital service manual — NHS England — https://service-manual.nhs.uk/
14. Clinical risk management standards DCB0129 and DCB0160 — NHS England (Clinical Safety) — https://digital.nhs.uk/services/clinical-safety
15. DevOps Research and Assessment (DORA) capabilities — Google Cloud / DORA — https://dora.dev/
16. Continuous delivery — Jez Humble and David Farley — https://continuousdelivery.com/
17. Data protection impact assessments (DPIAs) — Information Commissioner's Office (ICO) — https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/data-protection-impact-assessments-dpias/
18. Evidence standards framework for digital health technologies — NICE — https://www.nice.org.uk/about/what-we-do/digital-health
