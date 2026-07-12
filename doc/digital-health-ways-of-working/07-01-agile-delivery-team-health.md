# Chapter 7.1 — Agile Delivery Practices & Team Health

**In one sentence:** How a delivery team actually works week to week — its cadence, its ceremonies, its working agreements, and above all its health — is not soft-skills decoration but the operating system that determines whether safe, usable digital care gets shipped and sustained.

## Why this matters in health and care

Chapter 7.0 — Team Structures, Roles & Responsibilities drew the boundaries around your teams and named who does what. This chapter is about what happens inside those boundaries once the work starts: the rhythm of a fortnight, the meetings people actually attend, the agreements that govern behaviour, and the human sustainability that keeps a team functioning under load. Structure is the anatomy; ways of working are the physiology.

In health and care this matters more than in most sectors because the teams building and running digital services frequently support clinical operations that never stop. A team that maintains an electronic patient record, an e-prescribing system, or a bed-management platform is on the critical path of care delivery. When that team is exhausted, silenced, or drowning in unplanned work, the failure mode is not a missed marketing deadline — it is a delayed diagnosis, a medication error, or a safety incident that a rested, psychologically safe team would have caught and flagged.

There is strong evidence that team climate affects clinical outcomes. Research into patient safety consistently links the ability of staff to speak up about risk with the prevention of harm, and reviews of NHS failings — from Mid Staffordshire onward — repeatedly find cultures where concerns were not voiced or not heard. The way your delivery team runs its stand-ups and retrospectives is a small-scale version of the same question: can people say "this isn't safe" without fear? How you work is a clinical-safety and public-trust issue, not merely a productivity one.

## Core concepts

