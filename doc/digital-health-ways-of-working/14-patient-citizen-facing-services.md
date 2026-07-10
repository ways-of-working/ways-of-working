# Chapter 14 — Patient & Citizen-Facing Digital Services

**A patient-facing digital service is a public health intervention in its own right: it can widen access and confidence for millions, or quietly exclude the very people who need care most, and how you build it decides which.**

## Why this matters in health and care

When you put a service directly into the hands of the public, you change the relationship between a person and the system that cares for them. A staff-facing system is used by trained people inside a controlled environment; a patient-facing service is used by a frightened parent at 2am, an 84-year-old sharing a phone with a neighbour, someone with no fixed address, someone who reads little English, someone in crisis. You do not get to choose your users, train them, or stand beside them. The service has to work — safely, clearly, and fairly — for everyone the health system is obliged to serve, not merely for the confident and connected.

That obligation is what makes this different from consumer technology. In retail, a confusing checkout loses a sale. In health and care, a confusing online triage form, an unclear medication instruction, or a "book an appointment" flow that silently fails can lead to a missed diagnosis, a wrong dose, or a person who gives up and presents later and sicker. The stakes are clinical (see Chapter 5 — Clinical Safety & Risk Management), legal (equality and accessibility duties bind public bodies), and financial, because public money is spent whether or not the service actually helps anyone.

There is also a trust dimension that consumer products rarely carry. People bring their health data, their fears, and a lifetime of experience with the NHS to every screen you show them. If the service feels extractive, opaque, or unsafe, they will not simply churn — they will lose confidence in the institution behind it (see Chapter 7 — Data Ethics, Consent & Public Trust). And because the people least able to navigate a poor digital service are disproportionately older, poorer, disabled, or digitally excluded, badly designed patient-facing services actively widen health inequalities. Doing this well is not a matter of polish. It is a matter of equity, safety, and public confidence.

## Core concepts

