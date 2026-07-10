# Chapter 45 — OKRs & KPIs

**In one sentence:** Goals and measures are different tools — use objectives and key results (OKRs) to drive the change you want, key performance indicators (KPIs) to watch the health of what already runs, and design both so they cannot be gamed at the expense of patients and the public.

## Why this matters in health and care

Health and care organisations swim in numbers — waiting times, bed occupancy, appointment volumes, uptime, cost per case — but abundance is not the same as insight. A digital programme can hit every output target (records migrated, features shipped, users trained) while the outcome that justified the spend (fewer missed appointments, safer prescribing, faster diagnosis) never moves. When the money is public and the stakes include safety and equity, measuring the wrong thing is not a harmless error; it directs scarce clinical and financial resource toward activity that looks like progress.

Measurement in this sector also carries a specific hazard: numbers become targets, targets become pressure, and pressure distorts behaviour and data. The NHS has learned this the hard way through episodes where hitting a headline figure crowded out the care it was meant to represent. A senior leader's job is not to collect more metrics but to choose the few that matter, to know which are goals and which are gauges, and to build in the guardrails that keep a measure honest.

## Core concepts

**Metric, target, KPI, OKR.** A *metric* is any quantity you can observe (e.g. percentage of e-referrals auto-triaged). A *target* is a specific value you want a metric to reach by a date. A [key performance indicator (KPI)](https://en.wikipedia.org/wiki/Performance_indicator) is a metric elevated to "key" status because it signals the health of something that must keep working. An [objectives and key results (OKR)](https://en.wikipedia.org/wiki/OKR) statement is a goal-setting structure: an **Objective** (a qualitative, memorable statement of what you want to achieve) paired with 3–5 **Key Results** (measurable outcomes that prove you achieved it). [John Doerr](https://en.wikipedia.org/wiki/John_Doerr) popularised OKRs in *Measure What Matters*, tracing them from Intel to Google.

**KPIs measure health; OKRs measure change.** This is the cleanest way to hold the two apart. A KPI such as "system availability ≥ 99.9%" should stay green forever — it is a vital sign. An OKR such as "make the shared care record trusted by front-line clinicians" describes a deliberate push over a quarter or two and is expected to retire once achieved. Confusing them leads teams to set OKRs on things that should simply stay well, and to treat steady-state gauges as if they were ambitions.

**Outcomes over outputs.** An *output* is what you produced (a portal launched, 500 staff onboarded). An *outcome* is the change in the world that resulted (referral-to-treatment time fell; duplicate testing dropped). Good key results are outcomes; weak ones are outputs dressed as goals. "Ship the new triage tool" is an output. "Cut inappropriate A&E attendances by X% in the pilot ICS" is an outcome.

**Leading vs lagging indicators.** *Lagging* indicators confirm results after the fact (annual mortality, year-end benefits realised). *Leading* indicators move earlier and predict the lag (weekly active clinician usage, time-to-first-value for a new user). Leaders need both: lagging measures for accountability, leading measures to steer while there is still time to act.

**Cascading vs aligning.** Naive OKR rollouts *cascade* — the chief executive's OKRs are chopped into departmental sub-goals, top-down. Mature ones *align* — teams write their own OKRs and negotiate the fit against organisational objectives, so front-line knowledge shapes the goal rather than merely receiving it. Doerr's guidance favours a mix, with a bias toward bottom-up ownership.

## Best practices

1. **Separate your gauges from your goals explicitly.** Keep a short KPI dashboard of steady-state health measures (availability, safety incidents, data quality, cost) that you expect to stay green, and a separate, smaller set of OKRs for the deliberate changes you are pursuing this quarter. Do not mix them on one list; the psychology of "keep this well" and "move this hard" is different.

2. **Write objectives that are qualitative, ambitious, and memorable.** An objective should inspire and set direction without a number in it: "Make discharge summaries something GPs actually trust." The measurement lives in the key results, not the objective. If a clinician cannot repeat the objective back from memory, it is too complicated.

3. **Make key results outcomes, and make them uncomfortable.** Each key result must be a measurable result, not a task, and should be set so that reaching 70% is a genuine stretch. Doerr distinguishes *committed* OKRs (must hit 100%) from *aspirational* ones (a 70% score is success); label which is which so nobody mistakes a moonshot for a broken promise.

4. **Limit to three to five per level.** The discipline of OKRs is subtraction. Three objectives, each with three to five key results, forces an organisation to say what matters most this quarter. A list of fifteen objectives is a list of none.

5. **Adopt DORA and flow metrics for delivery health.** For the health of your software delivery, use the four [DORA](https://en.wikipedia.org/wiki/DevOps) "keys" — deployment frequency, lead time for changes, change failure rate, and failed-deployment recovery time — with a fifth reliability signal. These are balanced by design: two throughput measures paired with two stability measures, so teams cannot ship faster by breaking more. Complement with flow metrics (flow time, work-in-progress, throughput) to see where value stalls.

6. **Pair every metric with a guardrail.** The concrete defence against gaming is to never let a metric travel alone. If you push deployment frequency, hold change failure rate as its counterweight; if you push referral throughput, hold a quality or safety measure beside it. A metric with no guardrail is an invitation to optimise the number and neglect the reality.

7. **Use a balanced scorecard to avoid single-lens tunnel vision.** Kaplan and Norton's [balanced scorecard](https://en.wikipedia.org/wiki/Balanced_scorecard) (Harvard Business Review, 1992) reminds leaders to view performance through several perspectives at once — financial, customer/patient, internal process, and learning and growth. In health and care, add a safety-and-quality lens. Balance stops a programme from winning on cost while losing on experience.

8. **Read health data with statistical process control, not month-on-month arrows.** A single "up or down since last month" comparison mistakes normal variation for signal. [Statistical process control](https://en.wikipedia.org/wiki/Statistical_process_control) (SPC) charts — championed across the NHS through the *Making Data Count* programme — distinguish [common-cause variation (noise) from special-cause variation](https://en.wikipedia.org/wiki/Common_cause_and_special_cause_(statistics)) (a real change), so you act on signal and ignore the rest. This is one of the highest-leverage measurement habits a health leader can build.

9. **Fix a cadence of check-ins.** OKRs are worthless if reviewed only at quarter-end. Run a lightweight weekly or fortnightly check-in on confidence and blockers, a mid-quarter reset, and an end-of-quarter score-and-reflect. The rhythm, not the spreadsheet, is what makes OKRs a management practice rather than a filing exercise (see Chapter 48 — Visibility for the CEO & Senior Leaders for how this feeds governance).

## Questions to discuss with your team

1. **Which of our current "key" metrics are genuinely goals we are trying to move, and which are gauges we simply need to keep well — and are we treating any of them as the wrong kind?**
   This is the foundational sort that most measurement conversations skip. A team that runs an OKR on system availability is trying to "move" a number that should simply stay green forever, wasting the ambition the framework exists to create; a team that files patient-facing outcomes on a steady-state KPI dashboard quietly stops pushing on the very change that justified the programme. Walk your actual dashboard line by line and force each metric into one bucket, because the psychology of "guard this" and "drive this" is different and mixing them dulls both. The honest tension is that some measures — data quality, say — can be both a health gauge and, for a quarter, a deliberate improvement goal; naming which role it plays *right now* is the discipline. Expect disagreement, especially where a KPI has become someone's comfort blanket or where an "objective" is really a laundry list of business-as-usual tasks. A good answer leaves you with a short, separate OKR set for this quarter's changes and a stable KPI layer everyone agrees should not be the subject of stretch goals, and it names at least one metric you have been mis-classifying.

2. **For each headline number we report upward, what is its named guardrail — and where are we currently exposed to gaming or Goodhart's law?**
   Every metric that carries pressure will, given time, be optimised at the expense of the reality it was meant to represent; the NHS's own history of stopped four-hour clocks and reclassified waiting lists is the cautionary evidence, not an abstraction. The exercise here is concrete: take your top five reported figures and, for each, name the counterweight that would go red if someone gamed it — throughput paired with a safety or quality measure, deployment frequency paired with change failure rate, referral volume paired with an appropriateness check. Where you cannot name a guardrail, you have found an exposure, and the debate should be whether the metric is safe to report at all without one. The trade-off to surface is that guardrails cost attention and can feel like distrust of good people, yet their absence is precisely what lets well-intentioned pressure distort behaviour and corrupt the underlying data. A strong answer produces a paired list — every headline number beside its counterweight — plus an honest register of the one or two numbers currently travelling alone and a plan to pair or retire them.

3. **How would we know whether a month-on-month move in one of our measures is a real signal or just noise, and what would we do differently if we read it on a statistical process control chart?**
   Reading performance as "up or down since last month" is one of the most common and most expensive measurement errors a health leader can make, because normal variation constantly produces arrows that mean nothing and tempt boards into reacting to noise. Statistical process control — embedded across the NHS through *Making Data Count* — distinguishes common-cause variation (the natural wobble of a stable system) from special-cause variation (a genuine change worth acting on), and the discussion should test whether your team can actually tell the two apart on your own data today. The tension is cultural as much as technical: SPC often reveals that a celebrated improvement or a panicked decline was within normal limits all along, which can be unwelcome to whoever claimed credit or sounded the alarm. Consider a live example — pick a metric that moved recently and ask what you *did* in response, then ask what SPC would have told you to do. A good answer commits to reading your most consequential measures on SPC charts, names who will build and maintain them, and identifies a recent decision that would have been different under this discipline.

## In practice: a health & care example

An integrated care system (ICS) is rolling out a shared care record so clinicians across acute, community, and social care see one view of a person. Six months in, the programme board is proud: the record is live in four of five places, 6,000 staff are trained, uptime is 99.95%. Yet clinicians still phone each other for information they distrust on screen.

The board had been managing outputs. It resets around one objective — **"Clinicians rely on the shared record instead of working around it"** — with three key results: (1) weekly active clinical users rise from 1,800 to 5,000; (2) the proportion of records with a complete, current medication list reaches 90%; (3) self-reported trust in the record (a short pulse survey) moves from 42% to 70%. These are outcomes, and 70% attainment would be a real stretch.

Alongside, the ICS keeps a separate KPI dashboard as steady-state gauges: availability, data-quality error rate, and information-governance incidents — each expected to stay green, each with a guardrail so the push for usage never comes at the cost of safety. Usage is plotted on an SPC chart, so when active users jump in one region the board can tell whether it is a genuine shift or a seasonal blip before it celebrates. Weekly check-ins surface the real blocker — a slow single-sign-on step that adds ninety seconds per login — which no output metric had exposed. The change that moves the outcome is a two-line authentication fix, not another training cohort.

## Three sector lenses

### Startup

A digital-health startup lives or dies by a handful of leading indicators, so its OKRs should track the change that proves the business model, not the vanity of shipping. With a runway measured in months, a sensible objective is "prove clinicians will use the product unprompted", with key results such as weekly active users, activation rate, and retention at 30 days — the same signals a [minimum viable product](https://en.wikipedia.org/wiki/Minimum_viable_product) is meant to test. Keep the KPI list tiny: cash runway, uptime, and one safety measure. The founder can run the whole OKR cadence on a single board, and should resist a funder's pull toward output metrics ("features delivered") that flatter the deck but predict nothing. The discipline here is honesty under pressure — a seed-stage team that games its own retention number is only lying to itself.

### Enterprise

An NHS trust, an integrated care system, or a large health-tech supplier has many programmes competing for the same board attention, so the risk is metric sprawl rather than metric scarcity. Enterprises should hold a stable KPI layer (availability, data quality, safety incidents, cost per case) that steady-state services must keep green, and reserve OKRs for the two or three deliberate changes each directorate is driving this quarter — aligned to strategy, not cascaded as compliance. Delivery health uses the full DORA and flow set because there are enough teams to compare, and every headline number carries a guardrail because scale multiplies the cost of gaming. The reporting rhythm must feed the governance machinery (see Chapter 48 — Visibility for the CEO & Senior Leaders), so OKR check-ins and board assurance stay reconciled rather than telling two different stories.

### Government

A national or local public body — NHS England, DHSC, UKHSA, or a local authority — sets measures that become de facto national targets, so Goodhart's and Campbell's laws bite hardest here. When a single figure (a four-hour wait, a referral-to-treatment clock) is published and tied to accountability, behaviour bends to the number and the underlying data degrades; guardrails, SPC, and outcome-not-output framing are not refinements but statutory safeguards of public money. Government measurement must also be transparent and auditable, because the numbers are matters of public record and Parliamentary scrutiny. The lesson from the NHS's own history is to publish few measures, pair every target with a counterweight, and read them as signals of a system's health rather than as levers to be yanked.

## Common failure modes

- **Vanity metrics.** Counting logins, page views, or deployments in isolation. Deploying forty times a day means nothing if half are hotfixes. Ask "so what changed for a patient?" of every headline number.
- **[Goodhart's](https://en.wikipedia.org/wiki/Goodhart%27s_law) / [Campbell's Law](https://en.wikipedia.org/wiki/Campbell%27s_law) in action.** "When a measure becomes a target, it ceases to be a good measure." Set a hard target on one number and behaviour bends to hit it — four-hour clocks stopped, waiting lists reclassified — while the underlying reality and the data itself degrade. Guardrails and SPC are the antidotes.
- **OKRs tied to pay.** Doerr is explicit: divorce OKRs from compensation. Link them to bonuses and teams sandbag the targets, killing the ambition the framework exists to create.
- **Cascade-only rollout.** Chopping the top team's goals downward with no negotiation produces compliance, not commitment, and wastes front-line insight.
- **Too many OKRs.** Fifteen objectives signal an organisation that has not chosen. The value is in the ruthless shortlist.
- **Confusing lagging accountability with leading control.** Reporting only year-end benefits leaves no lever to pull mid-flight. Pair every lagging outcome with a leading indicator you can act on now.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Goals vs gauges | Metrics and goals conflated in one list | KPIs listed, but no distinct change goals | OKRs and KPIs kept separate and understood | OKRs drive change; KPIs guard health; both reviewed on their own rhythm |
| Outcome focus | Reports outputs (delivered, trained) | Some outcome measures, mostly lagging | Key results are outcomes with leading + lagging pairs | Outcomes traced to patient/population benefit and cost |
| Delivery health | No delivery metrics | Ad-hoc velocity counts | DORA four keys + flow metrics with guardrails | Balanced throughput/stability tuned; SPC-read |
| Gaming defence | Single targets, no guardrails | Awareness of gaming, few controls | Every metric paired with a guardrail | Culture treats metrics as learning, not fear; SPC filters noise |
| Cadence | Quarter-end review only | Irregular check-ins | Weekly check-in + quarterly score | Embedded rhythm feeding governance and reprioritisation |

## Checklist

- [ ] Every "key" metric is labelled either a KPI (health, stay green) or an OKR key result (change, this quarter).
- [ ] Objectives are qualitative and memorable; key results are measurable outcomes, not tasks.
- [ ] No more than three to five objectives per level, each with three to five key results.
- [ ] Committed vs aspirational OKRs are labelled; 70% on an aspirational one counts as success.
- [ ] Each key result has at least one leading indicator you can act on before quarter-end.
- [ ] Delivery health uses the DORA four keys plus a reliability signal, balancing throughput and stability.
- [ ] Every headline metric has a named guardrail measure beside it.
- [ ] Health data is read on SPC charts, not month-on-month arrows.
- [ ] OKRs are explicitly not linked to individual pay.
- [ ] A fixed check-in cadence (weekly/fortnightly + quarterly score) is in the calendar and honoured.

## Key sources

- John Doerr, *Measure What Matters* (2018), and the What Matters resource library — OKR definition, committed vs aspirational goals, cadence, and the "divorce OKRs from compensation" principle. https://www.whatmatters.com/
- Kaplan & Norton, "The Balanced Scorecard — Measures that Drive Performance," *Harvard Business Review* (1992) — the multi-perspective performance framework.
- DORA (DevOps Research and Assessment), *DORA's software delivery performance metrics* — the four keys plus reliability. https://dora.dev/guides/dora-metrics/
- NHS England, *Making Data Count* — statistical process control for NHS performance data; distinguishing common-cause from special-cause variation.
- Goodhart's Law and Campbell's Law — the foundational cautions on target-driven measurement distortion.
- NHS England, *NHS Oversight Framework 2025/26* — outcome-based performance measurement in the NHS context. https://www.england.nhs.uk/long-read/nhs-oversight-framework-2025-26/

## References

1. OKR — Wikipedia — https://en.wikipedia.org/wiki/OKR
2. Performance indicator — Wikipedia — https://en.wikipedia.org/wiki/Performance_indicator
3. John Doerr — Wikipedia — https://en.wikipedia.org/wiki/John_Doerr
4. DevOps (DORA metrics) — Wikipedia — https://en.wikipedia.org/wiki/DevOps
5. Balanced scorecard — Wikipedia — https://en.wikipedia.org/wiki/Balanced_scorecard
6. Statistical process control — Wikipedia — https://en.wikipedia.org/wiki/Statistical_process_control
7. Common cause and special cause (statistics) — Wikipedia — https://en.wikipedia.org/wiki/Common_cause_and_special_cause_(statistics)
8. Goodhart's law — Wikipedia — https://en.wikipedia.org/wiki/Goodhart%27s_law
9. Campbell's law — Wikipedia — https://en.wikipedia.org/wiki/Campbell%27s_law
10. Minimum viable product — Wikipedia — https://en.wikipedia.org/wiki/Minimum_viable_product
11. *Measure What Matters* — John Doerr — https://www.whatmatters.com/
12. DORA's software delivery performance metrics — DevOps Research and Assessment (Google Cloud) — https://dora.dev/guides/dora-metrics/
13. The Balanced Scorecard — Measures that Drive Performance — Kaplan & Norton, *Harvard Business Review* (1992) — https://hbr.org/1992/01/the-balanced-scorecard-measures-that-drive-performance-2
14. Making Data Count — NHS England — https://www.england.nhs.uk/publication/making-data-count/
15. NHS Oversight Framework 2025/26 — NHS England — https://www.england.nhs.uk/long-read/nhs-oversight-framework-2025-26/
