# Chapter 13 — User Research & Service Design

**In health and care, understanding the people who use and deliver a service is not a preliminary courtesy but the primary safety, equity, and trust discipline that determines whether anything you build actually helps.**

## Why this matters in health and care

The first point of the NHS Service Standard, inherited from the Government Digital Service (GDS), is "understand users and their needs." It is placed first deliberately. Almost every avoidable failure in a digital health service traces back to a service that was designed around an assumption about people rather than evidence about them: a booking flow that assumes everyone has a smartphone and a stable address, a symptom checker validated only on people who read fluent English, a discharge letter written for clinicians and handed to a frightened patient.

In most sectors, misunderstanding users produces waste. In health and care it can produce harm. A person who cannot complete an online referral does not simply abandon a shopping basket; they may go without care, present later and sicker, or fall out of a pathway entirely. Because the people who most need care are frequently those least able to navigate a poorly designed service — older people, people with cognitive impairment, people in crisis, people who do not speak English, people with no digital access — bad design actively widens inequality. This connects directly to Chapter 8 — Digital Inclusion & Accessibility, and it is why user research in this sector is a governance concern, not merely a design nicety.

Health services are also unusually complex to understand. The "user" is rarely one person acting alone. It is a patient and a carer, a receptionist and a GP, a district nurse and a hospital pharmacist, each with different needs, moving through a pathway that crosses organisational boundaries. Service design gives you the tools to see that whole system rather than the single screen in front of you. Doing this work well is how you earn the right to make evidence-driven decisions (Chapter 4 — Evidence-Driven Decisions) instead of defending opinions in a meeting room.

## Core concepts

