# Chapter 43 — Collaborating with Partner Organisations

**In one sentence:** Digital health and care outcomes now depend less on what any single organisation builds and more on how honestly, safely, and durably it collaborates across the boundaries between NHS trusts, councils, social care, the voluntary sector, universities, and suppliers.

## Why this matters in health and care

No single organisation holds the whole of a person's care. A frail older adult moves between a GP practice, an acute trust, a community team, a council reablement service, a care home, and perhaps a hospice — each a separate legal entity, with its own systems, governance, and incentives. The value your programme delivers is realised at these seams, and it is at these seams that harm accumulates: the missed allergy, the duplicated assessment, the discharge that collapses because the package of care was never arranged.

Collaboration is therefore not a soft skill layered on top of delivery; it is the delivery. [Integrated Care Systems](https://en.wikipedia.org/wiki/Integrated_care_system) (ICS) in England, and Regional Partnership Boards in Wales, exist precisely because Parliament judged that competition between organisations had gone too far and that population health requires organisations to plan and act together. The legal architecture — the [Health and Care Act 2022](https://en.wikipedia.org/wiki/Health_and_Care_Act_2022), Integrated Care Boards (ICBs), and Integrated Care Partnerships (ICPs) — is a statutory instruction to collaborate.

The stakes are concrete. Collaboration touches public money (shared platforms funded from multiple budgets), safety (data flowing between clinicians who have never met), equity (whether the third sector reaches communities the NHS cannot), and statutory duty (each partner remains individually accountable to its own regulator and to the [Information Commissioner](https://en.wikipedia.org/wiki/Information_Commissioner%27s_Office)). Get the collaboration right and you compound everyone's effort; get it wrong and you multiply everyone's risk.

## Core concepts

**The partner landscape.** Your collaborators are not interchangeable. NHS trusts and foundation trusts operate under NHS England oversight and national contracts. Local authorities are democratically accountable, cash-constrained, and own adult social care and public health. Social care providers are largely private or voluntary, fragmented, and thinly resourced for digital. The [voluntary, community and social enterprise](https://en.wikipedia.org/wiki/Voluntary_sector) (VCSE) sector brings reach and trust but little infrastructure. Universities bring evidence and evaluation. Industry suppliers bring capability and a commercial motive. Each has a different clock, a different funding cycle, and a different definition of success.

**Integrated Care Systems.** An ICS is a partnership of the organisations in a geography that plan and deliver joined-up health and care. It has two statutory bodies: the ICB (an NHS body that plans and funds most NHS services) and the ICP (a broader committee, jointly convened with local government, that sets the integrated care strategy). Crucially, an ICS is not a single organisation and not a single data controller — it is a set of controllers who must agree how to act together.

**Governance of collaboration.** Because no partner can direct another, collaboration runs on *agreements* rather than *authority*. The instruments are a [Memorandum of Understanding](https://en.wikipedia.org/wiki/Memorandum_of_understanding) (MOU) to set intent, a joint committee or programme board to make decisions, terms of reference that name who decides what, a shared roadmap so partners invest in step, and — where personal data moves — a Data Sharing Agreement (DSA) or Information Sharing Agreement (ISA) underpinned by Data Protection Impact Assessments (DPIAs).

**Information governance and the Caldicott Principles.** [Information governance](https://en.wikipedia.org/wiki/Information_governance) sets the framework; the eight Caldicott Principles govern the use of confidential patient information: justify the purpose, use it only when necessary, use the minimum necessary, access on a strict need-to-know basis, ensure everyone is aware of their responsibilities, comply with the law, and — the newer principles — the duty to share information can be as important as the duty to protect it, and inform patients about how their data is used. Every partnership needs a named [Caldicott Guardian](https://en.wikipedia.org/wiki/Caldicott_Guardian) and a Senior Information Risk Owner (SIRO) at each controller, working under [UK GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation) and the [Data Protection Act 2018](https://en.wikipedia.org/wiki/Data_Protection_Act_2018).

**Interoperability and open standards.** Shared care records only work if systems can exchange meaning, not just files. That means [interoperability](https://en.wikipedia.org/wiki/Interoperability) built on recognised standards — HL7 [FHIR](https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources) for exchange, [SNOMED CT](https://en.wikipedia.org/wiki/SNOMED_CT) for clinical terms, and NHS England's data and interoperability standards — and rejecting bespoke point-to-point integrations that lock value inside one vendor relationship.

## Best practices

1. **Start from a shared population outcome, not a shared system.** Anchor the collaboration in an outcome every partner already cares about — reducing emergency admissions from care homes, say — and let the technology follow. Partners will compromise on architecture far more readily than on purpose, so make the purpose the thing you agree first and revisit often.

2. **Make governance proportionate and visible.** Stand up a joint board with clear terms of reference, a single shared roadmap, and named decision rights before you write a line of code. Keep it light enough to move but formal enough to survive a change of personnel; document who can commit each organisation, because verbal agreements evaporate when the sponsoring director leaves.

3. **Treat information governance as an enabler, not a gate.** Engage Caldicott Guardians, SIROs, and Data Protection Officers at the start, complete a joint DPIA, and put a signed Data Sharing Agreement in place that names purposes, lawful bases, controllers, and retention. Invoke the seventh Caldicott Principle explicitly: for direct care, the duty to share can be as important as the duty to protect, and framing IG this way turns it from a blocker into a partner.

4. **Mandate open standards and interoperability in every agreement.** Require FHIR-based exchange and recognised terminologies (SNOMED CT, dm+d) as a condition of participation, and align to NHS England's shared care record and interoperability requirements. Open standards are how you keep future options open; they are the single most effective defence against [vendor lock-in](https://en.wikipedia.org/wiki/Vendor_lock-in) (see Chapter 44 — Working with Local & National Governments on national mandates).

5. **Manage suppliers as a portfolio, and design against lock-in from day one.** Insist on data portability, exit clauses, documented APIs, and ownership of your own configuration and data. Follow the Provider Selection Regime for in-scope health care services and public procurement rules elsewhere; a supplier who resists open standards or an exit plan is telling you their commercial strategy is your dependency.

6. **Invest in the shared care record as shared infrastructure.** A shared care record — the read-only view across a system, distinct from any one [electronic patient record](https://en.wikipedia.org/wiki/Electronic_health_record) — is a collaboration asset owned by the ICS, not by a vendor. Govern it jointly, fund it jointly, and hold its data quality to a common standard, because a record that partners do not trust is a record they will not use.

7. **Align incentives before you rely on goodwill.** Collaboration fails when the organisation asked to invest is not the one that reaps the benefit — a hospital funds a scheme that saves a council money. Surface these asymmetries early and use pooled budgets, gain-share arrangements, or [Better Care Fund](https://en.wikipedia.org/wiki/Better_Care_Fund) mechanisms so that effort and reward sit together.

8. **Build trust deliberately and protect it.** Trust is the operating currency of partnership and it is built by keeping small promises, sharing bad news early, and never surprising a partner in public. Create the routines — regular joint stand-ups, a shared risk log, a single version of the truth — that let trust accumulate rather than reset with every reorganisation.

## Questions to discuss with your team

1. **When a partner's interests diverge from ours mid-programme, how do we decide whether to compromise, escalate, or walk away?**
   Every partnership starts with a shared purpose, but purposes drift: a council faces an in-year budget cut, a trust reorganises, a supplier is acquired, an election changes a leader's mandate. Because no partner can direct another, the collaboration runs on agreement rather than authority, so the team needs a settled view of how it will behave when goodwill is tested rather than improvising under pressure. The tension is between protecting the relationship — the operating currency of partnership — and protecting the outcome, the patients, and your own statutory accountability, which cannot be delegated to a joint board. Consider concrete triggers: what would make you invoke the exit clause in a supplier contract, escalate to the ICP, or accept a smaller shared scope rather than lose the partner entirely? An honest answer names the few red lines that are non-negotiable (patient safety, lawful basis for data sharing, your own regulatory duties), distinguishes them from the many things that are genuinely tradeable, and agrees who holds the authority to make the call so it does not fall to whoever happens to be in the room. It also acknowledges that walking away is sometimes the responsible choice, and that a partnership kept alive only to avoid an awkward conversation quietly multiplies everyone's risk.

2. **Are we treating social care providers and the voluntary sector as genuine partners, or as afterthoughts we expect to keep pace with the NHS?**
   Partnerships default to NHS-to-NHS deals because those partners share systems, funding language, and a national regulator, while care homes, domiciliary providers, and VCSE organisations are fragmented, thinly resourced for digital, and operating on margins that leave no room to absorb integration costs. Yet these are precisely the partners who reach the people the NHS struggles to reach and who often carry the workload when a scheme succeeds. The trade-off is uncomfortable: designing for the thinnest-resourced partner slows the programme and raises its cost, but excluding them hollows out the very integration the ICS exists to deliver. Concrete angles worth debating include whether your governance has committing officers from social care at the table or only NHS directors, whether your data-sharing agreements assume infrastructure a small care home simply does not have, and whether incentive asymmetry — a hospital funding a scheme that saves a council money, or a care home bearing monitoring workload for someone else's benefit — is being addressed through pooled budgets or gain-share, or quietly ignored. A good answer is specific about which under-resourced partners matter most for your population outcome, what practical support (funding, kit, training, simplified onboarding) they need to participate as equals, and how you will know whether they are genuinely engaged or merely nominally signed up.

3. **How do we make information governance an enabler that partners trust, rather than a gate that stalls every data flow?**
   Confidential patient information moving between organisations that have never met is where collaboration creates its most acute risk and its most valuable benefit, and IG is the mechanism that decides which. Teams routinely treat IG as a late sign-off, which guarantees that Caldicott Guardians, SIROs, and DPOs raise objections at go-live that could have been designed out months earlier — but the opposite failure is just as real, where an over-cautious reading of the rules blocks sharing that is lawful and in the patient's direct-care interest. The seventh Caldicott Principle is the crux of the debate: the duty to share information can be as important as the duty to protect it, yet organisations instinctively over-weight protection because the penalties for a breach are visible and the harms of not sharing — the missed allergy, the duplicated assessment — are diffuse and unattributed. The team should examine whether it engages IG at inception with a joint DPIA and a signed Data Sharing Agreement naming purposes and lawful basis, or whether it treats IG as a hurdle to clear at the end; and whether each controller's Caldicott Guardian and SIRO understand the shared purpose well enough to say yes quickly. A strong answer frames IG as a partner in the design, is precise about the lawful basis and the minimum necessary dataset, and can point to the routines — a shared risk log, named accountable people at each controller — that let partners trust each other with data rather than defaulting to defensive refusal.

## In practice: a health & care example

A fictional ICS, "Rivermouth", wants to cut avoidable A&E attendances from its 60 care homes. The partners are two acute trusts, a community trust, the county council (which commissions the homes), the homes themselves (mostly small private providers), a local hospice, a university evaluation team, and a telehealth supplier.

Rivermouth resists the temptation to procure a platform first. Instead the ICP agrees a single outcome — a 20% reduction in avoidable conveyances over two years — and stands up a joint delivery board with terms of reference naming decision rights and each partner's committing officer. A shared roadmap sequences the work: first a shared care record view for care home staff, then remote vital-signs monitoring.

Information governance runs in parallel, not after. The ICB's Caldicott Guardian convenes the controllers, a joint DPIA is completed, and a Data Sharing Agreement names the lawful basis for direct care and the minimum dataset the homes may see. The telehealth contract is let under the Provider Selection Regime with mandated FHIR interfaces, an exit plan, and council ownership of the configuration.

The asymmetry is addressed head-on: the acute trusts benefit from fewer admissions, but the homes bear the workload. A gain-share from the Better Care Fund reimburses homes for staff time on monitoring. Eighteen months in, conveyances are down 14%, the university's independent evaluation confirms the trend, and — because the standards were open — the ICS can swap one homes-facing app without renegotiating the whole record.

## Three sector lenses

### Startup

A small digital-health company collaborates from a position of weakness: it needs the partnership more than the partnership needs it, and a single stalled Data Sharing Agreement can burn the runway. Keep the ask narrow — one dataset, one lawful basis, one named outcome — so a partner's Caldicott Guardian and DPO can say yes quickly, and lead with your own DPIA and clinical-safety case rather than waiting to be asked. Sign a lightweight Memorandum of Understanding to establish intent, but push hard for an early paid pilot with a real trust or council, because reference customers and evidence of interoperability are what unlock the next round of investment. Above all, design for exit and portability from day one: a founder who quietly engineers lock-in may win one contract but forfeits the NHS's trust, and the sector talks.

### Enterprise

A large NHS trust, ICS, or health-tech supplier collaborates from a position of strength but slowness: many controllers, layered governance, and a natural gravity toward NHS-to-NHS deals that leave social care and the VCSE behind. The task is to make governance proportionate — a standing joint board with named committing officers and a shared roadmap — rather than letting each partnership reinvent its terms of reference. Mandate open standards (FHIR, SNOMED CT) and data portability in every contract, and use your procurement weight to shape the market away from lock-in rather than accumulating bespoke point-to-point integrations. Deliberately fund and design for the thinnest-resourced partners, because the enterprise is usually the only actor with the balance sheet to carry them.

### Government

A national or local public body — NHS England, DHSC, a local authority — collaborates by setting the rules others collaborate within: it mandates the interoperability standards, funds the shared infrastructure, and legislates the duty to cooperate through instruments such as the Health and Care Act 2022. Its leverage is the standard and the pound, so it should mandate open standards and shared care records as conditions of funding rather than negotiating them partner by partner. It also holds the levers to fix incentive asymmetry across whole systems — pooled budgets and the Better Care Fund exist precisely so that the body reaping a saving is not the only one asked to invest. The accountability is public and severe: decisions are read by auditors, select committees, and the Information Commissioner, so collaboration must be transparent and defensible, not merely expedient.

## Common failure modes

- **Procuring a platform before agreeing a purpose.** The technology becomes the project; partners defend their systems instead of pursuing the outcome. Fix: agree the population outcome and decision rights first.
- **Treating information governance as a late sign-off.** IG raises objections at go-live that could have been designed out. Fix: bring Caldicott Guardians, SIROs, and DPOs in at inception and complete the joint DPIA early.
- **Point-to-point integrations and de facto lock-in.** Bespoke connectors calcify into dependencies no one can afford to replace. Fix: mandate open standards and data portability in every agreement.
- **Ignoring incentive asymmetry.** The organisation asked to invest is not the one that benefits, so it quietly disengages. Fix: use pooled budgets or gain-share so effort and reward align.
- **Governance by the absent.** Boards staffed by people who cannot commit their organisations, so nothing sticks. Fix: name committing officers in the terms of reference.
- **Forgetting social care and the VCSE.** Partnerships default to NHS-to-NHS and leave the sectors with the least digital capacity behind. Fix: fund and design explicitly for the thinnest-resourced partners.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Governance | Ad hoc, personality-led | MOU and a board exist | Terms of reference, decision rights, shared roadmap | Self-renewing governance that survives reorganisation |
| Information sharing | Case-by-case, informal | DPIA done per project | Standing DSA/ISA, named Caldicott Guardians | Federated IG treated as an enabler across the ICS |
| Interoperability | Point-to-point, bespoke | Some standards used | Open standards (FHIR, SNOMED CT) mandated | Plug-and-play; components swapped without renegotiation |
| Supplier management | Reactive, lock-in unnoticed | Contracts have exit clauses | Portfolio view, portability designed in | Active market-shaping; commodity components |
| Incentive alignment | Benefit and cost misaligned | Asymmetry acknowledged | Pooled budgets / gain-share in place | Shared accountability for shared outcomes |

## Checklist

- [ ] The collaboration is anchored in a shared population outcome, agreed before any technology.
- [ ] A joint board exists with terms of reference naming decision rights and each partner's committing officer.
- [ ] Caldicott Guardians, SIROs, and DPOs were engaged at inception, not at go-live.
- [ ] A joint DPIA is complete and a signed Data Sharing / Information Sharing Agreement is in place.
- [ ] Open standards (HL7 FHIR, SNOMED CT) and data portability are mandated in every partner and supplier agreement.
- [ ] Procurement of in-scope services follows the Provider Selection Regime; other buys follow public procurement rules.
- [ ] Every supplier contract has an exit plan, documented APIs, and your ownership of data and configuration.
- [ ] Incentive asymmetries are surfaced and addressed through pooled budgets or gain-share.
- [ ] Social care providers and the VCSE sector are funded and designed for, not assumed to keep up.
- [ ] A shared risk log and a single version of the truth are maintained across all partners.

## Key sources

- NHS England — *Integrated care systems (ICSs), integrated care boards (ICBs) and integrated care partnerships (ICPs): a quick guide* (transform.england.nhs.uk, information governance guidance).
- NHS England — *Data and clinical record sharing* and shared care record guidance (england.nhs.uk).
- UK Caldicott Committee / National Data Guardian — *The eight Caldicott Principles*.
- Information Commissioner's Office — *Data sharing: a code of practice*; UK GDPR and Data Protection Act 2018.
- Health and Care Act 2022 (legislation.gov.uk) — statutory basis for ICBs and ICPs.
- NHS England — *The Provider Selection Regime: statutory guidance*; Health Care Services (Provider Selection Regime) Regulations 2023.
- HL7 FHIR standard and NHS England data and interoperability standards; SNOMED CT.
- Better Care Fund policy framework (GOV.UK / NHS England) — pooled budgets across NHS and local government.

## References

1. Integrated care system — Wikipedia — https://en.wikipedia.org/wiki/Integrated_care_system
2. Health and Care Act 2022 — Wikipedia — https://en.wikipedia.org/wiki/Health_and_Care_Act_2022
3. Health and Care Act 2022 — UK Parliament / legislation.gov.uk — https://www.legislation.gov.uk/ukpga/2022/31
4. Voluntary sector — Wikipedia — https://en.wikipedia.org/wiki/Voluntary_sector
5. Memorandum of understanding — Wikipedia — https://en.wikipedia.org/wiki/Memorandum_of_understanding
6. Information governance — Wikipedia — https://en.wikipedia.org/wiki/Information_governance
7. Caldicott guardian — Wikipedia — https://en.wikipedia.org/wiki/Caldicott_Guardian
8. The Caldicott Principles — National Data Guardian (GOV.UK) — https://www.gov.uk/government/publications/the-caldicott-principles
9. General Data Protection Regulation — Wikipedia — https://en.wikipedia.org/wiki/General_Data_Protection_Regulation
10. Data Protection Act 2018 — Wikipedia — https://en.wikipedia.org/wiki/Data_Protection_Act_2018
11. Information Commissioner's Office — Wikipedia — https://en.wikipedia.org/wiki/Information_Commissioner%27s_Office
12. Data sharing: a code of practice — Information Commissioner's Office — https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/data-sharing/data-sharing-a-code-of-practice/
13. Interoperability — Wikipedia — https://en.wikipedia.org/wiki/Interoperability
14. Fast Healthcare Interoperability Resources (FHIR) — Wikipedia — https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources
15. SNOMED CT — Wikipedia — https://en.wikipedia.org/wiki/SNOMED_CT
16. Electronic health record — Wikipedia — https://en.wikipedia.org/wiki/Electronic_health_record
17. Vendor lock-in — Wikipedia — https://en.wikipedia.org/wiki/Vendor_lock-in
18. Better Care Fund — Wikipedia — https://en.wikipedia.org/wiki/Better_Care_Fund
19. The Provider Selection Regime: statutory guidance — NHS England — https://www.england.nhs.uk/publication/the-provider-selection-regime-statutory-guidance/
