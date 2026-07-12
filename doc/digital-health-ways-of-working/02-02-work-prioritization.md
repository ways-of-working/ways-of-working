# Chapter 2.2 — Work Prioritization

**In one sentence:** Prioritization is the deliberate, transparent ordering of the work that survived triage — balancing value, urgency, risk, and effort against finite capacity — so that at any moment the organization is doing the most valuable things it can, and can explain why.

## Why this matters in health and care

Prioritization is where strategy becomes real. An organization's true strategy is not its published plan but the order in which it actually does things — and in health and care that order carries safety, equity, and public-money consequences. Deprioritize the interoperability work and a shared care record stalls; deprioritize technical debt and a system fails at 2 a.m. on a bank holiday; deprioritize the accessibility fix and you exclude the people who need the service most.

The pressure is structural: demand always exceeds capacity, and much of that demand is legitimate. Leaders therefore need methods that make trade-offs explicit and defensible, not a process where the last email wins or every project is "top priority." Transparent prioritization also changes the political weather: when stakeholders can see the criteria and the ordering, negotiation shifts from lobbying to a shared conversation about value and cost of delay. This chapter follows intake (Chapter 2.0) and triage (Chapter 2.1); it assumes you already have a visible, assessed backlog to order, and it feeds the delivery lifecycle (Chapters 3.4–8) and portfolio management (Chapter 5.3 — EPPM).

## Core concepts

