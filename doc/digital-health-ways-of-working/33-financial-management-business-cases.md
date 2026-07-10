# Chapter 33 — Financial Management & Business Cases

**In health and care, a business case is not a funding formality but a clinical, ethical, and public-trust argument: it commits scarce public money to one patient benefit instead of another, and you are accountable for both the spending and the outcome.**

## Why this matters in health and care

Every pound you spend on a digital service is a pound not spent on a hip replacement, a district nurse, or a mental-health crisis line. That is the uncomfortable truth beneath financial management in health and care. You are not deploying private capital in pursuit of a return to shareholders; you are stewarding public money raised through taxation, and the people who pay are also the people who depend on the services you fund. A weak business case does not merely waste money — it diverts care from people who needed it and erodes the public trust that lets the system function at all.

The financial rules of UK health and care are also genuinely different from those of a commercial organisation, and directors who ignore this get caught out. Money arrives in fixed annual envelopes, split into capital and revenue with a firm wall between them. Approvals run through layered spend controls that can add months. Benefits are frequently non-cash — hours of clinical time released, harm avoided, waits reduced — so they never show up cleanly in a profit-and-loss account and are easy to overstate on the way in and forget on the way out. And the standard appraisal method, the HM Treasury Green Book with its Five Case Model, is not optional guidance you can route around: for material investment it is the language in which your case will be judged.

Getting this right is a safety and equity issue as much as a money issue. Underfunding the boring parts — service management, cyber resilience, accessibility, benefits tracking — is how digital services quietly decay until they fail patients. Overstating benefits is how organisations sink money into products that never deliver the clinical time they promised. Your job as a director is to get money approved, spend it well, and prove afterwards that it did what you said it would.

## Core concepts

