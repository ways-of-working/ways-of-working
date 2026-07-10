# Chapter 3 — Evidence-Driven Decisions

**In one sentence:** Evidence-driven decision-making means deciding what to build, buy, and scale on the strength of the best available evidence — clinical and delivery — proportionate to the risk, and recording the reasoning so it survives the people who made it.

## Why this matters in health and care

In most sectors a bad product decision costs money. In health and care it can cost safety, equity, and trust — and it is made with public funds under statutory duty. A decision to deploy a digital diagnostic that has never been evaluated is not a commercial gamble; it is a clinical risk. This raises the bar for evidence far above "the demo looked good."

The domain is also distinctive because it demands **two kinds of evidence at once**. *Clinical evidence* answers "does this technology work, and is it safe and effective for patients?" *Delivery evidence* answers "are we building the right thing well, and is it being adopted and used?" A service can be clinically sound but a delivery failure (no one uses it), or a delivery success but clinically unproven (widely used, never validated). Senior leaders must demand both and never let one masquerade as the other. And because health decisions attract scrutiny — from regulators, the public, and clinicians — the *record* of why you decided matters as much as the decision.

## Core concepts

**The [hierarchy of evidence](https://en.wikipedia.org/wiki/Hierarchy_of_evidence).** [Evidence-based medicine](https://en.wikipedia.org/wiki/Evidence-based_medicine) ranks study designs by how well they control bias: at the top, [systematic reviews](https://en.wikipedia.org/wiki/Systematic_review) and [meta-analyses](https://en.wikipedia.org/wiki/Meta-analysis) of [randomised controlled trials](https://en.wikipedia.org/wiki/Randomized_controlled_trial) (RCTs); then individual RCTs; then cohort and case-control studies; then case series; and at the base, expert opinion and anecdote. The hierarchy is a guide, not a straitjacket — but it disciplines you to notice when a claim rests on anecdote dressed as proof.

**NICE Evidence Standards Framework (ESF) for digital health technologies.** NICE, with NHS England and partners, created the ESF to set out what level of evidence a digital health technology (DHT) needs, proportionate to its function and the risk it carries. It tiers DHTs by potential risk — from simple system services, through tools that inform or drive care, to those that directly diagnose or treat — and specifies the clinical effectiveness and economic evidence expected at each tier. The higher the clinical risk, the stronger the evidence required. The ESF is the reference point for commissioners and developers deciding whether a DHT is ready.

**Real-world data and [real-world evidence](https://en.wikipedia.org/wiki/Real_world_evidence).** Real-world data (RWD) comes from routine care — electronic health records, registries, patient-reported outcomes, device telemetry — rather than controlled trials. Analysed well (through prospective observational studies, pragmatic trials, or careful EHR analysis) it becomes real-world evidence (RWE) about how a technology performs in practice. RWE is essential for technologies that learn or change (AI, wearables), where a one-off trial cannot capture ongoing behaviour, but it carries confounding risks that must be handled honestly.

**Clinical evidence vs delivery evidence.** Keep these on separate axes. Clinical evidence uses the hierarchy above and the ESF: efficacy, safety, effectiveness. Delivery evidence uses product and service analytics: is the service usable, adopted, completing the user's task, reducing failure demand? Both are needed; conflating them is a classic error (a high usage figure is not clinical proof).

**Evaluation designs.** A **[logic model](https://en.wikipedia.org/wiki/Logic_model)** (or [theory of change](https://en.wikipedia.org/wiki/Theory_of_change)) makes explicit how inputs and activities are meant to produce outputs and outcomes — it is the map any evaluation tests. An **RCT** gives the strongest causal answer but is slow, costly, and sometimes impractical or unethical for a fast-moving service. **Pragmatic evaluation** — pragmatic trials, [interrupted time series](https://en.wikipedia.org/wiki/Interrupted_time_series), before/after with controls, mixed-methods service evaluation — trades some certainty for speed and real-world relevance. Choose the design proportionate to the risk and the decision at stake.

**[A/B testing](https://en.wikipedia.org/wiki/A/B_testing) and analytics.** For lower-risk, delivery-side questions (which wording increases appointment attendance? which flow reduces drop-off?), controlled online experiments (A/B tests) give fast, causal delivery evidence. They are powerful for optimisation but must never be used to make unassessed clinical changes, and must respect consent and information-governance boundaries.

**HiPPO decisions.** "HiPPO" — the Highest-Paid Person's Opinion — names the failure where seniority overrides evidence. Evidence-driven cultures make it safe and normal to say "what does the data show?" to anyone in the room, and treat a senior hunch as a hypothesis to test, not a conclusion.

**Decision records.** A decision record (or decision log / [architecture decision record](https://en.wikipedia.org/wiki/Architectural_decision)) captures, briefly: the decision, the options considered, the evidence weighed, who decided, and when. It makes reasoning auditable, survives staff turnover, and prevents the same argument being re-run every quarter.

## Best practices

1. **Match the strength of evidence to the level of risk.** Use the NICE ESF tiers as your yardstick: a low-risk system tool needs light evidence; a tool that diagnoses or drives treatment needs high-quality clinical effectiveness evidence. Proportionality lets you move fast on the safe and slow on the dangerous, rather than applying one bar to everything.

2. **Demand clinical and delivery evidence, and never confuse them.** For any significant investment, ask two separate questions — "is it clinically effective and safe?" and "is it usable and adopted?" — and require evidence for each. Adoption metrics are not a substitute for clinical validation, and a positive trial is not a guarantee of real-world use.

3. **Start every initiative with a logic model.** Before building, write down how you believe the intervention will produce the outcome you want. This exposes untested assumptions early, defines the metrics that matter, and gives your later evaluation something concrete to test.

4. **Use real-world evidence for technologies that learn or persist.** For AI, algorithms, and long-lived services, complement or follow initial trials with structured monitoring of routine data — prospective observational designs, pragmatic evaluation — so you know how performance holds up in practice and can catch drift.

5. **Experiment on delivery questions; evaluate clinical ones.** Use A/B testing and analytics freely for delivery optimisation (wording, flow, prompts), within information-governance and consent limits. Reserve formal evaluation (trials, pragmatic studies) for questions of clinical effect. Route each question to the right method.

6. **Kill HiPPO decisions culturally, not just procedurally.** Make it explicitly acceptable to ask any decision-maker for the evidence, frame senior views as hypotheses, and pre-commit to what evidence would change your mind. A team that can safely challenge seniority makes better decisions.

7. **Record decisions and their evidence.** Keep a lightweight decision log for every significant choice — what, why, what evidence, who, when. This creates auditability for regulators and the public, prevents endless re-litigation, and preserves institutional memory through staff churn.

8. **Attend to data ethics.** Evidence work uses patient data; treat lawfulness, consent, proportionality, and fairness as design constraints. Guard against biased datasets that entrench inequity, respect the duty of confidentiality, and ensure your evidence practices would themselves survive public scrutiny.

## Questions to discuss with your team

1. **For our most significant recent decision, can we point to both clinical evidence and delivery evidence — kept distinct — or did one quietly stand in for the other?**
   This question tests the chapter's insistence that clinical evidence ("does it work and is it safe?") and delivery evidence ("is it usable and adopted?") sit on separate axes and that conflating them is a classic, dangerous error. It matters because a service can be clinically sound yet unused, or heavily used yet clinically unvalidated, and in health and care mistaking a high usage figure for clinical proof can put patients at risk while looking like success. The tension to surface is that delivery evidence is fast, cheap, and flattering — analytics dashboards fill up quickly — whereas clinical evidence is slow, costly, and often inconclusive, so there is constant pressure to let adoption metrics carry the argument. Take a real board paper or investment case and audit it: are the two kinds of evidence separated, is each actually present, and does the clinical claim rest on anything above the vendor demo or a single-site study? A good, honest answer identifies a specific decision, admits where one evidence type was thin or absent, and commits to demanding both explicitly and separately in future significant choices rather than letting a strong usage number reassure everyone.

2. **How proportionate is our evidence bar really — are we demanding gold-standard trials for low-risk changes while waving through higher-risk tools on thin evidence?**
   The chapter frames proportionality through the NICE ESF tiers: light evidence for a low-risk system tool, high-quality clinical effectiveness evidence for a tool that diagnoses or drives treatment, so this question checks whether your organisation actually calibrates the bar to risk or applies one blunt standard. It matters because both failure directions are costly — analysis paralysis stalls a useful low-risk content change behind an unnecessary RCT, while an under-scrutinised AI tool that informs clinical decisions slips through on a compelling demo — and each undermines trust in the evidence culture. The trade-off to debate is that proportionality requires judgement and confidence to defend, which is harder than a uniform rule; a blanket "everything needs a trial" or "if it's digital, just pilot it" is easier to administer but wrong. Work through two or three current or recent technologies, place each in its ESF tier together, and check whether the evidence you demanded matched the tier or was driven by who was championing it. An honest answer shows the team can locate a technology's risk tier, admits where the bar has been mis-set in either direction, and treats proportionality as an explicit, defensible standard rather than an instinct.

3. **How safe is it, culturally, to ask the most senior person in the room "what's the evidence?" — and when did we last treat a leader's hunch as a hypothesis to test rather than a decision?**
   This question confronts the HiPPO failure mode directly, where the highest-paid person's opinion overrides evidence, and tests whether your stated commitment to evidence survives contact with hierarchy and the vendor demo that impressed a respected director. It matters because in health and care a demo-driven decision to deploy an unassessed tool is not a commercial gamble but a clinical-safety and public-money risk, and the moment challenge becomes unsafe is the moment evidence stops governing decisions. The real tension is that psychological safety cannot be mandated by policy; it is built by senior leaders visibly inviting challenge, framing their own views as hypotheses, and pre-committing to what evidence would change their mind — behaviours that feel exposing and are easy to skip under time pressure. Ground the conversation in specifics: recall a recent decision driven more by seniority or enthusiasm than data, and ask whether anyone challenged it, whether that felt safe, and what a decision record would have captured. A good answer is candid about where hierarchy currently wins, names concrete behaviours leaders will adopt to make challenge normal, and pairs the cultural commitment with the lightweight decision log that makes reasoning auditable and prevents the same argument being re-run.

## In practice: a health & care example

A community trust is offered an AI tool that flags patients at risk of deterioration from vital-signs data. A HiPPO decision would deploy it because a respected director was impressed by the vendor demo.

Instead the trust treats the pitch as a hypothesis. It places the tool in the NICE ESF risk tier appropriate to a technology that informs clinical decisions, and asks the vendor for effectiveness evidence at that level; the strongest thing offered is a small single-site study. The trust writes a **logic model** (better early warning → earlier escalation → fewer avoidable deteriorations) and designs a **pragmatic evaluation**: a shadow-mode deployment where the tool's alerts are logged but not acted on, compared against actual outcomes, plus qualitative interviews with nurses about workflow fit.

In parallel it gathers **delivery evidence**: would clinicians actually notice and trust the alerts? It runs A/B-style tests on alert presentation. The information-governance and clinical-safety leads sign off the data use and hazard log. After three months the RWE shows a modest but real improvement and an acceptable false-alert rate, and the delivery evidence shows clinicians engage with the redesigned alerts. The decision to proceed — with staged rollout and continued monitoring — is written into a decision record citing the evidence weighed. Two years later, when a new director questions the tool, the record answers.

## Three sector lenses

Everyone owes the same duty to match evidence to risk, but the resources, incentives, and accountability around evidence differ sharply by organisation.

### Startup

A startup's constraint is that gold-standard clinical evidence is slow and expensive while runway is short, so the temptation is to sell adoption metrics as if they were proof of clinical effect. The honest move is to place the product in the right NICE ESF tier early and be candid with buyers about the evidence gap, using a clear logic model and a cheap pragmatic evaluation (a shadow-mode pilot, an interrupted time series against a single site) to generate the first real-world evidence. Decision records cost almost nothing and are disproportionately valuable to a small team, preserving reasoning through rapid pivots and giving diligence-minded investors and NHS assessors an audit trail. The discipline that pays off is resisting the HiPPO founder-hunch and treating every "the demo landed well" as a hypothesis to test.

### Enterprise

An NHS trust or ICS has the routine data, the patient volumes, and the analytics capability to do serious evaluation — and the accountability that demands it, because deploying an unproven tool at scale is a clinical-safety and public-money risk simultaneously. The failure mode is institutional: a respected director championing a vendor demo, or a business case built on projected benefits no one later checks. The corrective is to make it culturally safe to ask any decision-maker "what's the evidence?", to keep clinical and delivery evidence on separate axes in every board paper, and to fund ongoing real-world monitoring for AI and long-lived services rather than validating once. A large pharma or health-tech enterprise brings formal trial machinery but must guard against publication bias and confounding in the real-world evidence it generates.

### Government

A national body — NICE, NHS England, DHSC, the MHRA, UKHSA — often sets the evidence bar others must clear, so its ways of working shape the whole market: the ESF, DTAC, and software-as-a-medical-device regulation are instruments of population-scale accountability. Decisions here attract regulatory, parliamentary, and public scrutiny, so the record of *why* a technology was recommended or procured matters as much as the decision, and transparency about evidence limitations is a duty, not a courtesy. The risk at this scale is mandating a technology across the system on thin evidence, or conversely demanding an RCT for a low-risk change and stalling useful innovation. The corrective is proportionality made explicit in published standards, plus attention to data ethics and fairness, because a biased dataset endorsed nationally entrenches inequity at scale.

## Common failure modes

- **Demo-driven decisions.** Buying because a demonstration impressed a senior leader. Antidote: treat pitches as hypotheses; demand tier-appropriate evidence.
- **Usage mistaken for validation.** Citing adoption numbers as proof a tool is clinically effective. Antidote: keep clinical and delivery evidence on separate axes.
- **One-and-done evaluation.** Validating once and never monitoring, especially for AI that drifts. Antidote: real-world evidence and ongoing monitoring.
- **Analysis paralysis.** Demanding an RCT for a low-risk content change. Antidote: proportionate methods; A/B and pragmatic evaluation where risk is low.
- **Unrecorded decisions.** No trace of why a choice was made, so it is re-argued and unauditable. Antidote: a lightweight decision log.
- **Ethics as paperwork.** Treating data ethics as a form to sign rather than a design constraint. Antidote: bake lawfulness, consent, and fairness into the evidence design.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Basis of decisions | Seniority / demos (HiPPO) | Some data consulted | Evidence routinely required, tiered to risk | Pre-committed evidence thresholds; hunches tested |
| Clinical vs delivery | Conflated or one ignored | Both mentioned | Both demanded and distinguished | Both continuously monitored |
| Evaluation | None or after the fact | Occasional, ad hoc | Logic models + proportionate designs | RWE and ongoing evaluation embedded |
| Data ethics | Afterthought | Compliance-only | Ethics designed in | Fairness and bias actively monitored |
| Decision records | None | Inconsistent notes | Standard decision log | Logs reused, audited, and learned from |

## Checklist

- [ ] Each technology is placed in a NICE ESF risk tier, with evidence demanded to match.
- [ ] Every significant decision has both clinical and delivery evidence, kept distinct.
- [ ] A logic model exists before building, naming the outcomes and metrics.
- [ ] Evaluation design is proportionate to risk (A/B and pragmatic for low; trials/RWE for high).
- [ ] Real-world evidence and monitoring are in place for AI and long-lived services.
- [ ] It is culturally safe to ask any decision-maker "what's the evidence?"
- [ ] Every significant decision is captured in a decision log (what, why, evidence, who, when).
- [ ] Data use is lawful, consented, proportionate, and checked for bias and fairness.

## Key sources

- NICE — *Evidence Standards Framework for digital health technologies (ESF)* (nice.org.uk).
- NHS England / NHSX — *Digital Technology Assessment Criteria (DTAC)*.
- MHRA — guidance on *software and AI as a medical device*.
- Oxford Centre for Evidence-Based Medicine — *Levels of Evidence* (hierarchy of evidence).
- HM Treasury — *The Magenta Book* (guidance on evaluation, logic models, and evaluation designs).
- MRC — *Developing and evaluating complex interventions* framework.
- Ron Kohavi et al. — *Trustworthy Online Controlled Experiments* (A/B testing).
- Michael Nygard — *Architecture Decision Records* (decision-log pattern).

## References

1. Hierarchy of evidence — Wikipedia — https://en.wikipedia.org/wiki/Hierarchy_of_evidence
2. Evidence-based medicine — Wikipedia — https://en.wikipedia.org/wiki/Evidence-based_medicine
3. Systematic review — Wikipedia — https://en.wikipedia.org/wiki/Systematic_review
4. Meta-analysis — Wikipedia — https://en.wikipedia.org/wiki/Meta-analysis
5. Randomized controlled trial — Wikipedia — https://en.wikipedia.org/wiki/Randomized_controlled_trial
6. Real world evidence — Wikipedia — https://en.wikipedia.org/wiki/Real_world_evidence
7. Logic model — Wikipedia — https://en.wikipedia.org/wiki/Logic_model
8. Theory of change — Wikipedia — https://en.wikipedia.org/wiki/Theory_of_change
9. Interrupted time series — Wikipedia — https://en.wikipedia.org/wiki/Interrupted_time_series
10. A/B testing — Wikipedia — https://en.wikipedia.org/wiki/A/B_testing
11. Architectural decision (Architecture Decision Records) — Wikipedia — https://en.wikipedia.org/wiki/Architectural_decision
12. Evidence Standards Framework for digital health technologies (ESF) — NICE — https://www.nice.org.uk/about/what-we-do/digital-health
13. Digital Technology Assessment Criteria (DTAC) — NHS England — https://www.nhs.uk/digital-technology-assessment-criteria-dtac/
14. Software and AI as a Medical Device — MHRA, GOV.UK — https://www.gov.uk/government/publications/software-and-artificial-intelligence-ai-as-a-medical-device
15. Oxford Centre for Evidence-Based Medicine: Levels of Evidence — University of Oxford — https://www.cebm.ox.ac.uk/resources/levels-of-evidence/ocebm-levels-of-evidence
16. *The Magenta Book* (guidance on evaluation) — HM Treasury, GOV.UK — https://www.gov.uk/government/publications/the-magenta-book
17. *Developing and evaluating complex interventions* — Medical Research Council (MRC) — https://www.mrc.ukri.org/documents/pdf/complex-interventions-guidance/
18. *Trustworthy Online Controlled Experiments* — Ron Kohavi, Diane Tang & Ya Xu, Cambridge University Press — https://experimentguide.com/
