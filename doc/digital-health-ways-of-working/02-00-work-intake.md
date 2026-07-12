# Chapter 2.0 — Work Intake

**In one sentence:** How work enters your organization — through one visible front door, captured consistently, and acknowledged promptly — determines whether you ever get to choose what you do, or merely react to whoever shouts loudest.

## Why this matters in health and care

In health and care, the cost of chaotic intake is not just wasted effort — it is clinical risk, inequity, and eroded trust. When a ward's request for a safer e-observations workflow, a supplier's pitch, a national mandate, and a board member's pet idea all arrive through different channels with no common record, the organization cannot see its own demand, let alone govern it. Safety-critical requests get buried behind well-connected but low-value ones.

Public money compounds the stakes. Every unit of digital capacity you spend on unassessed, unrecorded demand is capacity not spent on the waiting list, the shared care record, or the interoperability work a system depends on. Regulators, auditors, and Integrated Care Boards (ICBs) increasingly expect a defensible answer to "how did this get prioritized?" — and you cannot answer that if you cannot even show how it arrived. Good intake is the first control point in a governable, equitable, evidence-driven operating model (see Chapter 1.1 — The Operating Model, and Chapter 1.3 — Evidence-Driven Decisions).

## Core concepts

**Intake** is the disciplined process of receiving, recording, classifying, and acknowledging every unit of demand before any decision is made about whether or how to do it. It is deliberately separate from triage (assessing and routing — Chapter 2.1) and prioritization (ordering — Chapter 2.2). Intake's only job is to make demand *visible and comparable*.

