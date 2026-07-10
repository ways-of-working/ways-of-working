# Chapter 5 — Regulation & Compliance Landscape

**In one sentence:** Compliance in digital health and care is not a legal afterthought but a map of overlapping statutory duties, mandatory standards, and voluntary assurance that you must navigate deliberately, proportionate to risk, with clear ownership — because getting it wrong is a safety, equity, and public-trust failure, not merely a fine.

## Why this matters in health and care

In most sectors, regulation sets a floor: obey it and you avoid penalties. In health and care, the regulatory landscape encodes hard-won lessons about how digital systems harm people when they go wrong — a mislabelled dose, a lost record, a biased algorithm, a breach that exposes the most sensitive data a person owns. Compliance here is a proxy for whether you have thought about those harms at all. A leader who treats it as paperwork is telling you they have not.

The landscape is also genuinely crowded, and that is the difficulty. A single patient-facing app might simultaneously be a medical device regulated by one body, process personal data under the remit of another, be commissioned only if it clears a national assessment, sit inside a service inspected by a care regulator, and be built by clinicians accountable to their own professional regulators. No one wrote this map as a coherent whole; it accreted. Your job as a leader is not to memorise every rule but to hold the *shape* of the terrain — who covers what, which instruments are mandatory versus advisory, and where your specific service sits within it.

Finally, this is public money and statutory duty. When you deploy a non-compliant system you are not just exposing your organisation to enforcement; you may be breaching duties owed to patients and citizens, and spending public funds on something you cannot lawfully run. That is why this chapter frames the more detailed chapters that follow on clinical safety (Chapter 6 — Clinical Safety & Risk Management), information governance (Chapter 7 — Information Governance, Data Protection & Cyber Security), data ethics (Chapter 8 — Data Ethics, Consent & Public Trust), and assurance (Chapter 37 — Governance & Assurance). This chapter is the navigator; those are the detailed charts.

## Core concepts