A [business case](https://en.wikipedia.org/wiki/Business_case) is the structured argument for why an investment should be made and how it will be delivered and controlled. In UK central government and the NHS, business cases follow the Five Case Model set out in HM Treasury's Green Book, which requires five linked arguments: the *strategic case* (why this is needed and how it fits strategy), the *economic case* (which option delivers best public value), the *commercial case* (whether it is deliverable through the market), the *financial case* (whether it is affordable), and the *management case* (whether you can actually deliver it). A case that is strong on strategy but silent on affordability or delivery is not a case at all.

Business cases progress through three stages as certainty grows: the Strategic Outline Case (SOC) establishes the need and a preferred way forward; the Outline Business Case (OBC) identifies the preferred option after detailed appraisal; and the Full Business Case (FBC) confirms arrangements after procurement, immediately before contract signature and full spend. Each stage is a decision gate, and the effort you invest should match the money at stake.

The economic case rests on comparing options by value. [Cost–benefit analysis](https://en.wikipedia.org/wiki/Cost%E2%80%93benefit_analysis) values costs and benefits in money and nets them off; [cost-effectiveness analysis](https://en.wikipedia.org/wiki/Cost-effectiveness_analysis) compares cost per unit of outcome when the outcome resists monetary valuation, which is common in health. The detailed valuation of health outcomes — quality-adjusted life years, willingness-to-pay thresholds — belongs to Chapter 34 — Health Economics; here you need to know which method your case demands and why. Both methods discount future cash flows to present value, so understanding [net present value](https://en.wikipedia.org/wiki/Net_present_value) matters when you compare options with different timing.

Two cost concepts protect you from short-termism. [Whole-life cost](https://en.wikipedia.org/wiki/Whole-life_cost), and its close cousin [total cost of ownership](https://en.wikipedia.org/wiki/Total_cost_of_ownership), count everything from build through years of operation, support, licensing, and eventual decommissioning — not just the shiny implementation cost. Ignoring these is the single most common way a "cheap" option turns out ruinously expensive. Meanwhile [opportunity cost](https://en.wikipedia.org/wiki/Opportunity_cost) — the value of the best alternative you gave up — is the real price of any choice in a fixed budget, and it should be explicit in every prioritisation conversation.

Two further concepts shape credibility. [Optimism bias](https://en.wikipedia.org/wiki/Optimism_bias) is the well-documented human tendency to underestimate cost and time and overestimate benefit; the Green Book requires you to correct for it with explicit uplifts to your estimates. And [benefits realisation management](https://en.wikipedia.org/wiki/Benefits_realisation_management) is the discipline of defining, tracking, and actually banking the benefits you promised, rather than declaring victory at go-live and moving on. Finally, the NHS distinction between [capital expenditure](https://en.wikipedia.org/wiki/Capital_expenditure) and revenue spending — the Capital and Revenue Departmental Expenditure Limits, CDEL and RDEL — governs which money you can spend on what, and is explained in the best-practices section because it trips up almost everyone.

## Best practices

1. **Write the Five Case Model as one argument, not five documents.** The strategic, economic, commercial, financial, and management cases must reinforce each other. A common failure is a compelling strategic case bolted to a financial case that does not add up or a management case that names no accountable owner and no delivery plan. Draft the cases together, check they tell a consistent story, and make sure the benefits claimed in the economic case are the same benefits your management case commits to tracking. Reviewers approve coherence; they reject cases that contradict themselves.

2. **Match the business-case stage to the decision, and do not over-engineer early cases.** A Strategic Outline Case should be light — enough to test the need and secure permission to invest in a proper Outline Business Case. Reserve deep appraisal for the OBC, when you are choosing between real options, and confirm arrangements at Full Business Case after procurement. Spending months on a granular FBC-quality analysis before you have even confirmed the need wastes effort and delays value; conversely, rushing an FBC on the back of a thin SOC invites nasty surprises after contracts are signed. See Chapter 4 — Evidence-Driven Decisions for how to calibrate the evidence you gather to the weight of the decision.

3. **Cost the whole life, not the launch.** Estimate the total cost of ownership across the realistic service life: build, licences, hosting, third-line support, clinical safety maintenance, security patching, accessibility upkeep, and decommissioning. Digital services are not one-off projects that end at go-live; they are living systems that cost money every year they run. A business case that shows a large capital build with no honest revenue tail for operations is not affordable — it is a future crisis. Chapter 21 — Service Management & Live Operations describes what those running costs actually buy.

4. **Correct for optimism bias explicitly, then reduce it with evidence.** Apply the Green Book's optimism-bias uplifts to cost and duration, and state your assumptions plainly. Better still, narrow the uplift with reference-class forecasting: look at what comparable projects actually cost and how late they ran, and anchor your estimates to that reality rather than to your team's best-case hopes. Reviewers trust a case that names its uncertainty and shows how it will be managed far more than one that presents suspiciously precise single-point numbers.

5. **Design benefits so they cannot quietly evaporate.** For every benefit you claim, name the metric, the baseline, the owner, and the date by which it must be visible. If the benefit is released clinical time, say who will use that time for what, because "hours saved" that are never redeployed are not benefits — they are a spreadsheet fiction. Build benefits tracking into the operating model from day one and report against it after go-live, not just at approval. This is the difference between a case that promised value and a case that delivered it.

6. **Respect the capital–revenue wall and plan for it.** In the NHS, capital (CDEL) and revenue (RDEL) budgets are separate and tightly controlled, and you generally cannot move freely between them. Cloud-hosted, subscription-based digital products are largely revenue spending, which can clash with an organisation's capital-heavy funding and its annual capital cycle. Work out early which envelope funds which part of your case, secure a recurring revenue line for the years of operation, and never assume a one-off capital grant will keep the lights on. Getting this wrong is how funded builds die for want of running costs.

7. **Make opportunity cost visible in every prioritisation.** Because the budget is fixed, funding your case means not funding something else. State what you are displacing and why this investment delivers more public value. This honesty strengthens your case with boards who see too many proposals presented as free, and it aligns your financial argument with portfolio decisions made through Chapter 31 — Enterprise Project Portfolio Management (EPPM).

8. **Plan the approval and spend-controls route before you need it.** Material NHS and central-government digital spend passes through layered approvals — internal capital groups, regional or Integrated Care Board sign-off, and national spend controls above defined thresholds — and these add time. Map the route, thresholds, and evidence each gate expects at the start, and sequence your case so approvals do not block delivery. Coordinate with procurement early, because commercial and financial approvals interlock; Chapter 36 — Procurement & Commercial covers that handshake.

## Questions to discuss with your team

1. **Are the benefits in our business case real, owned, and trackable — or are they decoration to get money approved?** Walk through each claimed benefit and ask whether it has a named owner who will be accountable after go-live, a baseline you can actually measure today, and a credible mechanism by which it converts into value. Released clinical time is the classic trap: hours "saved" that no one plans to redeploy deliver nothing. Interrogate whether cash-releasing benefits will genuinely leave the budget or merely shift work around. Discuss how you will report benefits realisation quarterly after launch, not just claim it at approval. Consider what happens, and who is accountable, if a benefit does not materialise. Be honest about which benefits are firm and which are aspirational, and label them as such in the case. A team that cannot answer these questions has written a funding request, not a business case.

2. **Do we understand the whole-life cost, and have we secured recurring revenue to run this for years?** Push past the implementation cost to the total cost of ownership across the service's realistic life, including support, licensing, security, accessibility, and eventual replacement. Ask specifically which parts are capital (CDEL) and which are revenue (RDEL), and whether you have a committed recurring revenue line or merely a one-off capital pot that ends at go-live. Discuss how the annual capital cycle interacts with a product that needs continuous, predictable funding to stay safe and useful. Consider what the service will cost in year three and year five, not just year one. Explore what you will decommission or stop funding to make room for these running costs. If the answer to "who pays to run this next year" is unclear, you have found the biggest risk in the case.

3. **Where is optimism bias hiding in our numbers, and what would an honest sceptic say?** Examine your cost and timeline estimates and ask whether they reflect what comparable projects actually cost or what you hope this one will cost. Discuss whether you have applied Green Book optimism-bias uplifts and whether you can narrow them with reference-class evidence from similar deliveries. Consider inviting someone outside the team to challenge the estimates before the board does. Ask what assumptions, if wrong, would break the case, and how sensitive the conclusion is to each. Talk about how you present uncertainty honestly without undermining the case — a well-managed risk is more credible than a false precision. Think about the incentive to lowball costs to clear an affordability threshold, and how that always surfaces later as an overspend. A case that survives friendly scepticism will survive the real thing.

## In practice: a health & care example

An Integrated Care Board (ICB) wants to fund a shared digital platform that lets community nurses, GPs, and social-care teams see a single coordinated care record for people with complex long-term conditions. The director of digital, Priya, is asked to build the business case.

She starts with a Strategic Outline Case, deliberately light: the strategic case links the platform to the ICB's aim of reducing avoidable admissions among frail patients, and to the operating model in Chapter 2. It secures permission to invest in a proper appraisal. At Outline Business Case stage she works through the Five Case Model in earnest. The economic case uses cost-effectiveness analysis rather than pure cost–benefit analysis, because the core benefit — avoided admissions and released community-nursing time — resists clean monetary valuation; she hands the health-outcome valuation to her health-economics colleague per Chapter 34. She appraises a shortlist against a "do minimum" baseline and calculates each option's whole-life cost over seven years, not just the build.

The numbers force honesty. The implementation cost is capital, but the platform is a cloud subscription, so the bulk of the seven-year cost is recurring revenue — RDEL — that the ICB must commit annually. Priya applies Green Book optimism-bias uplifts to cost and timeline, then narrows them using data from two neighbouring ICBs that ran similar programmes; both overran their first estimates by roughly a third, which she now builds in. For benefits, she names an owner for each: the chief nurse owns "community-nursing hours released" and commits to redeploying them to proactive visits, so the benefit does not evaporate into an untracked spreadsheet line.

At the board, a non-executive challenges affordability. Priya is ready: she states the opportunity cost plainly — this platform means deferring a separate diagnostics project — and shows the recurring revenue line secured for all seven years. The board approves the OBC. After procurement, the Full Business Case confirms the supplier and final costs, and it passes national spend-control review because the route was mapped from the start. Eighteen months after go-live, the quarterly benefits report shows admissions down and evidence that released nursing hours were actually redeployed — because someone was accountable for making that happen.

## Three sector lenses

### Startup

A digital-health startup selling into the NHS lives on the other side of these business cases, and understanding them is a commercial advantage. Your buyer needs a Five Case argument to justify purchasing your product, so package evidence that helps them: credible whole-life cost figures, realistic benefit estimates they can defend, and reference data from comparable deployments that narrows their optimism-bias adjustment. Be honest about running costs, because a case built on unrealistic savings collapses at the first benefits review and poisons the relationship. Startups that help customers build defensible cases — rather than pushing inflated return-on-investment claims — win renewals, because the same discipline of tracking whether promised value actually landed protects your credibility with every future buyer.

### Enterprise

A large NHS trust or arms-length body runs the full apparatus: Five Case Model, SOC–OBC–FBC progression, capital and revenue controls, and layered internal approvals before national spend controls. The strength here is rigour; the risk is that the process becomes theatre, where cases are written to clear gates rather than to make good decisions, and benefits are claimed at approval then never tracked. Guard against a widening gap between the confident numbers in the business case and the reality after go-live. Invest in genuine benefits realisation and portfolio-level visibility (Chapter 31) so the organisation learns from what it funded. Enterprises that treat the business case as a live instrument, revisited and reconciled against reality, spend far better than those that treat it as a one-time hurdle.

### Government

At regional and national level — an ICB, NHS England, or a government department — you set the appraisal rules others follow and you steward the largest envelopes, so the Green Book, capital–revenue distinction, and spend controls are your native language. Your challenge is that annual capital cycles and rigid CDEL/RDEL splits clash badly with modern digital products that need continuous revenue funding, and this mismatch quietly kills good work. Use your position to push for funding models that fund products through their life, not just projects to a go-live. Hold the system to honest benefits realisation across portfolios, and resist the pressure to approve cases on optimistic numbers to hit political timelines. Chapter 51 — Working with Local & National Governments explores this stewardship role further.

## Common failure modes

- **Benefits that evaporate.** Value is claimed at approval — released time, avoided harm — but no one owns it, tracks it, or redeploys it, so it never materialises. This is the most common and most damaging failure.
- **Ignoring whole-life cost.** The case shows an attractive build cost and stays silent on the years of operation, support, and licensing, so a "cheap" option becomes a running-cost crisis.
- **Optimism-bias theatre.** Estimates are lowballed to clear an affordability threshold, uplifts are applied token-only or not at all, and the overspend surfaces after commitment when it is too late to change course.
- **Capital–revenue mismatch.** A product needing recurring revenue is funded with one-off capital, or the capital–revenue split is worked out too late, and the funded build dies for want of running money.
- **A five-case document that does not cohere.** Each case is written in isolation; the benefits in the economic case are not the benefits the management case tracks, and the financial case does not reconcile to the economic one.
- **Approval surprise.** Spend-control thresholds and the approval route are discovered late, adding months and forcing rushed, weakened cases against a deadline.
- **Gaming the gate.** Cases are written to pass review rather than to make a good decision, so the organisation learns nothing and repeats its mistakes.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Business-case rigour | Ad hoc funding requests; no consistent structure | Five Case Model used for large cases only | Five Case Model and SOC/OBC/FBC applied proportionately across investments | Cases are living instruments, reconciled against reality and used to improve future appraisal |
| Whole-life costing | Only build cost estimated | Running costs acknowledged but not fully quantified | Total cost of ownership estimated across service life | Whole-life cost tracked against actuals and fed back into estimates |
| Benefits realisation | Benefits claimed at approval, never tracked | Benefits defined but ownership weak | Every benefit has owner, baseline, metric, and date; tracked post-go-live | Benefits reported at portfolio level; unrealised benefits trigger action and learning |
| Bias and uncertainty | Single-point optimistic estimates | Green Book uplifts applied mechanically | Uplifts narrowed with reference-class data; sensitivity analysis shown | Estimating accuracy improves measurably over time from banked evidence |
| Funding and approvals | Capital–revenue confusion; approvals discovered late | Splits understood; approval route mapped for major cases | Recurring revenue secured; approval route planned from the start | Funding models flex to fund products through life, not just to go-live |

## Checklist

- [ ] The case is structured as one coherent Five Case argument, not five disconnected documents.
- [ ] The business-case stage (SOC, OBC, or FBC) matches the decision and the money at stake.
- [ ] Whole-life cost / total cost of ownership is estimated across the realistic service life, including operations, support, security, and decommissioning.
- [ ] Capital (CDEL) and revenue (RDEL) portions are identified, and a recurring revenue line is secured for the years of operation.
- [ ] Optimism-bias uplifts are applied and, where possible, narrowed with reference-class evidence from comparable deliveries.
- [ ] Every claimed benefit has a named owner, a baseline, a metric, and a date, with a plan to bank it after go-live.
- [ ] Opportunity cost is stated: what this investment displaces and why it delivers more public value.
- [ ] The correct appraisal method (cost–benefit or cost-effectiveness) is used, with health-outcome valuation handled per Chapter 34.
- [ ] The approval and spend-controls route, with thresholds, is mapped and sequenced so it does not block delivery.
- [ ] Sensitivity analysis shows which assumptions, if wrong, would break the case.
- [ ] A post-go-live benefits realisation report is scheduled and owned.

## Key sources

- HM Treasury, *The Green Book: appraisal and evaluation in central government* — the definitive UK appraisal guidance, including the Five Case Model and optimism-bias adjustment.
- HM Treasury and the UK Government Finance Function, *Guide to Developing the Project Business Case* (the "Five Case Model" guidance) — how to write SOC, OBC, and FBC.
- NHS England, guidance on capital and revenue (CDEL/RDEL) budgeting and business-case approvals.
- Infrastructure and Projects Authority (IPA), guidance on benefits management and reference-class forecasting.
- Association for Project Management (APM), *Benefits Realisation Management* body of knowledge.

## References

1. Business case — Wikipedia — https://en.wikipedia.org/wiki/Business_case
2. Cost–benefit analysis — Wikipedia — https://en.wikipedia.org/wiki/Cost%E2%80%93benefit_analysis
3. Cost-effectiveness analysis — Wikipedia — https://en.wikipedia.org/wiki/Cost-effectiveness_analysis
4. Net present value — Wikipedia — https://en.wikipedia.org/wiki/Net_present_value
5. Whole-life cost — Wikipedia — https://en.wikipedia.org/wiki/Whole-life_cost
6. Total cost of ownership — Wikipedia — https://en.wikipedia.org/wiki/Total_cost_of_ownership
7. Opportunity cost — Wikipedia — https://en.wikipedia.org/wiki/Opportunity_cost
8. Optimism bias — Wikipedia — https://en.wikipedia.org/wiki/Optimism_bias
9. Benefits realisation management — Wikipedia — https://en.wikipedia.org/wiki/Benefits_realisation_management
10. Capital expenditure — Wikipedia — https://en.wikipedia.org/wiki/Capital_expenditure
11. The Green Book: appraisal and evaluation in central government — HM Treasury (GOV.UK) — https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-government
12. Guide to Developing the Project Business Case (Five Case Model) — HM Treasury (GOV.UK) — https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-government/the-green-book-2020
13. NHS capital regime, investment and property business case approvals guidance — NHS England — https://www.england.nhs.uk/publication/capital-regime-investment-and-property-business-case-approval-guidance-for-nhs-trusts-and-foundation-trusts/
14. Benefits Realisation Management — Association for Project Management (APM) — https://www.apm.org.uk/resources/what-is-project-management/what-is-benefits-management-and-project-success/
