# Chapter 35 — Health Economics

**Health economics is how you turn "we built a thing and people used it" into a defensible claim that your digital service made a population healthier for the money it consumed — and the discipline that stops you fooling yourself.**

## Why this matters in health and care

Every pound spent on a digital service is a pound not spent on something else — a district nurse, a diagnostic scanner, a mental-health worker. In a tax-funded system with fixed budgets, that trade-off is not abstract; it is the daily reality of every integrated care board (ICB) finance meeting. If your service consumes resource without producing health, someone somewhere gets less care. That is the moral weight [health economics](https://en.wikipedia.org/wiki/Health_economics) places on your work.

Digital delivery leaders routinely over-claim on the wrong evidence. They report that an app was downloaded two hundred thousand times, that a portal sent a million messages, that appointments were "saved" — and mistake this activity for benefit. Activity is not health. A message delivered to someone who ignores it changes nothing; an appointment "saved" that pushes a patient into an avoidable admission has made things worse. Without a disciplined way to distinguish what you *did* from what *changed*, you cannot tell a genuinely valuable service from an expensive placebo.

Consistent, comparable measurement is also a matter of equity and public trust. If each service invents its own metric, no one can weigh a diabetes app against a falls-prevention service against a new triage tool. The whole point of a shared unit of value is that it lets you compare unlike things and allocate scarce resource honestly across a population — including to the people whose health is worst and whose voices are quietest. This chapter gives you the vocabulary and the guardrails to do that. It builds on Chapter 4 — Evidence-Driven Decisions and Chapter 34 — Financial Management & Business Cases, and feeds Chapter 54 — Objectives & Key Results (OKRs).

## Core concepts

Start with the distinction that trips up most digital programmes: **outputs versus outcomes**. Outputs are the activity you produce — appointments delivered, messages sent, users onboarded, referrals processed. Outcomes are the change in health or wellbeing that follows — symptoms reduced, admissions avoided, life extended, quality of life improved. Outputs are cheap to count and easy to game; outcomes are what the system exists to create. A [logic model](https://en.wikipedia.org/wiki/Logic_model) makes the link explicit by mapping **inputs → activities → outputs → outcomes → impact**, forcing you to state the causal chain by which your spend becomes health, and to expose the assumptions in it.

Value in health and care is best framed in terms of [population health](https://en.wikipedia.org/wiki/Population_health): the health outcomes of a defined group and the distribution of those outcomes within it. Population health management is the operational practice of using linked data to segment a population, target interventions, and track whether the whole group — not just the enthusiastic early adopters — got healthier. This framing matters because a digital service can improve the average while widening the gap, and a system accountable for a population must watch both.

To compare value across unlike interventions you need a common currency for health. The dominant one is the [quality-adjusted life year](https://en.wikipedia.org/wiki/Quality-adjusted_life_year) (QALY), which combines length of life and quality of life into a single number: one year in full health equals one QALY, a year at half quality equals 0.5 QALY, and death equals zero. Quality of life is usually measured with a standardised instrument such as the [EQ-5D](https://en.wikipedia.org/wiki/EQ-5D), a short questionnaire covering five dimensions (mobility, self-care, usual activities, pain/discomfort, anxiety/depression) that converts a patient's self-report into a single utility score. The [disability-adjusted life year](https://en.wikipedia.org/wiki/Disability-adjusted_life_year) (DALY) is a complementary measure — years of healthy life *lost* to illness and premature death — used heavily in public-health and global burden-of-disease work; QALYs measure health gained, DALYs measure health lost.

Economic evaluation then compares cost against effect. [Cost-effectiveness analysis](https://en.wikipedia.org/wiki/Cost-effectiveness_analysis) (CEA) expresses value as cost per unit of a natural outcome (for example, cost per case detected). [Cost–utility analysis](https://en.wikipedia.org/wiki/Cost%E2%80%93utility_analysis) (CUA) is the special case that uses QALYs as the outcome, so different interventions become directly comparable. The headline statistic is the [incremental cost-effectiveness ratio](https://en.wikipedia.org/wiki/Incremental_cost-effectiveness_ratio) (ICER): the *extra* cost of your intervention divided by the *extra* QALYs it produces, relative to whatever it replaces. In the United Kingdom, the National Institute for Health and Care Excellence (NICE) commonly judges interventions against a cost-effectiveness threshold in the region of £20,000–£30,000 per QALY, above which an intervention is generally considered poor value — though this is a decision aid, not a mechanical rule, and higher thresholds apply in specific circumstances such as end-of-life or highly specialised care.

Underneath all this sit two efficiencies. Technical efficiency is doing a given thing at least cost (delivering the same outcomes with fewer inputs). Allocative efficiency is doing the *right* things — distributing resource across competing uses so total population health is maximised. The bridge between them is [opportunity cost](https://en.wikipedia.org/wiki/Opportunity_cost): the value of the best alternative you gave up. Every "yes" in a fixed budget is a silent "no" to something else, and the discipline of health economics is to make that silent no visible.

Two further families of measure keep the patient in view. [Patient-reported outcome](https://en.wikipedia.org/wiki/Patient-reported_outcome) measures (PROMs) capture health status as the patient reports it — did the pain, function, or quality of life actually change. Patient-reported experience measures (PREMs) capture what the encounter was like — was it accessible, respectful, coordinated. Outcomes tell you whether the service worked; experience tells you whether people can and will use it, which is itself a determinant of outcome.

Finally, hold the honest critique. QALYs embed value judgements — they can systematically undervalue interventions for older, disabled, or already-unwell people, because such people have fewer or lower-quality life-years available to gain. This is the equity critique, and it connects directly to [health equity](https://en.wikipedia.org/wiki/Health_equity) and the reduction of health inequalities. Some frameworks respond with explicit *equity weighting*, giving greater value to health gains for the worst-off. You do not have to resolve this debate, but you must not pretend the QALY is value-neutral.

## Best practices

1. **Define your primary outcome measure before you build anything.** The single most common failure in digital health economics is retrofitting an outcome to a service that is already live, at which point no baseline exists and any claim is contestable. Decide up front what health change you expect, how you will measure it (a validated PROM, a routine clinical metric, a linked-data outcome such as admissions), and what "success" looks like numerically. Write it into the business case (Chapter 34 — Financial Management & Business Cases) so evaluation is a design constraint, not an afterthought.

2. **Build a logic model and put it on the wall.** Map inputs, activities, outputs, outcomes, and impact for your service, and name the assumption on every arrow. The value of the exercise is that it exposes the weak links — the step where "people receive a reminder" is assumed to become "people attend and get healthier" — so you can test exactly those. Revisit it each phase; a logic model that never changes is a logic model no one is using.

3. **Report outputs and outcomes separately, and never let outputs stand in for outcomes.** It is legitimate to track activity as a leading indicator and an operational health check, but label it as such. In every board pack, pair the output with the outcome it is meant to drive and the assumption connecting them, so no one can quietly promote "messages sent" into "lives improved." If you only have outputs so far, say so plainly and state when outcome data will arrive.

4. **Choose a comparable unit of value and stick to it.** Where you plausibly affect length and quality of life, use QALYs (via CUA) so your service can be weighed against others in the portfolio. Where a QALY is a poor fit — many digital services shift experience, access, or process rather than measurable health state — use a defensible intermediate outcome and be explicit that it is not directly comparable to a QALY. Consistency across your portfolio matters more than sophistication in any one case: comparable-but-simple beats brilliant-but-unique.

5. **Compute value at the margin, not the average.** Decisions are incremental, so the number that matters is the ICER: the extra cost per extra QALY versus the realistic alternative (usual care, or the tool you would decommission). Averages flatter you; a service can look cheap per user yet deliver almost no additional health over what people already had. Always name your comparator explicitly, because the ICER is meaningless without it.

6. **Make opportunity cost explicit in every recommendation.** State what you would *stop* or forgo to fund this, and what health the population loses by that choice. This turns a one-sided "invest in our thing" pitch into an allocative-efficiency argument a finance director can trust. It also disciplines your own thinking: if you cannot name a credible thing worth displacing, the case is probably weaker than it looks.

7. **Measure the distribution, not just the mean — and weight for equity where you can.** Break outcomes down by deprivation, age, ethnicity, disability, and digital access, and check whether your service narrowed or widened gaps (see Chapter 9 — Digital Inclusion & Accessibility). A service that improves the average by helping the already-advantaged is failing the population-health test. Where your organisation has an equity-weighting or health-inequalities framework, apply it, and at minimum report equity impact alongside the headline ICER.

8. **Use NICE's Evidence Standards Framework to right-size your evidence.** NICE's Evidence Standards Framework for Digital Health Technologies (ESF) tiers evidence expectations by the risk and function of the product, so a simple information tool is not held to the same bar as a treatment-guiding algorithm. Use it early to decide what evidence you genuinely need — and pair it with the Digital Technology Assessment Criteria (DTAC) for the safety, clinical-safety, and interoperability baseline (Chapters 6 and 26). Right-sizing prevents both under-evidenced hype and paralysing over-evidencing.

9. **Prefer routine, linked data and validated instruments over bespoke surveys.** Wherever possible measure outcomes through data the system already collects — attendances, admissions, prescriptions, coded clinical results — linked at population level, so your evidence is comparable, cheap to sustain, and hard to game. Where you need patient report, use validated PROMs and PREMs rather than inventing questions, so your numbers mean the same thing as everyone else's. Handle all of this within your information-governance and data-protection duties (Chapter 7).

10. **Plan the evaluation and its funding at the same time as the build.** Economic evaluation is not free; it needs a baseline, a comparator, analytic capability, and time before benefits mature. Budget for it explicitly, agree who is accountable for the evaluation, and set honest timeframes — many population-health outcomes take one to three years to move. An unfunded evaluation is a decision to never really know whether the money bought health.

## Questions to discuss with your team

1. **What is the single health outcome this service must change, and how will we know we changed it rather than merely observed it changing?** This forces the team past comfortable activity metrics to the causal claim underneath. Debate whether your chosen measure is truly an outcome (a change in health or wellbeing) or a dressed-up output, and whether you can attribute the change to your service rather than to secular trend, regression to the mean, or a parallel initiative. Consider whether a randomised or stepped-wedge design is feasible, or whether you will rely on a well-constructed before-and-after with a matched comparator. Talk honestly about the baseline: do you have one, and if not, is it already too late to get it. A good answer names one primary outcome, a measurement instrument, a comparator, a plausible attribution story, and the date by which you will have real data — and admits what you cannot yet prove.

2. **When our outputs look great but our outcomes are flat, what will we do?** Every digital team eventually faces a service with soaring usage and no measurable health gain, and the honest response is uncomfortable. Discuss in advance what evidence would make you iterate, pause, or decommission, so the decision is not hostage to sunk cost and reputational face-saving. Surface the tension between operational leaders who are rewarded for activity and finance or public-health leaders accountable for population outcomes, because they will read the same dashboard differently. Consider whether flat outcomes mean the service does not work, or that you are measuring the wrong outcome, or that benefits lag — and how you would tell these apart. A good answer sets stopping and pivoting criteria now, in writing, and names who owns the call.

3. **Whose health are we improving, and whose are we leaving behind or actively disadvantaging?** The QALY and the average both hide distribution, and a service can raise the mean while widening inequality — often by working best for the confident, connected, digitally included. Debate which groups are likely to gain least (people with low digital access, sensory or cognitive impairment, limited English, the most deprived) and whether the service risks diverting resource away from them. Discuss whether to apply equity weighting, or at least to report outcomes disaggregated by deprivation and protected characteristics, and what you would change if the gap widened. Weigh the tension between technical efficiency (cheapest average gain) and allocative fairness (gain for those in greatest need). A good answer commits to measuring distribution from the start and states a clear position on the equity trade-off rather than hiding behind a single headline number.

## In practice: a health & care example

An ICB commissions a digital remote-monitoring service for people with moderate-to-severe heart failure: patients weigh themselves and answer a short symptom check daily on an app, and a nursing team reviews flagged cases. The supplier's pitch leads with outputs — thirty thousand readings a month, 82% daily adherence, four thousand alerts triaged — and a claim of "reduced admissions."

The delivery lead insists on a logic model before go-live. It reads: inputs (app licences, nursing time, devices) → activities (daily monitoring, triage, early medication adjustment) → outputs (readings, alerts, contacts) → outcomes (fewer unplanned heart-failure admissions, better symptom control) → impact (QALYs gained, sustainable secondary-care demand). The weak arrow is obvious: alerts only become health if nurses act early and patients respond. That becomes the thing to measure.

The team defines the primary outcome up front as unplanned heart-failure admissions per patient-year, drawn from linked routine data against a matched comparator cohort, with EQ-5D collected at enrolment and six months as a secondary QALY measure and a short PREM on accessibility. Using the ESF, they place the product in a mid-risk tier and size the evidence accordingly, rather than commissioning an expensive trial or waving it through on adherence figures alone.

At twelve months the picture is mixed and honest. Admissions in the monitored group are meaningfully lower than the comparator; EQ-5D shows a modest quality-of-life gain. The provisional ICER lands within NICE's usual range, so the service looks like reasonable value — but the disaggregated data shows enrolment skewed to less deprived, English-speaking patients, and adherence collapsing among those with the lowest digital access. The board's decision is not a simple renewal. It is to continue, fund a supported-onboarding and phone-based pathway for the excluded groups, and re-evaluate the distribution in a year — an allocative-efficiency and equity judgement the raw output numbers would never have surfaced.

## Three sector lenses

### Startup
A small digital-health company lives or dies on a credible outcome claim, but has little data and less time. Concentrate scarce evidence budget on one well-chosen primary outcome and a defensible comparator rather than a scattershot of vanity metrics, and use the ESF to avoid both under- and over-evidencing. Be candid with commissioners about what is proven versus promising; an honest "leading indicators are positive, definitive outcomes pending" builds more trust than an over-claimed ICER built on twenty users. Design outcome capture into the product from day one, because retrofitting a baseline after launch is usually impossible.

### Enterprise
An NHS trust or large ICS already holds the linked data that makes real outcome measurement possible, and is accountable for a whole population, so it should insist on QALYs or comparable units to weigh services against each other across a portfolio. The risk is organisational: activity dashboards proliferate, each service defends its own bespoke metric, and no one can compare a diabetes app with a falls service. Standardise on a small set of comparable outcome measures, a shared logic-model template, and disaggregated equity reporting, and route economic evaluation through a single analytic function so numbers are consistent and hard to game.

### Government
A national body — NICE, NHS England, DHSC, or a devolved government — sets the rules of the game: the QALY threshold, the ESF tiers, the equity expectations that everyone else must work within. Its duty is to make the value framework transparent, comparable, and legitimate, and to own the equity critique openly rather than let the QALY masquerade as neutral. It must resist the political pull toward funding visible activity over measured outcomes, and hold the line that opportunity cost is real: money for a headline-friendly app is care withdrawn elsewhere. Its published methods and thresholds become the shared language that lets startups and enterprises make comparable cases at all.

## Common failure modes

- **Output theatre.** Reporting appointments, messages, and downloads as if they were health. Fix: pair every output with its intended outcome and the assumption linking them.
- **Retrofitted evaluation.** Choosing an outcome after launch, with no baseline. Fix: define the primary outcome and baseline before build.
- **No comparator.** Claiming an ICER or "admissions saved" with nothing to compare against. Fix: always name the realistic alternative and measure at the margin.
- **Average-only reporting.** A rising mean that hides a widening gap. Fix: disaggregate by deprivation and protected characteristics; report distribution.
- **QALY over-reach.** Forcing a QALY onto a service that changes experience or access, not health state. Fix: use an honest intermediate outcome and label it as non-comparable.
- **Threshold worship.** Treating £20,000–£30,000 per QALY as a mechanical pass/fail. Fix: use it as a decision aid alongside equity, uncertainty, and context.
- **Unfunded evaluation.** Expecting rigorous outcome measurement with no budget or owner. Fix: fund and assign the evaluation at business-case stage.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Outputs vs outcomes | Only outputs counted; treated as benefit | Some outcome metrics, chosen after launch | Primary outcome defined up front, baseline captured | Outcomes routinely linked to spend; outputs used only as leading indicators |
| Comparability | Every service invents its own metric | A few shared metrics, inconsistently applied | Standard outcome set and logic-model template across portfolio | QALYs/CUA used to compare services; ICERs benchmarked consistently |
| Equity | Distribution ignored; average reported | Some disaggregation, ad hoc | Routine reporting by deprivation and protected characteristics | Equity weighting or explicit inequality goals inform allocation |
| Evidence rigour | Anecdote and vendor claims | Before/after with no comparator | Matched comparator; ESF-tiered evidence plan | Robust attribution; evaluation funded, owned, and acted upon |
| Decision use | Evidence not used in decisions | Evidence reviewed but sunk cost dominates | Stated stop/pivot criteria | Opportunity cost and ICER routinely drive invest/stop decisions |

## Checklist

- [ ] The primary health outcome is defined, validated, and written into the business case before build.
- [ ] A logic model maps inputs → activities → outputs → outcomes → impact, with assumptions named.
- [ ] Outputs and outcomes are reported separately; no output is presented as a benefit.
- [ ] A realistic comparator is named and the value claim is expressed at the margin (ICER where relevant).
- [ ] Where health state changes, value is expressed in QALYs (CUA) for portfolio comparability.
- [ ] Opportunity cost is stated: what is forgone or displaced to fund this service.
- [ ] Outcomes are disaggregated by deprivation and protected characteristics; equity impact is reported.
- [ ] Evidence expectations are right-sized using NICE's Evidence Standards Framework (and DTAC for safety/interoperability).
- [ ] PROMs and PREMs use validated instruments; outcomes use routine linked data where possible.
- [ ] The economic evaluation is funded, owned, and has an agreed timeframe and stop/pivot criteria.

## Key sources

- NICE — Evidence Standards Framework for Digital Health Technologies (ESF).
- NICE — Guide to the Methods of Technology Appraisal / health technology evaluation manual (QALY, ICER, cost-effectiveness threshold).
- NHS England / NHS Digital — Digital Technology Assessment Criteria (DTAC).
- EuroQol Group — EQ-5D instrument and user guides.
- NHS England — Patient-Reported Outcome Measures (PROMs) programme.
- The King's Fund — Population health and population health management explainers.
- HM Treasury — The Green Book: appraisal and evaluation in central government (opportunity cost, social value).
- World Health Organization — Global Burden of Disease / DALY methodology.

## References

1. Health economics — Wikipedia — https://en.wikipedia.org/wiki/Health_economics
2. Population health — Wikipedia — https://en.wikipedia.org/wiki/Population_health
3. Quality-adjusted life year — Wikipedia — https://en.wikipedia.org/wiki/Quality-adjusted_life_year
4. EQ-5D — Wikipedia — https://en.wikipedia.org/wiki/EQ-5D
5. Disability-adjusted life year — Wikipedia — https://en.wikipedia.org/wiki/Disability-adjusted_life_year
6. Cost-effectiveness analysis — Wikipedia — https://en.wikipedia.org/wiki/Cost-effectiveness_analysis
7. Cost–utility analysis — Wikipedia — https://en.wikipedia.org/wiki/Cost%E2%80%93utility_analysis
8. Incremental cost-effectiveness ratio — Wikipedia — https://en.wikipedia.org/wiki/Incremental_cost-effectiveness_ratio
9. Patient-reported outcome — Wikipedia — https://en.wikipedia.org/wiki/Patient-reported_outcome
10. Opportunity cost — Wikipedia — https://en.wikipedia.org/wiki/Opportunity_cost
11. Logic model — Wikipedia — https://en.wikipedia.org/wiki/Logic_model
12. Health equity — Wikipedia — https://en.wikipedia.org/wiki/Health_equity
13. Evidence standards framework (ESF) for digital health technologies — NICE — https://www.nice.org.uk/about/what-we-do/digital-health/evidence-standards-framework-for-digital-health-technologies
14. NICE health technology evaluations: the manual — NICE — https://www.nice.org.uk/process/pmg36/chapter/introduction-to-health-technology-evaluation
15. Digital Technology Assessment Criteria (DTAC) — NHS England — https://www.nhsengland.nhs.uk/long-read/digital-technology-assessment-criteria-dtac/
16. EQ-5D — EuroQol Group — https://euroqol.org/eq-5d-instruments/
17. Patient Reported Outcome Measures (PROMs) — NHS England — https://www.england.nhs.uk/statistics/statistical-work-areas/proms/
18. The Green Book: appraisal and evaluation in central government — HM Treasury — https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-government
