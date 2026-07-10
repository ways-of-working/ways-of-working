# Chapter 1.7 — Information Governance, Data Protection & Cyber Security

**In health and care, protecting information is inseparable from delivering care: the same data that saves a life can, if mishandled, break the trust that makes treatment possible — so how you govern, share, and secure it is a clinical, ethical, and public-trust obligation, not a compliance afterthought.**

## Why this matters in health and care

Health and care data is among the most sensitive information a person will ever create. It records diagnoses, medications, mental-health episodes, sexual health, immigration-linked entitlements, and the intimate details of frail and vulnerable lives. People disclose these things to clinicians on an implicit promise: that the information will be used to help them and will not be spread carelessly. When that promise breaks — through a leak, a ransomware outage, or an unexplained data-sharing deal — patients withhold information, opt out of records, or avoid care altogether. That is not an abstract harm; it degrades clinical safety and population health directly.

The stakes are also operational. A modern hospital cannot function without its electronic systems: order communications, results, e-prescribing, imaging, and patient administration are all digital. When those systems go down, ambulances divert, operations cancel, and clinicians revert to paper in ways that introduce their own errors. Information governance and cyber security are therefore continuity-of-care disciplines. They belong beside clinical safety (Chapter 1.6 — Clinical Safety & Risk Management), not in a separate compliance silo.

Finally, there is a genuine and unavoidable tension at the centre of this chapter. The public rightly expects the health service to use data to improve care, plan services, and support research that finds tomorrow's treatments. It also expects confidentiality and control. These goals pull against each other, and your job as a leader is not to pretend the tension away but to manage it openly — enabling legitimate use while making the safeguards, and the choices patients have, visible and honest. Get that balance wrong in either direction and you lose: either you starve care and research of data, or you erode the trust the whole system depends on.

## Core concepts

