# Chapter 10.1 — Key Performance Indicators (KPIs)

**A key performance indicator (KPI) is a small, carefully chosen number that tells you whether a service is safe, fair, effective, and trusted — and in health and care, choosing and reading those numbers well is itself a matter of clinical safety and public accountability, not administrative housekeeping.**

## Why this matters in health and care

In health and care, the numbers you watch shape the care people receive. A waiting-list KPI that counts "patients booked" but not "patients seen" can hide a cohort quietly deteriorating at home. A digital service dashboard that is green on uptime but silent on whether disabled users can complete a booking will let an access problem grow into a health inequality. What you measure signals what you value, and staff, suppliers, and algorithms all optimize towards the measured target — sometimes at the expense of the unmeasured thing that actually mattered.

The stakes are higher here than in most sectors because the failure modes are human. The Mid Staffordshire and other inquiries repeatedly found organizations that hit their headline financial and activity targets while care quality collapsed underneath. Metrics were reported upwards as green while patients came to harm — the pattern now widely called "watermelon reporting" (green on the outside, red on the inside), which Chapter 10.4 — Visibility for the CEO & Senior Leaders examines in depth. Good KPIs are one of your defences against that gap between the reported picture and the real one.

KPIs also spend public money and public trust. Every indicator you publish becomes part of how citizens, regulators, and commissioners judge the system. Over-claiming, cherry-picking, or gaming a target is not just poor management; it erodes the trust that digital health depends on to get people to share data and adopt new services. This chapter is the measurement partner to Chapter 10.0 — Objectives & Key Results (OKRs): where OKRs drive focused change, KPIs monitor the ongoing health of the services and systems you run.

## Core concepts