[User-centred design](https://en.wikipedia.org/wiki/User-centered_design) (UCD) is a framework in which the needs, characteristics, tasks, and environment of the people who will use a product or service are given sustained attention at every stage, so that the service adapts to people rather than forcing people to adapt to it. Its broader relative, [human-centred design](https://en.wikipedia.org/wiki/Human-centered_design) (HCD), applies the same philosophy to whole systems, services, and policies, and is codified in the international standard ISO 9241-210.

[Service design](https://en.wikipedia.org/wiki/Service_design) is the practice of planning and arranging the people, infrastructure, communication, and material components of a service to improve its quality and the interactions between the service and its users. It differs from — and depends on — narrower disciplines: interaction design shapes how a person moves through an individual interface, and content design ensures the words, structure, and information meet a user need in the clearest possible way. Service design zooms out to the entire journey, including the parts that happen offline, over the phone, or between staff.

The [Double Diamond](https://en.wikipedia.org/wiki/Double_Diamond_(design_process_model)), popularised by the UK Design Council, describes design as two linked phases of divergent then convergent thinking: **discover** (explore the problem widely), **define** (converge on the right problem to solve), **develop** (explore possible solutions), and **deliver** (converge on one that works and refine it). The first diamond guards against solving the wrong problem; the second against building the solution badly. It maps naturally onto Chapter 15 — Discovery Phases.

Your evidence comes from [qualitative research](https://en.wikipedia.org/wiki/Qualitative_research) — non-numerical data that explains *why* and *how* people behave — and quantitative research, which tells you *how many* and *how often*. Qualitative methods include [contextual inquiry](https://en.wikipedia.org/wiki/Contextual_inquiry) and [ethnography](https://en.wikipedia.org/wiki/Ethnography), where you observe people in their real environment; depth interviews; and [usability testing](https://en.wikipedia.org/wiki/Usability_testing), where you watch a person attempt real tasks with a prototype or live service. Quantitative methods include surveys, analytics, and A/B testing. You need both: numbers show you where a problem is; stories show you what it is.

You make findings usable through design artefacts. A [persona](https://en.wikipedia.org/wiki/Persona_(user_experience)) is an evidence-based, representative characterisation of a group of users. A [user journey](https://en.wikipedia.org/wiki/User_journey) map traces a person's experience across time and touchpoints, exposing where effort and anxiety cluster. A [service blueprint](https://en.wikipedia.org/wiki/Service_blueprint) extends the journey below the "line of visibility" to show the front-stage and back-stage staff actions and support systems that make each step possible.

Finally, [co-production](https://en.wikipedia.org/wiki/Co-production_(approach)) is an approach in which patients, carers, and the public are not merely consulted but are genuine partners in conceiving, designing, and running a service. In the NHS this overlaps with patient and public involvement (PPI), the expectation that people affected by a service help shape it.

## Best practices

1. **Start with a need, not a solution.** Write down the user need before anyone sketches a screen or names a technology. A good need statement is expressed from the user's point of view ("As someone recently discharged, I need to know who to call if my wound looks wrong, so that I do not end up back in A&E"). If you cannot evidence the need from research, you are working from an assumption — label it as such and go and test it before you spend money on it.

2. **Research the whole service, not the interface.** Map the journey end to end, including the phone call, the letter, the waiting room, and the handover between teams. Build a service blueprint so that the invisible back-stage work — the staff who re-key data, chase results, or work around a broken system — becomes visible. Most of the pain patients feel is created in the seams between organisations, which is exactly where a single screen redesign cannot reach.

3. **Use mixed methods and triangulate.** Pair qualitative depth with quantitative breadth so that each checks the other. Analytics might show a large drop-off at a particular step; interviews and usability sessions tell you it is because the wording implies a charge that does not exist. Do not let a compelling anecdote override the data, or a large dataset hide the human reason behind the pattern. Small, frequent rounds of research beat one large study delivered too late to change anything.

4. **Recruit for the edges, deliberately.** If you recruit only confident, digitally able, English-speaking people, you will build a service that works for them and excludes everyone else. Set explicit recruitment quotas for people who are older, digitally excluded, clinically vulnerable, neurodivergent, or who use assistive technology, and go to them rather than expecting them to come to you. Partner with charities, community groups, and clinical teams to reach people you cannot recruit through a panel.

5. **Make research ethical and safe by design.** Take informed consent seriously, explain clearly how data will be used, and let people withdraw at any time. Have a safeguarding plan for sessions with clinically or emotionally vulnerable participants, including what you will do if someone discloses risk or becomes distressed, and pay participants fairly for their time. Where research crosses into activities that require formal approval — for example involving patients as research subjects — check whether Health Research Authority (HRA) governance and ethics approval apply, and involve your Caldicott Guardian and information governance colleagues early (see Chapter 6 — Information Governance, Data Protection & Cyber Security).

6. **Co-produce, do not just consult.** Move up the ladder from informing people, to consulting them, to genuinely sharing power with patients, carers, and frontline staff throughout the work. Bring lived-experience partners into the team from discovery onward, give them real influence over decisions, and reimburse them properly. Consultation asks people to react to your finished idea; co-production means they helped shape it, which produces better services and far greater trust.

7. **Run research operations as shared infrastructure.** Treat "ResearchOps" as a capability, not an afterthought: standard consent forms, a participant recruitment pipeline, incentive processes, ethics checklists, and above all a searchable research repository where findings, clips, and insights are stored and tagged. Without this, every team re-researches the same things, insights evaporate when people move on, and the same vulnerable participants get asked the same questions repeatedly.

8. **Design inclusively and test with assistive technology.** Inclusive research and accessible design are the same discipline seen from two ends. Test your prototypes with screen readers, magnification, keyboard-only navigation, and plain-language content, and include disabled people in your participant pool as standard rather than as a special study. Meeting the Web Content Accessibility Guidelines (WCAG) is a floor, not a ceiling; observing a real screen-reader user complete a task teaches you things a checklist never will (Chapter 8 — Digital Inclusion & Accessibility).

9. **Close the loop from insight to decision to product.** Research only creates value when it changes what gets built. Connect insights to the backlog so that prioritisation reflects evidence of need (Chapter 23 — Product-Led Work), and feed research back to participants and staff so they see that their contribution mattered. Keep a visible record of "what we learned and what we changed," which protects the work when priorities are challenged and builds the organisation's memory.

## Questions to discuss with your team

1. **Whose needs are we actually designing for, and who is missing from the room?** Before you accept a research plan, interrogate the sample. List every type of person who will touch this service — patients, carers, and the specific staff roles — and mark honestly which of them you have real evidence about and which you are guessing at. Pay particular attention to people at the margins: those without digital access, those in crisis, those who do not speak English, those with cognitive or sensory impairments. Ask what it would take to reach them and what the cost of not reaching them would be in terms of harm and inequality. If your evidence base skews toward the easy-to-recruit, your service will too. This is the difference between a service that appears to work in a demo and one that works in the community.

2. **Where are we saying "we assume" and calling it "we know"?** Gather the team and list the beliefs your current plan depends on — about how people behave, what they want, what they can do, and what will help them. For each belief, ask what evidence you have: is it direct observation, a stakeholder's opinion, a vendor's claim, or genuinely nobody's idea dressed as fact? Rank the assumptions by how damaging it would be if they turned out to be wrong. The riskiest untested assumptions are where your next round of research should go, because that is where money and safety are most exposed. Making assumptions explicit is uncomfortable but far cheaper than discovering them after launch. A mature team treats "we assumed" as a red flag to investigate, not a phrase to defend.

3. **How will research change a decision, and what happens if it does not?** It is possible to do a great deal of research that changes nothing, which is worse than doing none because it consumes goodwill and participant time. For any planned study, agree in advance what decision it will inform and what different findings would lead you to do differently. Discuss who owns the decision, how insights reach them, and whether the team is genuinely willing to change course — including stopping — if the evidence points that way. Consider how you will keep insight alive: a repository nobody searches is a graveyard. Talk about how you will feed findings back to participants and frontline staff so that involvement feels real rather than extractive. If the honest answer is that the decision is already made, say so and save everyone's effort.

## In practice: a health & care example

An Integrated Care System (ICS) wants to reduce missed outpatient appointments, which are high in a deprived urban borough. The obvious solution on the table is a new SMS reminder and self-service rebooking app. The delivery lead insists on a two-week discovery before committing the budget.

The team recruits deliberately for the edges: alongside confident smartphone users, they include an older man who shares one phone with his wife, a woman who reads little English and relies on her adult daughter to translate letters, and a man in temporary accommodation whose address changes monthly. They run contextual inquiry in people's homes and shadow reception and booking staff for two days. A service blueprint reveals the back-stage truth: appointment letters are generated centrally and posted, often arriving after the appointment for people who move; the "confirmed" mobile numbers in the patient record are years out of date; and reception staff already spend hours re-keying corrections that never reach the source system.

The journey map shows that most "missed" appointments were never truly offered — people did not know, could not get through on the phone line that opens at 8am, or could not afford the bus on the day. The assumption that patients were choosing not to attend collapses under observation. A lived-experience panel, co-producing weekly, points out that a rebooking app would exclude precisely the people missing appointments now.

The team reframes the problem from "remind people better" to "make it possible to know about, reach, and afford your appointment." They still build reminders, but they also fix the address and phone-number data flow, add a call-back option, offer appointments closer to home, and rewrite the letter in plain language with a translation route. Consent, safeguarding, and information-governance sign-off were arranged before any home visit, with the Caldicott Guardian consulted. Findings, anonymised clips, and the blueprint go into a shared repository so the next team inherits the knowledge. Missed appointments fall — and, more importantly, they fall most among the people who were being failed hardest.

## Three sector lenses

### Startup

A digital health startup lives or dies by finding real user need fast, and its advantage is speed. You can run guerrilla usability sessions and weekly interviews without heavy process, and you should, because building the wrong thing is the most common way early companies die. The danger is confusing enthusiasm from early adopters — typically young, digitally confident, and healthy — with evidence of broad need in a clinical population. Recruit at least a few genuinely representative and vulnerable users early, even when it is slow and expensive, and keep a lightweight repository from day one so hard-won insight is not lost in the next pivot. If you plan to sell into the NHS, understanding the whole service and its safety context is what separates a demo from a deployable product.

### Enterprise

A large provider or supplier has scale, existing users, and rich data, but often has research fragmented across teams who never share what they learn. The opportunity is a genuine research operations function: a shared repository, standard ethics and consent processes, a managed participant pool, and a discipline of triangulating qualitative insight with the analytics you already hold. The risk is research theatre — studies commissioned to justify decisions already taken, or personas printed on posters that no one uses. Insist that research connects to real decisions and to the backlog, and protect the independence of researchers so they can report inconvenient findings without career risk.

### Government

In UK government and the NHS, user-centred design is not optional: the NHS Service Standard and GDS service assessments require you to demonstrate that you understand users and their needs, and services are assessed against this at phase boundaries. This is a strength, because it gives researchers a mandate and a seat at the table. The obligations run deeper than compliance: public services must work for the whole population, including the most excluded, which makes inclusive recruitment and co-production a duty rather than a nicety. Work openly, publish findings where you can, and be alert to statutory duties on involvement and equality. The failure mode is treating the service assessment as a hurdle to clear rather than a genuine test of whether you have understood the people you serve.

## Common failure modes

- **"We assumed" dressed as fact.** Decisions built on stakeholder opinion or vendor claims, with no user evidence, and no one distinguishing the two.
- **Recruiting only the reachable.** Samples skewed toward digitally confident, English-speaking, healthy people, so the service excludes those who need it most.
- **Interface tunnel vision.** Redesigning a screen while ignoring the letters, phone lines, staff workarounds, and cross-organisation handovers where the real pain lives.
- **Research theatre.** Studies run to justify a decision already made, or to satisfy an assessment, with no willingness to change course.
- **Consultation masquerading as co-production.** Showing patients a finished design and calling their reaction "involvement," while never sharing real power.
- **The insight graveyard.** Findings trapped in slide decks and individual memories, so teams re-research the same questions and burn participant goodwill.
- **Extractive research.** Taking people's time and stories, sometimes on painful subjects, without consent care, safeguarding, fair payment, or ever telling them what changed.
- **Accessibility as an afterthought.** Testing only with able users and bolting on a WCAG audit at the end, instead of designing and researching inclusively from the start.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Evidence of need | Decisions based on assumption and opinion | Occasional research, often after build | Research precedes build; assumptions made explicit and tested | Continuous discovery feeds a living evidence base; needs re-checked over time |
| Scope of design | Individual screens and forms | Journeys mapped for some services | End-to-end journeys and service blueprints, including back-stage | Whole cross-organisation pathways designed and measured together |
| Inclusion of participants | Convenience sample of easy-to-reach users | Awareness of gaps; some outreach | Explicit quotas for excluded and vulnerable groups; assistive-tech testing | Co-production with lived-experience partners embedded from discovery |
| Research operations | Ad hoc, per person | Shared templates and some ethics practice | ResearchOps function: repository, consent, safeguarding, recruitment pipeline | Repository actively used across teams; insight reuse is the norm |
| Impact on decisions | Research rarely changes anything | Findings sometimes inform the backlog | Insights linked to prioritisation and fed back to participants | Evidence visibly drives, and sometimes stops, investment decisions |

## Checklist

- [ ] The user need is written from the user's point of view and backed by evidence, not assumption.
- [ ] You have identified every user type — patients, carers, and each staff role — and know where your evidence is thin.
- [ ] Recruitment includes digitally excluded, clinically vulnerable, non-English-speaking, and assistive-technology users, by explicit quota.
- [ ] Informed consent, safeguarding plans, fair participant payment, and information-governance sign-off are in place before fieldwork; HRA and Caldicott routes checked where relevant.
- [ ] You have mapped the end-to-end journey and built a service blueprint showing front-stage and back-stage.
- [ ] Qualitative and quantitative methods are used together and triangulated.
- [ ] Prototypes are tested with real assistive technology and plain-language content.
- [ ] Patients and staff co-produce the work with genuine influence, not just consultation.
- [ ] A searchable research repository holds findings, is tagged, and is actually used by other teams.
- [ ] Each study has a named decision it informs, and there is a visible record of what you learned and what you changed.

## Key sources

- NHS Service Standard — NHS England — the national standard whose first point is to understand users and their needs.
- GOV.UK Service Manual — Government Digital Service — practical guidance on user research, user needs, and running services user-first.
- Design Council: Framework for Innovation (the Double Diamond) — Design Council — the canonical description of discover, define, develop, deliver.
- ISO 9241-210: Human-centred design for interactive systems — International Organization for Standardization — the international standard for HCD process.
- Health Research Authority guidance — HRA — governance and ethics approval for research involving patients and the public.
- NIHR guidance on patient and public involvement and co-production — National Institute for Health and Care Research — standards for involving people in health research and service design.

## References

1. NHS Service Standard — NHS England — https://service-manual.nhs.uk/standards-and-technology/service-standard
2. Government Service Manual: User research — Government Digital Service — https://www.gov.uk/service-manual/user-research
3. Framework for Innovation: The Double Diamond — Design Council — https://www.designcouncil.org.uk/our-resources/the-double-diamond/
4. User-centered design — Wikipedia — https://en.wikipedia.org/wiki/User-centered_design
5. Human-centered design — Wikipedia — https://en.wikipedia.org/wiki/Human-centered_design
6. Service design — Wikipedia — https://en.wikipedia.org/wiki/Service_design
7. Double Diamond (design process model) — Wikipedia — https://en.wikipedia.org/wiki/Double_Diamond_(design_process_model)
8. Qualitative research — Wikipedia — https://en.wikipedia.org/wiki/Qualitative_research
9. Contextual inquiry — Wikipedia — https://en.wikipedia.org/wiki/Contextual_inquiry
10. Ethnography — Wikipedia — https://en.wikipedia.org/wiki/Ethnography
11. Usability testing — Wikipedia — https://en.wikipedia.org/wiki/Usability_testing
12. Persona (user experience) — Wikipedia — https://en.wikipedia.org/wiki/Persona_(user_experience)
13. User journey — Wikipedia — https://en.wikipedia.org/wiki/User_journey
14. Service blueprint — Wikipedia — https://en.wikipedia.org/wiki/Service_blueprint
15. Co-production (approach) — Wikipedia — https://en.wikipedia.org/wiki/Co-production_(approach)
16. ISO 9241-210: Ergonomics of human-system interaction — Human-centred design for interactive systems — International Organization for Standardization — https://www.iso.org/standard/77520.html
17. Health Research Authority — HRA — https://www.hra.nhs.uk/
18. Patient and public involvement and engagement — National Institute for Health and Care Research — https://www.nihr.ac.uk/patients-carers-and-the-public
