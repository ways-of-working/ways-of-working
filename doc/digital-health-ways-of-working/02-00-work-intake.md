# Chapter 2.0 — Work Intake

**In one sentence:** How work enters your organisation — through one visible front door, captured consistently, and acknowledged promptly — determines whether you ever get to choose what you do, or merely react to whoever shouts loudest.

## Why this matters in health and care

In health and care, the cost of chaotic intake is not just wasted effort — it is clinical risk, inequity, and eroded trust. When a ward's request for a safer e-observations workflow, a supplier's pitch, a national mandate, and a board member's pet idea all arrive through different channels with no common record, the organisation cannot see its own demand, let alone govern it. Safety-critical requests get buried behind well-connected but low-value ones.

Public money compounds the stakes. Every unit of digital capacity you spend on unassessed, unrecorded demand is capacity not spent on the waiting list, the shared care record, or the interoperability work a system depends on. Regulators, auditors, and Integrated Care Boards (ICBs) increasingly expect a defensible answer to "how did this get prioritised?" — and you cannot answer that if you cannot even show how it arrived. Good intake is the first control point in a governable, equitable, evidence-driven operating model (see Chapter 1.1 — The Operating Model, and Chapter 1.3 — Evidence-Driven Decisions).

## Core concepts

**Intake** is the disciplined process of receiving, recording, classifying, and acknowledging every unit of demand before any decision is made about whether or how to do it. It is deliberately separate from triage (assessing and routing — Chapter 2.1) and prioritisation (ordering — Chapter 2.2). Intake's only job is to make demand *visible and comparable*.

**[Demand management](https://en.wikipedia.org/wiki/Demand_management)**, in the [ITIL](https://en.wikipedia.org/wiki/ITIL) (IT Infrastructure Library) [service-management](https://en.wikipedia.org/wiki/IT_service_management) tradition, is the practice of anticipating and channelling demand so it can be met "without incurring unplanned costs." Its central device is the **single front door**: one route through which all requests are collected, so nothing is lost or processed through unofficial channels. ITIL 4 frames this as a [service catalogue](https://en.wikipedia.org/wiki/Service_catalog) (the front door itself) plus service request management (what happens once someone walks through it).

**Types of demand** are not interchangeable, and conflating them is a common source of dysfunction. A useful working taxonomy:

- **Ideas / opportunities** — "wouldn't it be good if…"; unproven, need discovery.
- **Requests / enhancements** — a defined change to an existing service.
- **Incidents / problems** — something is broken or unsafe now; usually a separate, faster operational path.
- **Mandates** — statutory, regulatory, or nationally-directed work (e.g. an NHS England national programme requirement) with limited discretion.

Each type deserves a different downstream path, but all should arrive through the same front door and be recorded in the same backlog of demand.

**Shadow intake** — the demand-side cousin of [shadow IT](https://en.wikipedia.org/wiki/Shadow_IT) — is the anti-pattern: demand that bypasses the front door — the corridor conversation, the direct email to a friendly developer, the "quick favour." Shadow intake is invisible, ungoverned, and the single biggest threat to a fair, safe system.

## Best practices

1. **Establish one visible front door.** Provide a single, well-publicised route for all new demand — typically a form backed by a queue or ticketing tool — and route everything through it, including senior leaders' requests. The front door need not be a single *team*, but it must be a single *record*. Visibility of demand is impossible if requests live in twelve inboxes.

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
   Executive bypass is the single behaviour most likely to collapse an intake discipline, because it signals to everyone that the front door is for other people, and it matters most in hierarchical NHS and government organisations where challenging seniority is culturally hard. The tension is real: the leader usually has a legitimate request and genuine authority, so the answer cannot be a flat refusal to help, but it also cannot be a quiet exception that becomes the norm within a month. The team should rehearse the specific script and escalation — does the coordinator log it into the front door on the leader's behalf and gently redirect future requests, and who has the standing to hold that line when it is resisted? Consider what visible executive compliance would look like as a positive signal: a director publicly submitting their own request through the form does more to legitimise the process than any policy document. A good answer names a concrete, repeatable response rather than a hope that it "won't be a problem," and it identifies the one or two senior sponsors whose own behaviour will make or break the culture. The dishonest answer is "our leaders wouldn't do that" — they will, and the plan needs to survive the first time they do.

## In practice: a health & care example

An Integrated Care System (ICS) had no shared way of receiving digital demand. Trusts emailed the programme director; suppliers lobbied clinical directors; a national interoperability mandate arrived by letter; ward staff raised safety concerns on paper that never reached the digital team. Nobody could say how much demand existed or why any given piece of work was underway.

The ICS introduced a single intake form in its existing service-management tool, with four demand types and a mandatory "clinical safety / personal data" flag. Every route — supplier, trust, national body, frontline — was pointed at that form; senior leaders agreed to model the behaviour by using it themselves. An intake coordinator acknowledged each item within two working days and ran a short weekly session to check completeness and classification before handing items to the triage board.

Within a quarter, three things changed. First, the ICS could for the first time show its board a single picture of digital demand by type and by originating organisation. Second, a cluster of frontline incidents about a medicines-reconciliation workflow — previously invisible — surfaced as a clear, evidence-backed candidate for change. Third, shadow requests fell sharply, because the front door now answered faster than the back channels ever had.

## Three sector lenses

### Startup

A small digital-health company lives or dies by focus, so its front door is less about governing many stakeholders and more about resisting the pull of every prospect, investor, and clinical advisor who wants a bespoke feature. Intake here is lightweight — a shared board or a single spreadsheet — but it must still be one record, because the founder-led "just build it" side channel is the startup's version of shadow intake and it silently reshapes the roadmap. Funding constraint is the sharpest classifier: each item is weighed against a short runway, so the intake form's most valuable field is "what customer or regulatory outcome does this unlock?" Clinical-safety and data-protection flags cannot be skipped even at this scale, because a startup handling patient data carries the same DCB0129 and UK GDPR duties as a trust. The discipline to say "captured, not yet started" is what stops a promising company from fragmenting into a dozen half-built pilots.

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

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| **Front door** | Many informal channels; much shadow intake | A form exists but is inconsistently used; leaders bypass it | Single, publicised front door used across all routes | One front door is the cultural norm; shadow intake rare and challenged |
| **Capture & classification** | Ad hoc; free-text emails; no demand types | Some structure; classification unreliable | Structured form; demand typed and safety-flagged at the door | Classification drives routing automatically; duplicates merged; patterns analysed |
| **Acknowledgement & visibility** | No SLA; requesters chase; demand invisible | Acknowledgement is best-effort; queue partly visible | Published acknowledgement SLA met; queue visible internally | SLA measured and reported; demand trends feed strategy and capacity planning |

## Checklist

- [ ] There is one publicised front door for all new digital demand.
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