A [performance indicator](https://en.wikipedia.org/wiki/Performance_indicator), or KPI, is a metric selected because it reflects progress against an objective that matters. A *performance metric* is any measurement of activity or state; a KPI is the subset you have deliberately elevated to "watch this one". The word *key* is load-bearing — if everything is a KPI, nothing is. A useful discipline is to hold a handful of KPIs per service, each with a named owner, a definition, a data source, and a reason it earns a place on the board.

A good KPI has four properties. It is **aligned** to an outcome that genuinely matters to patients, citizens, or clinicians, not merely to internal activity. It is **actionable** — when it moves, someone can do something about it. It is **timely** — it arrives soon enough to act on, not six weeks after the quarter closed. And it is **hard to game** — it cannot be improved on paper without improving the real thing. Metrics that fail the last test invite [Goodhart's law](https://en.wikipedia.org/wiki/Goodhart%27s_law): "when a measure becomes a target, it ceases to be a good measure."

Indicators are commonly split into leading and lagging. A *lagging indicator* confirms an outcome after the fact (30-day mortality, annual patient satisfaction). A *leading indicator* moves earlier and predicts the lagging one (medication-reconciliation completeness, deployment frequency, the proportion of referrals triaged within 24 hours). You need both: lagging indicators tell you whether you are winning, leading indicators tell you in time to change the result. Many economic and operational frameworks describe this leading/lagging distinction.

A parallel and equally important split is *process, output, and outcome measures*. A **process measure** counts whether you did the thing (appointments offered, records migrated). An **output measure** counts what was produced (letters sent, tests resulted). An **outcome measure** captures what actually changed for the person — an [outcome measure](https://en.wikipedia.org/wiki/Outcome_measure) such as symptom improvement, avoided admission, or a patient-reported quality-of-life score. Health and care systems have a chronic bias towards activity because activity is easy to count and often how money flows. Resist it: privilege outcomes and experience, and use process measures as the leading indicators that explain them.

Because no single number is safe on its own, use *balanced measurement*. The [balanced scorecard](https://en.wikipedia.org/wiki/Balanced_scorecard) discipline of Kaplan and Norton pairs each performance measure with others so that improving one at the expense of another becomes visible. The Institute for Healthcare Improvement formalizes this as outcome, process, and *balancing* measures — the balancing measure watches for the harm your improvement might cause elsewhere (faster discharge balanced against readmission, for instance).

Not every number that goes up is progress. A *vanity metric* looks impressive and rises reliably but does not inform a decision — total registered users, cumulative logins, page views. The [lean startup](https://en.wikipedia.org/wiki/Lean_startup) movement popularized the contrast between vanity and *actionable* metrics: an actionable metric ties a change you made to a change in behaviour or outcome you can act on. Cumulative counts are the classic tell — they only ever rise, so they can never signal that something is wrong.

Finally, distinguish measurement *for improvement* from measurement *for judgement*. Judgement asks "did you hit the target this month?" and reduces a living process to a two-point, red-or-green comparison against last period — a comparison that is almost always statistically meaningless because it cannot tell signal from noise. Improvement asks "is this process changing, and can we trust the change?" and answers it with [statistical process control](https://en.wikipedia.org/wiki/Statistical_process_control) (SPC): plotting a metric over time on a run chart or [control chart](https://en.wikipedia.org/wiki/Control_chart) with control limits, so you can see whether variation is ordinary (common-cause) noise or a genuine signal (special-cause) worth acting on. NHS England's *Making Data Count* programme has made this the recommended way to present operational data across the NHS, precisely to kill the "up on last month, down on target" reflex that drives bad decisions.

## Best practices

1. **Start from the outcome, then work back to the indicator.** Name the thing that must be true for a patient, citizen, or clinician — fewer avoidable admissions, faster access, safe medication — and only then ask what would tell you it is happening. This keeps you from the default trap of measuring what your systems happen to log. If you cannot connect a candidate KPI to an outcome anyone cares about, it is probably a vanity metric.

2. **Keep the set small and give every KPI an owner and a definition.** A board or service should watch a handful of KPIs, not fifty. Each needs a precise definition (what counts, what is excluded, over what period), a named owner accountable for it, and a documented data source. Ambiguous definitions are how two teams argue for a month about a number they were measuring differently.

3. **Balance every KPI so it cannot be gamed in isolation.** For each measure, ask "how would a rational person improve this number without improving the real thing, and what balancing measure would catch them?" Pair access with safety, throughput with readmission, cost with experience, delivery speed with change-failure rate. Balanced sets make gaming visible and honour the reality that health and care outcomes are multidimensional.

4. **Privilege outcome and experience measures over activity.** Activity counts are seductive because they are abundant and often tied to funding, but they answer "how busy were we?" not "did it help?". Wherever you can, elevate outcome measures and patient-reported experience and outcome measures (PREMs and PROMs) into the KPI set, and demote raw activity to the supporting layer. Where an outcome is slow or hard to measure, choose a validated leading process measure that reliably predicts it.

5. **Present KPIs as time series with SPC, not two-point comparisons.** Adopt the *Making Data Count* approach: plot the metric run-chart or control-chart style so common-cause variation and special-cause signals are distinguishable at a glance. This stops teams reacting to noise, celebrating a lucky month, or being punished for an unlucky one. It also changes the boardroom conversation from "why did we miss?" to "has the process actually changed?" — which is the improvement question (see Chapter 10.2 — Quality Improvement & Improvement Science).

6. **Segment KPIs by population to reveal inequality.** An aggregate number hides distribution. A "good" average waiting time can conceal that patients from the most deprived neighbourhoods, or those needing an interpreter, wait far longer. Break every equity-relevant KPI down by deprivation, ethnicity, age, disability, and digital access, in line with [health equity](https://en.wikipedia.org/wiki/Health_equity) duties and frameworks such as NHS Core20PLUS5. In digital services, segment adoption and completion rates too — a headline uptake figure can mask that your service excludes exactly the people who need it most (see Chapter 4.5 — Data, Analytics & Population Health Management).

7. **Treat data quality as a prerequisite, and measure it.** A KPI is only as trustworthy as the data beneath it. Track the [data quality](https://en.wikipedia.org/wiki/Data_quality) of the fields your KPIs depend on — completeness, validity, timeliness, coverage — using instruments like the NHS Data Quality Maturity Index, and show data-quality caveats alongside the number. If 30% of records are missing the field, say so on the dashboard; a confident-looking KPI built on poor data is worse than no KPI.

8. **Use delivery metrics for the digital service itself, chosen with the same rigour.** For the software you build and run, the [DevOps Research and Assessment](https://en.wikipedia.org/wiki/DevOps_Research_and_Assessment) (DORA) four keys — deployment frequency, lead time for change, change-failure rate, and time to restore service — give a balanced view of speed and stability. They resist gaming as a set: you cannot ship faster by breaking things, because change-failure rate and restore time will catch it. Complement them with reliability and safety KPIs that matter clinically, such as incident rates and availability of safety-critical functions (see Chapter 3.6 and Chapter 3.8).

9. **Layer your reporting so each audience gets the right altitude.** A frontline team needs granular, real-time process measures; a service board needs a balanced handful with SPC; a system leadership needs a curated few outcome and equity measures. Design the layers deliberately so the top view is an honest aggregation of the ones below, not a hand-picked flattering subset. This is your structural defence against watermelon reporting (Chapter 10.4).

10. **Review and retire KPIs on a schedule.** Indicators decay: a measure that drove real improvement can become a gamed ritual once the behaviour it targeted is embedded, and new risks emerge that nothing is watching. Put KPIs on a regular review where you ask of each one "is this still telling us something we act on?" and retire the dead wood. A stale KPI set is not neutral — it actively misdirects attention.

## Questions to discuss with your team

1. **For each of our headline KPIs, how would someone improve the number without improving the reality — and would we notice?** This is the Goodhart's law stress test, and it is best done as a deliberately adversarial exercise. Take each KPI and have the team play the role of a stretched service trying to hit it: discharge before midnight to reset the clock, re-band a waiting patient, close and reopen a ticket to reset resolution time, batch-register users who never return. The point is not cynicism about colleagues but recognition that pressure plus a single-number target produces predictable distortions, especially when pay, reputation, or contract penalties ride on the figure. A good answer names the specific gaming route for each KPI and identifies the balancing measure or data check that would expose it — and honestly flags any KPI where you currently have no such safeguard. If a metric cannot be defended this way, the discussion should end with a decision to pair it, redefine it, or drop it.

2. **Which of our numbers are we reporting for improvement, and which for judgement — and are we presenting each in a way that matches?** Teams routinely take a metric built to help a service learn and hand it, unchanged, to a committee that uses it to hold someone to account, or vice versa. The tension is real: leaders need assurance, and improvement needs safety to see problems honestly, and the same chart cannot always serve both without distortion. Walk through your actual board and operational packs and label each metric's true purpose, then ask whether the presentation fits — are you showing a two-point red/green comparison where an SPC chart would prevent knee-jerk reactions to noise? A good, honest answer will admit where judgement-culture has crept into improvement forums (making staff hide problems) and where vague improvement narratives are being used to dodge legitimate accountability. The aim is a conscious choice per metric, with SPC as the default presentation, rather than an accidental muddle.

3. **Do our KPIs reveal or conceal inequality, and whose experience is missing from them entirely?** Aggregate KPIs are comfortable precisely because they average away the people at the margins, and in health and care those margins are where avoidable harm concentrates. Discuss which of your indicators are segmented by deprivation, ethnicity, disability, age, and digital access — and which are still reported only as a single system-wide figure that could look healthy while a subgroup is failed. Push further to the people who never enter your data at all: patients who could not get past the login, who abandoned the digital form, who were never referred, who declined to share the demographic field you segment by. A strong answer identifies at least one KPI where segmentation changed or would change the story, acknowledges the data-quality and consent limits on segmentation honestly, and commits to a specific step — even a proxy or a small qualitative study — to see the currently invisible. Anything less risks a dashboard that is technically accurate and morally blind.

4. **How many KPIs are we actually watching, and which ones would we lose nothing by retiring?** The word *key* only means something if the set is small, yet indicators accumulate faster than anyone removes them — a national return here, a contractual metric there, a number a former director once asked for and no one has dared drop since. The tension is that every KPI feels defensible in isolation, so the set grows until the board packs are a hundred pages that no one reads and the genuinely important signals are buried among zombie metrics produced out of habit. Walk your actual reporting and count the indicators honestly, then ask of each one whether anyone acted on it in the last year and what decision it informs; the metrics that survive neither test are dead wood that still consumes analyst time and dilutes attention. A good answer names a specific number you will hold per service, identifies at least one KPI to retire outright, and puts in place a scheduled review so the set stays curated rather than quietly re-inflating. Be wary of the reflex that retiring a metric is an admission of failure — a disciplined subtraction is a sign of maturity, not neglect.

5. **How much do we actually trust the data beneath each headline KPI, and does the dashboard say so?** A confident-looking number built on a field that is 30% incomplete is more dangerous than no number at all, because it invites decisions that the data cannot support while wearing the authority of a clean figure. In health and care this is acute: demographic fields needed for equity segmentation are often sparse, coding practice varies between sites, and the very act of digitizing a paper process can shift what gets recorded and when. Discuss, for each KPI, whether you know its completeness, validity, timeliness and coverage, and whether those caveats travel with the number onto the board pack or get quietly stripped away as it moves upward. A strong answer points to a concrete instrument — a data-quality check, the DQMI, a completeness threshold below which a metric is flagged — and shows at least one place where a data-quality caveat is displayed alongside the KPI rather than hidden. The honest version admits where you are currently reporting a number you cannot fully stand behind, and treats fixing the data as part of the KPI, not a separate backlog item.

6. **Do the layers of our reporting honestly roll up, and where could red turn green on the way to the board?** Different audiences legitimately need different altitudes — a frontline team wants granular real-time process measures, a board wants a balanced handful with SPC, a system wants a curated few outcomes — but each aggregation is an opportunity for the underlying picture to be smoothed, averaged or hand-picked into something more comfortable than the truth. This is the structural root of watermelon reporting: the more layers between the ward and the board, the more places a distribution can be flattened into a reassuring mean, or a struggling site can be netted off against a strong one. Trace one KPI from its frontline source all the way to the top view and ask whether the executive figure is a faithful aggregation or a flattering subset, and who — if anyone — audits that roll-up. A good answer shows that reporting layers were designed deliberately with agreed definitions and owners, identifies at least one point where the aggregation could mask a problem, and names the balancing measure or drill-down that keeps the top view truthful. Honesty here means admitting where the roll-up is currently taken on trust rather than checked (see Chapter 10.4).

## In practice: a health & care example

An integrated care system (ICS) launches a digital referral service that lets GPs refer directly into community musculoskeletal (MSK) physiotherapy, replacing a paper and fax process. The programme board's instinct is to report two KPIs: number of digital referrals received, and system uptime. Within three months both are strongly green — thousands of referrals, 99.9% uptime — and the board is ready to declare success.

The clinical director is uneasy and asks the analytics team (working with the pattern in Chapter 4.5) to rebuild the KPI set around outcomes. They land on a balanced handful: time from referral to first contact (access, shown as an SPC chart), the proportion of referrals returned or rejected as incomplete (a leading quality signal), a patient-reported outcome score at discharge (outcome), a short experience measure (did you feel involved in decisions?), and change-failure rate for the service's releases (delivery stability). Every access and outcome measure is segmented by deprivation decile and by whether the patient needed digital support.

The rebuilt view tells a very different story. Uptime is genuinely fine, but the return-to-referrer rate is 22% — one in five referrals bounces because the digital form makes a free-text history mandatory, so GPs game it by typing "see attached" and the triage team rejects them. The SPC chart shows access time is stable but sitting well above target with no improvement trend. And segmentation reveals that patients in the two most deprived deciles are half as likely to complete the self-referral route that the service was quietly nudging people towards, widening a gap the programme had assumed it was closing. None of this was visible in the original two green numbers. The board redesigns the form, adds an assisted-referral pathway, and keeps the balanced, segmented, SPC-based KPI set as its standing view — with the raw referral count demoted to a supporting metric where it belongs.

## Sector lenses

### Startup

A digital-health startup lives or dies by a few actionable metrics, so the discipline is ruthless focus and honesty. Founders are tempted to show investors vanity metrics — cumulative downloads, total registered users — because they only ever rise; resist, and lead with activation, retention, and, where you can measure it, clinical outcome or a validated proxy. With small numbers, SPC and segmentation are harder but even more important: a handful of poor experiences can be your whole safety signal. Instrument the product from day one so that every KPI ties a change you shipped to a change in real behaviour, and be candid with clinical and regulatory partners about data-quality limits rather than polishing a thin dataset.

### Small business

An established small provider — a GP practice, a community pharmacy, a care home, a domiciliary-care agency, a single-site clinic, or a small health-tech supplier past the pre-revenue stage — carries the same measurement and equity duties as a large trust but with no dedicated analyst and little spare time. The trap is drowning in the KPIs that national returns, CQC, and commissioners already demand while measuring nothing that helps you run the place; the antidote is to choose a genuinely small handful of outcome and experience measures you can actually act on, and lean on what your existing clinical or practice-management system already captures rather than building new instrumentation. SPC is still worth it even by hand or in a spreadsheet — a simple run chart of, say, weekly time-to-appointment will stop you chasing the noise of a single bad week. Segmentation matters just as much at this scale, but with small numbers a couple of individual patients can swing a percentage, so read breakdowns as a prompt to look closer rather than a verdict. Be honest with commissioners about the data-quality limits of a lean operation, and resist adopting a big organization's fifty-metric dashboard when five well-chosen numbers will serve your patients better.

### Enterprise

A large NHS trust or health-tech supplier already drowns in indicators — national returns, contractual KPIs, board metrics, operational dashboards — so the challenge is curation and coherence, not collection. Adopt SPC across board and operational reporting (as *Making Data Count* intends) to stop the monthly noise-chasing, and build explicit reporting layers so the executive view is an honest roll-up of the frontline one. Watermelon reporting is the enterprise-scale risk: the more layers between the ward and the board, the easier for red to turn green on the way up, so invest in the balancing measures and data-quality caveats that keep the top view truthful. Retire legacy KPIs deliberately; large organizations accumulate zombie metrics that nobody acts on but everyone still produces.

### Government

A national or local public body sets KPIs that ripple across a whole system and become political targets, which makes Goodhart's law a systemic hazard rather than a local one — a national waiting-time target reshapes clinical priorities everywhere overnight. Design published indicators knowing they will be optimized towards, pair them with balancing measures and equity segmentation, and be transparent about definitions and data quality because public trust depends on it. Frameworks like the NHS Outcomes Framework and Core20PLUS5 exist precisely to keep national attention on outcomes and inequalities rather than raw activity. Government also carries a duty the others do not: to measure the people its services exclude, not just the people they serve, because the excluded rarely appear in the administrative data.

## Common failure modes

- **Counting activity and calling it success.** Referrals received, logins, appointments offered — busy is not the same as effective. Elevate outcomes and experience; demote activity to the supporting layer.
- **The single number with no balancing measure.** Any lone KPI under pressure will be gamed. Always pair measures so improving one at the expense of another is visible.
- **Two-point, red/green reporting.** "Down on last month, below target" tells you almost nothing about whether the process changed. Use SPC run and control charts instead.
- **Watermelon dashboards.** Aggregation that turns underlying red into surface green. Build honest reporting layers and audit the roll-up (Chapter 10.4).
- **Vanity metrics.** Cumulative, ever-rising counts that cannot signal a problem. Prefer actionable metrics tied to a decision.
- **Unsegmented equity blindness.** Averages that hide the people being failed. Segment by population and hunt for who is missing entirely.
- **KPIs built on unexamined data.** A confident number on poor data misleads. Measure and disclose data quality alongside the KPI.
- **Zombie KPIs.** Metrics still produced out of habit that no one acts on. Review and retire on a schedule.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| What is measured | Whatever the systems happen to log; mostly activity | A mix of activity and some outcomes, chosen ad hoc | A small balanced set of outcome, process, experience and balancing measures per service | The balanced set is tracked against explicit targets, with owners accountable for each KPI's performance | Outcome- and equity-led KPIs, reviewed and retired on a cycle, tied to strategy and OKRs |
| How it is presented | Red/green tables, two-point comparisons | Some trend lines, mostly point-in-time | SPC run/control charts standard for operational data | SPC charts reviewed on a governed cadence, with signals triaged and actions logged and followed up | SPC embedded in decision-making; noise vs signal understood by leaders |
| Equity | Aggregate figures only | Occasional ad hoc breakdowns | Routine segmentation of key KPIs by population | Equity gaps tracked against targets, with named owners and remedial actions monitored to closure | Segmentation plus deliberate effort to see the excluded and act on gaps |
| Gaming & data quality | Not considered; single targets under pressure | Awareness of gaming; data quality patchy and undisclosed | Balancing measures in place; data quality tracked and caveated | Balancing measures and data-quality thresholds actively assured, with breaches escalated and controlled | Metrics stress-tested against gaming; data quality measured as its own KPI |
| Reporting layers | One flattering view sent upward | Separate packs, inconsistent definitions | Layered reporting with agreed definitions and owners | Roll-up routinely reconciled against source data, with any divergence investigated and corrected | Honest, audited roll-up from frontline to board; no watermelon gap |

## Checklist

- [ ] Every KPI is traceable to an outcome that matters to a patient, citizen, or clinician.
- [ ] The KPI set per service is small, and each has an owner, a written definition, and a named data source.
- [ ] Each KPI has at least one balancing measure so it cannot be gamed in isolation.
- [ ] Outcome and experience measures are prioritized; raw activity sits in the supporting layer.
- [ ] Operational KPIs are presented as SPC run/control charts, not two-point red/green comparisons.
- [ ] Equity-relevant KPIs are segmented by deprivation, ethnicity, disability, age, and digital access.
- [ ] Data quality for the fields behind each KPI is tracked and caveated on the dashboard.
- [ ] Delivery of the digital service is measured with a balanced set (e.g. DORA four keys plus safety/reliability).
- [ ] Reporting layers are designed so the top view is an honest roll-up of the frontline one.
- [ ] KPIs are reviewed on a schedule, with dead or gamed metrics retired.
- [ ] You have asked, for each KPI, "who is missing from this number entirely?"

## Key sources

- NHS England — *Making Data Count* (statistical process control for NHS operational data)
- Institute for Healthcare Improvement — Science of Improvement: outcome, process, and balancing measures
- NHS England — NHS Outcomes Framework; Core20PLUS5 approach to reducing healthcare inequalities
- NHS England — Data Quality Maturity Index (DQMI)
- Robert S. Kaplan & David P. Norton — *The Balanced Scorecard: Translating Strategy into Action*
- Nicole Forsgren, Jez Humble & Gene Kim — *Accelerate* (DORA metrics); Google Cloud DORA *State of DevOps* reports
- Jerry Z. Muller — *The Tyranny of Metrics*
- Donald J. Wheeler — *Understanding Variation: The Key to Managing Chaos*
- GOV.UK Service Manual — Measuring success / measuring the performance of your service
- The Health Foundation — guidance on measurement for improvement

## References

1. Performance indicator — Wikipedia — https://en.wikipedia.org/wiki/Performance_indicator
2. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
3. Statistical process control — Wikipedia — https://en.wikipedia.org/wiki/Statistical_process_control
4. Control chart — Wikipedia — https://en.wikipedia.org/wiki/Control_chart
5. Balanced scorecard — Wikipedia — https://en.wikipedia.org/wiki/Balanced_scorecard
6. Outcome measure — Wikipedia — https://en.wikipedia.org/wiki/Outcome_measure
7. Health equity — Wikipedia — https://en.wikipedia.org/wiki/Health_equity
8. Data quality — Wikipedia — https://en.wikipedia.org/wiki/Data_quality
9. DevOps Research and Assessment — Wikipedia — https://en.wikipedia.org/wiki/DevOps_Research_and_Assessment
10. Lean startup (vanity vs actionable metrics) — Wikipedia — https://en.wikipedia.org/wiki/Lean_startup
11. Making Data Count — NHS England — https://www.england.nhs.uk/publication/making-data-count/
12. Science of Improvement: Establishing Measures — Institute for Healthcare Improvement — https://www.ihi.org/resources/how-to-improve/science-improvement-establishing-measures
13. NHS Outcomes Framework — NHS England / Department of Health and Social Care — https://digital.nhs.uk/data-and-information/publications/statistical/nhs-outcomes-framework
14. Core20PLUS5 – reducing healthcare inequalities — NHS England — https://www.england.nhs.uk/about/equality/equality-hub/national-healthcare-inequalities-improvement-programme/core20plus5/
15. Data Quality Maturity Index (DQMI) — NHS England — https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/data-quality
16. The Balanced Scorecard: Translating Strategy into Action — Robert S. Kaplan & David P. Norton (Harvard Business Review Press) — https://en.wikipedia.org/wiki/Balanced_scorecard
17. Accelerate: The Science of Lean Software and DevOps — Nicole Forsgren, Jez Humble & Gene Kim (IT Revolution) — https://itrevolution.com/product/accelerate/
18. DORA / State of DevOps research — Google Cloud DORA — https://dora.dev/
19. The Tyranny of Metrics — Jerry Z. Muller (Princeton University Press) — https://press.princeton.edu/books/hardcover/9780691174952/the-tyranny-of-metrics
20. Measuring the performance of your service — GOV.UK Service Manual — https://www.gov.uk/service-manual/measuring-success
21. Understanding Variation: The Key to Managing Chaos — Donald J. Wheeler (SPC Press) — https://www.spcpress.com/book_understanding_variation.php