A patient-facing service is the "digital front door": the online entry point through which a person finds information, proves who they are, and starts a task. In England the two national platforms most people meet are the [NHS App](https://en.wikipedia.org/wiki/NHS_app) and NHS login. The NHS App, developed by NHS England, lets people in England book and manage GP appointments, order repeat prescriptions, view their GP-held record, access NHS 111 online, and set data-sharing and organ-donation preferences. NHS login is the separate identity and authentication service that verifies who a person is (to a proportionate level of assurance) so that they can safely reach their own record across many different NHS and partner services — much as [GOV.UK Verify](https://en.wikipedia.org/wiki/GOV.UK_Verify) once aimed to do for central government. It is important to describe these accurately: the NHS App is a front door and an app, while NHS login is the identity layer that many apps and websites, not just the NHS App, can use.

Behind the front door sit records and tools. An [electronic health record](https://en.wikipedia.org/wiki/Electronic_health_record) (EHR) is the clinician-maintained record held by a provider. A [personal health record](https://en.wikipedia.org/wiki/Personal_health_record) (PHR) is a record that the patient can see, add to, and sometimes control, giving them a fuller view of their own care. A [patient portal](https://en.wikipedia.org/wiki/Patient_portal) is the web or app interface through which people view results, messages, letters, and records, and communicate with their care team. "Patient access to records" — the right to read your own GP and increasingly hospital record — is now a default expectation in England, not a favour.

Several service types run on top. Online consultation and online triage let a person describe a problem digitally so it can be routed and prioritised without a phone queue. [Shared decision-making in medicine](https://en.wikipedia.org/wiki/Shared_decision-making_in_medicine) is the practice of clinician and patient reaching care decisions together, supported by clear information and decision aids — captured in the NHS phrase "no decision about me, without me". Self-management tools help people manage long-term conditions day to day. [Remote patient monitoring](https://en.wikipedia.org/wiki/Remote_patient_monitoring) and [telehealth](https://en.wikipedia.org/wiki/Telehealth) extend care into the home through devices, video, and asynchronous messaging.

The concepts that decide whether any of this works are about people, not features. Adoption is whether people start using a service; activation is whether they reach the point of getting value from it; and sustained engagement is whether they keep using it when it matters. The [Patient Activation Measure](https://en.wikipedia.org/wiki/Patient_Activation_Measure) (PAM) is a validated instrument for a related idea — a person's knowledge, skills, and confidence to manage their own health. Set against all of this is the [digital divide](https://en.wikipedia.org/wiki/Digital_divide): the gap in access, connectivity, and confidence that means a purely [digital health](https://en.wikipedia.org/wiki/Digital_health) service will leave some people behind unless assisted-digital and non-digital routes are deliberately preserved (see Chapter 8 — Digital Inclusion & Accessibility).

## Best practices

1. **Design the whole front door, not one app.** Decide deliberately which channels a person can use to reach each task — app, website, phone, in person, via a carer or proxy — and make them consistent rather than competing. A patient-facing service is a set of routes to a need, not a single download. Map where the digital route hands off to a human one and make that seam graceful, because most real journeys cross it. Treat channel choice as the user's to make, not yours to force.

2. **Use national platforms rather than rebuilding them.** Where NHS App and NHS login already provide identity, records access, appointments, and prescriptions, integrate with them instead of building a parallel front door that fragments the experience and the security model. This gives users one trusted identity and one place to look, and it inherits assurance work you would otherwise repeat. Reserve bespoke build for genuinely local needs the national platforms do not meet, and feed those needs back to the national teams (see Chapter 43 — Collaborating with Partner Organisations).

3. **Give people real access to their own records, and make it legible.** Access to records builds trust and supports self-management, but a record dumped on screen in clinical shorthand can confuse or frighten. Invest in content design so results, letters, and coded entries are understandable, and think carefully about sensitive information, safeguarding, and how a proxy or carer sees another person's data (see Chapter 9 — Safeguarding in Digital Services). Patient access is a design problem, not just a switch to turn on.

4. **Preserve assisted-digital and non-digital routes as a permanent feature.** For every online task, keep a supported and a fully offline way to complete it, and resource them properly rather than treating them as legacy overhead. "Digital by default" must never mean "digital only", because a meaningful proportion of the population cannot or will not use the digital route, and they are disproportionately those in greatest need. Design the assisted route — a phone line, a receptionist, a library helper, a family proxy — with the same care as the app (see Chapter 8 — Digital Inclusion & Accessibility).

5. **Make online triage clinically safe by design.** Any tool that asks about symptoms and routes people must be built and governed as a clinical-safety activity, with clear escalation for red-flag symptoms and a bias toward safe over-triage. Apply the relevant clinical-risk-management standards, keep a named clinical-safety officer involved, and monitor outcomes for missed or delayed care (see Chapter 5 — Clinical Safety & Risk Management). A triage flow that fails silently is not a usability defect; it is a patient-safety incident.

6. **Support shared decision-making, not just transactions.** The highest value in patient-facing digital is helping people understand options and make choices that fit their lives, not merely booking slots. Offer decision aids, plain-language information, and prompts that invite questions, and design so a person can pause, involve family, and return. Measure whether people feel more informed and more in control, because that is the point of the tool. Transactions are necessary; deliberation is where outcomes improve.

7. **Instrument for outcomes and experience, not vanity metrics.** Downloads and registrations tell you almost nothing; a service can have millions of registered users and change no one's health. Measure activation and sustained, meaningful use, task completion, and — where you can — real clinical outcomes and patient-reported experience and outcome measures (PREMs and PROMs). Publish these alongside adoption numbers so the organisation cannot mistake reach for value (see Chapter 45 — OKRs & KPIs).

8. **Build trust through clarity, consent, and safety.** Tell people plainly what a service does, what it does not do, who sees their data, and how to get help or reach a human. Make consent and data-sharing choices genuine and reversible, and never dark-pattern people into sharing more than they intend (see Chapter 7 — Data Ethics, Consent & Public Trust). In health, trust is the platform everything else runs on; one breach of it costs far more than any feature earns.

9. **Design for interoperability from the start.** A patient-facing service that cannot read from and write to the underlying records is a silo that creates double-keying and error. Use open standards so bookings, messages, and observations flow to and from the systems clinicians actually use, and so a person's data follows them across a fragmented care landscape (see Chapter 21 — Interoperability & Data Standards). The public experiences interoperability as "I don't have to repeat myself" — and its absence as danger and frustration.

10. **Close the loop with continuous research and live operations.** Keep researching with real, diverse users after launch, not just before it, and route what you learn back into the backlog (see Chapter 13 — User Research & Service Design). Run the service as a live product with proper support, monitoring, and incident response, because a patient-facing service that is down or broken erodes trust instantly (see Chapter 18 — Service Management & Live Operations). Adoption is earned continuously, not captured once.

## Questions to discuss with your team

1. **Who cannot use this service the way we have designed it, and what happens to them?** Every patient-facing service embeds assumptions — that people have a smartphone, data, an email address, a fixed identity to verify against, the literacy and confidence to complete a form, and the sight, dexterity, and language to do so. Name the groups your current design excludes or disadvantages, and be specific: people with no NHS-verifiable identity, people sharing one device, people fleeing abuse who cannot risk a digital trail, people with cognitive impairment. For each, decide what the assisted or non-digital route actually is, who resources it, and how you will know it works. A good, honest answer does not claim to serve everyone through the app; it names the excluded, quantifies them where possible, and shows a funded, dignified alternative rather than a token phone number nobody answers. This is where equity is won or lost, and it connects directly to Chapter 8 — Digital Inclusion & Accessibility.

2. **How will we know this service actually improves health, not just that people signed up?** It is easy to celebrate registrations and downloads because they are countable and they rise; it is much harder, and far more important, to show that anyone is better off. Discuss what outcome you are actually trying to move — fewer missed appointments, better-controlled long-term conditions, earlier presentation, more informed decisions — and how you would detect a change in it. Debate the trade-off between metrics you can gather cheaply now and the harder measures of activation, sustained use, and clinical outcome that tell the truth. Consider who is accountable if adoption is high but outcomes are flat, and whether you are willing to change or stop the service if the evidence says it is not helping. A strong answer ties the service to a small number of honest outcome and experience measures, admits what you cannot yet measure, and refuses to let vanity metrics stand in for value (see Chapter 4 — Evidence-Driven Decisions and Chapter 45 — OKRs & KPIs).

3. **Where does digital convenience trade off against clinical safety, and who decides?** Patient-facing tools create real tensions: faster access can mean less clinical oversight; self-service triage can miss the subtle presentation a clinician would catch; showing people their raw results can inform or alarm; letting people book directly can undermine prioritisation. Work through where your service leans toward convenience and where it must lean toward caution, and make those choices explicit rather than emergent. Ask who owns the clinical-safety case, how red-flag symptoms escalate, and how you monitor for harm that only shows up in aggregate over time. Consider the safeguarding angle too — a service that assumes the person on screen is who they say they are, and is safe, is not always right (see Chapter 9 — Safeguarding in Digital Services). A good answer treats safety as a design input from day one, with a named clinical-safety officer and live monitoring, not as a compliance sign-off at the end.

## In practice: a health & care example

An integrated care system (ICS) covering a mixed urban and coastal population wants to reduce pressure on GP phone lines and improve access, and proposes rolling out an online consultation and triage tool integrated with the NHS App and NHS login. The temptation is to measure success by the number of registrations and the fall in call volumes, and to declare victory within a quarter.

The delivery lead insists on framing it differently. In discovery, the team researches with a deliberately broad group: confident app users, but also an older woman on the coast with intermittent broadband, a man with low literacy who has never used email, a carer managing appointments for her mother as a proxy, and a woman in a refuge who cannot risk her whereabouts being logged. They find that the triage form's red-flag handling is sound but that its language defeats the low-literacy user, that the proxy journey is confusing, and that the identity verification in NHS login excludes people with no passport or driving licence. Crucially, they find that when the phone line is de-prioritised in favour of the app, the coastal and vulnerable users simply drop out of contact rather than switching channel.

So the ICS resets its plan. It keeps the phone line fully staffed as the assisted-digital route, not a legacy cost, and funds a community "digital health helper" scheme through libraries and pharmacies. It works with the national NHS App team on the proxy journey rather than building a workaround, and appoints a clinical-safety officer to own the triage risk case with monitoring for cases where digital triage under-routed a patient who later presented acutely. It also changes its measures: alongside adoption, it tracks task completion by user group, sustained use, patient-reported experience, and a small set of clinical outcomes. Six months in, downloads are lower than a pure app-first push would have produced, but access has improved across every group including the most excluded, and the triage tool has safely escalated several serious presentations. The board accepts the slower adoption because the service is demonstrably fairer and safer.

## Three sector lenses

### Startup

A small digital-health company lives or dies on adoption and retention, so it will instrument engagement obsessively and iterate fast — a genuine strength the wider system can learn from. The danger is optimising for the metrics that impress investors (downloads, monthly active users) rather than health outcomes, and designing for the confident early adopters who are cheapest to acquire. A startup selling into the NHS must show it meets the Digital Technology Assessment Criteria (DTAC), integrates with NHS login and open standards rather than trapping users in a silo, and has a credible clinical-safety case. The founders who win long-term contracts are the ones who treat inclusion and safety as product requirements, not compliance drag.

### Enterprise

A large NHS trust or ICS runs patient-facing services at scale across a fragmented estate, so its central problem is coherence: multiple portals, letters, and apps that each solve one task and collectively bewilder the patient. Its advantage is reach and the ability to fund assisted-digital and non-digital routes properly; its risk is inertia, siloed procurement, and a tendency to buy another portal rather than integrate with national platforms. Governance is heavier and slower, which protects safety but can starve iteration, so the enterprise needs product teams with real mandate to keep improving live services (see Chapter 23 — Product-Led Work). The measure of maturity is whether a patient experiences one coherent front door or a dozen disconnected ones.

### Government

A national body such as NHS England builds the platforms — the NHS App, NHS login, records access — that everyone else builds upon, so its decisions set the ceiling for equity and interoperability across the whole system. Its accountability is to Parliament and the public for spending, safety, and fairness, which rightly raises the bar on accessibility, transparency, and the preservation of non-digital routes. The hard task is balancing a single, consistent national experience against genuine local variation, and resisting the political pull to celebrate headline registration figures over real outcomes. Government's unique lever is standards and defaults: what it mandates for identity, interoperability, and accessibility shapes millions of interactions it will never directly design.

## Common failure modes

- **Registration theatre.** Reporting downloads and sign-ups as success while nobody checks whether anyone gets value or better health. Fix it by measuring activation, sustained use, and outcomes from the start.
- **Digital-only creep.** Quietly withdrawing or under-funding phone and in-person routes once the app exists, which excludes the most vulnerable. Fix it by treating assisted-digital and non-digital as permanent, funded features.
- **Portal proliferation.** Every service buying its own patient portal, so the public faces a maze of logins. Fix it by integrating with national platforms and open standards.
- **Triage as a feature, not a safety case.** Shipping symptom-routing without clinical-safety governance or monitoring for harm. Fix it by applying clinical-risk standards and appointing a clinical-safety officer.
- **Records without comprehension.** Exposing raw clinical data with no content design, alarming or confusing patients. Fix it with plain-language content and thoughtful handling of sensitive and proxy access.
- **Consent by dark pattern.** Nudging people into data-sharing they do not understand, corroding trust. Fix it with genuine, plain, reversible consent.
- **Launch-and-leave.** Treating the service as a project that ends at go-live rather than a live product that must be researched, supported, and improved.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Channels & inclusion | Digital-only or bolt-on phone; excluded users invisible | Assisted route exists but under-funded | Assisted-digital and non-digital funded and designed | Channels co-designed with excluded groups; equity actively monitored |
| Platforms & integration | Bespoke silo, own login | Some reuse of NHS login; partial integration | Integrated with NHS App / NHS login and open standards | Contributes improvements back to national platforms |
| Safety | No clinical-safety case for public-facing flows | Sign-off at launch only | Clinical-safety officer, standards applied, escalation designed | Live harm monitoring drives continuous safety improvement |
| Measurement | Downloads and registrations only | Basic usage analytics | Activation, sustained use, task completion tracked | Real clinical outcomes and PREMs/PROMs drive decisions |
| Trust & consent | Opaque data use | Privacy notice present but unread | Plain-language, genuine, reversible consent | Transparency and public involvement build durable trust |

## Checklist

- [ ] For every task, a digital, an assisted-digital, and a non-digital route exist and are funded
- [ ] The service integrates with NHS App and NHS login rather than duplicating identity or the front door
- [ ] Patients can access their own records in language they can understand, with safe proxy and sensitive-data handling
- [ ] Any triage or symptom-routing has a clinical-safety case, a named safety officer, and red-flag escalation
- [ ] Success measures include activation, sustained use, task completion, and real outcomes — not just downloads
- [ ] Consent and data-sharing choices are plain, genuine, and reversible, with no dark patterns
- [ ] Accessibility meets WCAG and is tested with assistive technology and real excluded users
- [ ] Bookings, messages, and observations flow to and from clinical systems via open standards
- [ ] The service is run as a live product with support, monitoring, and incident response
- [ ] Research with a diverse population continues after launch and feeds the backlog

## Key sources

- NHS England — NHS App and NHS login guidance and developer documentation
- NHS Service Standard and NHS Digital Service Manual — designing accessible, inclusive public services
- GOV.UK Service Manual (Government Digital Service) — assisted digital, channel choice, and service design
- NHS England — DCB0129 and DCB0160 clinical risk management standards for health IT
- Digital Technology Assessment Criteria (DTAC) — NHS England baseline for digital health technologies
- NICE Evidence Standards Framework for Digital Health Technologies
- Web Content Accessibility Guidelines (WCAG) — W3C
- NHS RightCare Shared Decision-Making Programme
- Insignia Health / Judith Hibbard — Patient Activation Measure (PAM)

## References

1. NHS app — Wikipedia — https://en.wikipedia.org/wiki/NHS_app
2. Personal health record — Wikipedia — https://en.wikipedia.org/wiki/Personal_health_record
3. Electronic health record — Wikipedia — https://en.wikipedia.org/wiki/Electronic_health_record
4. Patient portal — Wikipedia — https://en.wikipedia.org/wiki/Patient_portal
5. Shared decision-making in medicine — Wikipedia — https://en.wikipedia.org/wiki/Shared_decision-making_in_medicine
6. Remote patient monitoring — Wikipedia — https://en.wikipedia.org/wiki/Remote_patient_monitoring
7. Telehealth — Wikipedia — https://en.wikipedia.org/wiki/Telehealth
8. Patient Activation Measure — Wikipedia — https://en.wikipedia.org/wiki/Patient_Activation_Measure
9. Digital divide — Wikipedia — https://en.wikipedia.org/wiki/Digital_divide
10. Digital health — Wikipedia — https://en.wikipedia.org/wiki/Digital_health
11. GOV.UK Verify — Wikipedia — https://en.wikipedia.org/wiki/GOV.UK_Verify
12. NHS App — NHS England — https://www.nhs.uk/nhs-app/
13. NHS login — NHS England — https://www.nhs.uk/nhs-services/online-services/nhs-login/
14. NHS Service Manual and Service Standard — NHS England — https://service-manual.nhs.uk/
15. GOV.UK Service Manual: Assisted digital and channel choice — Government Digital Service — https://www.gov.uk/service-manual/helping-people-to-use-your-service
16. Clinical risk management standards DCB0129 and DCB0160 — NHS England — https://digital.nhs.uk/services/clinical-safety
17. Digital Technology Assessment Criteria (DTAC) — NHS England — https://www.nhs.uk/about-us/digital-technology-assessment-criteria-dtac/
18. Evidence Standards Framework for Digital Health Technologies — NICE — https://www.nice.org.uk/about/what-we-do/digital-health
19. Web Content Accessibility Guidelines (WCAG) 2.2 — W3C — https://www.w3.org/TR/WCAG22/