**[Demand management](https://en.wikipedia.org/wiki/Demand_management)**, in the [ITIL](https://en.wikipedia.org/wiki/ITIL) (IT Infrastructure Library) [service-management](https://en.wikipedia.org/wiki/IT_service_management) tradition, is the practice of anticipating and channelling demand so it can be met "without incurring unplanned costs." Its central device is the **single front door**: one route through which all requests are collected, so nothing is lost or processed through unofficial channels. ITIL 4 frames this as a [service catalogue](https://en.wikipedia.org/wiki/Service_catalog) (the front door itself) plus service request management (what happens once someone walks through it).

**Types of demand** are not interchangeable, and conflating them is a common source of dysfunction. A useful working taxonomy:

- **Ideas / opportunities** — "wouldn't it be good if…"; unproven, need discovery.
- **Requests / enhancements** — a defined change to an existing service.
- **Incidents / problems** — something is broken or unsafe now; usually a separate, faster operational path.
- **Mandates** — statutory, regulatory, or nationally-directed work (e.g. an NHS England national programme requirement) with limited discretion.

Each type deserves a different downstream path, but all should arrive through the same front door and be recorded in the same backlog of demand.

**Shadow intake** — the demand-side cousin of [shadow IT](https://en.wikipedia.org/wiki/Shadow_IT) — is the anti-pattern: demand that bypasses the front door — the corridor conversation, the direct email to a friendly developer, the "quick favour." Shadow intake is invisible, ungoverned, and the single biggest threat to a fair, safe system.

## Best practices

1. **Establish one visible front door.** Provide a single, well-publicized route for all new demand — typically a form backed by a queue or ticketing tool — and route everything through it, including senior leaders' requests. The front door need not be a single *team*, but it must be a single *record*. Visibility of demand is impossible if requests live in twelve inboxes.

2. **Capture demand with a lightweight, structured form.** Ask only for what you need to triage: requester and service, the problem or outcome sought (not the solution), affected users and volumes, any safety or statutory driver, and a rough sense of urgency. Resist bloating the form into a full business case — over-heavy intake pushes people back into shadow channels.

3. **Classify at the door.** Tag each item by demand type (idea / request / incident / mandate), originating service, and whether it touches clinical safety or personal data. Classification is what lets you send incidents down a fast operational path while ideas go to discovery, without making requesters understand your internal machinery.

4. **Separate the incident path — but still record it.** Something unsafe or broken now must not queue behind change requests. Route incidents to your operational/service-desk process immediately, but ensure the volume and pattern of incidents remains visible to intake, because recurring incidents are often the strongest signal of where change investment should go.

5. **Ask for just enough of a [business case](https://en.wikipedia.org/wiki/Business_case) — proportionate to size.** For small requests, a sentence of expected benefit is enough. For larger bids, use a lightweight one-page case: problem, intended outcome and who benefits, rough size, key risks, and the cost of *not* doing it. Reserve full business-case rigour (Green Book / Treasury five-case model) for genuine investment decisions, not for every idea.

6. **Set and publish an acknowledgement SLA.** Commit to a [service-level agreement](https://en.wikipedia.org/wiki/Service-level_agreement) for *acknowledgement* — for example, "every request acknowledged within two working days, with an indication of next steps and expected triage date." Acknowledgement is not agreement to do the work; it is the promise that the request has been seen and will be assessed. This single discipline does more than anything else to kill shadow intake, because people use back channels mainly when the front door feels like a black hole.

7. **Make the intake queue visible to everyone.** Publish the backlog of demand — at least internally — so requesters can see their item, its status, and its place relative to others. Transparency converts "why hasn't anyone dealt with my thing?" into a self-service answer and builds trust in the fairness of the process.

8. **Name an intake owner and cadence.** Someone must own the front door: ensuring items are complete, correctly classified, de-duplicated, and passed to triage on a predictable rhythm (see Chapter 2.1). Intake without an owner silts up within weeks.

9. **Make intake routes accessible and equitable.** The people with the most acute needs — frontline staff, social-care providers, and seldom-heard communities — are often the least able to submit a polished request. Offer more than one way in, keep the language plain, and help requesters articulate the underlying problem rather than pre-specifying a solution. An intake process that only the well-resourced can navigate quietly skews the whole portfolio.

10. **Close the loop with requesters.** Tell people what happened to their request — accepted, merged, parked, or declined — and why, on a predictable timescale. Silent intake destroys trust and drives shadow demand and workarounds, whereas honest, timely feedback (even a "no") keeps the front door credible and reduces chasing.

## Questions to discuss with your team

1. **How would we actually know how much shadow intake is bypassing our front door right now?**
   This question matters because you cannot govern demand you cannot see, and most leaders badly underestimate how much work enters through corridor conversations, direct emails to friendly developers, and "quick favours" for well-connected stakeholders. The tension is that the very people running the front door are often the least aware of what routes around it, so an honest answer requires asking the developers and delivery teams what they are actually being pulled into, not just reading the queue. Consider concrete probes: audit a sample of the last quarter's completed work and ask "where did this originate, and is there an intake record for it?"; ask frontline and clinical staff how they would raise a concern today and see whether the front door is even in their answer. A good answer resists the comforting assumption that "we have a form, so demand is visible" and instead names specific back channels, estimates their volume, and identifies why people prefer them — usually because the front door is slower or feels like a black hole. The evidence to look for is the gap between recorded demand and delivered work; a large gap is a measure of your blind spot, not your capacity.

2. **What is the smallest set of fields we can demand at the door without pushing people back into shadow channels?**
   This is a genuine design trade-off with no free lunch: every field you add improves your ability to triage later but raises the cost of submitting, and above some threshold people stop using the front door altogether. In a health and care setting the stakes are sharper because a mandatory clinical-safety and personal-data flag is non-negotiable, yet a form bloated into a full business case will suppress exactly the early, tentative safety signals you most want to catch. The debate should surface who your hardest-to-reach requesters are — frontline ward staff and social-care colleagues without bid-writing support — and design for their effort budget, not the portfolio office's appetite for information. Concrete angles: draft the form and time yourselves completing it as a busy nurse would; distinguish fields needed to *route* an item from fields needed to *decide* on it, and defer the latter to triage or business-case stages. A strong answer articulates a principle — capture problem and outcome, not solution; capture enough to classify and acknowledge, no more — and accepts that some information will be chased later rather than demanded upfront. The honest version admits that a form which is easy for the coordinator is often hard for the requester, and consciously chooses the requester's convenience.

3. **When a senior leader tries to route a request around the front door, what will we actually do?**
   Executive bypass is the single behaviour most likely to collapse an intake discipline, because it signals to everyone that the front door is for other people, and it matters most in hierarchical NHS and government organizations where challenging seniority is culturally hard. The tension is real: the leader usually has a legitimate request and genuine authority, so the answer cannot be a flat refusal to help, but it also cannot be a quiet exception that becomes the norm within a month. The team should rehearse the specific script and escalation — does the coordinator log it into the front door on the leader's behalf and gently redirect future requests, and who has the standing to hold that line when it is resisted? Consider what visible executive compliance would look like as a positive signal: a director publicly submitting their own request through the form does more to legitimize the process than any policy document. A good answer names a concrete, repeatable response rather than a hope that it "won't be a problem," and it identifies the one or two senior sponsors whose own behaviour will make or break the culture. The dishonest answer is "our leaders wouldn't do that" — they will, and the plan needs to survive the first time they do.

4. **How will we make sure our front door is genuinely reachable by the people with the most acute needs, not just the digitally confident?**
   This question matters because an intake process quietly shapes the whole portfolio, and if only well-resourced teams can navigate it, the demand you see is systematically skewed away from frontline, social-care, and seldom-heard voices. The tension is that the same structure and rigour that make demand governable — forms, fields, service-management tooling — also raise the barrier for a busy district nurse, a care-home manager, or a patient-facing team without bid-writing support. Consider concrete angles: who has actually submitted through the front door in the last quarter, and does that population match where clinical risk and inequity really sit? Offer more than one way in — a phone call or a short conversation that a coordinator writes up — and check whether the language assumes internal jargon that excludes outsiders. An honest answer names the groups currently under-represented in the queue and commits to specific accommodations for them, rather than assuming a single online form is neutral. The evidence to look for is the demographic and organizational spread of who raises demand, not just the total volume.

5. **When two requests turn out to be the same underlying need, who decides they are duplicates, and how do we protect the requesters' trust when we merge them?**
   Duplication is inevitable at any scale — the same "e-obs" or medicines-reconciliation need arrives from several wards or sites — and left unmanaged it inflates the apparent backlog and fragments effort across half-built variants. The trade-off is that merging is an act of judgement that can quietly disenfranchise a requester: the person whose ticket was folded into another may feel their specific problem was dismissed, especially if the surviving item is framed in someone else's words. The team should decide where de-duplication authority sits — usually the intake owner — and what evidence justifies calling two things "the same," because superficially similar requests sometimes hide genuinely different clinical contexts. Concrete practice: keep every original request traceable even after a merge, and tell both requesters what happened and why, so consolidation feels like being heard together rather than overruled. A good answer treats de-duplication as a curation discipline with clear ownership and an audit trail, not as silent housekeeping. The dishonest version assumes duplicates are obvious and harmless to collapse, when in fact careless merging is a common reason people stop trusting the front door.

6. **What is our honest policy for saying "no" or "not now," and are we willing to make declined demand as visible as accepted demand?**
   Most intake conversations focus on how work gets in, but the health of the system depends just as much on how work is honestly turned away, because a front door that can only say "yes" or "silence" will silt up and lose credibility. In health and care the stakes are pointed: declining or parking a request may be the right call against a finite budget, but it can also bury a real safety or equity signal, so the reasoning must be recorded and revisitable rather than lost. The tension is cultural — a clear "no, and here is why" is more respectful and more useful than an indefinite "we'll look into it," yet it is harder to say, particularly to senior or clinical requesters. Consider concrete angles: do parked items have a review date, and can a requester see why their request was declined and what would change the decision? Making declined and parked demand visible alongside accepted demand is what lets the organization learn from its own choices and defend them to an ICB or auditor. An honest answer commits to timely, reasoned closure for every item — accepted, merged, parked, or declined — and accepts that a credible "no" protects the front door far more than a hopeful backlog of things no one will ever start.

## In practice: a health & care example

An Integrated Care System (ICS) had no shared way of receiving digital demand. Trusts emailed the programme director; suppliers lobbied clinical directors; a national interoperability mandate arrived by letter; ward staff raised safety concerns on paper that never reached the digital team. Nobody could say how much demand existed or why any given piece of work was underway.

The ICS introduced a single intake form in its existing service-management tool, with four demand types and a mandatory "clinical safety / personal data" flag. Every route — supplier, trust, national body, frontline — was pointed at that form; senior leaders agreed to model the behaviour by using it themselves. An intake coordinator acknowledged each item within two working days and ran a short weekly session to check completeness and classification before handing items to the triage board.

Within a quarter, three things changed. First, the ICS could for the first time show its board a single picture of digital demand by type and by originating organization. Second, a cluster of frontline incidents about a medicines-reconciliation workflow — previously invisible — surfaced as a clear, evidence-backed candidate for change. Third, shadow requests fell sharply, because the front door now answered faster than the back channels ever had.

## Sector lenses

### Startup

A small digital-health company lives or dies by focus, so its front door is less about governing many stakeholders and more about resisting the pull of every prospect, investor, and clinical advisor who wants a bespoke feature. Intake here is lightweight — a shared board or a single spreadsheet — but it must still be one record, because the founder-led "just build it" side channel is the startup's version of shadow intake and it silently reshapes the roadmap. Funding constraint is the sharpest classifier: each item is weighed against a short runway, so the intake form's most valuable field is "what customer or regulatory outcome does this unlock?" Clinical-safety and data-protection flags cannot be skipped even at this scale, because a startup handling patient data carries the same DCB0129 and UK GDPR duties as a trust. The discipline to say "captured, not yet started" is what stops a promising company from fragmenting into a dozen half-built pilots.

### Small business

An established small provider — a GP practice, a community pharmacy, a care home, or a single-site clinic — has real patients and ongoing operations but rarely a dedicated IT or digital function, so intake is a duty that lands on a practice manager or registered manager alongside everything else. The front door here is modest — often a shared mailbox or a single logbook — yet it still matters, because demand arrives from clinicians, a supplier's account manager, a CQC action, and an ICB request all at once, and without one record the smallest and loudest jobs crowd out the important ones. The binding constraint is people's time rather than funding rounds: the intake question that earns its place is "does this address a patient-safety, regulatory, or contractual obligation, or can it wait?" These organizations carry the same clinical-safety and UK GDPR duties as a large trust but must discharge them with a fraction of the capacity, so a lightweight, consistent way to capture and acknowledge demand is what stops statutory obligations from being missed in the daily rush. The realistic aim is not sophistication but reliability — every request written down once, in one place, and looked at on a regular, if simple, rhythm.

### Enterprise

An NHS trust or ICS has the opposite problem: many legitimate channels (wards, corporate services, suppliers, national bodies) and strong political currents, so the single front door is as much a cultural change as a tool. The intake function is usually a named coordinator or a small team inside a portfolio office, backed by an enterprise service-management platform, and its hardest task is convincing directors to route their own requests through it rather than around it. Volume forces real classification and de-duplication — the same "e-obs" request often arrives five times from five sites — and the safety flag must integrate with the trust's clinical risk management and hazard log. Accountability is external: an ICB, auditors, or a regulator may ask how any given programme was justified, so the intake record is a governance artefact, not just a queue.

### Government

At the level of NHS England, DHSC, a devolved government, or a local authority, intake shapes national demand and public money at scale, and much of it arrives as mandate rather than request — statutory duties, ministerial commitments, spending-review conditions. The front door is often a formal portfolio or investment pipeline governed by the Treasury five-case model and the Green Book, so even early ideas are captured against strategic fit and value-for-money from the outset. Risk appetite is low and scrutiny is high: National Audit Office and Public Accounts Committee interest means every accepted item must have a traceable origin and rationale. The challenge is proportionality — applying enough rigour to defend spend without a gate so heavy that frontline and local-authority voices, who lack bid-writing teams, are effectively locked out. Transparency of the demand pipeline is therefore both an efficiency measure and an equity duty.

## Common failure modes

- **The black-hole front door.** A form exists, but requests vanish into it with no acknowledgement. People revert to back channels within weeks. *Fix:* an acknowledgement SLA, ruthlessly kept.
- **Solution-shaped intake.** The form asks "what do you want built?" instead of "what problem are you trying to solve?", locking in a solution before discovery. *Fix:* capture outcomes and problems, not designs.
- **Heavyweight gate at the door.** Demanding a full business case to *submit* an idea suppresses good early signals and drives shadow intake. *Fix:* proportionate capture; rigour comes later.
- **Executive bypass.** Leaders route their own requests around the process, signalling that the front door is for other people. *Fix:* visible executive compliance; no exceptions.
- **Incidents lost in the change queue.** Safety-critical breakages wait behind enhancement requests. *Fix:* a separate, faster incident path that intake still sees.
- **Intake without an owner.** The queue fills but no one curates it. *Fix:* a named coordinator and a fixed cadence.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| **Front door** | Many informal channels; much shadow intake | A form exists but is inconsistently used; leaders bypass it | Single, publicized front door used across all routes | Front-door usage is measured; bypass rate tracked and governed against a target | One front door is the cultural norm; shadow intake rare and challenged |
| **Capture & classification** | Ad hoc; free-text emails; no demand types | Some structure; classification unreliable | Structured form; demand typed and safety-flagged at the door | Classification accuracy and safety-flag completeness audited and assured against controls | Classification drives routing automatically; duplicates merged; patterns analysed |
| **Acknowledgement & visibility** | No SLA; requesters chase; demand invisible | Acknowledgement is best-effort; queue partly visible | Published acknowledgement SLA met; queue visible internally | SLA performance reported to a target; breaches investigated and demand actively managed | SLA measured and reported; demand trends feed strategy and capacity planning |

## Checklist

- [ ] There is one publicized front door for all new digital demand.
- [ ] The intake form captures problem/outcome, not just a requested solution.
- [ ] Every item is classified by demand type (idea / request / incident / mandate).
- [ ] A clinical-safety and personal-data flag is mandatory at intake.
- [ ] Incidents have a separate faster path but remain visible to intake.
- [ ] A published acknowledgement SLA exists and is measured.
- [ ] The demand queue is visible to requesters and stakeholders.
- [ ] A named owner curates intake on a fixed cadence.
- [ ] Business-case effort is proportionate to the size of the request.
- [ ] Senior leaders use the front door like everyone else.

## Key sources

- ITIL 4 (AXELOS / PeopleCert) — Demand Management and Service Request Management practices; the "single front door" concept.
- NHS England — DCB0129 *Clinical Risk Management: its Application in the Manufacture of Health IT Systems* (safety flagging of change).
- GOV.UK Service Manual (Government Digital Service) — understanding user needs and problems before solutions.
- NHS Digital Service Standard — designing for user needs; making work visible.
- HM Treasury — *The Green Book* and the five-case model (proportionate business cases).
- Reinertsen, D. — *The Principles of Product Development Flow* (managing queues and demand).

## References

1. Demand management — Wikipedia — https://en.wikipedia.org/wiki/Demand_management
2. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
3. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
4. Service catalog — Wikipedia — https://en.wikipedia.org/wiki/Service_catalog
5. Service-level agreement — Wikipedia — https://en.wikipedia.org/wiki/Service-level_agreement
6. Shadow IT — Wikipedia — https://en.wikipedia.org/wiki/Shadow_IT
7. Business case — Wikipedia — https://en.wikipedia.org/wiki/Business_case
8. ITIL 4: Demand Management and Service Request Management practices — AXELOS / PeopleCert — https://www.peoplecert.org/itil
9. DCB0129: Clinical Risk Management: its Application in the Manufacture of Health IT Systems — NHS England — https://digital.nhs.uk/services/clinical-safety/documentation
10. GOV.UK Service Manual — Government Digital Service — https://www.gov.uk/service-manual
11. NHS Service Standard — NHS England — https://service-manual.nhs.uk/standards-and-technology/service-standard
12. The Green Book: appraisal and evaluation in central government (five-case model) — HM Treasury — https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-government
13. Reinertsen, D. — *The Principles of Product Development Flow* — Celeritas Publishing — https://www.celeritas.com/
