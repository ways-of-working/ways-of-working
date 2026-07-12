# Chapter 4.3 — Interoperability & Data Standards

**In health and care, interoperability is not a technical nicety but a clinical-safety and equity requirement: when systems cannot share the right data, in the right form, with unambiguous meaning, at the point of care, people are harmed and inequity is amplified.**

## Why this matters in health and care

A person's care rarely happens in one place. A single episode might touch a general practice, an ambulance service, an emergency department, a hospital ward, a community nurse, a pharmacy, a social care team, and a carer at home. Each of these holds part of the record. If those parts cannot be brought together safely and quickly, clinicians make decisions with missing information: an allergy not seen, a medication double-prescribed, a test needlessly repeated, a safeguarding flag invisible to the team that needs it.

Interoperability is what turns a set of disconnected systems into something that behaves, from the patient's point of view, like a joined-up service. It is the plumbing beneath integrated care. When it works, a clinician in one organization can see what another has recorded, and can trust that it means what they think it means. When it fails, the failure is often silent until someone is harmed.

This is also an equity issue. People with the most complex needs — frail older adults, those with multiple long-term conditions, people moving between services — are exactly the people whose data is most fragmented. Poor interoperability therefore harms the most vulnerable most. And it is a matter of public trust: people reasonably assume that the NHS already shares their information sensibly, and are dismayed to learn how often it does not.

Finally, interoperability protects public money. Proprietary systems that cannot exchange data lock organizations into expensive, hard-to-replace contracts and force costly point-to-point integrations. Building to open standards is how you keep options open, keep suppliers honest, and avoid paying repeatedly to solve the same problem.

## Core concepts

