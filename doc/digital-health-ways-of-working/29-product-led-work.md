# Chapter 29 — Product-Led Work

**In one sentence:** Product-led work funds durable, empowered teams to own a service over its whole life, holding them accountable for measurable outcomes rather than for delivering a fixed list of features.

## Why this matters in health and care

Most of what digital health and care organisations run is not a one-off delivery — it is a living service. The [NHS App](https://en.wikipedia.org/wiki/NHS_App), an [electronic patient record](https://en.wikipedia.org/wiki/Electronic_health_record), a shared care record, an e-referral pathway, a social-care case-management system: none of these are "finished". They must be continuously improved as clinical guidance changes, as safety incidents surface, as demand shifts, and as the estate around them evolves.

When you manage a living service as a series of disconnected projects, you get a predictable failure: a supplier builds to a specification, the money runs out, the team disbands, and the service is left to rot until the next capital bid. Clinicians work around the gaps, patient safety risks accumulate, and equity suffers because the people least able to tolerate a clunky service are those with the greatest need. Product-led work exists to break that cycle. It keeps a stable team close to users and to outcomes, so the service gets safer, more usable, and more equitable over time rather than degrading between funding rounds.

The stakes are also financial and statutory. Public money is better protected by a team that continuously validates whether a service actually improves care than by a project that measures success as "delivered on time and on budget" regardless of whether anyone benefited. This chapter sits alongside Chapter 30 — Project-Led Work and Chapter 31 — Programme-Led Work; the three are complementary tools, not rivals, and Chapter 32 — Enterprise Portfolio & Project Management (EPPM) explains how to hold them together.

## Core concepts

**Durable product team.** A [cross-functional](https://en.wikipedia.org/wiki/Cross-functional_team), long-lived team that owns a product or service across its whole lifecycle. The team persists; the work flows to it. This is the atomic unit of the product operating model described by Marty Cagan and the Silicon Valley Product Group (SVPG): a stable group of a product manager, a product designer, and engineers, supported by clinical and data expertise in a health context.

**Empowered team.** Cagan draws a sharp line between a "feature team" that is handed a roadmap of things to build, and an "empowered team" that is handed *problems to solve* and outcomes to achieve, and is trusted to find the best solution. Empowerment is not a licence to do anything; it is accountability for results within a clear strategic frame.

**Outcomes over outputs.** Output is what you ship — a feature, a release, a screen. An outcome is the change in the world that results — fewer missed appointments, faster discharge, reduced medication errors, more equitable uptake. Product-led work measures teams on outcomes, because shipping a feature that no one uses, or that no one is safer for, is waste dressed up as progress.

**Product manager.** The [product management](https://en.wikipedia.org/wiki/Product_management) lead, accountable for the *value and viability* of the product: is this worth building, will people use it, does it fit the organisation's strategy, regulations, and finances? In health and care this role must partner closely with clinical safety and information-governance leads, not sit above them.

**Product operating model.** SVPG is explicit that this is a *model*, not a methodology or a rigid framework: a set of principles about how a company builds and runs technology-enabled products — empowered teams, outcome accountability, continuous discovery, and product strategy — rather than a prescribed process you install.

**[Product lifecycle](https://en.wikipedia.org/wiki/Product_lifecycle).** Discovery (is there a real problem worth solving?), delivery (build it safely and well), growth and optimisation (improve adoption and outcomes), and eventually sunset (retire or replace gracefully). Product-led teams own all of it, which is why they can make sensible whole-life trade-offs a project team cannot.

## Best practices

1. **Fund the team, not the project.** Move money from time-boxed project budgets to standing product budgets tied to a [value stream](https://en.wikipedia.org/wiki/Value_stream), as Mik Kersten argues in *Project to Product*. Fund a persistent team to pursue outcomes over successive planning cycles, and re-authorise funding based on demonstrated results, not on a milestone plan agreed years earlier.

2. **Give teams problems and outcomes, not feature lists.** Frame the mandate as "reduce did-not-attend rates in outpatients" or "cut the time a clinician spends finding a result", then let the empowered team discover the best solution. A roadmap of committed features handed down from above recreates the feature-team anti-pattern Cagan warns against.

3. **Make outcome measures explicit and clinically meaningful.** Agree a small set of outcome metrics up front, ideally as [objectives and key results](https://en.wikipedia.org/wiki/OKR) (OKRs — see Chapter 41). Pair every efficiency metric with a safety and an equity metric, so a team is never rewarded for speed at the cost of harm or of widening inequality.

4. **Keep the team close to real users.** Embed continuous discovery: regular contact with clinicians, care workers, administrators, and patients. The NHS Service Manual and the GOV.UK Service Manual both make user research a standing discipline, not a one-off phase. A durable team makes this affordable because the relationships persist.

5. **Build multidisciplinary teams with clinical safety inside them.** A digital health product team needs, alongside product/design/engineering, a clinical safety officer (DCB0129/DCB0160), information governance, and data expertise. Safety and governance are design inputs owned within the team, not gates bolted on at the end.

6. **Instrument the product and act on the data.** Durable teams can invest in telemetry, so decisions are grounded in real usage and real outcomes rather than opinion. Watch adoption by cohort to catch [digital exclusion](https://en.wikipedia.org/wiki/Digital_divide) early.

7. **Own the whole lifecycle, including sunset.** Empowered teams plan for graceful retirement and migration, not just launch. Deciding *not* to keep building, and to consolidate onto a strategic platform, is a legitimate and valuable product decision.

8. **Align teams through strategy, not micromanagement.** Autonomy without alignment produces local optimisation and chaos. A clear product vision and strategy — and, at scale, a portfolio and programme frame (Chapters 31 and 32) — is what lets you empower teams safely.

## Questions to discuss with your team

1. **Which of the services we run today are genuinely living services that deserve a durable, funded product team, and which are finite work we are only pretending needs one?**
   This is the foundational sorting question, and getting it wrong in either direction is expensive. In a digital health and care organisation the estate is a mix — a shared care record or the patient-facing app is a living service, but a one-off data-centre exit or a hardware refresh is genuinely finite — and the honest answer requires naming each significant system and arguing its case rather than applying one funding model everywhere. The tension is that finance and governance machinery usually pushes everything toward time-boxed capital bids, so calling something a "product" can feel like special pleading, while calling a living service a "project" quietly guarantees the build-and-abandon decay described earlier in the chapter. Consider the whole-life cost, the rate at which clinical guidance and demand change around the service, and whether patient safety risk accumulates when no one owns continuous improvement. A good answer names two or three services where a durable team is clearly justified, is candid about the ones that are borderline, and explicitly parks the finite work for Chapter 30 rather than defending a blanket policy.

2. **What are the two or three outcome metrics we would actually stake a team's funding on, and how do we pair each with a safety and an equity measure so we are never rewarded for speed at the cost of harm?**
   Outcomes over outputs is easy to say and hard to operationalise, because the moment a metric drives money it starts to distort behaviour. A digital health team told to "reduce did-not-attend rates" can hit the number by nudging the most digitally-confident patients while quietly widening the gap for older or more deprived cohorts — so the debate has to surface which single efficiency metric each team might over-optimise, and what the paired safety and equity guardrail actually measures. Bring concrete candidates to the table (reduced medication errors, faster discharge, uptake by locality or digital-access proxy) and stress-test whether they are clinically meaningful or merely easy to instrument. Consider who owns each metric, what the baseline is, and how often it is reviewed, because an unowned or unbaselined outcome is decoration. An honest answer accepts that some outcomes we care about are slow or hard to measure, resists the pull toward vanity adoption numbers, and commits to publishing the equity measure alongside the efficiency one so the trade-off stays visible.

3. **How much real authority are we prepared to give an empowered team to change direction, and what strategic frame keeps that autonomy from fragmenting into local optimisation?**
   Empowerment is the crux of the product operating model and also its most common counterfeit, because organisations relabel teams "product teams" while still handing down a fixed roadmap and measuring delivery. The genuine question is where the boundary sits: can a team pivot from a board-sponsored feature to a different solution when discovery shows it will realise the outcome better, or will clinical governance, information governance, and existing supplier contracts veto that in practice? The tension is that autonomy without alignment produces duplication and drift across an ICS, while alignment enforced as micromanagement recreates the feature factory — so the answer lies in an explicit product vision and strategy, and at scale a portfolio frame, that constrains without dictating. Consider a recent decision where a team wanted to change course and ask honestly whether the system let it. A good answer defines the decisions a team may take alone versus those needing escalation, names the strategy document that provides the frame, and is candid about where the organisation currently confuses control with alignment.

## In practice: a health & care example

An integrated care system (ICS) runs a patient-facing appointment-management app used across several trusts. Historically each improvement was a separate project: a supplier was engaged to "add SMS reminders", delivered it, and left. Six months later the reminders were misfiring, no one owned the fix, and a capital bid was needed to reopen the contract.

The ICS shifts to a product-led model. It stands up a durable product team — a product manager, a designer, four engineers, a clinical safety officer, and an information-governance lead — funded on a rolling basis and mandated with an outcome, not a feature list: *reduce the did-not-attend (DNA) rate and improve equity of access across the population*.

The team runs continuous discovery with patients and outpatient schedulers. They learn that reminders help, but the bigger driver of DNAs in one deprived locality is that patients cannot easily rebook, so they simply miss the slot. Because the team owns the outcome rather than a specification, they pivot investment from a flashy notifications feature to a simple self-rebooking flow, and they instrument uptake by locality and by digital-access proxy.

Over three planning cycles the DNA rate falls, and — crucially — the team monitors the equity metric and spots that uptake lags among older patients, prompting a telephone-fallback pathway so the digital route does not widen inequality. Funding continues because the outcomes are demonstrable. No feature was ever "signed off and abandoned"; the service simply keeps improving. When a national platform later offers the same capability, the same team runs the migration and sunsets its own component — a whole-life decision a project team would never have been positioned to make.

## Three sector lenses

### Startup

In a small digital-health company, product-led work is the default — often the *only* — mode: a single empowered team, sometimes the whole company, owns the product end to end. Funding is the binding constraint, because investor runway or grant money means the team must show outcome traction (adoption, retention, an early clinical signal) fast enough to justify the next round, so continuous discovery and instrumentation are survival tools rather than luxuries. Risk appetite is high and accountability runs to founders and investors, not a board or the public, so the team can pivot in days. The trap is treating clinical safety and information governance (DCB0129, DPIA) as enterprise overhead to defer — in health that discipline is non-negotiable even at seed stage, and NHS buyers will demand DTAC evidence before they let you near patient data.

### Enterprise

In a large NHS trust, integrated care system (ICS), or health-tech firm, the durable-team model collides with annual capital budgeting and a project-shaped finance machine. The core work is converting standing services — the EPR-optimisation team, the shared-care-record team — from stop-start projects into funded product teams with rolling budgets tied to value streams, which is a finance and governance change as much as an org-chart one. Accountability is layered across clinical governance, information governance, board assurance, and supplier contracts, so empowerment has to be paired with an explicit product strategy and portfolio alignment (see Chapter 32 — Enterprise Portfolio & Project Management) to stop dozens of autonomous teams optimising locally. Scale is the enemy of proximity to users, so deliberate investment in embedded research is what keeps a large organisation's teams honest.

### Government

At national scale — NHS England, DHSC, UKHSA — product-led work funds long-lived platforms (the NHS App, NHS login, national interoperability APIs) as products rather than programmes, held to the GDS and NHS Service Standard and their service assessments. Funding flows through Spending Review settlements and business cases, so the hard part is sustaining stable teams across fiscal years and political cycles when the machinery around them is built for time-boxed projects. Accountability is to ministers, Parliament, and the public via the National Audit Office, and the equity duty is statutory, so outcome metrics must be paired with published population-level equity measures. The prize is reach: a single product improvement can touch tens of millions of users at once, which raises both the benefit and the cost of getting it wrong.

## Common failure modes

- **Product-led in name only ("feature factory").** The org relabels project teams as "product teams" but still hands them a fixed roadmap and measures them on delivery. Fix: change the mandate and the metrics, not just the job titles.
- **Outcomes with no safety or equity guardrail.** Optimising a single efficiency metric can hide harm or widen exclusion. Fix: every outcome metric is paired with a safety and an equity measure.
- **"Empowerment" without strategy.** Teams left to invent their own direction drift and duplicate. Fix: strong product vision and strategy, and portfolio-level alignment (Chapter 32).
- **Applying product-led to genuinely finite work.** A one-off data-centre migration or a hardware rollout does not need a perpetual team. Fix: use project-led work (Chapter 30) where scope really is fixed.
- **Funding that reverts to annual project bids.** A durable team on a stop-start budget cannot plan or retain people. Fix: rolling, outcome-reviewed funding for the value stream.
- **Product manager as ticket-writer.** Reducing the role to backlog administration wastes it. Fix: hold the product manager accountable for value, viability, and outcomes.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Team stability | Teams assembled per project, then disbanded | Some persistent teams for flagship services | Durable teams own named products across their lifecycle | Stable teams flow work to themselves; low churn, deep domain knowledge |
| Mandate | Feature lists handed down | Mix of features and goals | Teams given problems and outcomes to solve | Teams shape strategy and are trusted with outcome ownership |
| Measurement | Success = delivered on time/budget | Some usage metrics tracked | Outcome metrics (incl. safety & equity) agreed and reviewed | Outcomes drive funding and steering decisions continuously |
| Funding | Annual/capital project bids | Blended project + partial standing funding | Rolling product funding tied to value streams | Outcome-based reauthorisation; funding follows demonstrated value |
| Discovery | Requirements gathered once up front | Occasional user research | Continuous discovery with users and clinicians | Instrumented product; evidence-led decisions by default |

## Checklist

- [ ] Is this genuinely an ongoing service (not finite work) that suits a durable team?
- [ ] Does a stable, cross-functional team own the product across its whole lifecycle?
- [ ] Is the team mandated with problems and outcomes, not a fixed feature list?
- [ ] Are outcome metrics agreed — each paired with a safety and an equity measure?
- [ ] Is clinical safety (DCB0129/DCB0160) and information governance inside the team?
- [ ] Is the team funded on a rolling basis and reauthorised on demonstrated outcomes?
- [ ] Is continuous user research and discovery a standing practice?
- [ ] Is the product instrumented, with adoption watched by cohort to catch exclusion?
- [ ] Is there a clear product strategy aligning autonomy to organisational goals?
- [ ] Is graceful sunset/migration planned as an explicit lifecycle stage?

## Key sources

- Silicon Valley Product Group (SVPG), Marty Cagan — *The Product Operating Model: An Introduction* and *Empowered Product Teams* (svpg.com); books *Inspired*, *Empowered*, and *Transformed*.
- Mik Kersten — *Project to Product: How to Survive and Thrive in the Age of Digital Disruption with the Flow Framework* (IT Revolution, 2018).
- NHS England — NHS Service Manual and the NHS Digital Service Standard.
- GOV.UK — Government Digital Service (GDS) Service Manual and Service Standard.
- NHS Digital Clinical Safety standards DCB0129 (manufacture) and DCB0160 (deployment) of health IT systems.
- John Doerr — *Measure What Matters* (OKRs), for outcome-based goal setting.

## References

1. Product management — Wikipedia — https://en.wikipedia.org/wiki/Product_management
2. Product lifecycle — Wikipedia — https://en.wikipedia.org/wiki/Product_lifecycle
3. Cross-functional team — Wikipedia — https://en.wikipedia.org/wiki/Cross-functional_team
4. Value stream — Wikipedia — https://en.wikipedia.org/wiki/Value_stream
5. Objectives and key results (OKR) — Wikipedia — https://en.wikipedia.org/wiki/OKR
6. Electronic health record — Wikipedia — https://en.wikipedia.org/wiki/Electronic_health_record
7. NHS App — Wikipedia — https://en.wikipedia.org/wiki/NHS_App
8. Digital divide — Wikipedia — https://en.wikipedia.org/wiki/Digital_divide
9. The Product Operating Model / *Inspired*, *Empowered*, *Transformed* — Marty Cagan, Silicon Valley Product Group — https://www.svpg.com/
10. *Project to Product: How to Survive and Thrive in the Age of Digital Disruption with the Flow Framework* — Mik Kersten, IT Revolution (2018) — https://itrevolution.com/product/project-to-product/
11. NHS service manual and NHS Digital Service Standard — NHS England — https://service-manual.nhs.uk/
12. GOV.UK Service Manual and Service Standard — Government Digital Service — https://www.gov.uk/service-manual
13. Clinical risk management standards DCB0129 and DCB0160 — NHS England — https://digital.nhs.uk/services/clinical-safety
14. *Measure What Matters* — John Doerr — https://www.whatmatters.com/