Underpinning this field is the discipline of information governance — the framework of rules, roles, and controls through which an organisation handles information legally, securely, and ethically. In the United Kingdom, the primary legal foundations are the [UK General Data Protection Regulation](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation) (UK GDPR), the domestic version of the EU regulation retained after Brexit, and the [Data Protection Act 2018](https://en.wikipedia.org/wiki/Data_Protection_Act_2018) (DPA 2018), which supplements it. Together they require that personal data be processed lawfully, fairly, and transparently, and that every processing activity rest on a **lawful basis**. Health information is **special category data**, which needs both a lawful basis under Article 6 and an additional condition under Article 9 — for direct care, typically the provision of health or social care by a professional under a duty of confidence.

Data protection law is not the only constraint. The [common law duty of confidentiality](https://en.wikipedia.org/wiki/Duty_of_confidentiality) is a separate, older obligation: information given in confidence may not be disclosed without either consent, a legal requirement, or an overriding public interest. You can be fully compliant with UK GDPR and still breach confidentiality, so both must be satisfied.

Two health-specific frameworks translate these duties into practice. The **Caldicott Principles** — a set of principles (now eight) for handling confidential patient information, first set out in the 1997 Caldicott Report — are upheld inside each organisation by a [Caldicott Guardian](https://en.wikipedia.org/wiki/Caldicott_guardian), a senior person responsible for protecting patient confidentiality and enabling appropriate information sharing. Nationally, the [National Data Guardian for Health and Social Care](https://en.wikipedia.org/wiki/National_Data_Guardian_for_Health_and_Social_Care) (NDG) is an independent statutory voice advising on how patient data should be used and safeguarded. The **national data opt-out** gives patients a mechanism to prevent their confidential information being used for purposes beyond their direct care, such as planning and research, and organisations must honour it.

Operationally, a [Data Protection Impact Assessment](https://en.wikipedia.org/wiki/Privacy_impact_assessment) (DPIA) is the structured assessment you complete before processing that is likely to be high risk — which most new health data projects are — to identify and mitigate privacy risks. Each organisation must appoint a [Data Protection Officer](https://en.wikipedia.org/wiki/Data_protection_officer) (DPO), an independent role responsible for advising on and monitoring compliance. In England, the **Data Security and Protection Toolkit** (DSPT) is the annual self-assessment through which health and care organisations demonstrate they meet the data-security and information-governance standards required to handle NHS data.

On the security side, the [National Cyber Security Centre](https://en.wikipedia.org/wiki/National_Cyber_Security_Centre_(United_Kingdom)) (NCSC) provides authoritative UK guidance and, through its Cyber Assessment Framework (CAF), a structured way to measure cyber resilience. Sound practice rests on well-established fundamentals: [defence in depth](https://en.wikipedia.org/wiki/Defense_in_depth_(computing)), layering multiple controls so no single failure is catastrophic; the [principle of least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege), granting people and systems only the access they genuinely need; disciplined patching and tested backups; and preparedness for [ransomware](https://en.wikipedia.org/wiki/Ransomware), the malware that encrypts systems for extortion. Because prevention alone never holds, mature organisations also invest in operations: a [security operations centre](https://en.wikipedia.org/wiki/Information_security_operations_center) (SOC) — a capability, whether in-house or shared, that monitors logs and telemetry to detect and contain intrusions — and a practised [incident response](https://en.wikipedia.org/wiki/Incident_response) process to move quickly from detection to recovery. The 2017 [WannaCry ransomware attack](https://en.wikipedia.org/wiki/WannaCry_ransomware_attack), which disrupted around a third of NHS trusts in England and caused an estimated £92 million in impact, remains the defining cautionary example — its damage flowed largely from unpatched systems, not exotic hacking.

## Best practices

1. **Start every data project with a DPIA, and treat it as design, not paperwork.** Before you build or procure anything that processes personal data, work through a Data Protection Impact Assessment with your DPO and Caldicott Guardian. Done early, it shapes the design — minimising the data collected, choosing pseudonymisation, tightening access — rather than rubber-stamping decisions already made. A DPIA parked until go-live is a warning sign that governance is theatre.

2. **Name your lawful basis and confidentiality basis explicitly, and write them down.** For every flow of health data, state the Article 6 lawful basis, the Article 9 special-category condition, and how the common law duty of confidentiality is satisfied — consent, a statutory gateway, or public interest. Ambiguity here is where projects stall or get pulled after launch. Being explicit also lets you explain the processing to patients in plain language, which is itself a legal requirement.

3. **Apply least privilege and role-based access everywhere.** Grant clinicians, administrators, researchers, and systems only the access their role requires, and review it regularly as people move and leave. Log access to sensitive records and audit it, because the credible threat of detection deters inappropriate curiosity as much as any technical control. Most real-world breaches are mundane — the wrong person seeing the wrong record — not sophisticated intrusions.

4. **Get the cyber fundamentals right before buying advanced tools.** The NCSC's guidance is unglamorous and effective: patch promptly, especially internet-facing and clinical systems; enforce multi-factor authentication; segment networks so an infection cannot spread freely; and maintain offline, tested backups. WannaCry spread through unpatched Windows systems, and the lesson endures — basic hygiene prevents the majority of incidents. Spend on fundamentals first; buy sophisticated detection once the basics are solid.

5. **Assume you will be attacked, and rehearse your response.** Maintain and exercise an incident-response and business-continuity plan that assumes systems will be unavailable, including clinical fallback to paper and a communications plan for staff and patients. Test your backups by actually restoring from them, because a backup you have never restored is a hope, not a control. Run tabletop exercises so that the first time your team handles a ransomware outage is not during a real one.

6. **Complete the DSPT honestly and use it as a real assessment.** The Data Security and Protection Toolkit is a requirement for handling NHS data, but its value comes from treating it as an honest yearly stocktake rather than a box-ticking ritual. Where you cannot meet a standard, record the gap and a credible improvement plan rather than overstating your position. An inflated DSPT return gives your board false assurance, which is worse than none.

7. **Make information sharing a designed capability, not an obstacle.** Across an integrated care system (ICS), good care depends on data crossing organisational boundaries between trusts, GP practices, social care, and community providers. Put clear information sharing agreements (ISAs) and data sharing agreements in place, agree the lawful and confidentiality bases jointly, and design shared records so the right professional sees the right information at the point of care. The goal is safe sharing, not no sharing — withholding data that a clinician needs is itself a patient-safety failure. This connects directly to Chapter 4.2 — Interoperability & Data Standards.

8. **Honour patient choice and be transparent about secondary uses.** Respect the national data opt-out in every secondary-use flow, and publish clear, accessible information about how data is used for planning and research. When data is shared with commercial partners or used to train models, disclose it proactively rather than letting it surface through a leak — hidden arrangements have repeatedly triggered public backlash and opt-out surges. Transparency is not a courtesy; it is what keeps the data flowing at all.

9. **Manage records across their whole lifecycle.** Apply retention schedules based on the NHS Records Management Code of Practice, disposing of records securely when their retention period ends and keeping them accessible and intact while it lasts. Poor records management creates both risk (holding data you no longer need) and harm (losing data clinicians rely on). Migration between systems is a high-risk moment — plan for data quality, mapping, and archiving deliberately.

10. **Build governance into procurement and supplier management.** Bake data protection and security requirements into contracts: data processing terms, DSPT or equivalent certification, breach-notification timelines, and the right to audit. A supplier's weak security becomes your incident and your headline, so assess the supply chain, not just your own perimeter. Work this jointly with commercial colleagues as covered in Chapter 6.3 — Procurement & Commercial, and demand clear answers about where data is hosted and who can access it.

11. **Invest in detection, not just prevention.** Assume some attacks will get through your defences, and build the capability to see them: centralised logging, monitoring of key systems, and a security operations centre — in-house, shared across an ICS, or drawing on national services such as the NCSC and NHS England's cyber operations — so that suspicious activity is spotted and contained rather than discovered weeks later. Pair this with continuous vulnerability management and threat detection, so you patch the weaknesses attackers actually exploit. Detection buys you the time to contain an incident before it becomes an outage.

12. **Treat a serious cyber attack as a clinical-continuity event.** Write, resource, and rehearse a cyber incident response plan that names who declares an incident, who leads technical response, and who owns clinical safety and external communications while systems are down. Wire it directly into your business continuity and disaster recovery arrangements (see Chapter 3.9 — Business Continuity & Disaster Recovery) and your major-incident and EPRR processes (see Chapter 3.10 — Emergency Preparedness, Resilience & Response), so a ransomware outage is handled with the same discipline as any threat to patient care. A plan that lives only in the IT department will fail the moment an attack becomes a clinical crisis.

## Questions to discuss with your team

1. **Where in our services are we sharing too little, and where are we sharing too much — and how would we even know?** Information governance failures run in both directions. Over-sharing shows up as breaches and eroded trust; under-sharing shows up quietly, as a clinician who could not see an allergy, a safeguarding concern that fell between agencies, or a discharge that went wrong because community teams lacked context. Discuss concrete cases from your own setting. Do you have a bias — often defensive — that treats withholding as automatically safe? What signals would tell you a sharing boundary is harming patients, and who is accountable for noticing? A mature team can name examples of both failure modes and has a route to escalate each.

2. **If a ransomware attack took our clinical systems offline tomorrow morning, what would actually happen in the first hour?** Move past the plan on paper to the lived reality. Who declares the incident, and how do staff find out when email and the intranet may be down? What is the clinical fallback for prescribing, results, and patient identification, and have frontline staff ever practised it? How long can each service run on paper before patient safety degrades, and how do you decide to divert or cancel? When did you last restore from backup to prove it works? The honesty of this conversation — especially the gaps people are reluctant to admit — is a better measure of resilience than any framework score.

3. **How would we explain our data uses to a sceptical patient, and would they feel we had been straight with them?** Public trust is earned in plain language, not legal notices. Pick a real secondary use of data in your organisation — service planning, a research partnership, a supplier arrangement, an AI tool — and try to explain it to an ordinary person: what data, for what purpose, who benefits, what safeguards, and what choice they have. Where does the explanation get uncomfortable or evasive? That discomfort usually marks something you should either change or communicate more openly. Consider how the national data opt-out and your transparency materials would look to someone predisposed to distrust, and connect this to the governance of AI in Chapter 8.4 — AI & Emerging Technology Governance.

## In practice: a health & care example

Meadowford Integrated Care System is standing up a shared care record so that hospital clinicians, GPs, community nurses, and social workers can see a unified view of each person. The programme is popular with clinicians and politically visible, and the temptation is to move fast.

The programme director insists on sequencing governance alongside build rather than behind it. A DPIA is opened at the outset, led jointly by the DPO and the lead Caldicott Guardian drawn from the partner organisations. It forces early, useful decisions: the record will show a curated clinical summary rather than every historical document; social care records with third-party information will be handled under tighter rules; and access will be role-based, with a legitimate-relationship check so a professional can only open a record for someone in their care. Every access is logged and audited, and staff are told so plainly.

The partners agree a single information sharing agreement covering the common law duty of confidentiality and the lawful bases — direct care under Article 6(1)(e) and Article 9(2)(h) — and they confirm the shared record is used only for direct care, so the national data opt-out does not restrict it. When a separate proposal arrives to use the same data for population-health analytics, the team treats it as a distinct flow with its own DPIA, its own lawful basis, opt-out compliance, and public communications, rather than quietly extending the existing agreement.

Six weeks before go-live, the security lead runs a tabletop ransomware exercise. It exposes that the shared record has no clinical fallback if it becomes unavailable and that backups have never been test-restored. Go-live slips by a month while the team adds an offline read-only copy refreshed nightly, proves the restore works, and briefs frontline staff on paper fallback. The delay is unpopular, but when a supplier patching error takes the main system offline for a morning three months later, care continues on the fallback and no appointments are lost. The programme's credibility — and clinicians' trust in the record — survives intact. The trade-off was explicit: a slower launch bought resilience that a faster one would have gambled away.

## Three sector lenses

### Startup

A health-tech startup often has the strongest technical security instincts and the weakest grasp of health-specific confidentiality and NHS-specific expectations. If you are a startup, expect to complete the DSPT or demonstrate equivalent assurance before an NHS body will share data with you, and appoint or contract a DPO early. Your biggest risk is moving fast on data uses — analytics, model training, partnerships — without the lawful basis, DPIA, and transparency that the sector demands, and losing an NHS customer overnight when it surfaces. Treat information governance as a market-access requirement, not overhead, and build it in while you are small.

### Enterprise

A large trust or established supplier has mature policies but struggles with scale, legacy, and fragmentation: dozens of systems, inconsistent access controls, unpatched estate, and governance spread thinly across teams. Your challenge is coherence — a single view of risk, a real asset inventory, and enough security investment to fix fundamentals rather than only buying tools. WannaCry hit large organisations hardest precisely because of unpatched legacy estate. Use the DSPT and NCSC Cyber Assessment Framework to drive genuine improvement, and make sure board-level ownership is real rather than delegated into invisibility.

### Government

National bodies and commissioners set the frameworks — the Caldicott Principles, the National Data Guardian's guidance, the national data opt-out, the DSPT — and carry responsibility for public trust at population scale. Your data initiatives are large, visible, and politically charged, and past programmes have shown how quickly hidden or poorly explained data sharing triggers backlash and mass opt-outs. Lead with transparency, meaningful public engagement, and independent oversight before scaling, not after. Recognise the trade-off you own: overly cautious national policy starves care and research of data, while careless policy forfeits the consent of the public whose data it is.

## Common failure modes

- **Governance as theatre.** DPIAs completed after launch, DSPT returns inflated to look compliant, and policies no one follows. This produces false assurance, which is more dangerous than acknowledged weakness.
- **Security fundamentals neglected while buying shiny tools.** Unpatched systems, no multi-factor authentication, flat networks, and untested backups — the exact conditions that let WannaCry spread — dressed up with an expensive detection platform.
- **Defensive over-caution dressed as safety.** Refusing to share data that a clinician legitimately needs, treating "no" as risk-free when a missed allergy or safeguarding gap is itself serious patient harm.
- **Hidden secondary uses.** Extending data collected for care into analytics, commercial deals, or model training without a fresh lawful basis, opt-out compliance, or public transparency — until it leaks and trust collapses.
- **Backups that were never restored.** Discovering during a live ransomware incident that the backups are incomplete, corrupted, or encrypted along with everything else.
- **Orphaned accountability.** A DPO or Caldicott Guardian who exists on the org chart but is not consulted, resourced, or listened to, so risks are neither surfaced nor owned.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Data protection & DPIAs | DPIAs done rarely or after launch | DPIAs done for major projects, inconsistently | DPIA embedded at project start with DPO sign-off | Privacy-by-design routine; lawful bases documented and reviewed |
| Cyber fundamentals | Ad hoc patching, no MFA, flat network | Patching and MFA in progress; some segmentation | Fundamentals enforced; measured against NCSC CAF | Continuous hardening, threat-informed, regularly tested |
| Incident readiness | No tested plan; backups unverified | Plan exists on paper; backups taken | Plan rehearsed; backups test-restored; clinical fallback defined | Regular exercises drive improvement; response is muscle memory |
| Information sharing | Sharing blocked or done informally | Some ISAs; bases unclear or inconsistent | ISAs in place with agreed lawful and confidentiality bases | Safe sharing designed into services; balance actively managed |
| Trust & transparency | Secondary uses opaque; opt-out patchy | Opt-out honoured; notices exist but unclear | Clear public information; opt-out reliably applied | Proactive engagement; commercial and AI uses disclosed openly |

## Checklist

- [ ] A DPIA is opened at the start of every new data project and signed off by the DPO.
- [ ] The lawful basis, special-category condition, and confidentiality basis are documented for each data flow.
- [ ] A Caldicott Guardian and a Data Protection Officer are appointed, resourced, and actually consulted.
- [ ] Least-privilege, role-based access is enforced and access to sensitive records is logged and audited.
- [ ] Systems are patched promptly, multi-factor authentication is enforced, and networks are segmented.
- [ ] Backups are taken, held offline, and test-restored on a regular schedule.
- [ ] An incident-response and business-continuity plan, including clinical paper fallback, is documented and rehearsed.
- [ ] The DSPT is completed honestly, with recorded gaps and credible improvement plans.
- [ ] Information sharing agreements are in place across ICS partners with agreed bases.
- [ ] The national data opt-out is applied to all secondary uses and transparency materials are published.
- [ ] Records retention and secure disposal follow the NHS Records Management Code of Practice.
- [ ] Data protection and security requirements are written into supplier contracts and the supply chain is assessed.

## Key sources

- Information Commissioner's Office (ICO) — Guide to UK GDPR, DPIAs, and lawful bases.
- National Data Guardian — reviews and guidance on data security and the Caldicott Principles.
- NHS England — Data Security and Protection Toolkit and the national data opt-out.
- National Cyber Security Centre (NCSC) — cyber security guidance and the Cyber Assessment Framework.
- UK Caldicott Guardian Council — role and responsibilities of the Caldicott Guardian.
- National Audit Office — investigation into the WannaCry cyber attack and the NHS (2017–18).
- NHS Records Management Code of Practice.

## References

1. Information governance — Wikipedia — https://en.wikipedia.org/wiki/Information_governance
2. General Data Protection Regulation — Wikipedia — https://en.wikipedia.org/wiki/General_Data_Protection_Regulation
3. Data Protection Act 2018 — Wikipedia — https://en.wikipedia.org/wiki/Data_Protection_Act_2018
4. Duty of confidentiality — Wikipedia — https://en.wikipedia.org/wiki/Duty_of_confidentiality
5. Caldicott guardian — Wikipedia — https://en.wikipedia.org/wiki/Caldicott_guardian
6. National Data Guardian for Health and Social Care — Wikipedia — https://en.wikipedia.org/wiki/National_Data_Guardian_for_Health_and_Social_Care
7. Data protection impact assessment (Privacy impact assessment) — Wikipedia — https://en.wikipedia.org/wiki/Privacy_impact_assessment
8. Data protection officer — Wikipedia — https://en.wikipedia.org/wiki/Data_protection_officer
9. National Cyber Security Centre (United Kingdom) — Wikipedia — https://en.wikipedia.org/wiki/National_Cyber_Security_Centre_(United_Kingdom)
10. Defense in depth (computing) — Wikipedia — https://en.wikipedia.org/wiki/Defense_in_depth_(computing)
11. Principle of least privilege — Wikipedia — https://en.wikipedia.org/wiki/Principle_of_least_privilege
12. Ransomware — Wikipedia — https://en.wikipedia.org/wiki/Ransomware
13. WannaCry ransomware attack — Wikipedia — https://en.wikipedia.org/wiki/WannaCry_ransomware_attack
14. Guide to the UK GDPR — Information Commissioner's Office — https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/
15. Data Security and Protection Toolkit — NHS England — https://www.dsptoolkit.nhs.uk/
16. National data opt-out — NHS England — https://digital.nhs.uk/services/national-data-opt-out
17. Cyber Assessment Framework — National Cyber Security Centre — https://www.ncsc.gov.uk/collection/cyber-assessment-framework
18. Investigation: WannaCry cyber attack and the NHS — National Audit Office — https://www.nao.org.uk/reports/investigation-wannacry-cyber-attack-and-the-nhs/
19. Information security operations center — Wikipedia — https://en.wikipedia.org/wiki/Information_security_operations_center
20. Incident response — Wikipedia — https://en.wikipedia.org/wiki/Incident_response