**[Prioritisation](https://en.wikipedia.org/wiki/Prioritization)** orders a backlog or portfolio; it is distinct from triage (which assessed and routed each item in isolation). Prioritization compares items *against each other* for finite capacity, and re-does that comparison as reality changes.

**[Cost of Delay](https://en.wikipedia.org/wiki/Cost_of_delay)** is the economic lens underneath the best methods: what does it cost — in value, harm, or money — for each week this is *not* done? Making cost of delay explicit reframes prioritization from "what is most important?" (everything) to "what is most expensive to delay?" (a rankable question).

**Common frameworks**, each with a fit:

- **WSJF (Weighted Shortest Job First)**, from the [Scaled Agile Framework](https://en.wikipedia.org/wiki/Scaled_agile_framework) (SAFe): score Cost of Delay (user/business value + time criticality + risk-reduction/opportunity-enablement) and divide by job size. Highest WSJF is done first. It naturally favours small, high-value, time-critical work and ignores sunk cost.
- **RICE** (Reach × Impact × Confidence ÷ Effort, popularized by Intercom): a product-management score that tempers enthusiasm with a Confidence factor.
- **[MoSCoW](https://en.wikipedia.org/wiki/MoSCoW_method)** (Must / Should / Could / Won't-this-time), from [DSDM](https://en.wikipedia.org/wiki/Dynamic_systems_development_method): a categorization, excellent for scoping a release or a fixed-date programme, weaker as a fine-grained ordering.
- **Value-versus-effort** (a 2×2): the quick visual for spotting quick wins and money pits; coarse but fast.
- **[Kano model](https://en.wikipedia.org/wiki/Kano_model)**: classifies features as basic (must-haves), performance, or delighters — useful for balancing table-stakes against differentiators.

No framework is "correct"; each encodes a different definition of value, and the act of scoring together is often more valuable than the number.

**Run versus change** is the portfolio-level balance: "keep-the-lights-on" operational work (run) versus new capability (change). Prioritization must span both, or the invisible run work — including **[technical debt](https://en.wikipedia.org/wiki/Technical_debt)** and **safety/security remediation** — loses every contest with shiny new features until it fails catastrophically.

**Capacity-based versus date-based** prioritization: capacity-based ordering fills a known, finite throughput (a sustainable pace); date-based ordering works back from an immovable deadline (a regulatory go-live) and uses MoSCoW to flex scope. Most portfolios need both, applied to different items.

## Best practices

1. **Choose one primary framework and apply it consistently.** Pick the method that fits your work — WSJF for a mixed change portfolio with real time-criticality, RICE for product feature backlogs, MoSCoW for fixed-date releases — and use it consistently so scores are comparable. Switching frameworks per item makes the backlog incomparable and invites gaming.

2. **Make Cost of Delay explicit, especially for safety and statutory work.** Ask of each item, "what does a month's delay cost?" For a safety fix or a regulatory deadline the answer is often severe and non-linear, which is precisely why these must be scored, not assumed. Cost of Delay is the common currency that lets a compliance deadline and a user-experience improvement be compared honestly.

3. **Reserve explicit capacity for run, tech debt, and safety.** Do not let keep-the-lights-on work, technical debt, and security/safety remediation compete feature-by-feature with new capability — they will lose until something breaks. Ring-fence a standing percentage of capacity (a common rule of thumb is a meaningful, protected slice) for this work, and treat it as non-negotiable.

4. **Prioritize on outcomes and value, not on requester rank.** Score against the organization's stated outcomes and priorities (ideally its [OKRs](https://en.wikipedia.org/wiki/Objectives_and_key_results) — see Chapter 10.0) rather than who asked. When a senior stakeholder's item scores low, that is the system working; the framework gives you a fair, non-personal basis to have that conversation.

5. **Match the method to the constraint: capacity or date.** For a sustainable flow of change, order by value and pull work to a known capacity. For an immovable date, work backwards and use MoSCoW to protect the "Musts" and flex the "Coulds." Confusing the two — trying to fit fixed scope into fixed time and fixed capacity — is the classic route to a failed programme.

6. **Prioritize transparently and negotiate in the open.** Publish the ranked backlog and the scoring behind it. Transparency turns prioritization from a series of private deals into a shared negotiation where trade-offs are visible: to move your item up, something else must move down, and everyone can see the cost. This is the single most powerful de-politicizing move available to a delivery leader.

7. **Re-prioritize on a regular cadence — and only then.** Set a rhythm (for example a monthly or quarterly portfolio review, plus lighter backlog refinement between) at which priorities are revisited against new evidence. Between reviews, hold the line so teams get stable runways. Constant re-prioritization is as damaging as never re-prioritizing — it destroys flow and finishes nothing.

8. **Guard against gaming and false precision.** Relative scores (Fibonacci, t-shirt sizes) are estimates, not truths; a WSJF of 8.3 is not meaningfully better than 7.9. Use the numbers to *inform* a ranked conversation, watch for inflated inputs, and let experienced judgement override an obviously perverse score — while recording why.

## Questions to discuss with your team

1. **What is our honest answer to "what does a month's delay actually cost?" for the work we keep deferring?**
   Cost of delay is the common currency that lets a compliance deadline and a user-experience tweak be compared honestly, yet most organizations never make it explicit and so default to "everything is important" — which is not a rankable statement. This matters acutely in health and care because the cost of delaying some work is severe and non-linear: a deferred safety fix or interoperability dependency can sit harmlessly for months and then fail catastrophically, while a deferred convenience feature costs almost nothing. The team should debate whether they can actually articulate the delay cost for their top contested items, and confront the uncomfortable cases where the honest answer is "very little" for a popular project and "potentially a serious incident" for an invisible one. Concrete angles: take three items currently stuck in the middle of the backlog and force a delay-cost sentence for each; ask whether technical debt and safety remediation have ever been scored on cost of delay at all, or simply lose every contest by never entering it. A good answer distinguishes items whose delay cost is roughly linear from those where it spikes at a deadline or a failure point, and uses that shape to justify the order. The dishonest version hides behind "it's all a priority," which is precisely the absence of prioritization this question is meant to expose.

2. **How much capacity are we willing to ring-fence for run, technical debt, and safety — and will we defend it when a shiny new bid arrives?**
   This is the trade-off that most reliably goes wrong: keep-the-lights-on work, technical debt, and security or safety remediation are invisible and lose feature-by-feature against new capability until something breaks at 2 a.m. on a bank holiday. The debate is not whether to protect some capacity — nearly everyone agrees in principle — but the specific percentage, and, far harder, whether leadership will actually hold that line the first time a senior sponsor's exciting project wants to raid the ring-fence. In health and care the stakes include patient safety and the reliability of systems clinicians depend on, so treating the slice as non-negotiable is a safety posture, not just good hygiene. Concrete angles: look back at the last major incident or near-miss and ask whether it traces to deferred run or debt work that never won a priority contest; name the person with authority to refuse a raid on the protected capacity and test whether they really would. A strong answer commits to a specific, protected slice and, crucially, describes the governance that keeps it protected under pressure rather than trusting good intentions. The honest version admits that the ring-fence is only real if it survives contact with the most powerful stakeholder in the room.

3. **When a senior stakeholder's item scores low, do we have the transparency and the nerve to let the ranking stand?**
   Prioritizing on outcomes rather than requester rank sounds obvious, but the HiPPO effect — the Highest-Paid Person's Opinion silently overriding the scoring — is the default failure in hierarchical NHS and government settings, and it is corrosive precisely because it is quiet. The tension is that a low-scoring senior item is often the system working correctly, yet without a transparent, published ranking and its scoring rationale, the delivery leader has no non-personal basis to have that conversation and will usually fold. The team should debate whether their backlog and scores are genuinely visible to the requesting organizations, because open trade-off negotiation — "to move yours up, which higher-scoring item moves down, and are you comfortable with that delay's cost?" — is the single most powerful de-politicizing move available, and it only works in the open. Concrete angles: recall the last time a senior request jumped the queue and ask what would have happened had the ranking been public; consider retaining the scoring rationale as a governance record you could show a board, an ICB, or auditors. A good answer pairs transparency (publish the order and the scores) with a rehearsed, non-personal script for the override conversation, and identifies who has the standing to hold it. The evasive answer treats this as a hypothetical; in reality it happens most weeks, and the plan must survive it.

4. **Have we actually committed to one prioritization framework, or are we quietly scoring each item by whatever method flatters it?**
   Choosing one primary framework and applying it consistently is what makes a backlog comparable; the moment WSJF is used for one bid, a value-versus-effort hunch for another, and "the director really wants it" for a third, the ordering stops meaning anything and gaming creeps in. The tension is that no single framework fits every kind of work — WSJF suits a mixed change portfolio, RICE a product feature backlog, MoSCoW a fixed-date release — so the honest debate is which one is your *primary* method and where a second is legitimately allowed rather than a convenient escape hatch. In health and care this matters because a compliance deadline, a clinician-requested feature, and a database upgrade must be weighed on the same scale, and only a consistent method lets a statutory item and a convenience item be ranked against each other without special pleading. Concrete angles: audit the last dozen prioritization decisions and check whether the same method was genuinely applied, or whether the method shifted to justify a predetermined answer; watch for "framework theatre," where elaborate scoring produces a number nobody then acts on. A good answer names the primary framework, explains the narrow, principled cases where another is used, and treats the score as informing a ranked conversation rather than as a truth. The weak answer lets every requester bring their own maths, which is indistinguishable from having no method at all.

5. **Are we honest about which work is capacity-bound and which is date-bound — or are we trying to fix scope, date, and capacity all at once?**
   Prioritization must match the constraint: a sustainable flow of change is ordered by value and pulled to a known capacity, while an immovable regulatory go-live is worked backwards from the date with MoSCoW protecting the "Musts" and flexing the "Coulds." The classic route to a failed programme is confusing the two — locking scope, date, and capacity simultaneously — and it is especially seductive in health and care, where a statutory deadline feels non-negotiable and stakeholders assume the full scope is equally non-negotiable. The team should debate, item by item, whether each major piece of work is really capacity-bound or date-bound, because treating a date-driven programme as if it had elastic time, or a business-as-usual flow as if it had a hard deadline, mis-prioritizes everything downstream. Concrete angles: take an immovable go-live and ask which requirements are genuinely "Must" for the legal minimum versus "Should" or "Could" that have been smuggled into the mandatory set; look for the programme where all three constraints are quietly fixed and name what will actually give when reality bites. A good answer classifies work by its binding constraint and applies the matching method deliberately, keeping capacity-based flow and date-based delivery as separate disciplines. The unrealistic answer promises full scope, on the fixed date, within fixed capacity, and hopes.

6. **What is our re-prioritization cadence, and do we have the discipline to hold the order steady between reviews?**
   Priorities must be revisited against new evidence, but on a rhythm — a monthly or quarterly portfolio review with lighter refinement between — because constant re-prioritization is as damaging as never re-prioritizing: it destroys flow and finishes nothing. The tension is real: reality genuinely changes, a new safety signal or funding shift can warrant reordering, yet every mid-flight reshuffle costs teams their runway and leaves half-built work stranded. In health and care, where delivery teams are often stretched and dependencies span multiple organizations, thrash is expensive and morale-sapping, so the stable runway between reviews is a productivity and retention issue as much as a delivery one. Concrete angles: check how many times in the last quarter the top of the backlog changed outside a scheduled review, and what shipped as a result; agree in advance the narrow criteria — a genuine emergency, not a loud stakeholder — that justify breaking cadence. A good answer sets an explicit cadence, defends the runway between reviews, and can point to work that actually finished because the order held. The failing answer re-prioritizes whenever the last email lands, mistaking motion for responsiveness while nothing crosses the line.

## In practice: a health & care example

An ICB digital portfolio team faced twelve competing bids and capacity for perhaps five. Historically the ordering had followed organizational seniority, and technical debt never featured at all. They adopted WSJF for change work and ring-fenced a fixed slice of capacity for run, tech debt, and safety.

Each bid was scored together — business value, time criticality, risk-reduction/opportunity-enablement, and job size — in a single session with delivery, clinical, and finance voices. A statutory data-returns deadline scored very high on time criticality and, being modest in size, rose to the top on WSJF. A large, popular analytics platform scored well on value but its size pushed it down the order — a result that would have been unthinkable under seniority-based ranking, and that the framework made defensible. A long-deferred database upgrade, previously invisible, was funded from the ring-fenced run slice before it could fail.

Crucially, the ranked backlog and its scores were shared with all the requesting organizations. When one trust pushed for its bid to jump the queue, the conversation was not "who do you know?" but "which of these higher-scoring items should move down, and are you comfortable with that delay's cost?" The negotiation happened in the open, and the ICB could evidence to its board that the order reflected value and cost of delay, not politics.

## Sector lenses

### Startup

A funding-constrained digital-health startup prioritizes against runway above all else, so its ordering method should be light and value-led — a value-versus-effort 2×2 or a simple RICE score is usually enough, and elaborate WSJF machinery is overkill for a backlog of thirty items. The dominant cost of delay is existential: missing the evidence a NICE evaluation or a lead customer needs can end the company, which sharply out-ranks a nice-to-have feature. The hardest discipline is reserving any capacity for technical debt and safety remediation when every week screams for the next revenue feature, yet skipping it entirely is what causes a young product to seize up just as it scales. Re-prioritization is frequent and founder-driven, so the risk is thrash — the antidote is holding a stable order for at least a short sprint so something actually ships.

### Small business

An established small provider — a GP practice, a community pharmacy, a care home, or a single-site clinic — prioritizes with almost no slack: the same handful of people run the service and any change work, so ordering has to be brutally simple, and a value-versus-effort 2×2 that anyone in the team can read is worth more than a scoring model no one has time to maintain. The dominant cost of delay is usually statutory or safety-driven — a data-security toolkit deadline, a clinical-safety fix, a mandated system upgrade from a national supplier — and these must sit at the top because a small provider carries the same duties as a large trust without the resources to absorb a failure. Discretionary improvements genuinely compete with running the service, so the honest discipline is to protect a small, regular slice of time for the non-negotiable run and remediation work rather than let it lose every week to patient-facing demands. With thin or no dedicated IT capability, much of the "how" is set by suppliers and framework contracts, so prioritization is often about sequencing supplier-driven changes and the few things the practice can control, and holding a steady order long enough that something finishes between one busy week and the next.

### Enterprise

An NHS trust or ICS runs a mixed change portfolio with genuine time-criticality and heavy run obligations, which is exactly the shape WSJF and a ring-fenced run/tech-debt/safety slice were designed for. The politics are the real challenge: multiple sponsoring organizations, HiPPO pressure, and legacy expectations that seniority sets the order, so transparency of the ranked backlog and its scores is the enterprise's chief de-politicizing tool. Prioritization here spans a portfolio office and must reconcile capacity-based flow for business-as-usual change with date-based programmes working back from immovable regulatory go-lives, flexing scope via MoSCoW. Because a trust must evidence value-for-money to its board, an ICB, and auditors, the scoring rationale is retained as a governance record, not discarded once the decision is made.

### Government

At NHS England, DHSC, or a devolved government, prioritization is portfolio management at national scale, formalized through Management of Portfolios (MoP) and the Treasury five-case model, where cost of delay is measured in population health, statutory compliance, and billions of pounds. Much of the portfolio is non-discretionary — mandated returns, legal deadlines, ministerial commitments — so the method must rank the *how* and *when* of obligated work rather than whether to do it, and immovable-date programmes dominate. Risk appetite is low and scrutiny is adversarial: the National Audit Office and Public Accounts Committee will test whether the order reflected value and cost of delay or merely political convenience, so an explicit, published prioritization basis is a defence as much as a management tool. Equity is a statutory dimension of value, so a government scoring model should weight impact on the least-served populations, not just aggregate benefit, or it will systematically favour the already well-served.

## Common failure modes

- **Everything is priority one.** No real ordering exists, so the loudest voice or nearest deadline governs. *Fix:* force a strict rank; ties are not allowed at the top.
- **Run and tech debt always lose.** Invisible operational and remediation work is starved until it fails. *Fix:* ring-fenced, protected capacity.
- **HiPPO override.** The Highest-Paid Person's Opinion silently overrides the scoring every time. *Fix:* transparent scores and open trade-off negotiation.
- **Framework theatre.** Elaborate scoring produces a number nobody acts on. *Fix:* let the score inform a real, acted-on ranked order.
- **Fixed scope + fixed date + fixed capacity.** All three constraints locked, guaranteeing failure. *Fix:* flex scope via MoSCoW, or capacity, or date.
- **Thrash.** Priorities change weekly; nothing finishes. *Fix:* a set re-prioritization cadence and stable runways between.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| **Method & basis** | No method; order by seniority or deadline | A framework used inconsistently or for some work only | One primary framework applied consistently; Cost of Delay considered | Scoring inputs governed and calibrated; prioritization decisions measured against stated outcomes | Framework tuned to outcomes/OKRs; capacity- and date-based methods used deliberately |
| **Run/change & tech debt balance** | Run and tech debt invisible; only new work funded | Some awareness of run/debt but no protected capacity | Ring-fenced capacity for run, tech debt, and safety | Protected slice tracked as a metric; run/debt and safety remediation assured against target | Run/change balance actively managed and reviewed against value |
| **Transparency & cadence** | Priorities opaque; changed reactively and constantly | Backlog partly visible; irregular reviews | Ranked backlog published; fixed re-prioritization cadence | Cadence adherence and re-prioritization churn tracked; scoring rationale retained as a governed record for boards and auditors | Open trade-off negotiation is the norm; cadence stable; scores sanity-checked against results |

## Checklist

- [ ] One primary prioritization framework is chosen and applied consistently.
- [ ] Cost of Delay is made explicit, especially for safety and statutory work.
- [ ] Capacity is ring-fenced for run, technical debt, and safety/security work.
- [ ] Items are scored against outcomes/OKRs, not requester seniority.
- [ ] Capacity-based and date-based methods are used for the right items.
- [ ] The ranked backlog and its scoring are published to stakeholders.
- [ ] Trade-offs are negotiated in the open: to move one up, another moves down.
- [ ] Re-prioritization happens on a set cadence, with stable runways between.
- [ ] Scores are treated as estimates; gaming and false precision are watched for.
- [ ] The current order can be explained and defended to the board.

## Key sources

- Scaled Agile Framework (SAFe) — Weighted Shortest Job First (WSJF) and Cost of Delay.
- Reinertsen, D. — *The Principles of Product Development Flow* (Cost of Delay, queueing economics).
- Intercom — the RICE scoring model (Reach, Impact, Confidence, Effort).
- DSDM / Agile Business Consortium — MoSCoW prioritisation.
- Kano, N. — the Kano model of customer satisfaction.
- Cabinet Office / AXELOS — Management of Portfolios (MoP) — portfolio prioritisation and balance.
- NHS Digital Service Standard & GOV.UK Service Manual — prioritising the most important user needs; OKRs (Doerr, *Measure What Matters*) for outcome alignment.

## References

1. Prioritization — Wikipedia — https://en.wikipedia.org/wiki/Prioritization
2. Cost of delay — Wikipedia — https://en.wikipedia.org/wiki/Cost_of_delay
3. Scaled agile framework — Wikipedia — https://en.wikipedia.org/wiki/Scaled_agile_framework
4. MoSCoW method — Wikipedia — https://en.wikipedia.org/wiki/MoSCoW_method
5. Dynamic systems development method — Wikipedia — https://en.wikipedia.org/wiki/Dynamic_systems_development_method
6. Kano model — Wikipedia — https://en.wikipedia.org/wiki/Kano_model
7. Technical debt — Wikipedia — https://en.wikipedia.org/wiki/Technical_debt
8. Objectives and key results — Wikipedia — https://en.wikipedia.org/wiki/Objectives_and_key_results
9. Weighted Shortest Job First (WSJF) and Cost of Delay — Scaled Agile Framework (SAFe) — https://framework.scaledagile.com/wsjf
10. Reinertsen, D. — *The Principles of Product Development Flow* — Celeritas Publishing — https://www.celeritas.com/
11. The RICE scoring model (Reach, Impact, Confidence, Effort) — Intercom — https://www.intercom.com/blog/rice-simple-prioritization-for-product-managers/
12. MoSCoW prioritisation — DSDM / Agile Business Consortium — https://www.agilebusiness.org/dsdm-project-framework/moscow-prioritisation.html
13. Management of Portfolios (MoP) — AXELOS / Cabinet Office — https://www.axelos.com/
14. Doerr, J. — *Measure What Matters* (OKRs) — Portfolio/Penguin — https://www.whatmatters.com/
15. The Green Book: appraisal and evaluation in central government (five-case model) — HM Treasury — https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-government
