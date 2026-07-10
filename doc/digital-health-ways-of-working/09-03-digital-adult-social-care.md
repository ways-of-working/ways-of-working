# Chapter 9.3 — Digital in Adult Social Care

**Adult social care is not "NHS-lite": it is a fragmented, means-tested, provider-led market with its own workforce, funding, and information realities, and delivering digital well there means designing for those realities rather than importing acute-hospital assumptions.**

## Why this matters in health and care

Adult social care in England supports around a million people at any one time — older people, disabled adults, people with learning disabilities, people with mental ill health — to live with dignity, safety, and as much independence as possible. It is delivered not by a single national organisation but by roughly 18,000 independent, voluntary, and public providers running care homes and domiciliary ("home care") services, commissioned by 150-odd local authorities and paid for by a mix of means-tested public funding and self-funders. This is a different shape of system from the NHS, and digital ways of working that ignore the difference tend to fail.

The stakes are high and specific. Social care records describe the most intimate details of a person's life — continence, capacity, finances, relationships, risk of abuse — held often by small organisations with thin governance and, historically, low digital maturity. Care is delivered by a workforce of around 1.5 million people, much of it low-paid, high-turnover, and digitally under-supported, using their own phones or none at all. When you get digital right here, you reduce medication errors, speed hospital discharge, spot deterioration earlier, and give overstretched carers time back. When you get it wrong, you create data breaches, safeguarding failures, and exclusion of the very people least able to advocate for themselves. How you work is a safety, equity, and public-trust issue, not merely an efficiency one.

## Core concepts

