# Chapter 3.4 — Discovery Phases

**In one sentence:** Discovery is the disciplined, time-boxed effort to understand your users and the real problem *before* you commit money, clinical risk, or reputation to building a solution.

## Why this matters in health and care

In most sectors, building the wrong thing wastes money. In health and care, it can also waste clinical time, entrench health inequalities, and — at the extreme — harm patients. A digital service that assumes every user has a smartphone, reliable broadband, and confident English quietly excludes the frail, the poor, and the [digitally marginalised](https://en.wikipedia.org/wiki/Digital_divide): precisely the people the NHS and social care exist to serve. Discovery is where you find that out for the price of a few weeks of research, rather than after a national rollout.

Health and care spending is public money held in trust, and much of it flows through statutory duties: the [NHS Constitution](https://en.wikipedia.org/wiki/NHS_Constitution_for_England), the public sector equality duty under the [Equality Act 2010](https://en.wikipedia.org/wiki/Equality_Act_2010), and the Caldicott principles for handling confidential patient information. Discovery is the phase where you test whether a proposed service is *needed*, *lawful*, *safe*, and *equitable* — before those questions become expensive to answer. Skipping it does not remove the questions; it merely defers them to a point where the honest answer is politically impossible to accept.

The NHS Digital Service Standard and the GOV.UK Service Manual both make discovery the mandatory first phase of any user-facing digital service for exactly this reason. It is not bureaucratic theatre. It is the cheapest insurance you will ever buy.

## Core concepts

**Discovery, defined.** Discovery is a short (typically 6–10 week) phase whose goal is to understand a problem space: who the users are, what they are trying to do, what stops them, what already exists, and whether there is a problem worth solving at all. Its output is *understanding and evidence*, not a product. A good discovery can validly conclude "do nothing" or "this is a policy problem, not a digital one."

**The double diamond.** The [Design Council's](https://en.wikipedia.org/wiki/Design_Council) [double diamond](https://en.wikipedia.org/wiki/Double_Diamond_(design_process_model)) (2005) frames design as two linked diamonds. The first — **Discover** then **Define** — diverges to explore the problem widely, then converges to frame it precisely. The second — **Develop** then **Deliver** — diverges to explore solutions, then converges to build one. Discovery, as a delivery phase, lives almost entirely in the first diamond. The recurring failure is teams sprinting into the second diamond before the first is finished.

**User need versus stakeholder want.** A *user need* is something a person is trying to accomplish, expressed from their point of view ("I need to know my appointment is confirmed so I don't take a day off work for nothing"). A *stakeholder want* is a feature or solution someone has already decided on ("we need an app"). Discovery's core discipline is translating wants back into needs, because needs are stable and solutions are cheap and interchangeable once the need is clear.

**Problem framing.** How you state a problem constrains every solution you will consider. "Patients miss appointments" invites a reminder app. "Patients cannot easily rearrange appointments that no longer suit them" invites self-service rebooking. Same symptom, different problem, radically different service. Discovery earns its keep largely in the quality of the [problem statement](https://en.wikipedia.org/wiki/Problem_statement) it produces.

**Assumptions, hypotheses, and evidence.** Every project rests on assumptions. Discovery makes them explicit, ranks them by risk, and tests the riskiest ones with real users. The goal is not certainty — that is unattainable — but *reduced uncertainty on the things that would sink the project*.

## Best practices

1. **Start from a problem, not a solution.** Write the problem statement before anyone names a technology. If the funding bid, the board paper, or the supplier pitch already specifies "an app" or "a portal," treat that as an assumption to test, not a decision to implement. Solutions arrived at before the problem is understood are almost always someone's habit, not the user's need.

2. **Do real [user research](https://en.wikipedia.org/wiki/User_research) with real users.** Interview and observe the actual people who will use the service — patients, carers, receptionists, community nurses, social workers — in their real context, not a workshop of managers speaking on their behalf. Aim for depth over volume; a dozen well-chosen [contextual interviews](https://en.wikipedia.org/wiki/Contextual_inquiry) reveal more than a thousand-response survey. Recruit deliberately for the users who are hardest to reach, because they are the ones a service most often fails.

3. **Map the whole service, not the digital sliver.** Users experience an end-to-end service — a referral, an assessment, a treatment, a follow-up — of which your digital component is one step. Map the current journey across every channel and organization, including the paper, phone, and face-to-face parts. Digital changes routinely fail because they optimize one step and break the two on either side of it.

4. **Frame the problem explicitly and get it agreed.** Produce a written problem statement and the evidence behind it, and secure explicit agreement from your senior sponsor. This artefact is your contract: it defines what "done" means for the next phases and gives you the standing to say no to scope that does not serve the agreed problem.

5. **Size the opportunity and the risk honestly.** Estimate how many people are affected, how badly, and what it costs the system today. Pair this with the risks a solution would introduce — clinical, information governance, equity, delivery. Leaders fund discoveries; they *decide* on the basis of a defensible opportunity-and-risk picture, so give them one.

6. **Design for the edges from day one.** Recruit research participants across the digital-inclusion spectrum, test against [Web Content Accessibility Guidelines](https://en.wikipedia.org/wiki/Web_Content_Accessibility_Guidelines) (WCAG 2.2 AA) expectations early, and treat assisted-digital and offline routes as first-class, not afterthoughts. In health and care, the excluded user is often the high-need user; a service that works only for the confident and connected widens inequality.

7. **Keep it multidisciplinary and time-boxed.** Staff discovery with a user researcher, a service designer, a product person, a technical architect, and — for anything touching care — clinical and information-governance input. Time-box it hard (weeks, not quarters) to force convergence. An open-ended discovery is a warning sign that the team is avoiding a decision.

8. **Write down what would make you stop.** Agree, at the start, the conditions under which the honest recommendation would be "do not proceed": no genuine user need, an insurmountable IG or safety barrier, a better non-digital fix, or a problem owned by another team. A discovery that *cannot* recommend stopping is not a discovery; it is a pre-justified build.

## Questions to discuss with your team

1. **What would we have to see in discovery to honestly recommend "do not proceed", and does anyone in this room have the standing to say it?**
   Stop conditions are worthless if they cannot be exercised, and in health and care the pressure not to exercise them is intense: a director has announced the app, a supplier contract is half-signed, or a funding window closes if the team hesitates. This question forces a team to name the specific evidence — no genuine user need, an insurmountable information-governance or clinical-safety barrier, a better non-digital fix, a problem owned by another service — that would flip the recommendation to stop, and to write it down before the research begins so it cannot be quietly redefined later. The tension worth debating is between sponsor confidence and researcher independence: a discovery that structurally cannot say no is a pre-justified build wearing discovery's clothes. Consider who protects the researcher's findings from editing, whether an outsider reviews the evidence, and what the last discovery your organization actually stopped was — if there isn't one, that is itself a finding. An honest answer identifies the real reasons "no" is hard here and a concrete mechanism (agreed stop criteria, an independent challenge, a sponsor who has publicly blessed the possibility of stopping) that makes it sayable.

2. **Who are the users we are most likely to exclude, and how will we get them into the research rather than deferring them to beta?**
   In health and care the excluded user — the frail, the digitally marginalized, the person with low confidence in English, the carer juggling three systems — is disproportionately the high-need user the service exists to serve, so sampling for convenience quietly designs inequality into the architecture. The trade-off to debate is depth and inclusion versus the schedule and recruitment cost: reaching the hardest-to-reach takes time, community partners, incentives, and assisted or offline research methods that a rushed discovery is tempted to skip "for now". Concrete angles include mapping the digital-inclusion spectrum explicitly, recruiting through voluntary-sector and clinical gatekeepers rather than a mailing list, and treating assisted-digital and non-digital routes as first-class findings rather than afterthoughts. It is worth naming the public sector equality duty and the Caldicott context so inclusion is understood as a legal and ethical obligation, not a nicety. A good answer produces a named recruitment plan that deliberately over-samples the edges, and a clear statement of which users the team will treat as the design's centre of gravity.

3. **Have we framed a problem, or have we smuggled a solution into the problem statement?**
   How a problem is stated silently constrains every solution the team will consider — "patients forget appointments" invites a reminder app, while "patients cannot easily rearrange appointments that no longer suit them" invites self-service rebooking and a slot-policy review — so the wording of the problem statement is where discovery earns most of its keep. The debate is whether the funding bid, board paper, or supplier pitch has already fixed the answer ("an app", "a portal", "an AI triage tool") and dressed it as a need, and whether the team has the discipline to translate that want back into the underlying user goal. Useful angles include banning solution nouns from the problem statement, mapping the whole end-to-end service across every channel and organization so the digital sliver is seen in context, and checking each stated need is expressed from the user's point of view rather than the organization's. Evidence matters here: a framing should be traceable to what real users said and did, not to a habit or a strategy slide. An honest answer either confirms the statement names a stable user need with evidence behind it, or admits a solution has been assumed and reopens the framing before any alpha is scoped.

4. **Do we have the right disciplines in the room, and are clinical safety and information governance shaping the work rather than signing it off at the end?**
   A discovery staffed only by a product manager and a delivery lead will find product and delivery problems; the users, clinicians, and legal duties it never invites into the room become the risks that surface expensively in alpha or, worse, after go-live. The tension is that a genuinely multidisciplinary team — user researcher, service designer, technical architect, clinical safety officer, information-governance and Caldicott expertise — is scarce, competed-for, and slow to convene, so teams are tempted to "borrow" a clinician for an hour or bolt IG on as a final gate. That sequencing is the trap: clinical safety and IG are cheap to design in during framing and ruinously expensive to retrofit once an architecture assumes data will flow across organizational boundaries. Concrete angles include naming a clinical safety officer from week one for anything touching care, treating a data protection impact assessment as a live discovery artefact rather than a later formality, and checking whether the people who understand the frontline workflow are contributors or merely consultees. An honest answer names who is actually in the team, which duties are represented by a person versus a checkbox, and where the discovery would be blind because a discipline is missing.

5. **How will we know discovery is finished, and what stops it drifting for months or being cut off after a fortnight?**
   Discovery has two opposite failure modes and both are about time: the unbounded study that maps everything and decides nothing, and the truncated fortnight that rushes to a foregone conclusion because a delivery date was fixed before the research began. The discipline the double diamond demands is convergence — knowing when the problem is understood well enough to make a defensible decision, not when every question has been answered, because certainty is unattainable and the goal is reduced uncertainty on the things that would sink the project. The trade-off worth debating is depth versus momentum: a hard time-box of weeks forces the team to prioritize the riskiest assumptions, but a box set too tight starves the inclusive, hard-to-reach research that this domain most needs. Useful angles include agreeing the decision the discovery must inform and the artefacts a sponsor needs to make it, ranking assumptions so the box is spent on what matters, and naming a decision point rather than letting the phase dribble into an unacknowledged alpha. An honest answer states how long the box is, what "understood enough" looks like for this problem, and who calls the end.

6. **When discovery ends, can we hand a funding board a defensible picture of the opportunity and the risk — or only a story?**
   Leaders do not fund understanding; they fund decisions, and a discovery that produces rich insight but no board-legible account of how many people are affected, how badly, what it costs the system today, and what a solution would put at risk leaves the decision to whoever tells the most confident story. The tension is between the researcher's nuanced, caveated findings and the board's need for a sized, comparable, defensible case — compress too hard and you lose the equity and safety subtleties that were the point; refuse to compress and the evidence never reaches the people who allocate money. In health and care the picture must pair opportunity with the risks a solution introduces — clinical, information-governance, equity, delivery — because a board that sees only upside is being set up to make a bad bet. Concrete angles include sizing the affected population from real data rather than a hopeful estimate, making findings traceable so a sceptic can follow them back to what users said, and framing the recommendation (including "do not proceed" or "alpha this narrower thing") in terms the next phase can act on. An honest answer shows the team can move from evidence to a recommendation a funding board could scrutinize in the open without it falling apart.

## In practice: a health & care example

An integrated care system (ICS) is under pressure to reduce did-not-attend (DNA) rates at outpatient clinics. A supplier has pitched an AI-powered reminder app, and a director is keen to fund it. Instead of buying, the ICS runs an eight-week discovery.

The user researcher interviews eighteen patients who recently missed appointments, plus receptionists and two clinic managers. A pattern emerges that the reminder theory missed: many "no-shows" had *tried* to rearrange but hit an engaged phone line for days, or had been given an appointment during working hours they could not take without losing pay. A subset had died or been admitted elsewhere and were still on the list. Reminders would not touch any of these causes.

The team maps the end-to-end booking journey and finds three organizations, two patient administration systems, and a fax machine in the loop. They reframe the problem from "patients forget appointments" to "patients cannot easily reach us to rearrange appointments that no longer work for them." They quantify it: roughly 40% of DNAs at the sampled clinics involved a failed prior contact attempt. They flag an information-governance question (a shared rebooking tool would cross organizational boundaries) and an equity finding (the highest DNA rates were among patients in the most deprived postcodes, for whom the working-hours slot was the barrier).

The discovery recommends *against* the app, and *for* an alpha exploring self-service rebooking plus a review of slot-scheduling policy. The reframed problem is agreed by the sponsor, a clinical safety officer is named for the alpha, and a [data protection impact assessment](https://en.wikipedia.org/wiki/Privacy_impact_assessment) is commissioned. The ICS has spent eight weeks and avoided funding a solution that would have failed measurably in public.

## Sector lenses

### Startup

A digital-health startup runs discovery on a shoestring and against the clock — often the "discovery" is the founders' own lived experience plus a fortnight of user interviews squeezed between investor meetings. The funding pressure is to show traction, which tempts founders to skip straight to a demo; the discipline that matters most is naming the riskiest assumption and killing the idea cheaply if it fails, because a startup cannot afford to build the wrong thing even once. Accountability runs to investors and early adopters rather than a statutory board, so stop conditions are commercial (no willingness to pay, no reachable market) as much as clinical. The upside is speed and the freedom to pivot; the risk is mistaking a compelling founder narrative for evidence of a real user need.

### Small business

An established small provider — a GP practice, a community pharmacy, a care home, a domiciliary-care agency, a single-site clinic, or a small health-tech supplier past the pre-revenue stage — has real patients and running operations, but rarely a spare user researcher or service designer to staff a formal discovery. Here discovery is lightweight and opportunistic: the "research" is the receptionist who already knows why patients cannot get through on the phone, the care workers who see the paperwork duplication daily, and a handful of deliberate conversations with the users a change would affect. The trap is that the same statutory duties — Caldicott, UK GDPR, the equality duty, clinical safety — apply in full whether or not there is anyone in-house who owns them, so the discipline that matters most is framing the problem honestly and testing the riskiest assumption before committing scarce cash to a supplier's product. Because ongoing operations cannot pause, a small provider often runs its discovery around a single concrete pain point rather than a broad problem space, and its most valuable stop condition is recognizing when the fix is a process change or a shared regional platform rather than a system to buy.

### Enterprise

An NHS trust or large health-tech supplier can staff a proper multidisciplinary discovery — user researchers, service designers, clinical safety, information governance — but must fight organizational gravity: an incumbent supplier contract, a board that has already announced "the app", or a business case that pre-decided the solution. Here discovery's hardest work is political — reframing a sanctioned solution back into a user need without losing sponsor support. Funding is annual and committee-bound, so discoveries compete for slots and must produce board-legible artefacts. Risk appetite is low and accountability broad (regulators, auditors, the public), which makes an honest "do not proceed" both more valuable and harder to say aloud.

### Government

A national or local public body — NHS England, DHSC, a devolved government, a local authority — runs discovery under the full weight of the Service Standard, spend-control gates, and public scrutiny, where the discovery report itself may be published and challenged. The user base is enormous and the duty to include the marginalized is a legal, not optional, concern, so inclusive recruitment and assisted-digital routes are mandatory from the first week. Accountability runs to ministers, Parliament, and the electorate, so a discovery must be defensible in the open and can be halted by spend controls when the evidence is weak. The trade-off is rigour versus pace: government discovery is slower and more assured, which protects public money but can frustrate teams used to moving fast.

## Common failure modes

- **Solutioning too early.** The team enters discovery with the answer already chosen and spends the weeks building a business case for it. Antidote: ban solution nouns from the problem statement; make the riskiest assumption a research question.
- **Research theatre.** A few friendly stakeholders are consulted, hard-to-reach users are skipped "for time," and the findings conveniently confirm the plan. Antidote: recruit for the edges; have research findings challenged by someone outside the team.
- **The discovery that cannot say no.** Funding, politics, or a signed contract make "do not proceed" unsayable, so discovery becomes ritual. Antidote: agree stop conditions up front and protect the researcher's independence.
- **Boiling the ocean.** An unbounded discovery drifts for months, mapping everything and deciding nothing. Antidote: a hard time-box and a named decision at the end.
- **Ignoring the non-digital service.** The team studies the screen and misses the phone line, the letter, and the receptionist that actually carry the journey. Antidote: map all channels and organizations end to end.
- **Treating accessibility and inclusion as later.** Edge users are deferred to beta, by which point the architecture excludes them. Antidote: recruit inclusively and test against WCAG from the first prototype.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| Problem framing | Solution assumed; no written problem statement | Problem written but solution-shaped | Explicit, evidence-based problem statement agreed with sponsor | Framing quality assured against agreed criteria at a decision gate; each statement's evidence and scope reviewed | Problem framing routinely reshapes strategy and stops weak ideas |
| User research | Opinions of managers stand in for users | Some user interviews, convenience-sampled | Contextual research with a deliberate, inclusive sample | Inclusion and sample coverage tracked against targets; research quality assured through a repeatable, governed process | Continuous research capability; edge users routinely included |
| Decision to proceed | Build was pre-decided; discovery is ritual | Go/no-go exists but rarely "no" | Documented stop conditions; "do nothing" is a real outcome | Decisions governed against agreed criteria; stop and proceed rates and their rationale tracked and reviewed | Portfolio-level triage kills weak discoveries early and cheaply |
| Health-specific risk | Clinical safety, IG, equity considered post-build | Raised late, by exception | Clinical, IG, and equity input embedded in the team | Clinical safety, IG and equity risks logged, quantified and assured against controls and targets | Safety and equity findings shape the problem, not just the sign-off |
| Outputs | Slide deck, no evidence trail | Report with mixed evidence | Traceable findings, prioritized assumptions, clear recommendation | Output quality and uptake measured; recommendations tracked to the decisions they informed | Reusable insight feeding the wider portfolio and reused across services |

## Checklist

- [ ] There is a written problem statement that names a user need, not a solution.
- [ ] Real users — including the hardest to reach — have been interviewed or observed in context.
- [ ] The end-to-end service is mapped across all channels and organizations.
- [ ] The riskiest assumptions are listed, ranked, and the top ones tested.
- [ ] Clinical safety, information governance (Caldicott, UK GDPR/DPIA), and health-inequality risks are identified.
- [ ] Accessibility (WCAG 2.2 AA) and digital inclusion are considered from the first prototype.
- [ ] Stop conditions were agreed at the start, and "do not proceed" is a genuine possible outcome.
- [ ] The opportunity is sized and the recommendation is defensible to a funding board.
- [ ] A multidisciplinary team (including clinical/IG input) ran the phase within a fixed time-box.
- [ ] The sponsor has agreed the problem statement before any alpha begins.

## Key sources

- NHS England — NHS Digital Service Manual and NHS Service Standard (service.nhs.uk).
- GOV.UK Service Manual — "How the discovery phase works" and the Government Service Standard (Government Digital Service).
- Design Council — *The Double Diamond* design process framework.
- NHS England — Digital Technology Assessment Criteria (DTAC): clinical safety, data protection, technical assurance, interoperability, usability and accessibility.
- NICE — Evidence Standards Framework for Digital Health Technologies.
- Web Content Accessibility Guidelines (WCAG) 2.2, W3C; and GOV.UK guidance on accessibility and assisted digital.
- UK Caldicott Principles and the Data Protection Act 2018 / UK GDPR (data protection impact assessments).
- Equality Act 2010 — the public sector equality duty (relevant to health-inequality assessment in discovery).

## References

1. Double Diamond (design process model) — Wikipedia — https://en.wikipedia.org/wiki/Double_Diamond_(design_process_model)
2. Design Council — Wikipedia — https://en.wikipedia.org/wiki/Design_Council
3. User research — Wikipedia — https://en.wikipedia.org/wiki/User_research
4. Contextual inquiry — Wikipedia — https://en.wikipedia.org/wiki/Contextual_inquiry
5. Problem statement — Wikipedia — https://en.wikipedia.org/wiki/Problem_statement
6. Web Content Accessibility Guidelines — Wikipedia — https://en.wikipedia.org/wiki/Web_Content_Accessibility_Guidelines
7. Equality Act 2010 — Wikipedia — https://en.wikipedia.org/wiki/Equality_Act_2010
8. NHS Constitution for England — Wikipedia — https://en.wikipedia.org/wiki/NHS_Constitution_for_England
9. Digital divide — Wikipedia — https://en.wikipedia.org/wiki/Digital_divide
10. Privacy impact assessment (data protection impact assessment) — Wikipedia — https://en.wikipedia.org/wiki/Privacy_impact_assessment
11. How the discovery phase works — Government Digital Service, GOV.UK Service Manual — https://www.gov.uk/service-manual/agile-delivery/how-the-discovery-phase-works
12. NHS service standard and NHS digital service manual — NHS England — https://service-manual.nhs.uk/
13. The Double Diamond — Design Council — https://www.designcouncil.org.uk/our-resources/the-double-diamond/
14. Web Content Accessibility Guidelines (WCAG) 2.2 — W3C — https://www.w3.org/TR/WCAG22/
15. Equality Act 2010 — UK legislation (legislation.gov.uk) — https://www.legislation.gov.uk/ukpga/2010/15/contents
16. Data protection impact assessments (DPIAs) — Information Commissioner's Office (ICO) — https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/accountability-and-governance/data-protection-impact-assessments-dpias/
17. The Caldicott Principles — National Data Guardian, GOV.UK — https://www.gov.uk/government/publications/the-caldicott-principles
18. Evidence standards framework for digital health technologies — NICE — https://www.nice.org.uk/about/what-we-do/digital-health