**Three tiers of obligation.** The single most useful distinction is between statutory regulation, mandatory standards, and voluntary assurance. [Statutory regulation](https://en.wikipedia.org/wiki/Regulatory_compliance) is law — enforced by a regulator with legal powers, and non-negotiable (for example, data protection law, or the requirement to register a medical device). *Mandatory standards* are contractual or policy requirements you must meet to operate within a system even where they are not primary legislation — for example, national NHS instruments that commissioning is conditional upon. *Voluntary assurance* is where you choose to demonstrate quality against a recognised benchmark to build trust, win procurements, or pre-empt future regulation. Knowing which tier a given requirement sits in tells you what happens if you miss it: prosecution, exclusion from the market, or reputational disadvantage.

**The Care Quality Commission (CQC).** The [Care Quality Commission](https://en.wikipedia.org/wiki/Care_Quality_Commission) is the independent regulator of health and adult social care in England. It registers, inspects, and rates providers against whether services are safe, effective, caring, responsive, and well-led. Digital services do not escape it: where technology is part of care delivery, the CQC's questions about safety and leadership reach the systems you run, and its "well-led" domain increasingly probes digital and data maturity.

**The MHRA and medical devices.** The [Medicines and Healthcare products Regulatory Agency](https://en.wikipedia.org/wiki/Medicines_and_Healthcare_products_Regulatory_Agency) (MHRA) regulates medicines and [medical devices](https://en.wikipedia.org/wiki/Medical_device) in the UK. Crucially, software can *be* a medical device: Software as a Medical Device (SaMD) is software intended for a medical purpose — diagnosis, prevention, monitoring, treatment — without being part of a hardware device. If your app calculates a dose, triages a symptom, or interprets an image, it is very likely a medical device and must be classified, registered, and carry the appropriate conformity marking before it is placed on the market.

**Conformity marking: UKCA and CE.** A medical device placed on the Great Britain market needs [UKCA marking](https://en.wikipedia.org/wiki/UKCA_marking) (UK Conformity Assessed), the post-Brexit British counterpart to [CE marking](https://en.wikipedia.org/wiki/CE_marking) (Conformité Européenne). For now, CE-marked devices remain accepted in Great Britain under transitional arrangements, and Northern Ireland follows EU rules — so the marking you need depends on where you place the device. This is a live, shifting area; treat the exact requirement as something to confirm, not assume.

**NICE and the Evidence Standards Framework.** The [National Institute for Health and Care Excellence](https://en.wikipedia.org/wiki/National_Institute_for_Health_and_Care_Excellence) (NICE) produces guidance on what works and what is cost-effective. Its Evidence Standards Framework (ESF) for digital health technologies sets out, proportionate to risk, the evidence a digital product should show before the system adopts it. NICE is not a licensing gatekeeper like the MHRA, but its judgements shape commissioning heavily — passing MHRA registration proves a device is safe to sell; clearing NICE-aligned evidence expectations helps prove it is worth buying (see Chapter 4 — Evidence-Driven Decisions).

**The ICO and data protection law.** The [Information Commissioner's Office](https://en.wikipedia.org/wiki/Information_Commissioner%27s_Office) (ICO) is the UK's independent regulator for data protection and freedom of information. It enforces the UK [General Data Protection Regulation](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation) (GDPR) and the [Data Protection Act 2018](https://en.wikipedia.org/wiki/Data_Protection_Act_2018), which govern how you may lawfully process personal data — and health data is a "special category" attracting the strongest protections. The ICO can investigate, order changes, and impose significant fines. The substance is covered in Chapter 7; here, simply hold that the ICO is your data-protection regulator and that health data carries a higher bar.

**Mandatory NHS instruments.** Beyond primary law, the NHS runs its own mandatory instruments. The Data Security and Protection Toolkit (DSPT) is the annual self-assessment every organisation handling NHS patient data must complete to demonstrate data-security and information-governance standards. The Digital Technology Assessment Criteria (DTAC) is the baseline a digital health technology must meet to be commissioned by NHS organisations, spanning clinical safety, data protection, technical security, interoperability, and usability. The clinical-safety standards DCB0129 (for manufacturers) and DCB0160 (for deploying organisations) mandate a documented clinical-risk-management process — a hazard log, a clinical safety officer, a safety case — and are the backbone of Chapter 6.

**Professional regulators.** People, not just products, are regulated. The [General Medical Council](https://en.wikipedia.org/wiki/General_Medical_Council) (GMC) registers and sets standards for doctors, and the [Nursing and Midwifery Council](https://en.wikipedia.org/wiki/Nursing_and_Midwifery_Council) (NMC) does the same for nurses and midwives. When clinicians design, approve, or operate digital services, their professional duties travel with them — a clinical safety officer signing off a system is acting under professional accountability, not just an org-chart role.

**Horizon and context: the EU regime.** Even outside the EU, the [Artificial Intelligence Act](https://en.wikipedia.org/wiki/Artificial_Intelligence_Act) and [Regulation (EU) 2017/745](https://en.wikipedia.org/wiki/Regulation_(EU)_2017/745) (the EU Medical Device Regulation, MDR) matter — they set the direction of travel, bind you if you serve EU markets or Northern Ireland, and often preview where UK rules head next. Horizon-scanning for such change is itself a compliance discipline.

**The compliance map and register.** A compliance map lists, for your service, every applicable obligation across all three tiers, and a compliance register records the status, owner, evidence, and review date for each. Together they turn a diffuse landscape into a managed, auditable position — the difference between "we think we're compliant" and "here is the named owner and current evidence for each duty."

## Best practices

1. **Classify your service before you argue about controls.** The first question is not "are we compliant?" but "what are we, legally?" Determine early whether your product is a medical device (and its risk class), whether you are a data controller or processor, and which mandatory NHS instruments apply. Getting the classification wrong makes every downstream decision wrong; getting it right tells you which of the tiers and bodies above actually bind you.

2. **Build and maintain a live compliance map and register.** Enumerate every applicable obligation for the service across statutory regulation, mandatory standards, and voluntary assurance, and record for each an owner, current status, supporting evidence, and next review date. Keep it living, reviewed on a schedule, not a document written once for a business case and never opened again. A good register answers, on any given day, "who owns this duty and where is the evidence?"

3. **Assign single-name accountability for each obligation.** Diffuse responsibility is how compliance fails: everyone assumes someone else holds it. Give each duty a named owner — a Data Protection Officer for data protection, a Clinical Safety Officer for DCB0129/0160, a Senior Information Risk Owner for the DSPT — and make the map's ownership column real, with the authority and time to discharge it. Accountability that is not named is not accountability.

4. **Be proportionate and risk-based, not tick-box.** Regulation deserves the same proportionality as evidence (see Chapter 4): concentrate rigour where the risk to patients, equity, and trust is highest, and keep low-risk work light. Tick-box compliance — completing the form while missing the intent — is both wasteful and dangerous, because it manufactures false assurance. Aim to satisfy the *purpose* of each requirement, which usually also satisfies the letter.

5. **Treat mandatory NHS instruments as design inputs, not exit gates.** The DTAC, DSPT, and DCB0129/0160 are cheapest and most effective when built into delivery from the start, not bolted on before go-live. A DTAC failure discovered at launch can cost months; a clinical safety case assembled retrospectively is thin and unconvincing. Fold these instruments into discovery and delivery so that meeting them is a by-product of working well.

6. **Horizon-scan for regulatory change and own the response.** Regulation moves — UKCA timelines shift, the EU AI Act phases in, the software-as-a-medical-device regime evolves. Assign someone to track relevant regulators and consultations, maintain a short "regulatory change" watchlist against your compliance map, and turn signals into planned work before deadlines become emergencies. Being surprised by a known-in-advance rule change is an avoidable, self-inflicted failure.

7. **Keep evidence continuously, and make it audit-ready.** Regulators, commissioners, and the CQC's "well-led" reviewers ask you to *show*, not assert. Keep hazard logs, Data Protection Impact Assessments, DSPT submissions, and DTAC evidence current and retrievable rather than reconstructing them under inspection pressure. Continuous evidence is also cheaper than the periodic scramble it replaces.

8. **Coordinate across regulators rather than in silos.** Because one service touches many bodies, its compliance functions must talk to each other: the clinical-safety, information-governance, and product owners should share one view of the service, not maintain three disconnected ones. A change that satisfies the MHRA can create a data-protection issue; a UX fix can alter the clinical risk profile. Run compliance as one coordinated picture, tied into your wider governance (Chapter 37 — Governance & Assurance).

## Questions to discuss with your team

1. **For our flagship digital service, can we name every regulator and mandatory standard that applies, who owns each, and where the current evidence lives — without anyone having to go and find out?**
   This tests whether you actually hold the map or merely believe you are compliant. It matters because in health and care the obligations genuinely overlap — a triage app can be a medical device under the MHRA, a data-processing operation under the ICO, a commissioned technology needing DTAC, and part of a CQC-inspected service all at once — and a gap in any one tier can halt the service or harm patients. The tension to surface is between the comfort of assuming "IG handles that" or "the supplier is regulated, not us" and the discomfort of confirming named ownership and live evidence for each duty. Work through the service concretely: list the bodies, place each obligation in its tier (statutory, mandatory, voluntary), and try to produce the current evidence for three of them on the spot. If you cannot, you have found your first gap. A good, honest answer is a populated compliance register with named owners and dated evidence, and candour about which duties are currently unowned or unevidenced rather than a confident wave at "we're compliant."

2. **Where are we doing tick-box compliance — satisfying the form while missing the point — and where are we over-engineering low-risk work?**
   The chapter argues for proportionate, risk-based compliance, and this question forces you to check both failure directions honestly. It matters because false assurance is actively dangerous in a safety-critical setting: a DSPT marked "met" or a clinical safety case assembled the week before go-live can look compliant while leaving real hazards unmanaged, and meanwhile a heavy assurance process throttling a low-risk content change wastes scarce capacity and breeds cynicism about the whole regime. The trade-off to debate is that proportionality demands judgement and the confidence to defend it, which is harder to administer than a uniform rule that treats everything as high-risk. Take two or three current items — one genuinely high-risk, one low — and ask whether the rigour you applied matched the risk to patients, equity, and trust, or was driven by habit and fear. Consider whether your DTAC and DCB0129/0160 work is genuinely shaping the design or being reverse-engineered to pass. A good answer names a specific instance of box-ticking and a specific instance of over-engineering, and commits to calibrating rigour to risk rather than applying one blunt standard everywhere.

3. **How would we know if a regulation that affects us is about to change — and who is responsible for turning that signal into planned work?**
   This probes horizon-scanning, the discipline that separates organisations surprised by deadlines from those that plan for them. It matters because the landscape is unusually live right now — UKCA and CE-marking timelines, the software-as-a-medical-device regime, the phased EU AI Act, evolving NHS instruments — and a rule change you knew was coming but did not prepare for is a self-inflicted wound that can pull a service off the market. The tension is that horizon-scanning has no immediate payoff, so it is the first thing dropped under delivery pressure, and its absence is invisible until the deadline arrives. Explore who currently tracks the relevant regulators and consultations, whether there is a watchlist tied to your compliance map, and how a signal becomes a ticket with an owner and a date rather than a worry in someone's inbox. Consider whether you would even hear about a change affecting only Northern Ireland or EU-facing parts of your service. A good answer names the person or role that owns regulatory horizon-scanning, points to a concrete watchlist, and describes the last time an upcoming change was turned into planned work ahead of the deadline.

## In practice: a health & care example

An integrated care system (ICS) plans to roll out a smartphone app that lets patients with long-term conditions record symptoms, and uses an algorithm to flag those who may be deteriorating for clinical review. The temptation is to treat it as "just an app" and push it live.

Instead, the digital director starts with classification. Because the algorithm interprets patient data to inform clinical action, legal advice confirms it is Software as a Medical Device, so the MHRA regime applies and the supplier must hold the correct conformity marking for the Great Britain market — a UKCA question the team flags to watch as transitional CE arrangements evolve. The ICS is a data controller for the patient data, so the ICO's data-protection duties bind it, and a Data Protection Impact Assessment is opened (feeding Chapter 7). Because it is being commissioned by NHS bodies, DTAC applies, and because it is deployed into clinical use, DCB0160 requires a clinical safety case, a hazard log, and a named Clinical Safety Officer (Chapter 6).

The team builds a compliance map: each obligation placed in its tier, each with a named owner — Data Protection Officer, Clinical Safety Officer, Senior Information Risk Owner, product lead — and a register tracking status and evidence. Rather than treat DTAC and the safety case as go-live gates, they fold them into delivery from discovery, so the hazard log grows with the design. NICE's Evidence Standards Framework shapes what effectiveness evidence they demand from the supplier before scaling. A horizon-scanning note flags the EU AI Act as relevant to the algorithm's future and to any EU-facing ambition. When the CQC later reviews the service's leadership, the ICS answers the "well-led" questions with a live register and current evidence rather than a scramble. The app ships later than the naive plan, and lawfully.

## Three sector lenses

The same landscape imposes very different burdens depending on where you sit.

### Startup

A small digital-health company feels the medical-device and DTAC regimes most sharply, because clearing them costs money and time it may not have, and the temptation is to under-classify — to insist the product is "just a wellness app," not a medical device — to dodge the burden. That is the most dangerous move available: mis-classification is the fastest route to an enforcement action and a collapsed NHS sales pipeline. The disciplined path is to classify honestly and early, build a lightweight but real compliance map, and treat DTAC and a clean data-protection posture as sales assets that open the NHS market rather than obstacles to it. A named owner for regulatory horizon-scanning may be a single founder wearing another hat, but the watchlist still needs to exist.

### Enterprise

An NHS trust or large ICS holds many services at once, so its challenge is portfolio-scale coordination: dozens of systems, each touching several regulators, with obligations that must not fall between teams. The failure mode is organisational silos — clinical safety, information governance, and procurement each holding a partial view, so no one sees the whole compliance position of a given service. The corrective is a shared compliance map per service, single-name accountability tied into board-level governance (Chapter 37), and continuous audit-ready evidence so a CQC "well-led" review or an ICO enquiry is answered from a live position. A large health-tech or pharma enterprise brings mature regulatory-affairs machinery but must guard against treating it as a compliance factory disconnected from how products are actually built.

### Government

A national body — NHS England, the Department of Health and Social Care, the MHRA, NICE — often *is* the regulator or the author of the mandatory instrument, so its ways of working set the bar the whole system must clear, and its decisions attract parliamentary and public scrutiny. Here compliance work is population-scale accountability: an instrument like DTAC or the ESF shapes an entire market, so proportionality and clarity in the standard itself are duties, not niceties, because a badly calibrated national requirement either stalls useful innovation everywhere or waves through risk everywhere. National bodies also carry the horizon-scanning responsibility for the system, anticipating how the EU AI Act, the MDR, and conformity-marking regimes should shape UK policy. Transparency about what a standard requires and why is part of maintaining public trust at scale.

## Common failure modes

- **Mis-classification.** Insisting a product is not a medical device, or that you are a processor not a controller, to dodge a burden. Antidote: classify honestly and early, with legal advice; classification drives everything else.
- **Tick-box compliance.** Completing the DSPT or a safety case to pass, while the underlying risk is unmanaged. Antidote: satisfy the purpose, not just the form; test whether the artefact actually shaped the design.
- **Compliance as a go-live gate.** Discovering DTAC or clinical-safety gaps at launch. Antidote: fold mandatory instruments into delivery from discovery.
- **Diffuse ownership.** Every duty assumed to be someone else's. Antidote: single-name accountability per obligation in a live register.
- **Silomised regulators.** Clinical safety, IG, and product holding disconnected views of one service. Antidote: one shared compliance map, coordinated governance.
- **No horizon-scanning.** Being surprised by a rule change you could have seen coming. Antidote: an owned watchlist tied to the compliance map.
- **Stale evidence.** Reconstructing hazard logs and assessments under inspection pressure. Antidote: continuous, audit-ready evidence.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Classification | Assumed or avoided | Done late, informally | Formal, early, legally reviewed | Revisited as the product changes |
| Compliance map & register | None | Ad hoc list for a business case | Live register, owners, evidence, review dates | Integrated with delivery and board governance |
| Accountability | Diffuse / unclear | Some named roles | Single-name owner per obligation | Owners resourced, empowered, audited |
| Proportionality | Tick-box or absent | One-size rigour | Risk-based, calibrated to harm | Explicit, defensible, continuously tuned |
| Horizon-scanning | Reactive to deadlines | Occasional awareness | Owned watchlist | Signals routinely become planned work |

## Checklist

- [ ] The service's legal classification (medical device and class; controller/processor) is confirmed and documented.
- [ ] A live compliance map lists every obligation across statutory, mandatory, and voluntary tiers.
- [ ] Each obligation has a single named owner with the authority and time to discharge it.
- [ ] Mandatory NHS instruments (DTAC, DSPT, DCB0129/0160) are built into delivery, not bolted on at go-live.
- [ ] Rigour is calibrated to patient, equity, and trust risk — not uniform box-ticking.
- [ ] Evidence (hazard logs, DPIAs, DSPT, DTAC) is current, retrievable, and audit-ready.
- [ ] A named owner runs regulatory horizon-scanning against a maintained watchlist.
- [ ] Conformity-marking requirements (UKCA/CE) for the relevant market are confirmed, not assumed.
- [ ] Compliance functions share one coordinated view of each service, tied into governance (Chapter 37).
- [ ] The register is reviewed on a schedule, not written once and abandoned.

## Key sources

- Care Quality Commission — *How CQC regulates* and the single assessment framework (cqc.org.uk).
- MHRA — *Medical devices: software applications (apps)* and *Software and AI as a Medical Device* guidance (gov.uk).
- NICE — *Evidence Standards Framework for digital health technologies (ESF)* (nice.org.uk).
- Information Commissioner's Office — *Guide to Data Protection* and *Guide to the UK GDPR* (ico.org.uk).
- NHS England — *Data Security and Protection Toolkit (DSPT)* (dsptoolkit.nhs.uk).
- NHS England — *Digital Technology Assessment Criteria (DTAC)*.
- NHS Digital / NHS England — clinical risk management standards *DCB0129* and *DCB0160*.
- GMC — *Good medical practice*; NMC — *The Code* (professional standards).
- GOV.UK — *UKCA marking* and *CE marking* guidance for the Great Britain market.

## References

1. Regulatory compliance — Wikipedia — https://en.wikipedia.org/wiki/Regulatory_compliance
2. Care Quality Commission — Wikipedia — https://en.wikipedia.org/wiki/Care_Quality_Commission
3. Medicines and Healthcare products Regulatory Agency — Wikipedia — https://en.wikipedia.org/wiki/Medicines_and_Healthcare_products_Regulatory_Agency
4. Medical device — Wikipedia — https://en.wikipedia.org/wiki/Medical_device
5. UKCA marking — Wikipedia — https://en.wikipedia.org/wiki/UKCA_marking
6. CE marking — Wikipedia — https://en.wikipedia.org/wiki/CE_marking
7. National Institute for Health and Care Excellence — Wikipedia — https://en.wikipedia.org/wiki/National_Institute_for_Health_and_Care_Excellence
8. Information Commissioner's Office — Wikipedia — https://en.wikipedia.org/wiki/Information_Commissioner%27s_Office
9. General Data Protection Regulation — Wikipedia — https://en.wikipedia.org/wiki/General_Data_Protection_Regulation
10. Data Protection Act 2018 — Wikipedia — https://en.wikipedia.org/wiki/Data_Protection_Act_2018
11. General Medical Council — Wikipedia — https://en.wikipedia.org/wiki/General_Medical_Council
12. Nursing and Midwifery Council — Wikipedia — https://en.wikipedia.org/wiki/Nursing_and_Midwifery_Council
13. Artificial Intelligence Act — Wikipedia — https://en.wikipedia.org/wiki/Artificial_Intelligence_Act
14. Regulation (EU) 2017/745 (EU Medical Device Regulation) — Wikipedia — https://en.wikipedia.org/wiki/Regulation_(EU)_2017/745
15. *How CQC regulates* — Care Quality Commission — https://www.cqc.org.uk/about-us/how-we-do-our-job/how-we-regulate
16. *Software and AI as a Medical Device* — MHRA, GOV.UK — https://www.gov.uk/government/publications/software-and-artificial-intelligence-ai-as-a-medical-device
17. *Evidence Standards Framework for digital health technologies (ESF)* — NICE — https://www.nice.org.uk/about/what-we-do/digital-health
18. *Guide to the UK GDPR* — Information Commissioner's Office — https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/
19. *Data Security and Protection Toolkit* — NHS England — https://www.dsptoolkit.nhs.uk/
20. *Digital Technology Assessment Criteria (DTAC)* — NHS England — https://www.nhs.uk/digital-technology-assessment-criteria-dtac/
21. *Clinical risk management standards DCB0129 and DCB0160* — NHS England — https://digital.nhs.uk/services/clinical-safety
22. *UKCA marking* guidance — GOV.UK — https://www.gov.uk/guidance/using-the-ukca-marking
