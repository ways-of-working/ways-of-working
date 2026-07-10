# Chapter 32 — Team Structures, Roles & Responsibilities

**In one sentence:** Digital health delivery succeeds or fails on how you draw the boundaries between teams and how clearly you name who does what — so structure teams for fast, safe flow of value, staff them multidisciplinarily, and make responsibilities explicit.

## Why this matters in health and care

The way you organise your teams becomes the way your services behave. **[Conway's Law](https://en.wikipedia.org/wiki/Conway%27s_law)** — that a system's design mirrors the communication structure of the organisation that built it — is not a curiosity in health and care; it is a patient-safety risk. Fragmented teams produce fragmented care records, brittle integrations, and hand-offs where clinical risk hides.

In the NHS and social care you are also spending public money and carrying statutory duties: clinical safety under DCB0129/DCB0160, information governance under UK GDPR and the common law duty of confidentiality, and accessibility obligations. These duties cannot be bolted on at the end. They must be represented *inside* the team, by named people with the authority and time to discharge them.

Get the structure right and multidisciplinary teams ship working software that clinicians trust and patients can use. Get it wrong and you get busy specialists optimising their own silo while the service as a whole stalls — the classic pattern behind late, over-budget, and quietly abandoned digital programmes.

## Core concepts

**[Multidisciplinary teams](https://en.wikipedia.org/wiki/Interdisciplinarity) (MDTs).** A digital delivery team should contain every discipline needed to design, build, and run a service without constant external dependency — product, delivery, design, research, engineering, data, and the clinical and governance perspectives. This mirrors the clinical MDT concept staff already know: mixed expertise, shared accountability for an outcome.

**Team Topologies.** A model (Skelton & Pais) that reduces effective team design to four fundamental types and three interaction modes, all in service of *fast flow of value*:

- **Stream-aligned team** — organised around a single valuable stream of work (a service, a user journey, a product) and owning it end to end. This is the default team type; most people should be on one.
- **Platform team** — provides internal self-service capabilities (shared infrastructure, an integration engine, a login service, a shared care record API) so stream-aligned teams go faster without reinventing them.
- **Enabling team** — a time-boxed team of specialists (e.g. clinical safety, accessibility, test automation) that coaches others to raise a capability, then withdraws.
- **Complicated-subsystem team** — owns a part needing deep specialist knowledge (a risk-scoring algorithm, an NHS Spine interface) that would overload a generalist team.

The three **interaction modes** govern how any two teams relate: **collaboration** (working closely for a defined period, high-bandwidth, tolerating some inefficiency to discover things), **X-as-a-service** (one team consumes another's capability with minimal fuss, the low-friction default at scale), and **facilitating** (one team helps another learn). Naming the mode prevents the ambiguity that breeds delays and blame.

**[Cognitive load](https://en.wikipedia.org/wiki/Cognitive_load).** A team can only hold so much in its head. Team Topologies argues you should limit the *domain* each team owns to what it can reason about safely — a decisive principle when the domain is clinical.

**Conway's Law and the Inverse Conway Manoeuvre.** Since architecture follows org structure — a [sociotechnical system](https://en.wikipedia.org/wiki/Sociotechnical_system) view that treats teams and technology as one design — deliberately shape teams to produce the architecture you want. If you want a modular, interoperable care record, do not build it with one monolithic team.

## Best practices

1. **Staff a full multidisciplinary team around each service.** Include, at minimum, a product manager, a delivery manager, a user researcher, a service/interaction designer, engineers, and a data/analytics capability, plus named clinical safety and information governance input. A team missing a discipline will either wait on someone else or skip that work — and the skipped work in health is usually safety, accessibility, or governance.

2. **Make most teams stream-aligned and give them end-to-end ownership.** Organise around a user's journey (e.g. "outpatient referral") rather than a technology layer (e.g. "the database team"). End-to-end ownership shortens feedback loops and stops the hand-off gaps where clinical risk accumulates.

3. **Build platforms as products, consumed as a service.** Treat your integration engine, identity service, or shared care record API as an internal product with its own team, roadmap, and users. Publish it "as-a-service" so stream-aligned teams self-serve, rather than raising tickets and waiting.

4. **Use enabling teams to spread scarce expertise, not to hoard it.** Clinical safety officers, accessibility specialists, and security engineers are rare. Deploy them to coach delivery teams to a higher standard and then move on, rather than becoming a permanent bottleneck every team queues behind.

5. **Name every role and its decision rights explicitly.** Use a responsibility model — [RACI](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix) (Responsible, Accountable, Consulted, Informed) or a simpler "decider/adviser" split — for the decisions that matter: clinical safety sign-off, go-live, information governance approval, spend. Ambiguity here is where accountability evaporates.

6. **Give the Clinical Safety Officer real authority and real time.** DCB0129/0160 require a named, suitably trained Clinical Safety Officer who can stop a release. Make the role explicit in the team, protect its time, and ensure it can say no — a CSO in name only is a governance failure waiting to be found by an incident.

7. **Manage cognitive load by bounding the domain.** If a team owns too many services or too complex a clinical domain, split it. Watch for the signal: a team that can no longer confidently explain the safety implications of its own change is overloaded.

8. **Apply the Inverse Conway Manoeuvre deliberately.** Draw the team boundaries to match the architecture and interoperability you want — modular teams for modular, standards-based (e.g. [HL7 FHIR](https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources)) systems. Do not let an accidental org chart design your care record for you.

## Questions to discuss with your team

1. **Where is our current org chart already designing our architecture for us — and is that the architecture we actually want?**
   Conway's Law is not optional: whatever the shape of our teams, the systems will come to mirror it, so the honest first move is to look at the care record, the integrations, and the hand-offs we already have and ask which team boundary produced each seam. In a health and care setting those seams are where clinical risk hides — a fragmented record, a brittle Spine interface, a safety case no single team owns — so this is a patient-safety conversation, not an aesthetic one. The tension to debate is that redrawing team boundaries to get the architecture we want (the Inverse Conway Manoeuvre) is disruptive, threatens established fiefdoms, and cuts across funding and line-management structures we may not fully control. Consider mapping two or three of your most painful integrations back to the teams that own each end, and ask whether a stream-aligned boundary would have removed the hand-off entirely. A good answer names at least one concrete boundary you would move, is honest about who would resist and why, and distinguishes changes worth the disruption from those where an as-a-service interface would fix the friction more cheaply.

2. **Do our scarce specialists — clinical safety, information governance, accessibility — sit inside teams with real authority, or are they external gates everyone queues behind?**
   Every service in this family carries statutory duties (DCB0129/0160 clinical safety, UK GDPR and the common law duty of confidentiality, accessibility law) that cannot be bolted on at the end, yet these capabilities are rare and expensive, which pulls organisations toward hoarding them centrally. The trade-off is genuine: embed a Clinical Safety Officer in every team and you spread thin expertise until it is diluted; centralise it and you create the heroic bottleneck where one person is Consulted on everything and every release waits. The enabling-team pattern — time-boxed specialists who coach teams to run their own hazard workshops and then withdraw — is the proposed resolution, but it only works if leadership protects the specialists' time to teach rather than do. Look honestly at your own release history: how often did go-live slip waiting on a single named person, and did that person have the authority and protected time to say no safely? A strong answer faces the scarcity squarely, picks a deliberate position on embed-versus-enable for each duty, and names the specific authority (the power to stop a release) that must never be diluted however you spread the capacity.

3. **How would we know a team has taken on more cognitive load than it can safely carry — and what would we actually do about it?**
   Cognitive load is the quiet governor of safe delivery: a team can only reason about so much clinical domain and so many services before its confidence in the safety implications of its own changes starts to erode, and in health that erosion is invisible until an incident exposes it. The difficulty is that overload rarely announces itself — it looks like slightly slower delivery, more defects, more "let me check with someone", and teams under pressure tend to absorb rather than flag it, especially when splitting a team is politically costly or headcount is frozen. Debate what your early-warning signals would be (a team that can no longer confidently explain the safety case for its own release is a strong one), and whether you have any mechanism today that would surface overload before delivery visibly stalls. Consider the counter-pressure too: splitting teams creates new boundaries and hand-offs, so the cure can reintroduce the fragmentation risk of question one. An honest answer agrees on concrete, observable signals rather than a vague "we'd sense it", names who has the authority to bound a team's domain or split it, and admits the trade-off between load relief and boundary proliferation.

## In practice: a health & care example

An integrated care system (ICS) is rolling out a **shared care record** across acute, community, mental health, primary care, and social care.

The instinct is to create one large "shared care record team". Instead the ICS applies Team Topologies. A **platform team** owns the shared record's core: the person-matching index, the FHIR APIs, and the integration engine, published as self-service capabilities. Several **stream-aligned teams** each own a real user journey on top of it — "view a patient's record in A&E", "social worker safeguarding view", "GP medication reconciliation" — and consume the platform as-a-service. A **complicated-subsystem team** owns the probabilistic patient-matching algorithm, where a false match is a genuine safety incident. An **enabling team** of clinical safety and accessibility specialists rotates through the stream-aligned teams, coaching them to run their own DCB0160 hazard workshops rather than doing it for them.

Each team has a named product manager, delivery manager, and Clinical Safety Officer, and a RACI makes clear that go-live is *accountable* to the Senior Responsible Owner but *cannot proceed* without CSO and IG sign-off. When the A&E team needs a new data field, the interaction mode is explicit: X-as-a-service from the platform team via a documented API request, not a six-week collaboration. Delivery is faster and, crucially, the safety case for each journey is owned by the team that ships it.

## Three sector lenses

### Startup

A ten-person digital-health startup cannot staff four distinct team types — it usually *is* a single stream-aligned team in which one person wears several hats (an engineer who also runs user research, a clinician-founder who is the de facto Clinical Safety Officer). The priority is keeping the whole team inside one shared cognitive space so decisions are fast; a formal RACI is overkill when everyone is in the same room. The real risk is the founder-bottleneck: clinical safety and information governance rest on one busy person, and DCB0129/0160 obligations are easy to defer. As the company wins its first NHS contract, the first specialist hires should be the ones that de-risk that gate — a named CSO and an IG lead — before scaling engineering headcount.

### Enterprise

A large NHS trust or health-tech firm has the opposite problem: too many teams, drawn along legacy component and departmental lines, with hand-offs everywhere. This is where a deliberate team-design model earns its keep — reshaping component teams into stream-aligned ones, standing up platform teams for shared care-record and integration capabilities, and using enabling teams to spread scarce clinical-safety and accessibility expertise. RACI and explicit decision rights become essential because the sheer number of stakeholders makes informal coordination impossible. The Inverse Conway Manoeuvre is a live lever here: a decades-old org chart is already shaping the architecture, so leaders must redraw team boundaries intentionally rather than let the structure design the care record for them.

### Government

A national body (NHS England, DHSC) or local authority sets the standards others staff against — the Government Digital and Data capability framework, the Service Standard, DCB0129/0160 — and is accountable to Parliament and the public for how money buys team capacity. Structures here are shaped by procurement and funding rules: much delivery is contracted to suppliers, so the crucial roles to retain in-house are the intelligent-client ones (product ownership, technical assurance, clinical safety sign-off) that prevent capability being hollowed out. Accountability is formal and auditable — a named Senior Responsible Owner, published spend controls, transparency duties — so responsibility models are a matter of public record, not optional hygiene. The characteristic risk is that structure ossifies into permanent programme boards and gates that throttle flow; the countermove is to hold suppliers to stream-aligned, outcome-owning teams rather than staff-augmentation body-shops.

## Common failure modes

- **The component team trap.** Teams split by technology layer ("front-end team", "database team") create hand-offs on every feature and own no outcome. Reorganise around streams of value.
- **Cargo-cult Spotify.** Copying "squads, tribes, chapters, guilds" as labels without the underlying autonomy, alignment, and platform investment. The Spotify model was a snapshot of one company at one time — even Spotify moved on. Borrow principles, not the org chart.
- **The heroic bottleneck.** One CSO, one architect, or one IG lead as a Consulted party on everything, so every team waits. Convert them into an enabling capability that raises everyone's competence.
- **Governance as an afterthought.** Clinical safety and IG represented as external gates rather than embedded team members, so their concerns arrive too late to act on cheaply.
- **Unbounded teams.** A team that keeps absorbing services until no one understands the whole. Cognitive overload shows up as slowing delivery and eroding safety confidence.
- **Permanent collaboration.** Two teams "collaborating" indefinitely is usually a missing boundary. Time-box collaboration and move to a clean as-a-service interface.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Team shape | Split by technology component; hand-offs everywhere | Some cross-functional teams, still dependency-heavy | Stream-aligned teams own services end to end | Team boundaries deliberately shape architecture (Inverse Conway) |
| Multidisciplinary staffing | Roles borrowed ad hoc from silos | Core roles present, clinical/IG part-time | Full MDT incl. named CSO with authority | Teams self-assess and fill capability gaps proactively |
| Interaction clarity | Undefined; escalation by relationship | Some processes, still ticket queues | Interaction modes named per dependency | Modes reviewed and evolved; low-friction platforms dominate |
| Responsibilities | Unclear who decides | RACI exists on paper | RACI live and used for key decisions | Decision rights continuously tuned to reduce delay |
| Cognitive load | Overloaded teams, safety confidence low | Load recognised but not managed | Domains bounded to team capacity | Load actively monitored; teams split before overload |

## Checklist

- [ ] Every service has a stream-aligned team that owns it end to end.
- [ ] Each team contains, or has named access to, product, delivery, research, design, engineering, data, clinical safety, and information governance.
- [ ] A named, trained Clinical Safety Officer per team has protected time and authority to stop a release.
- [ ] Shared capabilities (integration, identity, care record APIs) are run as internal platforms consumed as-a-service.
- [ ] Scarce specialists work through time-boxed enabling teams, not permanent bottlenecks.
- [ ] A RACI (or equivalent) exists for clinical sign-off, go-live, IG approval, and spend, and is actually used.
- [ ] Each cross-team dependency has a named interaction mode (collaboration / X-as-a-service / facilitating).
- [ ] Team domains are bounded to a manageable cognitive load; overloaded teams are split.
- [ ] Team boundaries are chosen deliberately to produce the architecture and interoperability you want.

## Key sources

- Team Topologies — Matthew Skelton & Manuel Pais (four team types, three interaction modes, cognitive load): teamtopologies.com
- NHS Digital Service Standard and NHS Service Manual — multidisciplinary team roles and ways of working
- GOV.UK Service Manual (GDS) — "Set up a service team" and agile delivery guidance
- Government Digital and Data (formerly DDaT) Profession Capability Framework — role definitions: ddat-capability-framework.service.gov.uk
- Clinical Risk Management standards DCB0129 (manufacture) and DCB0160 (deployment), NHS Digital — Clinical Safety Officer role
- Conway's Law — Melvin Conway, "How Do Committees Invent?" (1968)
- Spotify engineering culture (Henrik Kniberg) — squads/tribes/chapters/guilds, read critically as a point-in-time model

## References

1. Conway's law — Wikipedia — https://en.wikipedia.org/wiki/Conway%27s_law
2. Cognitive load — Wikipedia — https://en.wikipedia.org/wiki/Cognitive_load
3. Responsibility assignment matrix (RACI) — Wikipedia — https://en.wikipedia.org/wiki/Responsibility_assignment_matrix
4. Interdisciplinarity — Wikipedia — https://en.wikipedia.org/wiki/Interdisciplinarity
5. Sociotechnical system — Wikipedia — https://en.wikipedia.org/wiki/Sociotechnical_system
6. Fast Healthcare Interoperability Resources — Wikipedia — https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources
7. Team Topologies: Organizing Business and Technology Teams for Fast Flow — Matthew Skelton & Manuel Pais — https://teamtopologies.com
8. NHS Service Manual and NHS Digital Service Standard — NHS England — https://service-manual.nhs.uk
9. Service Manual — Government Digital Service (GDS), GOV.UK — https://www.gov.uk/service-manual
10. Government Digital and Data Profession Capability Framework — GOV.UK — https://ddat-capability-framework.service.gov.uk
11. Clinical risk management standards DCB0129 and DCB0160 — NHS England — https://digital.nhs.uk/services/clinical-safety
12. "How Do Committees Invent?" (1968) — Melvin E. Conway — http://www.melconway.com/Home/Committees_Paper.html

*See also Chapter 33 — Workforce Planning, Chapter 34 — Workforce Strategy, Chapter 35 — People & Organisational Development, and Chapter 38 — Change Management.*
