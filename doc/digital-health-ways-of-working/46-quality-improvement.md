# Chapter 46 — Quality Improvement & Improvement Science

**Quality improvement gives frontline teams a disciplined, data-driven way to make care measurably better through small tests of change — and when you connect it to your digital tools, you turn dashboards and automation into engines of continuous learning rather than static reporting.**

## Why this matters in health and care

Quality improvement (QI) is the dominant improvement discipline across the National Health Service (NHS) and much of global health and care. It is taught in trusts, embedded in ward-level huddles, and championed by national bodies. If you lead digital delivery, you are not working alongside QI — you are working inside a system that already thinks in aims, measures, and tests of change. Ignoring that language isolates your team; speaking it fluently makes your digital work legible to clinicians, managers, and boards who already trust it.

The deeper reason matters more. In health and care, variation in how work is done is not a cosmetic problem. Unwarranted variation means some patients wait longer, some receive unsafe care, and some are excluded entirely. Improvement science exists precisely because good intentions and heroic effort do not reliably produce better outcomes — systems do. A digital service that shaves minutes off a clinical workflow, closes a safety gap, or removes a step that disproportionately excludes people with low digital confidence is doing improvement work, whether or not you call it that.

QI also protects you from a common digital failure: shipping a change and assuming it worked. Improvement science is built around a single humbling insight — most changes are not improvements, and you cannot tell which are without measurement over time. Adopting that discipline keeps your team honest, keeps your claims defensible to boards and regulators, and keeps your users safer. This chapter shows you how to run QI properly, how it differs from project delivery and research, and how to fuse it with the digital tooling you already own.

## Core concepts