[Interoperability](https://en.wikipedia.org/wiki/Interoperability) is the ability of different systems to exchange information and use it. It is useful to separate two layers. Syntactic or technical interoperability means two systems can exchange a message and each can parse its structure — the envelope arrives and can be opened. [Semantic interoperability](https://en.wikipedia.org/wiki/Semantic_interoperability) means the receiving system understands what the content means in the same way the sender did — that a code for "penicillin allergy" is interpreted identically on both sides. Technical interoperability without semantic interoperability is dangerous: data flows, but meaning is lost or distorted.

Health data is exchanged using standards. [Health Level 7 (HL7)](https://en.wikipedia.org/wiki/Health_Level_7) is the family of standards most used in healthcare. Its older HL7 version 2 (v2) messaging, using pipe-and-caret delimited text, still underpins a vast amount of hospital messaging and will for years. Its modern standard, [HL7 Fast Healthcare Interoperability Resources (FHIR)](https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources), models clinical information as "resources" exchanged over web-style [application programming interfaces (APIs)](https://en.wikipedia.org/wiki/API), which makes it far easier for modern developers to work with.

Standards for the message are not enough; you also need standard vocabularies for the content. [SNOMED CT (Systematized Nomenclature of Medicine — Clinical Terms)](https://en.wikipedia.org/wiki/SNOMED_CT) is the clinical terminology mandated across NHS care for recording diagnoses, symptoms, procedures and more. The NHS Dictionary of medicines and devices (dm+d) is the standard vocabulary for medicines and medical devices, and underpins electronic prescribing. The [International Classification of Diseases, 10th and 11th revisions (ICD-10 and ICD-11)](https://en.wikipedia.org/wiki/ICD-11), maintained by the World Health Organization, are used for classification, statistics and reimbursement rather than day-to-day clinical recording. [openEHR](https://en.wikipedia.org/wiki/OpenEHR) is an open specification for structuring the health record itself through shared, clinically governed "archetypes", and is used by some organizations to keep clinical data models independent of any single supplier.

Two further ideas are foundational. The [NHS Number](https://en.wikipedia.org/wiki/NHS_number) is the common patient identifier that lets records about the same person be linked reliably across organizations; without a shared identifier, matching is guesswork. And [Integrating the Healthcare Enterprise (IHE)](https://en.wikipedia.org/wiki/Integrating_the_Healthcare_Enterprise) publishes "profiles" that specify exactly how to combine existing standards to solve concrete problems such as sharing documents, so that different suppliers implement them the same way.

Underpinning all of this is a strategic choice. Building to [open standards](https://en.wikipedia.org/wiki/Open_standard) with published, reusable APIs keeps a market competitive and your data portable. Relying on proprietary interfaces creates [vendor lock-in](https://en.wikipedia.org/wiki/Vendor_lock-in), where switching supplier becomes so costly that you effectively cannot. None of it delivers value, however, without [data quality](https://en.wikipedia.org/wiki/Data_quality): accurate, complete, timely, consistently coded data is the precondition for interoperability, not an afterthought.

## Best practices

1. **Distinguish semantic from technical interoperability, and design for both.** It is easy to celebrate that a message now flows between two systems and miss that the receiving clinician cannot safely rely on its meaning. Always ask: does the other side interpret these codes, units, and negations exactly as we do? Invest in shared terminologies (SNOMED CT, dm+d) and value sets, not just message formats, because a correctly transmitted but misunderstood allergy is more dangerous than no message at all.

2. **Build to open standards and reuse platforms rather than reinventing.** Adopt the widely-endorsed principle: build to open standards, and reuse existing national platforms and services before building your own. In the NHS this means preferring HL7 FHIR APIs, using the NHS Number as the identifier, and connecting to national services such as the Spine, GP Connect, and shared care records rather than creating bespoke point-to-point links. Reuse reduces cost, spreads the maintenance burden, and means your data can travel.

3. **Make the NHS Number a non-negotiable in every record and message.** Reliable record linkage depends on a trustworthy common identifier. Ensure the NHS Number is captured, verified against the national demographic service, and carried on every relevant record and interface. Where it is missing or unverified, treat that as a data-quality defect to be resolved, because matching on name and date of birth alone produces both dangerous mismatches and missed links.

4. **Treat data quality as a first-class deliverable.** Interoperability exports your data quality problems to everyone downstream. Profile your data, measure completeness and coding consistency, and put in place stewardship so that errors are found and fixed at source. Coding drift, free-text where structured data is needed, and inconsistent units will quietly corrupt every downstream analysis and clinical view, so fund this work explicitly rather than assuming it happens by itself.

5. **Prefer API-first, loosely coupled architectures over tight integrations.** Design so that capabilities are exposed through well-documented, versioned APIs that others can consume without bespoke negotiation. This is slower at first than a direct database link, but it is what lets you replace one component without rebuilding everything around it. It also aligns with how national services and modern suppliers now expect to integrate, and it supports the delivery approaches in Chapter 3.5 — Delivery Lifecycles.

6. **Use published profiles and conformance testing, not local interpretations.** Standards are flexible, and two teams can implement "the same" FHIR resource incompatibly. Adopt national implementation guides and IHE profiles that pin down the details, and require suppliers to demonstrate conformance against them before go-live. Conformance testing turns "we support FHIR" — a claim that means very little on its own — into verifiable, contractual fact.

7. **Write interoperability and open-standards requirements into procurement and contracts.** The cheapest time to avoid lock-in is before you sign. Require open, documented APIs, the right to extract your own data in a standard format, adherence to named standards, and no charges for standard integrations. Work with your commercial colleagues (see Chapter 6.3 — Procurement & Commercial) so these become mandatory evaluation criteria, not aspirations negotiated away later.

8. **Govern interoperability with clinical safety and information governance in the room.** Every new data flow changes clinical risk and the handling of confidential information. Bring clinical safety officers and information governance leads into design decisions from the start, not as a final sign-off, so that shared records are both safe and lawful. This connects directly to Chapter 1.6 — Clinical Safety & Risk Management and Chapter 1.7 — Information Governance, Data Protection & Cyber Security.

## Questions to discuss with your team

1. **Where in our care pathways does missing or misunderstood data create the greatest clinical risk today?** Interoperability investment should follow harm and value, not architectural fashion. Map the journeys your most complex patients actually take and find the hand-offs where information is lost, delayed, or arrives without reliable meaning. Ask clinicians where they routinely work blind — the transfers, the out-of-hours gaps, the boundary between health and social care. Distinguish places where the data does not flow at all from places where it flows but cannot be trusted, because these need different fixes. Consider which populations are most affected, since fragmentation tends to fall hardest on people with the most complex needs. The answer tells you where to start, and gives you a clinical-safety case that will carry more weight than any technical argument.

2. **How exposed are we to vendor lock-in, and what would it actually cost us to switch our main clinical systems?** Many organizations discover the true price of a closed system only when they try to leave it. Work through, concretely, what it would take to extract your data in a usable, standard form and move to another supplier. Examine your contracts for who owns the data, what standard interfaces exist, and whether you are charged for integrations that ought to be routine. Identify the proprietary interfaces and data formats that would have to be unpicked. Weigh this against the openness of alternatives and national platforms you could reuse instead. This is not about churning suppliers; it is about understanding your leverage and reducing the risk that a single vendor's roadmap becomes your only option.

3. **Is our data good enough to share safely, and how would we know?** Sharing poor data does not just embarrass you — it propagates errors into other clinicians' decisions. Ask whether you actually measure the completeness, accuracy, timeliness, and coding consistency of the data you intend to expose. Discuss who owns data quality in your organization and whether they have the time and mandate to fix problems at source. Consider what proportion of records carry a verified NHS Number and how much clinically important information still sits in free text rather than coded fields. Think about how you would detect a systematic coding error before it reached a shared care record. If you cannot answer these questions with evidence, treat that as a finding in itself, and fund the data-quality work before you widen the pipe.

4. **When a supplier says "we support FHIR", how would we actually verify it before go-live?** A standards label is a marketing claim until it is tested against a specific implementation guide. Discuss whether your organization has any conformance-testing capability of its own, or whether you simply take suppliers at their word. Two systems can each be "FHIR-compliant" and still be unable to exchange a usable message, because the standard is deliberately flexible and the meaning lives in the profiles and value sets that pin it down. Ask what national implementation guides and IHE profiles apply to the interface in question, and who on your side is competent to read them. Consider whether conformance is written into the contract as a condition of connecting, or discovered painfully during integration. An honest answer names the specific profile you would test against, the person or function that would run the test, and the point in the timeline where a failing supplier is turned away rather than waved through.

5. **Who owns standards, terminology and conformance across our organization, and do they have the mandate to say no?** Interoperability decays without stewardship: value sets drift, local guides diverge, and each new project quietly invents its own interpretation. Ask whether there is a named function responsible for standards, SNOMED CT and dm+d subsets, and conformance, or whether this knowledge sits in a few individuals' heads. Consider the tension between central consistency and local delivery speed — teams under pressure will build the quickest thing unless a standards function has real authority to require reuse. Discuss how terminology maintenance is funded, given that it is unglamorous, continuous, and benefits everyone rather than any single project. Look at how you keep implementations aligned as FHIR, SNOMED CT and national guides evolve, rather than freezing at the version you first adopted. An honest answer identifies the accountable owner, their funding, and a recent example where they either enforced a standard or failed to.

6. **Are the people whose records we are joining up informed and content with how their data flows?** Interoperability is not only a technical and clinical matter but a question of public trust and lawful basis. People reasonably assume the NHS already shares their information sensibly, and are dismayed both when it does not and when it does so in ways they did not expect. Discuss whether patients understand which organizations can see their shared record, how a National Data Opt-Out or local consent model is honoured across the flow, and how access is recorded and auditable. Consider the equity dimension: the people whose data is most fragmented — those with complex needs — are also those least able to navigate opt-outs and information notices. Bring information governance and, where relevant, patients or their representatives into the design rather than treating consent as a box ticked at the end. An honest answer can describe the lawful basis for each flow, how a person would find out who has seen their record, and how their choices are respected end to end.

## In practice: a health & care example

An integrated care system in the north of England sets out to give clinicians a single view of shared medications across general practice, hospital, and community pharmacy, after a serious incident review found that a patient had been prescribed two interacting drugs by teams that could not see each other's records.

The temptation is to buy a "medicines dashboard" from one supplier and wire it directly into each system's database. The interoperability lead resists this. Instead the programme adopts a build-to-open-standards approach. Each source system exposes medication data as HL7 FHIR resources; every medicine is coded using the dm+d so that "the same drug" means the same thing everywhere; and every record is keyed on a verified NHS Number so that the right medications attach to the right person. GP data is drawn through GP Connect rather than a bespoke feed, reusing a national capability instead of inventing a local one.

Early data profiling proves its worth immediately. One practice's system has been recording certain medicines in free text rather than as coded dm+d entries, meaning they would have been invisible to any automated interaction check. This is fixed at source before go-live. The team also finds a cluster of records with unverified NHS Numbers and routes them through the national demographic service for matching.

The clinical safety officer and information governance lead are part of the design group throughout. Together they define exactly which data is shared, with whom, under what lawful basis, and how a clinician's access is recorded — the concerns of Chapter 1.7 — Information Governance, Data Protection & Cyber Security. Suppliers must pass conformance testing against the national FHIR implementation guide before connecting. Twelve months on, the joined-up medication view is live, an interaction that would previously have been missed has already been caught, and — because everything was built to open interfaces — a second use case, shared allergy information, reuses most of the same plumbing at a fraction of the original cost.

## Sector lenses

### Startup

A digital health startup lives or dies by how easily it plugs into existing systems, so treat interoperability as a core feature, not a compliance chore. Building FHIR APIs and using SNOMED CT and dm+d from the outset makes you far easier to buy and integrate, and signals maturity to cautious NHS buyers. Resist the urge to invent your own data model when a standard exists; your differentiation should be your product, not a proprietary format that becomes a liability. Getting the NHS Number handling and information governance right early is what lets you move from pilot to procurement. Design so that a customer could, in principle, extract their data and leave — paradoxically, that openness is what earns the trust to keep them.

### Small business

An established small provider — a GP practice, a community pharmacy, a care home, or a single-site clinic — carries the same duties to share data safely as the largest trust, but with a fraction of the technical capability. Here interoperability is mostly a procurement and configuration discipline rather than an engineering one: choose systems that already speak FHIR, connect to national services such as GP Connect and the Spine, and code with SNOMED CT and dm+d out of the box, so you inherit standards instead of building them. Make verified NHS Number capture part of everyday practice, because with no integration team to reconcile mismatches later, getting the identifier right at the point of registration is your cheapest safeguard. Lean on shared care record programmes and your integrated care system's shared infrastructure rather than commissioning bespoke links you cannot maintain. When you sign or renew a system contract, insist on data-extraction rights and open interfaces in plain terms, because a small organization feels vendor lock-in most acutely and has the least leverage to escape it after the fact.

### Enterprise

A large provider or supplier typically carries decades of legacy: HL7 v2 interfaces, multiple electronic record systems, and integration engines holding it all together. The realistic strategy is not to rip everything out but to put an API-first, standards-based layer in front of the estate, migrating flows to FHIR incrementally while keeping v2 running where it must. Guard hard against lock-in in every renewal, and insist on conformance testing so that "standards-compliant" is verified rather than asserted. Establish an internal standards and conformance function so that individual projects do not each invent their own interpretation. This is closely related to how you manage core operational platforms in Chapter 5.4 — Enterprise Resource Planning (ERP), where the same reuse-and-open-interface discipline applies.

### Government

National and regional bodies set the rules of the market, so their choices about standards ripple across every organization. The most valuable thing government can do is mandate open standards, publish clear implementation guides and conformance requirements, and provide reusable national platforms — the Spine, GP Connect, shared care record frameworks, the NHS Number service — so that local organizations build once and reuse. Consistency matters more than perfection: a firmly-enforced good-enough standard beats a theoretically superior one that everyone implements differently. Government must also fund the unglamorous work of terminology maintenance and data-quality improvement, because these are public goods that no single organization will finance alone. This stewardship role connects to Chapter 9.1 — Working with Local & National Governments and to how partners collaborate in Chapter 9.0 — Collaborating with Partner Organizations.

## Common failure modes

- **Confusing technical connection with semantic understanding.** Declaring victory when a message flows, without confirming that both sides interpret its codes, units, and negations identically. The result is data that looks integrated but is quietly misread.
- **Sharing poor data faster.** Widening the pipe before fixing data quality, so that coding errors, free text, and missing NHS Numbers propagate into other clinicians' decisions and every downstream analysis.
- **"We support FHIR" as an empty claim.** Accepting a standards label without conformance testing against a specific implementation guide, so that two "compliant" systems still cannot talk to each other.
- **Bespoke point-to-point integrations.** Building direct links between each pair of systems, producing a brittle web that becomes exponentially harder and more expensive to maintain as it grows.
- **Locking in by default.** Signing contracts with proprietary interfaces and no data-extraction rights, only discovering the cost of the trap when you try to change supplier.
- **Treating governance as a final gate.** Bringing clinical safety and information governance in only to sign off, so problems surface late and expensively, or are waved through under delivery pressure.
- **Standards without stewardship.** Adopting terminologies and profiles but funding no one to maintain value sets, monitor conformance, or keep implementations aligned as standards evolve.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| Standards adoption | Ad hoc, mostly proprietary or hand-rolled interfaces | HL7 v2 and some FHIR in use; choices vary by project | FHIR, SNOMED CT and dm+d adopted as default with local guides | Conformance to national guides tracked and reported; deviations governed and assured | Full conformance to national implementation guides and IHE profiles, verified by testing |
| Identifier & linkage | NHS Number often missing or unverified | Captured but not consistently verified | Verified against national service on most records | Verification rates measured against targets, with unmatched records actively worked | Verified everywhere; matching quality actively monitored |
| Data quality | Unmeasured; free text common where coding is needed | Measured in places; fixes reactive | Profiled, owned, and improved at source | Quality metrics tracked against thresholds, with stewardship held to account | Continuous monitoring with automated defect detection before data is shared |
| Architecture | Point-to-point, tightly coupled | Integration engine, mixed coupling | API-first, reusing national platforms | API performance and dependencies monitored; changes governed through versioning and testing | Loosely coupled, standards-based, components replaceable without rework |
| Lock-in & procurement | Proprietary contracts, no exit rights | Some standards clauses, weakly enforced | Open standards and data-extraction rights required | Contract compliance and exit readiness reviewed and assured across the portfolio | Open interfaces mandatory and verified; genuine supplier substitutability |

## Checklist

- [ ] Every relevant record and interface carries a verified NHS Number, with a process to resolve missing or unmatched ones.
- [ ] New interfaces use HL7 FHIR and named national implementation guides, with HL7 v2 retained only where migration is not yet justified.
- [ ] Clinical content is coded using SNOMED CT, and medicines using dm+d, against agreed value sets.
- [ ] Data quality for anything you intend to share is profiled, measured, owned, and improved at source before the pipe is widened.
- [ ] Suppliers must pass conformance testing against a specific profile before connecting — "supports FHIR" is never accepted on its own.
- [ ] National platforms (Spine, GP Connect, shared care records) are reused before any bespoke integration is built.
- [ ] Contracts mandate open, documented APIs, data-extraction rights in a standard format, and no charges for standard integrations.
- [ ] Clinical safety and information governance leads are in the design group from the start, not just at sign-off.
- [ ] Architecture is API-first and loosely coupled, so a component can be replaced without rebuilding everything around it.
- [ ] A named function owns standards, conformance, and terminology maintenance across the organization.

## Key sources

- NHS England — interoperability standards, the Spine, GP Connect, and shared care record programmes.
- HL7 International — the FHIR standard and HL7 v2 specifications.
- SNOMED International — SNOMED CT terminology and implementation guidance.
- NHS Business Services Authority — the Dictionary of medicines and devices (dm+d).
- Integrating the Healthcare Enterprise (IHE) — interoperability profiles.
- openEHR International — open specifications for structuring the health record.
- World Health Organization — the International Classification of Diseases (ICD-10 and ICD-11).

## References

1. Interoperability — Wikipedia — https://en.wikipedia.org/wiki/Interoperability
2. Semantic interoperability — Wikipedia — https://en.wikipedia.org/wiki/Semantic_interoperability
3. Health Level 7 — Wikipedia — https://en.wikipedia.org/wiki/Health_Level_7
4. Fast Healthcare Interoperability Resources — Wikipedia — https://en.wikipedia.org/wiki/Fast_Healthcare_Interoperability_Resources
5. SNOMED CT — Wikipedia — https://en.wikipedia.org/wiki/SNOMED_CT
6. ICD-11 — Wikipedia — https://en.wikipedia.org/wiki/ICD-11
7. ICD-10 — Wikipedia — https://en.wikipedia.org/wiki/ICD-10
8. openEHR — Wikipedia — https://en.wikipedia.org/wiki/OpenEHR
9. NHS number — Wikipedia — https://en.wikipedia.org/wiki/NHS_number
10. Integrating the Healthcare Enterprise — Wikipedia — https://en.wikipedia.org/wiki/Integrating_the_Healthcare_Enterprise
11. Open standard — Wikipedia — https://en.wikipedia.org/wiki/Open_standard
12. Vendor lock-in — Wikipedia — https://en.wikipedia.org/wiki/Vendor_lock-in
13. API — Wikipedia — https://en.wikipedia.org/wiki/API
14. Data quality — Wikipedia — https://en.wikipedia.org/wiki/Data_quality
15. FHIR standard — HL7 International — https://www.hl7.org/fhir/
16. SNOMED CT — SNOMED International — https://www.snomed.org/
17. Dictionary of medicines and devices (dm+d) — NHS Business Services Authority — https://www.nhsbsa.nhs.uk/pharmacies-gp-practices-and-appliance-contractors/dictionary-medicines-and-devices-dmd
18. GP Connect — NHS England Digital — https://digital.nhs.uk/services/gp-connect
19. Spine — NHS England Digital — https://digital.nhs.uk/services/spine
20. International Classification of Diseases (ICD) — World Health Organization — https://www.who.int/standards/classifications/classification-of-diseases