**[Agile software development](https://en.wikipedia.org/wiki/Agile_software_development).** A family of approaches, codified in the 2001 Agile Manifesto, that favour working software, close collaboration with users, and responding to change over exhaustive up-front planning. In health and care, agile is not licence to skip governance — it is a way to surface clinical-safety and information-governance questions early and often, rather than at the end. Agility is a means to safe, valuable delivery, not an end in itself.

**[Iterative and incremental development](https://en.wikipedia.org/wiki/Iterative_and_incremental_development).** Building a service in small increments, each usable and each generating feedback that shapes the next. This is the core mechanic beneath all agile methods: you learn by shipping thin slices and observing real use, rather than by predicting everything in advance.

**[Scrum](https://en.wikipedia.org/wiki/Scrum_(project_management)).** The most widely adopted agile framework, organizing work into fixed-length iterations called sprints (typically one to two weeks), each bracketed by planning at the start and a review and retrospective at the end, with a daily [stand-up meeting](https://en.wikipedia.org/wiki/Stand-up_meeting) to coordinate. Scrum's value is its predictable cadence and its built-in inspect-and-adapt loop; its risk is being adopted as ritual without the underlying transparency.

**[Kanban](https://en.wikipedia.org/wiki/Kanban_(development)).** A continuous-flow method that visualizes work on a board, limits the amount of work in progress (WIP) at each stage, and manages flow rather than time-boxed batches. Kanban suits teams doing operational and support work where demand is unpredictable — much of health and care live-service work — because it does not force irregular arrivals into artificial sprint boundaries. WIP limits are its signature discipline: a team that agrees to work on no more than, say, three items at once finishes things faster than one that starts everything and completes nothing.

**Definition of Ready and Definition of Done.** Two shared agreements that bound quality. A Definition of Ready states the conditions a piece of work must meet before the team will start it (clear user need, acceptance criteria, any clinical-safety or accessibility considerations identified). A Definition of Done states what "finished" means (tested, accessible, documented, safety impact assessed, deployed). In health and care, the Definition of Done is where you hard-wire non-negotiables — DCB0129/DCB0160 clinical-risk activities, accessibility to WCAG 2.2, information-governance sign-off — so they cannot be quietly dropped under deadline pressure.

**Team working agreement (or charter).** A short, team-owned document setting out how the team chooses to work: core hours, meeting norms, how decisions are made, how disagreement is handled, how on-call is shared. It converts implicit assumptions into explicit, revisable agreements, which is especially valuable in multidisciplinary teams where clinicians, engineers, and researchers arrive with very different professional norms.

**[Psychological safety](https://en.wikipedia.org/wiki/Psychological_safety).** The shared belief, studied extensively by Amy Edmondson, that a team is safe for interpersonal risk-taking — that you can ask a question, admit a mistake, or raise a concern without being punished or humiliated. It is the single strongest correlate of effective teams in Google's well-known Project Aristotle research, and in healthcare it is directly linked to error reporting and learning. A team without it will hide problems until they become incidents.

**[Occupational burnout](https://en.wikipedia.org/wiki/Occupational_burnout).** A syndrome, recognized by the World Health Organization, resulting from chronic unmanaged workplace stress, characterized by exhaustion, cynicism, and reduced efficacy. Sustainable pace — the agile principle that a team should be able to maintain its rhythm indefinitely — is the countermeasure. For teams supporting safety-critical clinical systems, burnout is a safety risk, because tired people supporting 24/7 services make errors.

**[Continual improvement](https://en.wikipedia.org/wiki/Continual_improvement_process).** The disciplined habit of making small, regular changes to how you work, informed by evidence. Team-level retrospectives are one instance of it; Chapter 10.2 — Quality Improvement & Improvement Science covers the broader science, including Plan-Do-Study-Act cycles, which apply as much to your ways of working as to clinical pathways.

## Best practices

1. **Choose cadence to match the nature of the work, not fashion.** Use time-boxed sprints (Scrum) where work is plannable and you benefit from a predictable heartbeat and stakeholder rhythm; use continuous flow with WIP limits (Kanban) where demand is unpredictable, as in live-service support and operational teams. Many health and care teams do both — a "Scrumban" hybrid — running discovery and build in sprints while handling live incidents on a flow board. Decide deliberately and revisit the decision, rather than inheriting whichever your last supplier used.

2. **Run ceremonies for their purpose, and kill them when they stop serving it.** A stand-up exists to surface blockers and coordinate the day, not to report status to a manager; a review or show-and-tell exists to get feedback from real users and stakeholders on working software; a retrospective exists to change how the team works next week. If a meeting no longer achieves its purpose, shorten it, restructure it, or stop it. The test is simple: would attendees pay to be there?

3. **Make show-and-tells the moment clinicians and users see real progress.** A fortnightly review that demonstrates working software to the clinicians, patients, and operational staff who will use it keeps the feedback loop tight and builds the trust that adoption depends on. Invite the people who will live with the service, demonstrate on realistic (not cherry-picked) scenarios, and capture what you learn as backlog changes. This is your cheapest insurance against building the wrong thing.

4. **Write a Definition of Ready and a Definition of Done, and put the non-negotiables in Done.** Agree the conditions for starting and finishing work, and encode clinical-safety activity, accessibility, information-governance sign-off, and adequate testing into your Definition of Done so they are structural, not heroic. When a deadline squeezes, an explicit Done gives the team the language to refuse to ship unsafe work. See Chapter 3.6 — DevOps & Engineering Excellence for how continuous delivery pipelines can automate parts of Done.

5. **Limit work in progress.** Starting is easy and satisfying; finishing is what delivers value and reduces risk. Agreeing WIP limits forces the team to swarm on completing work before pulling in more, which shortens lead times, exposes bottlenecks, and — critically in health — reduces the number of half-finished, partially-tested changes in flight at once. A visible board with explicit limits is often the single highest-leverage change a struggling team can make.

6. **Co-author a working agreement and treat it as living.** Have the team write its own charter — meeting norms, core collaboration hours, decision-making, on-call fairness, how to disagree well — and review it periodically. Because digital health teams are multidisciplinary, spanning clinical and technical cultures with different defaults, making norms explicit prevents the quiet friction that erodes trust. A charter imposed from above is theatre; one the team owns is a genuine instrument.

7. **Protect sustainable pace deliberately, and watch the leading indicators of burnout.** Plan to a capacity the team can hold indefinitely, not a heroic peak; guard against the permanent crunch that treats overtime as normal. Monitor leading signals — rising unplanned work, shrinking retrospective candour, people skipping leave, on-call fatigue — and act before they become resignations or incidents. For teams underpinning 24/7 clinical services, share on-call fairly, honour time back, and staff for resilience, not just the happy path (see Chapter 3.8 — Service Management & Live Operations).

8. **Build psychological safety on purpose.** Leaders set the tone: frame work as a learning problem, admit your own mistakes, respond to bad news with curiosity rather than blame, and thank people for raising concerns. Run blameless post-incident reviews. In a clinical-adjacent setting, the willingness to say "I think this release is unsafe" or "I don't understand this requirement" is the mechanism by which harm is prevented — so it must be actively cultivated, not assumed.

9. **Use lightweight team-health checks to make the invisible visible.** Periodically run a structured self-assessment — the "squad health check" model popularized by Spotify, where a team rates itself green/amber/red across dimensions such as delivering value, learning, fun, mission clarity, and support — to surface trends over time. The value is not the scores but the conversation they start and the way they let a team spot a slide before it becomes a crisis. Keep it fast, anonymous where helpful, and owned by the team.

10. **Run retrospectives that actually change behaviour.** A retrospective that generates a list of grumbles and no action is worse than none, because it teaches the team that speaking up is pointless. End each one with a small number of concrete, owned, time-bound experiments; start the next by checking whether the last ones happened. Treat improving your ways of working as its own continual-improvement backlog, linking to the improvement science in Chapter 10.2.

11. **Design for remote, hybrid, and asynchronous collaboration as the default.** Health and care delivery teams are frequently distributed across trusts, regions, and suppliers, so treat good written communication, well-run video ceremonies, and asynchronous decision records as core competencies, not fallbacks. Default to documenting decisions where absent colleagues can find them, minimize meetings that could be a written update, and be deliberate about the few high-bandwidth moments (planning, retro, incident response) that genuinely benefit from being synchronous.

## Questions to discuss with your team

1. **Does our cadence and set of ceremonies actually help us deliver safely, or are we performing agile rituals because we always have?**
   Many teams inherit a ceremony schedule — daily stand-up, two-week sprint, sprint review, retro — without asking whether it fits the work in front of them, and the result is meetings that consume real hours while delivering diminishing value. The honest debate is about purpose: what is each ceremony *for*, and would a neutral observer watching ours conclude it achieves that? A live-service team fielding unpredictable clinical incidents may be poorly served by rigid sprints and better served by Kanban flow, while a discovery team benefits from the sprint heartbeat and the stakeholder rhythm it creates. There is a real tension between the reassurance of a familiar routine and the discipline of running only the events that earn their place. Consider timing your ceremonies for a month and asking, per meeting, what decision or coordination it produced. A good answer is unsentimental about killing or reshaping ceremonies, distinguishes coordination needs from status-reporting habits, and ties the choice of cadence to the actual predictability of your work rather than to what the framework diagram shows.

2. **Is it genuinely safe on this team to say "I think this is unsafe" or "I made a mistake" — and how would we know?**
   Psychological safety is easy to claim and hard to possess, and in a team supporting clinical systems the cost of getting it wrong is measured in patient harm, not just missed deadlines. The uncomfortable question is not whether you *believe* your team is safe but what *evidence* you have: when did someone last admit an error in a stand-up, challenge a senior person's design, or halt a release on a hunch, and what happened to them afterwards? Look at your incident reviews — are they genuinely blameless, or does everyone quietly know who is being held responsible? There is a trade-off leaders must face honestly: the behaviours that feel like decisive leadership (moving fast, projecting certainty, reacting sharply to bad news) are often precisely the ones that teach people to stay quiet. Consider whether your quietest team members ever disagree in a meeting, and why they might not. A strong answer resists the comfortable assumption that "of course people can speak up here," points to concrete recent instances or admits their absence, and identifies specific leader behaviours to change rather than treating safety as a fixed trait of the group.

3. **Are we working at a pace we could sustain for a year — and what are we doing about the signals that we are not?**
   Sustainable pace is one of agile's founding principles and one of the first things abandoned under pressure, particularly for teams whose systems underpin services that cannot go down. The tension is that heroics are visible and rewarded in the moment — the person who worked the weekend to fix production is thanked — while the slow erosion of a team's health is invisible until people leave or make mistakes. Ask what your leading indicators are: unplanned work crowding out planned work, untaken annual leave, on-call disturbing sleep, retrospectives going quiet, cynicism creeping into language. In a safety-critical context, a tired team is not merely unhappy; it is more likely to miss the defect or misread the alert that prevents harm, so this is a clinical-risk conversation as much as a wellbeing one. Consider whether your capacity planning assumes the happy path or budgets for incidents, leave, and learning. A good answer treats burnout as a system property to be designed against rather than a personal weakness, names the specific signals the team will watch, and commits to a concrete change — resourcing, on-call fairness, WIP limits — rather than an exhortation to be more resilient.

4. **When a deadline is bearing down, what does our Definition of Done actually stop us from dropping — and have we ever proved it holds?**
   Every team can recite that clinical safety, accessibility, and information governance matter; the real test is what survives contact with a hard delivery date and an anxious stakeholder. The tension is that a Definition of Done is only meaningful when it costs you something — when it forces the team to *not* ship on the promised day because a DCB0160 hazard review or a WCAG 2.2 accessibility check is not complete. If your Done has never once caused you to hold a release, it may be decoration rather than a control. Look for the pressure points: who has the authority to say "this is not done", and would they be backed by leadership or overruled? Consider whether the non-negotiables are structural — encoded in the pipeline, in acceptance criteria, in sign-off gates — or whether they rely on someone remembering them at the worst possible moment. An honest answer can point to a specific occasion where Done was invoked under pressure, or admits candidly that it has not yet been tested and treats that as a gap to close rather than a comfort.

5. **Do the different professional cultures on this team — clinical, engineering, research, delivery — actually share a way of working, or are we quietly running on incompatible defaults?**
   Multidisciplinary teams are mandated in health and care for good reason, but bringing a clinician, an engineer, a user researcher, and a data analyst into one team means bringing four sets of professional instincts about evidence, risk, pace, and what "good" looks like. The friction is often invisible: an engineer's bias to ship and iterate can read as recklessness to a clinician trained to be certain before acting, while a clinician's caution can read as obstruction to someone used to reversible deploys. A working agreement that stays generic ("be respectful, attend stand-up") never surfaces these differences, whereas a good one names how *this* team makes decisions, handles disagreement between disciplines, and reconciles clinical caution with iterative delivery. Consider whether your norms were genuinely co-authored or imported from whichever discipline shouted loudest. A strong answer treats the diversity of professional cultures as a source of safety rather than an inconvenience, points to explicit agreements that translate between them, and can describe a recent disagreement that the team's norms helped resolve well rather than papered over.

6. **How do we know our retrospectives and health checks are changing anything — and what happens to candour when they don't?**
   A team can run a flawless retrospective every fortnight and a quarterly squad health check and still improve nothing, because the mechanism that matters is not the meeting but the follow-through. The corrosive failure mode is subtle: when actions are generated and never done, people slowly learn that raising problems is pointless, so candour decays and the very instrument meant to surface risk goes quiet — a particular danger where the unspoken problem is a safety concern. The honest question is evidential: of the last handful of retro actions or health-check signals, how many led to a visible change, and who owned them? There is a trade-off between generating a long, satisfying list of grievances and committing to a small number of owned, time-bound experiments the team will actually complete. Consider whether your next retro opens by checking whether the last one's actions happened, and whether amber-to-red health-check trends ever reach the people with the authority to resource a fix. A good answer measures the improvement habit by completed changes rather than meetings held, treats declining candour as an early warning in its own right, and links ways-of-working improvement to the same discipline the team would apply to a clinical pathway.

## In practice: a health & care example

A community NHS trust runs a **digital team supporting its electronic patient record (EPR) and a patient-facing appointments app**. The team is multidisciplinary — product manager, delivery manager, engineers, a user researcher, a clinical safety officer, and a data analyst — as set up under Chapter 7.0's structures. For a year they ran textbook Scrum: two-week sprints, full ceremony set. But they were also the team paged whenever the EPR misbehaved, and clinical incidents kept blowing up their sprint commitments, leaving them feeling perpetually behind and the retrospectives increasingly flat.

The delivery manager proposed a change. They split the work: planned product development on the appointments app stays in two-week sprints with fortnightly show-and-tells for the outpatient clinicians who use it, while live-service EPR support moves onto a **Kanban board with a strict WIP limit** and clear flow stages. They rewrote their **Definition of Done** to require, for any change touching the EPR, a completed DCB0160 hazard review and accessibility check before "done" — encoding safety into the process rather than leaving it to memory.

They also introduced a quarterly **squad health check**. The first one surfaced, in the "sustainable pace" and "support" dimensions going amber-to-red, that on-call was falling on the same two engineers and that leave was going untaken. The team used this evidence to make a concrete case to their director: a wider on-call rota and explicit recovery time after night pages. Six months on, retrospective actions are visibly being completed, the clinicians trust the fortnightly demos, and the last two potential safety issues were flagged *before* release by engineers who felt safe to say "hold on." Nothing here was exotic — it was the deliberate design of how the team works.

## Sector lenses

### Startup

A small digital-health startup often runs agile by instinct — everyone in one room, informal stand-ups, rapid iteration — which is a genuine strength for speed and learning. The risk is that "we're too small for process" quietly means the Definition of Done omits clinical safety and accessibility until an NHS buyer's Digital Technology Assessment Criteria (DTAC) review exposes the gap. Psychological safety is usually high while the team is tiny and founder-led, but a charismatic founder who reacts badly to bad news can destroy it invisibly. The move that pays off early is writing down a lightweight Definition of Done that bakes in the safety and accessibility non-negotiables, and protecting sustainable pace before the burn-rate culture of a funding round normalizes permanent crunch.

### Small business

An established small provider — a GP practice, a community pharmacy, a care home, or a single-site clinic — rarely has a "delivery team" at all: the ways of working are whatever the practice manager, a clinical lead, and perhaps one part-time IT contractor can sustain alongside seeing patients. There are no sprints or retrospectives to reform, so the practical move is to borrow the cheapest, highest-leverage habits — a visible board of outstanding digital changes with a hard limit on how many are in flight, and a short written agreement on who signs off a change before it goes live. The Definition of Done still has to carry the same statutory duties as a large trust — clinical safety, accessibility, information governance — but with no clinical safety officer on staff, this usually means a lightweight checklist and knowing which supplier or ICB contact to call for assurance. Because the same handful of people carry service delivery and change, sustainable pace is a real risk: an upgrade that goes wrong falls on staff who cannot simply page an on-call rota. The realistic ambition is not full agile ceremony but deliberate, written, safe-by-default habits that survive the departure of the one person who currently holds it all in their head.

### Enterprise

A large NHS trust or health-tech firm has many teams and the opposite problem: agile ceremonies proliferate, "agile" becomes a coat of paint over an unchanged command-and-control culture, and teams perform rituals without the autonomy that makes them worthwhile. Standardizing a single framework (often scaled agile) across dozens of teams risks imposing cadence that fits some and cripples others, so allow teams to choose Scrum, Kanban, or a hybrid within shared guardrails. At this scale, team-health checks aggregated across teams give leadership a real signal about organizational climate — but only if the data is used to help teams, never to rank or punish them. The enterprise's decisive advantage is the ability to invest in the platforms, on-call structures, and protected improvement time that make sustainable pace achievable rather than aspirational.

### Government

A national body such as NHS England or a local authority sets the standards others deliver against — the GOV.UK Service Manual and NHS Service Standard both mandate multidisciplinary teams working in agile, iterative ways — and is accountable to the public for how ways of working translate into value for money. Much delivery is contracted to suppliers, so the government's ways-of-working leverage is contractual: insist on genuine agile delivery with working software demonstrated at regular show-and-tells, rather than accepting documents against a waterfall plan dressed in agile language. Accountability is formal and auditable, which can pull towards heavy governance ceremonies that throttle team flow, so the discipline is to assure outcomes and safety without smothering the team's own cadence. The public-trust dimension is sharpest here: a demonstrably healthy, transparent delivery team is part of how a public body earns the confidence to hold sensitive data and run critical services.

## Common failure modes

- **Zombie ceremonies.** Stand-ups that are status theatre for a manager, reviews with no real users present, retrospectives that never change anything. The events run on autopilot, consuming time and teaching the team that participation is pointless. Fix by ruthlessly reconnecting each event to its purpose or stopping it.
- **Agile as cover for no plan or no governance.** "We're agile" used to justify skipping clinical-safety, accessibility, or information-governance work. Agility should surface these earlier, not excuse them; put them in the Definition of Done.
- **Cargo-cult framework adoption.** Copying Scrum or the Spotify model's labels without the autonomy, transparency, and trust underneath. Borrow principles, adapt to your context, and let teams choose their own cadence within guardrails.
- **Everything in progress, nothing done.** No WIP limits, so the team starts many things and finishes few, with lead times ballooning and half-tested changes piling up. Visualize the work and cap it.
- **Heroism as the operating model.** Sustained overtime and on-call carried by a few, celebrated rather than fixed. It burns out your best people and, for safety-critical systems, raises clinical risk. Design for sustainable pace and fair rotation.
- **Retro without follow-through.** Actions generated and never done, so candour decays. Limit to a few owned, time-bound experiments and check them next time.
- **Psychological safety assumed, not built.** Leaders declare the team safe while their own reactions teach people to stay quiet. Measure it by behaviour, not belief.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| Cadence & flow | Ad hoc; no reliable rhythm | Fixed sprints or a board, chosen by default | Cadence deliberately matched to work; WIP limited | Flow metrics (lead time, throughput) tracked and managed against targets | Teams self-select and evolve cadence; flow measured and improved |
| Ceremonies | Skipped or status-only | Full set run by rote | Each event serves a clear purpose and is adapted | Effectiveness of each event reviewed against its purpose on a regular cadence | Events continuously pruned and reshaped by the team |
| Definition of Ready/Done | None; "done" is subjective | Informal shared understanding | Written, includes safety, accessibility, IG | Compliance with Done measured and assured; exceptions logged and governed | Automated in pipeline where possible; regularly tightened |
| Psychological safety | Blame culture; problems hidden | Safety claimed but untested | Actively built; blameless reviews; concerns welcomed | Measured through surveys and behavioural signals; trends acted on | Measured, monitored, and improved as a first-class outcome |
| Sustainable pace | Permanent crunch; hidden burnout | Recognized but not managed | Capacity planned realistically; on-call shared fairly | Leading indicators quantified and reviewed against thresholds; on-call load balanced | Leading indicators tracked; team resourced for resilience |
| Improvement | No retros, or no follow-up | Retros held, actions rarely done | Owned, time-bound actions tracked to completion | Action completion and impact measured; improvement backlog prioritized on evidence | Ways of working treated as a continual-improvement backlog |

## Checklist

- [ ] The team has consciously chosen its cadence (sprints, flow, or hybrid) to fit the nature of its work, and revisits the choice.
- [ ] Each ceremony has a stated purpose everyone understands, and events that no longer serve it are changed or stopped.
- [ ] Regular show-and-tells demonstrate working software to real clinicians, patients, or operational users.
- [ ] A written Definition of Ready and Definition of Done exist, with clinical safety, accessibility, and information governance encoded in Done.
- [ ] Work in progress is visualized and explicitly limited.
- [ ] The team has co-authored a working agreement/charter and reviews it periodically.
- [ ] A lightweight team-health check runs on a regular cadence, owned by the team, and its trends inform action.
- [ ] Retrospectives end with a few owned, time-bound actions, and the next retro checks whether they happened.
- [ ] Leading indicators of burnout are monitored, on-call is shared fairly, and capacity is planned for a sustainable pace.
- [ ] Remote/hybrid/async collaboration is designed deliberately: decisions are documented where absent colleagues can find them.
- [ ] Leaders actively build psychological safety through blameless reviews and their own visible response to bad news.

## Key sources

- Agile Manifesto and its twelve principles (including "sustainable development … maintain a constant pace indefinitely") — agilemanifesto.org
- The Scrum Guide — Ken Schwaber & Jeff Sutherland — scrumguides.org
- Kanban — David J. Anderson — visualising flow and limiting work in progress
- NHS England — NHS Service Standard and NHS Service Manual — multidisciplinary agile delivery and show-and-tells
- GOV.UK Service Manual (Government Digital Service) — agile delivery, agile ceremonies, and sustainable ways of working
- Amy C. Edmondson, *The Fearless Organization* — psychological safety and team learning in healthcare
- Google re:Work — Project Aristotle findings on what makes teams effective
- Spotify "Squad Health Check" model — Henrik Kniberg & Kristian Lindwall
- World Health Organization — burnout classification in ICD-11 (QD85)

## References

1. Agile software development — Wikipedia — https://en.wikipedia.org/wiki/Agile_software_development
2. Iterative and incremental development — Wikipedia — https://en.wikipedia.org/wiki/Iterative_and_incremental_development
3. Scrum (project management) — Wikipedia — https://en.wikipedia.org/wiki/Scrum_(project_management)
4. Kanban (development) — Wikipedia — https://en.wikipedia.org/wiki/Kanban_(development)
5. Stand-up meeting — Wikipedia — https://en.wikipedia.org/wiki/Stand-up_meeting
6. Retrospective — Wikipedia — https://en.wikipedia.org/wiki/Retrospective
7. Psychological safety — Wikipedia — https://en.wikipedia.org/wiki/Psychological_safety
8. Occupational burnout — Wikipedia — https://en.wikipedia.org/wiki/Occupational_burnout
9. Continual improvement process — Wikipedia — https://en.wikipedia.org/wiki/Continual_improvement_process
10. Manifesto for Agile Software Development — Beck et al. — https://agilemanifesto.org
11. The Scrum Guide (2020) — Ken Schwaber & Jeff Sutherland — https://scrumguides.org
12. NHS Service Manual and Service Standard — NHS England — https://service-manual.nhs.uk
13. Service Manual (agile delivery) — Government Digital Service, GOV.UK — https://www.gov.uk/service-manual/agile-delivery
14. The Fearless Organization: Creating Psychological Safety in the Workplace for Learning, Innovation, and Growth — Amy C. Edmondson — https://fearlessorganization.com
15. re:Work — Guide: Understand team effectiveness (Project Aristotle) — Google — https://rework.withgoogle.com/guides/understanding-team-effectiveness/
16. Squad Health Check model — Henrik Kniberg & Kristian Lindwall, Spotify Engineering — https://engineering.atspotify.com/2014/09/squad-health-check-model
17. Burn-out an "occupational phenomenon": International Classification of Diseases (ICD-11) — World Health Organization — https://www.who.int/news/item/28-05-2019-burn-out-an-occupational-phenomenon-international-classification-of-diseases

*See also Chapter 3.6 — DevOps & Engineering Excellence, Chapter 3.8 — Service Management & Live Operations, Chapter 7.0 — Team Structures, Roles & Responsibilities, Chapter 7.5 — People & Organisational Development, and Chapter 10.2 — Quality Improvement & Improvement Science.*
