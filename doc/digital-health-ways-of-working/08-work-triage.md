# Chapter 8 — Work Triage

**In one sentence:** Triage is the clinical discipline of rapidly assessing each incoming piece of work for urgency, importance, and fit, then routing it — fast-track, standard queue, or a respectful "no" — so that scarce capacity flows to where it does the most good.

## Why this matters in health and care

Every clinician understands triage: when demand exceeds capacity, you do not treat in arrival order, you assess and sort by need. Digital and operational teams face the same reality — far more requests than hands — yet often handle work first-come-first-served, or worst-of-all by who is loudest. The result is that a low-risk convenience feature gets built while a patient-safety defect waits.

The analogy is more than rhetorical. Health and care organisations already trust triage as a fair, defensible way to allocate scarce resource under pressure; applying the same explicit, criteria-based sorting to digital demand inherits that legitimacy. It also protects the things that must not slip: safety-critical fixes, statutory deadlines (for example a regulatory or information-governance obligation), and equity of access. Triage done well means that when you tell a director "not yet," you can show *why* — against consistent criteria, not politics. It sits between intake (Chapter 7) and prioritisation (Chapter 9): intake makes demand visible, triage assesses and routes it, [prioritisation](https://en.wikipedia.org/wiki/Prioritization) orders what survives.

## Core concepts

**[Triage](https://en.wikipedia.org/wiki/Triage)** is a quick, structured assessment that answers three questions for each item: *How urgent is it? How important is it? Where should it go?* It is deliberately fast and coarse — a sort, not a full analysis. The clinical parallel is a triage nurse categorising arrivals (immediate / urgent / standard / signpost elsewhere), not a full diagnosis.

**Urgency versus importance** is the foundational distinction, popularised in general management by the [Eisenhower matrix](https://en.wikipedia.org/wiki/Time_management). *Urgent* work is time-sensitive: a statutory deadline, a live safety risk, an expiring contract. *Important* work has high value or consequence but may not be time-critical. The classic trap is letting the urgent-but-unimportant crowd out the important-but-not-yet-urgent — which in digital terms means firefighting forever while the strategic platform work never starts.

**Categorisation** is the triage output: each item is placed in a lane. A simple, robust scheme is **fast-track** (safety, statutory, or trivially small and clearly valuable — bypasses the queue), **standard** (goes forward to full prioritisation), and **signpost / decline** (belongs to someone else, duplicates existing work, or should not be done). This mirrors clinical streaming, as codified in tools like the [Manchester Triage System](https://en.wikipedia.org/wiki/Manchester_Triage_System).

**Sizing** at triage is a *rough* order-of-magnitude estimate — t-shirt sizes (S/M/L/XL) or a quick effort band — enough to route and to feed later prioritisation, never a detailed estimate. Precision here is false economy.

**[Cynefin](https://en.wikipedia.org/wiki/Cynefin_framework)** (Snowden) helps triage judge *how much discovery* an item needs: clear/obvious items can go straight to delivery; complicated ones need expert analysis; complex ones need discovery and experimentation (see Chapter 11 — Discovery Phases); chaotic ones need an incident response. Triage should recognise the domain and route accordingly rather than forcing everything down one path.

## Best practices

1. **Define explicit triage criteria and publish them.** Agree the factors that determine a lane: clinical-safety risk, statutory or regulatory deadline, size/effort, strategic fit, and dependency on or from other work. Weight them, write them down, and share them. Explicit criteria are what make triage fair, fast, and defensible — and what let you say "no" without it being personal.

2. **Put safety and statutory drivers above negotiation.** Anything with a genuine patient-safety or legal-deadline driver is fast-tracked or escalated, full stop. Guard this ruthlessly, because everything wants to claim urgency; require the safety or statutory driver to be *evidenced* (a clinical-safety flag, a named regulation, a hazard log entry), not merely asserted.

3. **Make triage a small, cross-functional decision, not a solo act.** Triage benefits from a handful of perspectives — delivery, clinical/operational, [information governance](https://en.wikipedia.org/wiki/Information_governance), and architecture — because a single triager will systematically under-weight risks outside their expertise. Keep the group small enough to be fast; a triage of two or three well-chosen people beats a committee of twelve.

4. **Run triage on a predictable cadence.** Hold a short, regular triage session — often weekly — so requesters know when their item will be assessed and the queue never silts up. A fixed cadence turns "when will someone look at this?" into a knowable date, reinforcing the acknowledgement promise made at intake.

5. **Separate the fast lane and protect it.** Reserve explicit capacity for fast-track work (safety, urgent statutory, tiny high-value fixes) so it does not compete in the main prioritisation. Equally, cap it: if everything is "fast-track," nothing is, and the discipline collapses. A small standing allocation for genuine urgent work is healthier than heroics.

6. **Size roughly, once, and record the basis.** Give each item a t-shirt size at triage and note the key assumption behind it. This is enough to route and to inform prioritisation without burning discovery effort on things that may be declined. Detailed estimation is earned by surviving triage, not spent before it.

7. **Say no — and signpost — with respect.** A good triage declines work clearly and kindly: it explains the criteria, names the alternative (another team, an existing product, a later cycle), and records the decision. Signposting — "this belongs to the service desk," "the shared care record programme already covers this" — is often more valuable than a flat refusal. The ability to decline is what makes a "yes" mean anything.

8. **Watch for [equity](https://en.wikipedia.org/wiki/Health_equity) and demand bias.** Well-resourced services submit polished requests; frontline and social-care voices may not. Triage should actively check that criteria are applied evenly and that quieter but high-need demand is not systematically down-ranked. Fairness of process is a governance requirement, not a nicety.

## Questions to discuss with your team

1. **What evidence will we require before we accept that something is genuinely urgent — and who gets to challenge an urgency claim?**
   This matters because "everything is urgent" is the failure mode that quietly destroys triage: if urgency is self-declared and unchallenged, the fast lane becomes the only lane and the discipline collapses. In health and care the difficulty is that some urgency claims are entirely real — a safety defect that could let a clinician miss a flagged patient, a statutory information-governance deadline — so the answer is not scepticism but a clear evidentiary bar: a named regulation, a hazard-log entry, a clinical-safety flag, not merely a stressed requester's assertion. The team should debate where that bar sits and who holds it, because the person with authority to say "your urgency claim is not evidenced" needs both the standing and the criteria to make it stick. Consider concrete tests: for the last ten items labelled urgent, how many could produce the evidence, and what would have happened if they had waited a cycle? A good answer defines the specific proofs that upgrade an item to the fast lane and pairs them with a hard cap on fast-track capacity, so that genuine safety and statutory work is protected precisely by refusing to dilute the lane. The honest version admits that most "urgent" requests are important-but-not-time-critical, and that naming that distinction out loud is what makes the safety-critical minority visible.

2. **Who actually needs to be in the room for a triage decision to be safe, and how do we keep it fast enough to happen weekly?**
   This is the core tension of triage: a single triager systematically under-weights the risks outside their own expertise — a delivery lead misses an information-governance trap, a technologist misses a clinical hazard — yet a committee of twelve is too slow to run on a predictable cadence and turns a coarse sort into full analysis. The debate should identify the minimum viable set of perspectives for *your* demand, which in most health and care settings means delivery, clinical or operational safety, and information governance, and then defend that group against both shrinkage (back to a solo act) and bloat (a stakeholder free-for-all). Concrete angles: time-box a real triage session and see how many items you can stream in the slot; look at past decisions that went wrong and ask which missing voice would have caught the problem. A strong answer treats the composition as a safety control, not a courtesy — the clinical-safety officer is there so hazard-flagged work is never buried, not to be consulted — while ruthlessly protecting speed by sizing roughly and deferring depth to discovery. The good version also names what happens when a needed expert is absent: does triage proceed and risk a blind spot, or defer the item, and who decides?

3. **How will we know whether our triage is quietly down-ranking the quieter, higher-need voices?**
   Equity of demand is easy to endorse and hard to verify, because well-resourced services submit polished, well-evidenced requests while frontline and social-care colleagues may raise real needs in ways that score poorly against criteria written for articulate requesters. This matters in health and care specifically because the public sector equality duty gives fairness of process statutory weight, and because the populations least able to lobby are often those with the greatest need. The team should debate how bias actually enters their criteria: does "strategic fit" implicitly favour national programmes over local ones, does requiring crisp evidence disadvantage those without analysts, does seniority creep back in through who gets heard? Concrete checks include periodically sampling declined and low-ranked items by originating service to see whether a pattern of quieter voices losing emerges, and inviting a frontline or social-care perspective into the criteria review, not just the triage session. An honest answer accepts that a process applied "consistently" can still be systematically unfair if the criteria themselves are tilted, and commits to a specific monitoring mechanism rather than a good intention. The best answers treat equity as something you measure in the outcomes of triage, not something you assume from the fairness of the room.

## In practice: a health & care example

A community and mental-health trust's digital team faced a backlog it could not see the top of. Everything arrived as "urgent." The team stood up a weekly triage board: a delivery lead, a clinical safety officer, and an information-governance lead, working from published criteria (safety risk, statutory deadline, rough size, strategic fit, dependencies).

Each intake item was assessed in a few minutes and streamed into three lanes. A defect in a risk-assessment form that could let a clinician miss a flagged patient was fast-tracked that day. A request for a cosmetic dashboard change was sized "S" but streamed to the standard queue with low strategic fit. A supplier's proposal to replace a working system was declined and signposted to the existing roadmap, with the reasoning recorded. A vague "we want an app" idea was routed to discovery under a Cynefin "complex" reading, rather than into delivery.

The effect was cultural as much as operational. Because the criteria were visible and applied consistently, a "not now" from the triage board was accepted where a "not now" from an individual manager had previously been fought. The safety officer's presence meant genuine risk items were never buried, and the trust could demonstrate to its board and regulator that safety-critical work was systematically prioritised.

## Three sector lenses

### Startup

In a small digital-health company the triage "board" may be two or three people around a laptop, and the dominant pressure is not internal politics but external pull — the customer who threatens to churn, the investor's feature request, the pilot site that wants a tweak. The scarce resource is engineering time against runway, so triage criteria collapse to a sharp few: does this unblock a paying customer or a regulatory gate, is it a genuine safety defect, and is it small? The fast lane exists but must be capped hard, because at this scale a single "urgent" custom build for one client can consume a sprint the whole company needs. The healthiest startups learn early to signpost respectfully — "not in this release, and here's why" — because the alternative is a product bent out of shape by whoever shouted last.

### Enterprise

An NHS trust or ICS triages high volume across many services, so triage becomes a standing cross-functional forum with published criteria, a fixed cadence, and named roles — typically delivery, a clinical safety officer, and an information-governance lead. The value of that formality is defensibility: when the board or a regulator asks why a request waited, the criteria and the decision log answer for it, and a clinical safety officer in the room ensures hazard-flagged work is never buried. Scale also breeds duplication and cross-site politics, so triage must de-conflict five versions of the same request and hold the line against seniority-based queue-jumping. The fast lane needs real, ring-fenced capacity here, because a large organisation generates a steady stream of genuine safety and statutory items that cannot wait for the next quarterly cycle.

### Government

At NHS England, DHSC, or a local authority, triage operates on demand that is often already mandated, so the question shifts from "should we do this?" to "how urgent and how large, given we must." Statutory deadlines, ministerial commitments, and legal obligations dominate the urgency axis, and the evidence bar for a claimed deadline is a named regulation or a formal commitment, not an assertion. Accountability is public and adversarial — the National Audit Office and select committees may examine why work was or was not prioritised — so the triage decision log is a formal governance record. Equity carries statutory weight through the public sector equality duty, so a government triage process must actively check that thinly-resourced local authorities and frontline services are not systematically out-competed by well-funded national programmes with polished submissions.

## Common failure modes

- **Everything is urgent.** With no evidenced test for urgency, every requester claims it, and the fast lane becomes the only lane. *Fix:* require evidence for safety/statutory claims; cap fast-track capacity.
- **Triage by seniority.** The most senior requester's item wins regardless of merit. *Fix:* explicit, published criteria applied by a group.
- **Triage that becomes full analysis.** The session tries to fully scope and estimate each item and grinds to a halt. *Fix:* time-box; size roughly; defer depth to discovery.
- **No one ever says no.** Everything is accepted "to keep the peace," and the backlog becomes a graveyard. *Fix:* empower the triage group to decline and signpost.
- **A single triager.** One person's blind spots (often information governance or clinical safety) become systemic. *Fix:* cross-functional triage.
- **Invisible criteria.** Decisions feel arbitrary and are re-litigated endlessly. *Fix:* publish the criteria and the decision log.

## Maturity model

| Level | Criteria & lanes | Who triages & cadence | Saying no & equity |
|---|---|---|---|
| **Initial** | No criteria; work handled in arrival or seniority order | Ad hoc individuals; no cadence | "No" is avoided; loudest voice wins |
| **Developing** | Some informal lanes (urgent vs not); criteria in people's heads | One person triages irregularly | Occasional declines, poorly explained |
| **Defined** | Published criteria (safety, statutory, size, fit, dependencies); clear fast-track/standard/decline lanes | Small cross-functional board on a fixed cadence | Declines are explained and signposted; criteria applied consistently |
| **Optimizing** | Criteria weighted and periodically reviewed against outcomes; Cynefin-informed routing to discovery vs delivery | Triage integrated with capacity; fast lane capped and protected | Decline/signpost is routine and trusted; equity of demand actively monitored |

## Checklist

- [ ] Triage criteria are explicit, weighted, and published.
- [ ] Safety and statutory drivers require evidence, not assertion, and are fast-tracked.
- [ ] Triage is done by a small cross-functional group, not one person.
- [ ] Triage runs on a predictable, published cadence.
- [ ] A capped fast-track lane exists and is protected.
- [ ] Every item gets a rough size and a recorded routing decision.
- [ ] The team can and does decline work, with respectful signposting.
- [ ] Decisions are logged so they are not re-litigated.
- [ ] Discovery-needing (complex) items are routed to discovery, not straight to build.
- [ ] Equity of demand — including quieter frontline and social-care voices — is checked.

## Key sources

- Snowden, D. & Boone, M. — the Cynefin framework, *A Leader's Framework for Decision Making* (Harvard Business Review).
- Covey, S. / Eisenhower matrix — urgency versus importance.
- NHS England — DCB0129 clinical risk management (evidencing safety-driven prioritisation).
- ITIL 4 (AXELOS / PeopleCert) — service request categorisation and streaming.
- NHS Digital Service Standard & NHS Service Manual — prioritising the most important user needs.
- Manchester Triage Group — the clinical triage categorisation model (as the domain analogy).

## References

1. Triage — Wikipedia — https://en.wikipedia.org/wiki/Triage
2. Time management (Eisenhower method / matrix) — Wikipedia — https://en.wikipedia.org/wiki/Time_management
3. Manchester Triage System — Wikipedia — https://en.wikipedia.org/wiki/Manchester_Triage_System
4. Cynefin framework — Wikipedia — https://en.wikipedia.org/wiki/Cynefin_framework
5. Information governance — Wikipedia — https://en.wikipedia.org/wiki/Information_governance
6. Health equity — Wikipedia — https://en.wikipedia.org/wiki/Health_equity
7. Prioritization — Wikipedia — https://en.wikipedia.org/wiki/Prioritization
8. Snowden, D. & Boone, M. — *A Leader's Framework for Decision Making* (Cynefin) — Harvard Business Review — https://hbr.org/2007/11/a-leaders-framework-for-decision-making
9. DCB0129: Clinical Risk Management: its Application in the Manufacture of Health IT Systems — NHS England — https://digital.nhs.uk/services/clinical-safety/documentation
10. ITIL 4: service request categorisation and management — AXELOS / PeopleCert — https://www.peoplecert.org/itil
11. NHS Service Standard — NHS England — https://service-manual.nhs.uk/standards-and-technology/service-standard
12. Manchester Triage Group — clinical triage categorisation model — Royal College of Emergency Medicine / Manchester Triage Group — https://www.triagenet.net/