**Adult social care** in England is governed principally by the [Care Act 2014](https://en.wikipedia.org/wiki/Care_Act_2014), which places statutory duties on local authorities to assess needs, promote wellbeing, and safeguard adults at risk. Quality is regulated by the [Care Quality Commission (CQC)](https://en.wikipedia.org/wiki/Care_Quality_Commission), which inspects and rates providers. Unlike NHS care, most publicly funded social care is subject to a financial [means test](https://en.wikipedia.org/wiki/Means_test): people above a capital threshold pay for their own care ("self-funders"), which shapes who commissions what and where the money flows.

The provider market is dominated by thousands of small independent businesses and [voluntary sector](https://en.wikipedia.org/wiki/Voluntary_sector) organisations, alongside some large national chains. This fragmentation is the single most important fact for anyone planning digital delivery: there is no single system to log into, no national roll-out lever, and no shared IT department.

A **digital social care record (DSCR)** is the sector's equivalent of an [electronic health record](https://en.wikipedia.org/wiki/Electronic_health_record), replacing the paper care plans and handover notes that still dominate many services. Assuring these records against a national standard, and connecting them to health, requires [interoperability](https://en.wikipedia.org/wiki/Interoperability) — the ability of systems to exchange and use each other's data.

**Technology-enabled care (TEC)** covers [telecare](https://en.wikipedia.org/wiki/Telecare) (alarms and sensors that summon help), [telehealth](https://en.wikipedia.org/wiki/Telehealth) (remote monitoring of health conditions), and broader [assistive technology](https://en.wikipedia.org/wiki/Assistive_technology). Much legacy telecare depends on the analogue [public switched telephone network (PSTN)](https://en.wikipedia.org/wiki/Public_switched_telephone_network), which is being retired in favour of digital telephony — a change with direct safety implications for alarm users.

Two further concepts run through the whole chapter. [Co-production (approach)](https://en.wikipedia.org/wiki/Co-production_(approach)) means designing services *with* people who draw on care and unpaid carers, not merely *for* them. And [safeguarding](https://en.wikipedia.org/wiki/Safeguarding) — protecting adults at risk of abuse or neglect — is a statutory duty that digital systems must actively support, never undermine.

## Best practices

1. **Start from the provider's reality, not the NHS template.** A domiciliary care worker moving between homes on foot with a five-year-old phone, a care-home nurse on a night shift, and a self-funding family choosing a service all operate very differently from a hospital ward. Do your discovery in real settings, watch a shift, and design for intermittent connectivity, shared devices, and low prior digital confidence. Solutions ported directly from acute NHS contexts — heavy clinical systems, single-sign-on estates, dedicated IT support — routinely collapse in the social care market because none of those preconditions hold.

2. **Treat the fragmented market as the delivery problem, not a footnote.** You cannot mandate change across 18,000 independent businesses; you have to make adoption attractive, affordable, and low-risk for each one. Use the national assured-solutions route so providers choose from suppliers that already meet a defined standard, and lean on local authorities, integrated care systems, and Care Provider Associations to broker, fund, and support at the local level (see Chapter 9.0 — Collaborating with Partner Organisations). Plan for a long tail of small providers who will move last and need the most hand-holding.

3. **Adopt digital social care records to a national standard, and fund the change, not just the software.** DSCRs cut duplicate recording, make information legible at handover, and support safer medication administration. But a licence is the cheap part: the cost and risk sit in data migration from paper, device provision, connectivity, and the weeks of frontline support needed before staff trust the system. Budget for change management and floor-walking (see Chapter 8.1 — Change Management), and measure adoption by real use at the point of care, not by contracts signed.

4. **Use the assured-supplier / assured-solutions approach to de-risk procurement.** Small providers cannot each run a rigorous supplier evaluation covering clinical safety, cyber security, and data protection. National assurance — where solutions are checked against standards before they reach the market — lets a care home make a safe choice from a shortlist rather than a cold procurement. Point providers to the assured list, and where you commission at scale, make assurance a contractual expectation rather than an afterthought (see Chapter 6.3 — Procurement & Commercial).

5. **Plan the PSTN-to-digital telecare switchover as a safety programme.** Millions of telecare alarms rely on the analogue phone network that is being switched off; a device that silently stops working is a life-safety risk for a person who has fallen. Maintain a register of telecare users, coordinate with telecoms providers and the local authority, prioritise vulnerable users for supported migration, and test end-to-end that an alarm still reaches a monitoring centre after the line changes. Never assume the switch is "just a telecoms upgrade" that will look after itself.

6. **Design information sharing around the person, and make it two-way with health.** The value of a shared care record is realised at the interfaces: a care home that can see a resident's medications, or a hospital discharge team that can see a person's home-care package. Connect DSCRs to shared care records and use recognised standards so data flows both ways (see Chapter 4.2 — Interoperability & Data Standards). Sharing must be lawful, proportionate, and explainable to the person, with a clear basis under data protection law and honest conversations about consent.

7. **Co-produce with people who draw on care and unpaid carers.** The people who use telecare, care planning, and family portals know where they fail in ways no procurement scorecard captures. Involve them and their unpaid carers from discovery through to live running, pay for their time, and reflect diverse needs — cognitive impairment, sensory loss, digital exclusion, English as an additional language. Co-production is both an ethical duty under the Care Act's wellbeing principle and the most reliable way to avoid building the wrong thing (see Chapter 1.9 — Digital Inclusion & Accessibility).

8. **Raise the cyber-security and data-protection floor in small providers.** A single care home may hold thousands of highly sensitive records with no dedicated IT and a manager who has never heard of multi-factor authentication. Offer practical, proportionate support — the national Data Security and Protection Toolkit, Cyber Essentials, template policies, and named help — rather than compliance paperwork that gets copied without understanding. Assume that ransomware and phishing will target the weakest link, and make good hygiene the path of least resistance.

9. **Build workforce digital capability as core, not optional.** A large part of the social care workforce has had little employer investment in digital skills, and turnover means training is never "done." Bake basic digital confidence into induction, provide role-relevant support in the flow of work, and identify digital champions on the floor (see Chapter 7.4 — Digital Skills & Capability Building). Capability is what turns a purchased system into daily practice; without it, adoption stalls and the investment is wasted.

10. **Make safeguarding an explicit design requirement.** Digital systems can strengthen safeguarding — flagging risks, evidencing concerns, speeding referrals — or weaken it, if surveillance-style monitoring erodes dignity or if access controls leak sensitive information. Design so that recording a safeguarding concern is easy, access is appropriately restricted, and the person's rights and voice are respected. Test explicitly for coercion, controlling family access, and the risk that "monitoring" tips into intrusion.

## Questions to discuss with your team

1. **Where are we unconsciously treating social care as "NHS-lite," and what would we do differently if we designed for the care market on its own terms?** This question forces the team to surface imported assumptions — that there is central IT, salaried digitally-confident staff, a single accountable body, or a mandate to roll out. In social care almost none of that holds, so a plan built on NHS reflexes will quietly fail. Debate concrete examples: are you assuming providers can absorb a procurement, spare staff for training, or run their own information governance? A good, honest answer names the specific NHS-shaped assumptions in your current plan, distinguishes what genuinely transfers from what does not, and reshapes ownership, funding, and support around a fragmented provider market rather than a single organisation.

2. **How will we support the long tail of small and voluntary providers who move last and need the most help, without either abandoning them or forcing a pace they cannot manage?** Averages hide the problem: national adoption figures can look healthy while the smallest, least-resourced providers — often serving the most marginalised people — remain on paper. The tension is between momentum and inclusion, and between standardising (efficient, but blunt) and tailoring support locally (effective, but costly). Consider who funds and delivers the hand-holding — local authority teams, Care Provider Associations, peer champions — and what "good enough" looks like for a six-bed home versus a national chain. A strong answer sets a realistic trajectory, names who owns support for the hardest-to-reach, and defines success as real use at the front line rather than licences sold or a headline percentage.

3. **How do we share information between health and social care in a way that is genuinely safe, lawful, and trusted by the people it describes?** Interoperability is usually framed as a technical challenge, but in social care the harder questions are ethical and relational: this is data about capacity, finances, abuse, and intimate care, held by many small organisations. Debate the lawful basis for sharing, when consent is meaningful versus when it is a tick-box, and how you explain sharing to someone with fluctuating capacity or an unpaid carer acting on their behalf. Weigh the safety benefit of a hospital seeing a care plan against the harm of over-broad access or a breach at a poorly defended provider. A good answer pairs the technical standards with a clear, person-centred information-governance story, proportionate access controls, and a plain-English account you would be comfortable giving to the person themselves.

## In practice: a health & care example

An integrated care system in the East Midlands sets out to lift digital maturity across adult social care. Baseline data shows that of 320 CQC-registered providers in its footprint, fewer than half use any digital care record; the rest run on paper, and a cluster of small domiciliary agencies have no shared devices at all. The system's digital team resists the temptation to run a single procurement and mandate one product. Instead, working with the two upper-tier local authorities and the local Care Association, they stand up a small support team and point providers to the nationally assured DSCR suppliers, so each provider chooses a solution that already meets clinical-safety, cyber, and data-protection standards.

Funding is routed to providers as grants that cover not just licences but devices, connectivity, and, critically, the staff time to migrate paper records and train teams. The support team offers floor-walking during go-live, template information-sharing agreements, and help completing the Data Security and Protection Toolkit. A local care-home manager, initially sceptical, adopts a DSCR after a peer champion from a neighbouring home shows how it cut two hours of nightly paperwork and made the morning handover legible. Within a year, medication administration errors flagged in the home fall, and the ambulance service reports faster, better-informed responses because paramedics can see current care plans.

In parallel, the system runs the PSTN switchover as a distinct safety programme. It builds a register of roughly 9,000 telecare users across the two authorities, coordinates with telecoms providers, prioritises people living alone with a history of falls, and tests that each migrated alarm still reaches the monitoring centre. Two "silent failure" cases — alarms that appeared connected but could not raise a call — are caught in testing rather than in an emergency. Throughout, an involvement group of people who draw on care and unpaid carers reviews the family portal and the telecare messaging; their feedback reshapes the consent wording and adds a large-text mode. The programme is judged a success not because every provider is digital, but because adoption is real at the front line, the most vulnerable were prioritised, and no one was left behind by the telephone switch-off.

## Three sector lenses

### Startup
A small health-tech company selling into social care faces a market of thousands of tiny buyers with little cash, low digital confidence, and no procurement capacity — the opposite of a single enterprise sale. Getting onto the national assured-solutions list is often the difference between a viable business and a stalled one, because assurance is what lets a wary care-home manager trust you. Design for shared, cheap devices and patchy connectivity, price for organisations running on thin margins, and invest in onboarding and support, because your churn will track your customers' staff turnover. Resist the urge to bolt on features for large chains at the expense of the small providers who are most of the market.

### Enterprise
A large care provider or an NHS trust integrating with social care has scale advantages — an IT function, buying power, the ability to standardise — but also legacy estates and the risk of imposing acute-shaped systems on care settings. An enterprise should use its weight to negotiate assured suppliers, fund proper change management, and drive interoperability with shared care records, while genuinely co-producing with frontline staff and the people they support. The failure mode is a top-down roll-out that treats domiciliary and residential care as junior versions of hospital wards. Scale should buy better support and standards, not a heavier system nobody at the front line can use.

### Government
National and local government set the conditions for the whole market: the Digitising Social Care programme, DSCR and cyber standards, funding routes, and the assurance regime that de-risks provider choices. Their lever is not mandate but enablement — funding, standards, assurance, and support brokered through local authorities and integrated care systems (see Chapter 9.1 — Working with Local & National Governments). They also carry the statutory duties under the Care Act and must ensure equity, safeguarding, and the PSTN switchover are handled so that no vulnerable person is harmed. The hardest task is designing incentives that move a fragmented market without excluding its smallest, least-resourced members.

## Common failure modes

- **NHS-lite thinking.** Assuming central IT, salaried digital-confident staff, and a roll-out mandate that do not exist in the care market, then blaming providers when the plan fails.
- **Buying software, not change.** Funding licences but not the device provision, data migration, connectivity, and floor-level support that actually drive adoption.
- **Averages that hide the tail.** Celebrating headline adoption figures while the smallest, most marginalised providers stay on paper and the people they serve are excluded.
- **PSTN complacency.** Treating the analogue switch-off as a telecoms matter and discovering silent alarm failures only in an emergency.
- **Information-governance theatre.** Copying template policies and toolkit answers without understanding, leaving small providers genuinely exposed to ransomware and breaches.
- **Consultation instead of co-production.** Showing people who draw on care a finished design and asking for approval, rather than building with them and their unpaid carers from the start.
- **Surveillance creep.** Framing intrusive monitoring as "safety" and eroding the dignity, autonomy, and rights the Care Act exists to protect.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Care records | Paper care plans and handover notes | Some providers piloting digital records | Assured DSCRs standard across most providers | DSCRs connected two-way to shared care records; data drives quality improvement |
| Market support | No coordinated support; providers left to fend for themselves | Ad hoc help from local authority | Funded, coordinated support via LA/ICS and Care Association | Sustained capability, peer champions, and a healthy assured-supplier market |
| Information sharing | Fax, phone, and paper between health and care | One-way visibility in limited cases | Standards-based sharing with clear governance | Person-centred, consented, two-way flows at every interface |
| Telecare / TEC | Analogue devices, no register | Register started, migration planned | PSTN switchover managed as a safety programme | Digital TEC proactively preventing crises and admissions |
| Workforce & cyber | Low digital confidence; minimal cyber hygiene | Basic training; toolkit begun | Digital skills in induction; DSPT and Cyber Essentials met | Continuous capability building; strong, tested security culture |

## Checklist

- [ ] We have based our plan on real care settings — domiciliary and residential — not an NHS or acute template.
- [ ] We are steering providers to nationally assured DSCR and TEC suppliers to de-risk their choices.
- [ ] Funding covers change — devices, connectivity, data migration, and frontline support — not just software licences.
- [ ] We have a named owner and a realistic trajectory for supporting the long tail of small and voluntary providers.
- [ ] A current register of telecare users exists and the PSTN switchover is run as a safety programme with end-to-end testing.
- [ ] Information sharing with health is lawful, proportionate, standards-based, and explainable to the person it describes.
- [ ] People who draw on care and unpaid carers are co-producing the service and are paid for their time.
- [ ] Small providers have practical support to meet the Data Security and Protection Toolkit and basic cyber hygiene.
- [ ] Digital skills are built into induction and supported in the flow of work, allowing for high turnover.
- [ ] Safeguarding is an explicit design requirement, with appropriate access controls and protection against surveillance creep.
- [ ] We measure success by real use at the point of care and by whether the most vulnerable were prioritised.

## Key sources

- Care Act 2014 and the statutory wellbeing and safeguarding duties — Department of Health & Social Care / GOV.UK.
- Digitising Social Care programme and the assured-solutions / assured-supplier approach — NHS England.
- Digital Social Care Records (DSCR) standard and adoption guidance — NHS England / former NHSX.
- Data Security and Protection Toolkit (DSPT) for social care providers — NHS England.
- CQC single assessment framework and provider quality regulation — Care Quality Commission.
- PSTN switch-off / analogue-to-digital telecare guidance — TSA (the TEC Services Association) and DHSC.
- Skills for Care workforce data and the adult social care digital skills / capability resources.
- Social Care Institute for Excellence (SCIE) guidance on co-production and strengths-based practice.

## References

1. Care Act 2014 — Wikipedia — https://en.wikipedia.org/wiki/Care_Act_2014
2. Care Quality Commission — Wikipedia — https://en.wikipedia.org/wiki/Care_Quality_Commission
3. Means test — Wikipedia — https://en.wikipedia.org/wiki/Means_test
4. Voluntary sector — Wikipedia — https://en.wikipedia.org/wiki/Voluntary_sector
5. Electronic health record — Wikipedia — https://en.wikipedia.org/wiki/Electronic_health_record
6. Interoperability — Wikipedia — https://en.wikipedia.org/wiki/Interoperability
7. Telecare — Wikipedia — https://en.wikipedia.org/wiki/Telecare
8. Telehealth — Wikipedia — https://en.wikipedia.org/wiki/Telehealth
9. Assistive technology — Wikipedia — https://en.wikipedia.org/wiki/Assistive_technology
10. Public switched telephone network — Wikipedia — https://en.wikipedia.org/wiki/Public_switched_telephone_network
11. Co-production (approach) — Wikipedia — https://en.wikipedia.org/wiki/Co-production_(approach)
12. Safeguarding — Wikipedia — https://en.wikipedia.org/wiki/Safeguarding
13. General Data Protection Regulation — Wikipedia — https://en.wikipedia.org/wiki/General_Data_Protection_Regulation
14. Care Act 2014 — legislation and statutory guidance — GOV.UK / Department of Health & Social Care — https://www.gov.uk/government/publications/care-act-statutory-guidance
15. Digitising Social Care and Assured Solutions — NHS England — https://www.digitalsocialcare.co.uk/
16. Data Security and Protection Toolkit — NHS England — https://www.dsptoolkit.nhs.uk/
17. The state of the adult social care sector and workforce in England — Skills for Care — https://www.skillsforcare.org.uk/
18. Co-production and strengths-based approaches — Social Care Institute for Excellence (SCIE) — https://www.scie.org.uk/