[Quality management](https://en.wikipedia.org/wiki/Quality_management) in health and care draws on a lineage that runs from manufacturing to the bedside. The intellectual root is the work of [W. Edwards Deming](https://en.wikipedia.org/wiki/W._Edwards_Deming), the statistician who taught that quality comes from understanding and reducing variation in systems, not from exhorting individuals to try harder. Deming's thinking, together with Walter Shewhart's, produced the [PDCA / Plan-Do-Study-Act](https://en.wikipedia.org/wiki/PDCA) cycle — the iterative Plan-Do-Study-Act loop that sits at the heart of modern healthcare QI.

Most NHS teams run PDSA inside the **Model for Improvement**, a framework popularised by the Institute for Healthcare Improvement (IHI) that pairs the cycle with three questions: What are we trying to accomplish? How will we know that a change is an improvement? What change can we make that will result in improvement? The first question is answered with an **aim statement** (specific, measurable, time-bound). The third is often mapped with a **driver diagram**, which links your aim to the primary and secondary drivers you believe influence it, and then to concrete change ideas.

QI is one member of a family of improvement approaches that share the [continual improvement process](https://en.wikipedia.org/wiki/Continual_improvement_process) philosophy. Two siblings you will meet constantly are [Lean](https://en.wikipedia.org/wiki/Lean_manufacturing), derived from the Toyota Production System and focused on removing waste and improving flow, and [Six Sigma](https://en.wikipedia.org/wiki/Six_Sigma), which uses statistical methods to reduce defects and variation. In healthcare these are frequently blended as "Lean Six Sigma".

Measurement for improvement relies on seeing data over time rather than in snapshots. The two workhorse tools are the [run chart](https://en.wikipedia.org/wiki/Run_chart) — observed data plotted in time sequence against a median — and the [control chart](https://en.wikipedia.org/wiki/Control_chart), a run chart with statistically derived limits, which underpins [statistical process control](https://en.wikipedia.org/wiki/Statistical_process_control) (SPC). SPC lets you distinguish common-cause variation (the ordinary noise of a stable system) from special-cause variation (a signal that something has genuinely changed). In the NHS this is taught as the "Making Data Count" approach.

None of this works without [psychological safety](https://en.wikipedia.org/wiki/Psychological_safety): the shared belief that people can raise problems, admit that a test failed, and challenge the status quo without being punished. Improvement is impossible where staff hide defects, and it is the precondition for everything else in this chapter.

## Best practices

1. **Start with an aim statement, not a solution.** Before you design anything, write down what you are trying to accomplish, for whom, by how much, and by when — for example, "reduce the median time from referral to first digital triage from 9 days to 3 days by March." A numeric, time-bound aim forces clarity and gives you something to measure against. Teams that skip this step end up debating features instead of outcomes, and can never tell whether they succeeded. This connects directly to Chapter 45 — OKRs & KPIs, but note that a QI aim is narrower and more testable than a typical objective.

2. **Use a driver diagram to expose your theory of change.** Map your aim to the primary drivers that most influence it, then to secondary drivers, then to specific change ideas. This makes your assumptions visible and debatable, and it stops teams from betting everything on a single intervention. It also helps you sequence tests: you can attack the highest-leverage driver first. Keep the diagram on the wall (physical or virtual) and revise it as you learn — it is a living hypothesis, not a one-off artefact.

3. **Run small, fast PDSA cycles rather than big-bang launches.** Test a change on one clinic, one ward, or one cohort before scaling. Predict what will happen, run the test, study the data against your prediction, and decide whether to adopt, adapt, or abandon. Small tests reduce risk, surface problems early, and build the evidence and confidence you need to spread. This is a fundamentally different rhythm from a fixed-scope project plan, and it is where digital teams most often need to unlearn habits.

4. **Measure over time with run charts and SPC, not before-and-after snapshots.** A single pair of numbers cannot tell you whether a change caused an improvement or whether you caught random variation. Plot your measure as a run chart or control chart so you can see trends, shifts, and special-cause signals. Adopt the NHS "Making Data Count" conventions so your charts are consistent and readable to others. This discipline also protects you from claiming credit for noise, which erodes trust with boards and regulators.

5. **Balance your measures.** Every improvement has the potential to make something else worse. Alongside your outcome measure, track process measures (is the change actually happening?) and balancing measures (is anything deteriorating as a side effect — safety, staff workload, equity of access?). A digital triage tool that speeds throughput but quietly excludes people without smartphones has not improved care. Balancing measures are your early-warning system for exactly this kind of harm.

6. **Give frontline teams genuine permission and capability to improve.** Improvement that is mandated top-down and executed by a central team rarely sticks. Invest in QI training, coaching, and protected time so the people doing the work can run their own tests. Build the infrastructure — a QI faculty, a measurement function, accessible data — that the IHI and mature NHS trusts describe as the backbone of a trust-wide programme. Your digital team's job is often to remove the data and tooling friction that stops frontline improvement.

7. **Design for spread and sustainability from the start.** A one-off gain on one ward that evaporates in six months is a common and demoralising outcome. Plan how a successful change will be standardised, embedded in workflow, and monitored so it holds — and how it will spread to comparable settings without simply copy-pasting. Digital tools help enormously here: automation and defaults can lock in an improved process far more reliably than a laminated poster. This is where QI meets Chapter 38 — Change Management.

8. **Fuse QI with your digital data and dashboards.** Improvement science is starved without timely data, and most NHS QI historically ran on hand-counted samples. If your team can surface near-real-time run charts and SPC charts from existing systems, you dramatically shorten the learning loop. Treat dashboards, automated data pipelines, and self-service analytics as improvement infrastructure, not just reporting. This is one of the clearest, highest-value contributions a digital function can make to clinical quality.

## Questions to discuss with your team

1. **Are we running quality improvement, project delivery, or research — and do we know the difference?** These three modes are routinely confused, and the confusion is expensive. Project delivery aims to deliver a defined scope on time and budget; research aims to produce generalisable knowledge with rigorous controls and ethics approval; QI aims to make a local system better through iterative small tests of change. Measurement for improvement is deliberately lighter than measurement for research — you want just enough data to guide the next cycle, not a publishable study. Applying research-grade rigour to a QI test paralyses the team; applying QI informality to something that is really research risks ethical and safety failures. Talk through where each of your current initiatives genuinely sits, and whether you have the right governance for each. Getting this wrong is a frequent reason digital improvement work stalls or draws unwarranted scrutiny.

2. **How will we know a change is an improvement, and not just noise or wishful thinking?** This is the second question of the Model for Improvement, and it is where most teams are weakest. Decide now what your outcome, process, and balancing measures are, how often you will collect them, and how you will display them over time. Commit to run charts or SPC before you launch, so you are not tempted to cherry-pick a favourable before-and-after comparison afterwards. Discuss what a "special-cause signal" would look like for each measure, and who is empowered to call it. Be honest about the uncomfortable corollary: you must be willing to see that a change you invested in did not work. Link this to Chapter 4 — Evidence-Driven Decisions, because the same intellectual honesty underpins both.

3. **Do our frontline teams actually have permission, time, and data to improve — or only pressure to deliver?** Improvement capability is not a slogan; it requires protected time, coaching, psychological safety, and accessible data. Ask candidly whether staff feel safe reporting that a test failed, or whether they expect blame. Ask whether the data they need arrives in days and weeks rather than months, and whether your digital systems help or hinder. Consider whether your organisation has genuine QI infrastructure — a faculty, a method, a measurement function — or whether improvement depends on a few enthusiasts. Discuss what your digital team could remove from the frontline's path: manual data collection, brittle spreadsheets, delayed reports. The answer usually reveals more about your culture than your technology, and it directly shapes what Chapter 48 — Visibility for the CEO & Senior Leaders should surface to the board.

## In practice: a health & care example

An integrated care board (ICB) is worried about its community physiotherapy service. Patients referred from primary care wait a median of 21 days for first contact, complaints are rising, and a new online self-referral form has not obviously helped. The digital team's instinct is to rebuild the form. Instead, the service's clinical lead and the digital product manager decide to run this as a quality improvement project.

They write an aim statement: reduce median time from referral to first meaningful contact from 21 days to 7 days within four months, without increasing the did-not-attend rate or reducing access for patients who cannot use online tools. They build a driver diagram. The primary drivers turn out to be referral quality, triage speed, and appointment availability — not, as first assumed, the form itself. The biggest bottleneck is triage: referrals sit in a shared inbox for days before a clinician reviews them.

They start small. In one PDSA cycle, a single physiotherapist trials same-day triage for one GP practice's referrals, using a simple digital worklist the team stands up in a week from existing data. They predict triage time will fall to under a day; the study phase confirms it, and reveals a surprise — a third of referrals lack the information needed to triage safely, forcing rework. The next cycle tests a structured referral template. Throughout, the digital team surfaces a run chart of daily triage times and an SPC chart of the median wait, following "Making Data Count" conventions, so the whole service can see progress in near-real time rather than waiting for a monthly report.

Crucially, they track a balancing measure: the proportion of referrals arriving by phone versus the online form, disaggregated by patient age and deprivation. When online self-referral climbs, they notice it is not reaching older patients in the most deprived neighbourhoods, so they keep the phone route fully staffed. By month four the median wait sits stable at six days — a genuine shift on the control chart, not a lucky month — and the improvement holds because the structured template and triage worklist are now the default workflow, embedded in the tooling rather than dependent on goodwill.

## Three sector lenses

### Startup

A health-tech startup rarely has a formal QI programme, and does not need one — but the core discipline is directly applicable and often neglected. The Model for Improvement maps naturally onto product experimentation: an aim statement is a hypothesis, a PDSA cycle is a build-measure-learn loop, and balancing measures guard against the classic startup failure of optimising one metric while quietly harming clinical safety or equity. The main risk is speed without measurement over time — shipping fast and declaring victory on a single week's uplift. Adopt run-chart thinking early; it is cheap and it makes your outcome claims credible to the NHS buyers and clinical partners you will eventually need. Treat psychological safety inside your small team as a competitive asset: honest reporting of failed tests is how you avoid building the wrong thing at scale.

### Enterprise

A large provider or supplier usually has an established QI infrastructure — a faculty, trained coaches, an improvement method, and a measurement function — sometimes running to hundreds of concurrent projects. The enterprise risk is the opposite of the startup's: bureaucratic QI that becomes a compliance ritual, with driver diagrams produced for governance rather than genuine tests of change. Your digital function's highest-value move is to industrialise measurement for improvement — automated, trustworthy, near-real-time SPC charts drawn from live systems — so improvement teams stop hand-counting and start learning faster. Guard against the enterprise habit of confusing a large transformation programme with improvement; the two need different governance, as Chapter 25 — Programme-Led Work makes clear. Sustainability and spread are your hardest problems at scale, so invest in them deliberately rather than assuming good local results propagate on their own.

### Government

National and regional bodies — NHS England, ICBs, arms-length bodies — shape QI through method, mandate, and infrastructure rather than by running tests themselves. The "Making Data Count" programme is a good model: a nationally promoted, consistent approach to SPC that raises the quality of improvement conversation everywhere. The risk at this level is confusing performance management with improvement — imposing targets and ranking organisations by two-point comparisons, which SPC thinking specifically warns against because it mistakes noise for signal. Government's best contribution is to build capability and shared method broadly, protect frontline permission to improve, and resist the temptation to turn every measure into a judgement. When you set national digital standards, embed measurement-for-improvement conventions so that improvement, not just assurance, becomes the default posture.

## Common failure modes

- **Solutioneering before an aim.** Jumping to "let us build a new app" without a specific, measurable aim, so success can never be judged and effort scatters across features nobody validated.
- **Before-and-after theatre.** Claiming improvement from two data points when a run chart would reveal ordinary variation. This is the single most common way teams fool themselves and their boards.
- **No balancing measures.** Improving throughput while silently worsening safety, staff workload, or equity of access — a particular danger for digital tools that exclude people with low digital confidence.
- **QI dressed up as project management.** Running a fixed-scope, big-bang plan and calling it QI, with no genuine tests of change, no PDSA, and no willingness to adapt or abandon.
- **Confusing improvement with research or performance management.** Applying research-grade rigour that paralyses fast learning, or weaponising improvement data as a league table that destroys psychological safety.
- **One-off gains that evaporate.** Celebrating a local success with no plan to standardise, embed, sustain, or spread it, so the system quietly reverts within months.
- **Central control without frontline permission.** Mandating improvement from the top while denying staff the time, safety, and data to run their own tests, guaranteeing shallow compliance.
- **Data starvation.** Running QI on manual, delayed, untrusted data when your digital systems could surface timely SPC charts, keeping the learning loop far slower than it needs to be.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Method | Ad hoc fixes; no shared improvement method | Some teams use PDSA and aim statements informally | Model for Improvement is the standard approach with driver diagrams | Improvement method is embedded, taught, and adapted intelligently to context |
| Measurement | Before-and-after snapshots; anecdote | Occasional run charts, inconsistently drawn | Run charts and SPC used routinely, "Making Data Count" conventions followed | Automated, near-real-time SPC from live systems; balancing measures standard |
| Capability & culture | Improvement depends on lone enthusiasts | Some training exists; permission is uneven | QI faculty, coaching, protected time, and psychological safety are established | Frontline-led improvement is the norm; failure is discussed openly and safely |
| Digital integration | Data hand-counted; systems hinder improvement | Dashboards exist but are reporting-only | Digital data pipelines feed improvement work directly | Automation and defaults lock in and spread improvements reliably |
| Sustainability & spread | Gains are one-off and fade | Successes shared informally, rarely embedded | Standardisation and spread are planned deliberately | Improvements sustain and spread across the system as designed |

## Checklist

- [ ] We have written a specific, measurable, time-bound aim statement for this improvement.
- [ ] We have a driver diagram that makes our theory of change explicit and revisable.
- [ ] We have defined outcome, process, and balancing measures, including an equity balancing measure.
- [ ] We are displaying data over time as run charts or SPC charts, following "Making Data Count".
- [ ] We are testing changes in small PDSA cycles before scaling, with a prediction for each test.
- [ ] We are clear whether this is improvement, project delivery, or research, and governed accordingly.
- [ ] Frontline teams have permission, protected time, and psychological safety to run their own tests.
- [ ] Our digital systems supply timely, trusted data to the improvement work, not delayed manual counts.
- [ ] We have a plan to sustain, standardise, and spread any change that proves to be an improvement.
- [ ] We report improvement to leaders using SPC thinking, not two-point comparisons.

## Key sources

- NHS England — Making Data Count: statistical process control resources and training for the NHS.
- Institute for Healthcare Improvement (IHI) — Model for Improvement, PDSA, and the Science of Improvement resources.
- Langley, Moen, Nolan, Nolan, Norman & Provost — *The Improvement Guide* (2nd edition), the foundational text on the Model for Improvement.
- The Health Foundation — *Quality Improvement Made Simple* and related evidence reviews on improvement in health care.
- W. Edwards Deming — *Out of the Crisis* and the System of Profound Knowledge.
- Amy C. Edmondson — *The Fearless Organization*, on psychological safety in teams.

## References

1. PDCA — Wikipedia — https://en.wikipedia.org/wiki/PDCA
2. W. Edwards Deming — Wikipedia — https://en.wikipedia.org/wiki/W._Edwards_Deming
3. Quality management — Wikipedia — https://en.wikipedia.org/wiki/Quality_management
4. Continual improvement process — Wikipedia — https://en.wikipedia.org/wiki/Continual_improvement_process
5. Lean manufacturing — Wikipedia — https://en.wikipedia.org/wiki/Lean_manufacturing
6. Six Sigma — Wikipedia — https://en.wikipedia.org/wiki/Six_Sigma
7. Run chart — Wikipedia — https://en.wikipedia.org/wiki/Run_chart
8. Control chart — Wikipedia — https://en.wikipedia.org/wiki/Control_chart
9. Statistical process control — Wikipedia — https://en.wikipedia.org/wiki/Statistical_process_control
10. Psychological safety — Wikipedia — https://en.wikipedia.org/wiki/Psychological_safety
11. Making Data Count — NHS England — https://www.england.nhs.uk/publication/making-data-count/
12. Science of Improvement — Institute for Healthcare Improvement — https://www.ihi.org/resources/how-to-improve
13. The Improvement Guide — Langley, Moen, Nolan, Nolan, Norman & Provost, Jossey-Bass — https://www.wiley.com/en-us/The+Improvement+Guide%3A+A+Practical+Approach+to+Enhancing+Organizational+Performance%2C+2nd+Edition-p-9780470192412
14. Quality Improvement Made Simple — The Health Foundation — https://www.health.org.uk/publications/quality-improvement-made-simple
