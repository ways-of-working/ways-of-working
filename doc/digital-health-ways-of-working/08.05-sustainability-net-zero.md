# Chapter 8.5 — Sustainability & Net Zero

**In health and care, cutting carbon is not a corporate-responsibility side-project bolted onto delivery — it is a clinical, ethical, and financial dimension of every digital service you build, buy, and run.**

## Why this matters in health and care

Climate change is a health emergency, not an abstract environmental concern. Heatwaves, floods, air pollution, shifting patterns of infectious disease, and disrupted food and water systems all land, eventually, in your clinics, ambulances, and waiting lists. The [effects of climate change on human health](https://en.wikipedia.org/wiki/Effects_of_climate_change_on_human_health) fall hardest on the same populations who already carry the heaviest burden of illness and the least access to services — so sustainability sits alongside the equity and inclusion concerns you met in Chapter 1.9 — Digital Inclusion & Accessibility.

The National Health Service (NHS) is a large emitter in its own right. It accounts for a substantial share of England's carbon footprint and a large slice of public-sector emissions, which means the way it delivers care is materially part of the problem or part of the solution. In October 2020 the NHS became the first national health service in the world to commit formally to reaching [net zero](https://en.wikipedia.org/wiki/Net-zero_emissions), through the Greener NHS programme and its report *Delivering a Net Zero National Health Service*.

Digital leaders sit at a pivotal point. Technology can strip enormous carbon out of the wider system — through virtual care, reduced travel, and paperlight working — while quietly generating its own footprint through data centres, cloud services, devices, and electronic waste. If you do not measure and manage both sides of that ledger, you risk congratulating yourself on savings you have merely moved somewhere less visible. Treating sustainability as a first-class delivery concern, with the same rigour you apply to clinical safety (Chapter 1.6) and information governance (Chapter 1.7), is how you keep that honest.

## Core concepts

**Net zero and the two NHS targets.** [Net-zero emissions](https://en.wikipedia.org/wiki/Net-zero_emissions) means balancing the greenhouse gases you emit with an equivalent amount removed, so your net contribution to warming is nil. The NHS sets two distinct goals. The **NHS Carbon Footprint** covers emissions the NHS controls directly — its own estate, fleet, and energy — with an ambition to reach net zero by 2040, and an interim milestone of an roughly 80% reduction in the late 2020s to early 2030s. The **NHS Carbon Footprint Plus** is wider, adding emissions the NHS can influence but not directly control, most importantly its supply chain and procured goods; the ambition there is net zero by 2045, with an 80% reduction milestone later in the 2030s. Treat the dates as directional ambitions rather than precise contractual deadlines, and check current Greener NHS guidance for the exact figures.

**Emission scopes.** Standardised carbon accounting, most commonly the [GHG Protocol Corporate Standard](https://en.wikipedia.org/wiki/GHG_Protocol_Corporate_Standard), divides emissions into three scopes. Scope 1 is direct emissions from sources you own or control. Scope 2 is indirect emissions from the electricity, heat, and cooling you buy. Scope 3 is everything else in your value chain — suppliers, cloud providers, staff travel, procured devices, and the disposal of what you throw away. For digital services, Scope 3 usually dominates, which is why procurement and supplier behaviour matter so much.

**Carbon footprint.** A [carbon footprint](https://en.wikipedia.org/wiki/Carbon_footprint) is the total greenhouse gas load attributable to an activity, product, or organisation, usually expressed in tonnes of carbon-dioxide equivalent. For a digital service, the footprint spans the manufacture and disposal of hardware, the energy consumed running it, and the network and [data center](https://en.wikipedia.org/wiki/Data_center) capacity behind it. Cloud does not make emissions disappear; it relocates them to a provider whose energy mix and efficiency you should still ask about.

**Green computing and sustainable ICT.** [Green computing](https://en.wikipedia.org/wiki/Green_computing) — sometimes called green software or sustainable information and communications technology (ICT) — is the practice of designing, running, and disposing of digital systems to minimise their environmental impact. It ranges from efficient code and right-sized infrastructure to renewable-powered hosting and hardware longevity.

**Electronic waste and circularity.** [Electronic waste](https://en.wikipedia.org/wiki/Electronic_waste), or e-waste, is discarded electrical and electronic equipment — laptops, tablets, phones, medical devices, servers. It is one of the fastest-growing waste streams globally and much of it is never properly recycled. A [circular economy](https://en.wikipedia.org/wiki/Circular_economy) approach — repairing, refurbishing, reusing, and recovering materials rather than defaulting to replacement — reduces both waste and the large embodied carbon locked up in manufacturing new devices.

**Sustainable and social-value procurement.** [Sustainable procurement](https://en.wikipedia.org/wiki/Sustainable_procurement) buys goods and services in a way that weighs environmental and social impact alongside price and quality across the whole life-cycle. In England, the [Public Services (Social Value) Act 2012](https://en.wikipedia.org/wiki/Public_Services_(Social_Value)_Act_2012) requires public bodies to consider economic, social, and environmental well-being when commissioning services, and NHS procurement policy now expects suppliers to publish carbon-reduction plans (see Chapter 6.3 — Procurement & Commercial).

**Greenwashing.** [Greenwashing](https://en.wikipedia.org/wiki/Greenwashing) is presenting something as more environmentally sound than it really is. In digital health it shows up as vague "carbon-neutral cloud" claims, unaudited offsets, or counting a saving twice. Naming and avoiding it is a matter of professional integrity.

## Best practices

1. **Measure before you claim, using recognised scopes.** You cannot manage what you have not counted. Establish a baseline for your digital estate across Scopes 1, 2, and 3 — energy for on-premises kit, cloud and hosting, staff devices, and the embodied carbon of hardware — using the GHG Protocol structure. Even a rough, well-documented estimate beats an eloquent claim with no numbers behind it, and it gives you something to improve against year on year.

2. **Make sustainability a stated criterion in every business case.** Fold carbon into the options appraisal alongside cost, benefit, and risk (see Chapter 6.0 — Financial Management & Business Cases). Ask each option "what is the carbon cost, and what is the carbon saving?" so the greener choice is visible rather than accidental. Where a lower-carbon option costs more up front, say so honestly and let decision-makers weigh it; do not bury the trade-off.

3. **Right-size and decarbonise your infrastructure.** Over-provisioned servers, idle test environments, and always-on workloads waste energy and money together. Turn off what you are not using, consolidate where you can, and prefer hosting regions and providers powered by renewable energy. Ask cloud suppliers for their power-usage effectiveness, their energy mix, and their own net-zero commitments — and treat evasive answers as a signal.

4. **Design services to cut system-wide carbon, not just IT carbon.** The biggest wins usually sit outside the data centre. Virtual appointments, remote monitoring, e-prescribing, and shared care records can remove millions of patient and staff miles and reams of paper. Design for these outcomes deliberately, and measure the travel and materials you displace so the saving is evidenced rather than assumed.

5. **Be honest about rebound effects.** Efficiency gains are often partly eaten by increased use — cheaper, easier virtual appointments can generate more appointments overall, and faster infrastructure invites heavier workloads. This rebound (or "Jevons") effect does not mean the intervention was wrong, but it does mean net savings are smaller than gross savings. Claim the net figure, and design demand-management and clinical-appropriateness rules so convenience does not quietly inflate consumption.

6. **Extend device life and design for a circular economy.** The embodied carbon in manufacturing a laptop or tablet typically dwarfs the energy it uses in service, so keeping devices in use longer is one of the highest-leverage things you can do. Set longer refresh cycles, repair rather than replace, buy refurbished where clinically safe, and route end-of-life kit to certified reuse and recycling — never landfill or informal export. Build these expectations into contracts with your hardware and managed-service suppliers.

7. **Weight procurement for social value and demand carbon-reduction plans.** Use the Social Value Act and NHS procurement policy to score suppliers on their environmental commitments, not just their price. Require credible, published carbon-reduction plans from significant suppliers, and check that a plan is a real trajectory with milestones rather than a glossy pledge. Since Scope 3 dominates the digital footprint, supplier behaviour is where most of your influence actually lies (see Chapter 6.3 — Procurement & Commercial and Chapter 9.0 — Collaborating with Partner Organisations).

8. **Report transparently and resist greenwashing.** Publish your emissions and your progress, including where you are behind. Be precise about offsets — say what is actually reduced versus what is compensated elsewhere, and prefer removing emissions to buying credits. Avoid double-counting savings that another organisation is also claiming, and never present an unaudited vendor slogan as your own achievement.

9. **Embed carbon into your metrics and governance.** Put a small number of sustainability measures into your organisational objectives and key results and your key performance indicators (see Chapter 10.0 — Objectives & Key Results (OKRs)), and review them in the same forums that review delivery and finance. Assign a named owner. Sustainability that lives only in an annual glossy report and never in an operational dashboard will not move.

## Questions to discuss with your team

1. **Where does the carbon in our digital services actually sit — and are we measuring it, or guessing?** This question forces you past comfortable assumptions. Most teams instinctively look at the data centre or the office lights, but for digital services the largest share is usually Scope 3: the embodied carbon of thousands of devices, the cloud capacity you rent, and the supply chain behind your software. The tension to debate is effort versus precision — a perfect carbon account is expensive and slow, while a rough one may mislead. A good, honest answer names your biggest emission sources with rough magnitudes, admits where the numbers are weak, and commits to improving the measurement over time rather than waiting for perfect data before acting. It also distinguishes what you control (your estate) from what you merely influence (your suppliers), because the tactics differ sharply between the two.

2. **When we claim a digital intervention saves carbon, are we counting the whole picture — including rebound and the footprint of the tech itself?** Virtual appointments are the classic example. It is easy to multiply avoided car journeys by an emission factor and declare victory, but the honest calculation subtracts the footprint of the devices, networks, and data centres that make the appointment possible, and adjusts for rebound — the extra appointments that happen precisely because the service is now easier to access. The trade-off to surface is optimism versus credibility: overstated savings feel good and win funding, but collapse under scrutiny and corrode trust. A good answer shows a net figure, states its assumptions plainly, and is comfortable saying the saving is real but smaller than the headline. It should also ask whether the intervention improves care and equity, not only carbon, because a greener service that widens the digital divide is not a win.

3. **How will we hold suppliers to account for their emissions without either greenwashing or excluding good small suppliers?** Because Scope 3 dominates, your leverage is largely through procurement — but this cuts two ways. Demand too little and you enable vague, unaudited claims; demand too much and you may lock out exactly the small, innovative digital-health suppliers the system needs, who lack the resources to produce elaborate carbon reports. The debate is about proportionality: what should you require of a two-person startup versus a hyperscale cloud provider? A good answer sets tiered, credible expectations — published carbon-reduction plans and evidence from large or high-impact suppliers, lighter proportionate commitments from small ones — and describes how you will verify claims rather than take them on faith. It should connect to your social-value scoring and to the collaboration practices in Chapter 9.0, treating suppliers as partners in reducing shared emissions rather than boxes to tick.

## In practice: a health & care example

An integrated care system (ICS) is rolling out a remote monitoring service for patients with heart failure across a largely rural region. The clinical case is strong: earlier detection of deterioration, fewer emergency admissions, and patients kept safely at home. The programme director, aware of the ICS Green Plan, insists sustainability is assessed from the start rather than retrofitted.

The team builds a simple carbon model. On the savings side, they estimate the patient and community-nurse miles displaced by monitoring at home instead of in clinic — significant in a rural area with long travel distances. On the cost side, they count the tablets and monitoring devices issued to patients, the cloud hosting for the platform, and the eventual disposal of the kit. Crucially, they apply a rebound adjustment: because the service surfaces problems earlier, some patients will now have appointments they would previously have gone without, so gross travel savings overstate the net figure. The honest net saving is still clearly positive, and now defensible.

Two design decisions follow directly. First, rather than issuing every patient a new tablet, the team sources refurbished devices and sets up a return-and-refurbish loop so kit is reissued rather than binned when a patient no longer needs it — cutting embodied carbon and cost together. Second, in the procurement for the monitoring platform, they score suppliers on published carbon-reduction plans and renewable hosting, applying the Social Value Act, while keeping the requirements proportionate so a promising small supplier is not excluded.

At the go-live review, the ICS reports the net carbon saving alongside the clinical and financial results, states its assumptions openly, and flags the device supply chain as its largest remaining Scope 3 exposure. No heroic claims, no buried trade-offs — a credible story that survives challenge from the finance committee and the local sustainability lead alike.

## Three sector lenses

### Startup

A small digital-health startup has little estate and few staff, so its own Scope 1 and 2 emissions are tiny — but its customers increasingly ask about sustainability, and NHS procurement will require a carbon-reduction plan. The pragmatic move is to get the basics credibly in place early: choose a renewable-powered cloud region, avoid over-provisioning, write architecturally efficient software, and produce an honest, proportionate carbon-reduction plan you can actually stand behind. Resist the temptation to buy cheap offsets and call yourself "carbon neutral" — buyers and regulators increasingly see through it, and a modest, truthful position ages far better than an inflated one. Sustainability done plainly can be a genuine differentiator when you sell into the NHS.

### Enterprise

A large NHS trust or health-tech firm has a sprawling estate, thousands of devices, legacy data centres, and a long supply chain, so its footprint is large and its Scope 3 dominant. The work is systematic: baseline emissions across all three scopes, publish a Green Plan with owners and milestones, rationalise and decarbonise infrastructure, extend device refresh cycles, and use procurement scale to demand carbon-reduction plans from suppliers. The hard part is governance — making sustainability a standing item alongside finance and delivery rather than a separate annual report, and resisting the internal pressure to claim savings that do not net out. Enterprises also have the leverage, through contract volume, to shift whole markets toward greener defaults.

### Government

A national body such as NHS England or the Department of Health and Social Care sets the ambition, the standards, and the accountability that everyone else operates within — the net-zero targets, the requirement for supplier carbon-reduction plans, and the reporting expectations. Its challenge is coherence and honesty at scale: setting targets that are stretching yet credible, avoiding the political temptation to overstate progress, and equipping local organisations with practical tools, emission factors, and guidance rather than mandates alone. Government also holds the biggest procurement lever in the country and can decarbonise supply chains faster through commercial policy than through exhortation. Consistency between national rhetoric and the funding and rules that reach the front line is what earns public trust.

## Common failure modes

- **Measuring only IT, ignoring the system.** Optimising your data centre while missing the millions of patient miles your service could displace means you count the small savings and miss the large ones.
- **Claiming gross savings and hiding rebound.** Headline figures that ignore increased usage and the footprint of the technology itself collapse under scrutiny and damage credibility.
- **Offsets as a fig leaf.** Buying cheap credits to declare "carbon neutral" while emissions keep rising is greenwashing, not decarbonisation.
- **Procurement that scores price only.** Ignoring the Social Value Act and supplier carbon means the dominant Scope 3 footprint goes unmanaged where you have the most leverage.
- **Device churn by default.** Short refresh cycles and landfill disposal waste the large embodied carbon of hardware and generate avoidable e-waste.
- **Sustainability as an annual report, not an operating metric.** Carbon that never appears on a live dashboard or in a governance forum does not change behaviour.
- **Perfection paralysis.** Waiting for a flawless carbon account before acting, when a rough baseline would let you start improving now.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Measurement | No carbon data; claims are anecdotal | Partial estimate of energy or IT only | Baseline across Scopes 1–3, reviewed annually | Live carbon data integrated with delivery and finance metrics |
| Design | Sustainability considered after go-live, if at all | Ad hoc green choices by individual teams | Carbon assessed in business cases and service design | Low-carbon and circular design is the default, with rebound accounted for |
| Procurement | Price-only scoring | Occasional social-value questions | Social Value Act applied; carbon-reduction plans required of key suppliers | Supplier decarbonisation actively managed and verified across the value chain |
| Devices & e-waste | Default refresh; landfill disposal | Some recycling in place | Extended life cycles and certified reuse/recycling | Circular-economy loops with reissue, repair, and material recovery |
| Governance | No owner; no reporting | Sustainability lead exists but is siloed | Named owner; targets in objectives; regular review | Transparent public reporting including shortfalls; board-level accountability |

## Checklist

- [ ] You have a documented carbon baseline for your digital estate across Scopes 1, 2, and 3, however rough.
- [ ] Sustainability is an explicit criterion in your business cases and options appraisals.
- [ ] Cloud and hosting choices consider energy mix, efficiency, and provider net-zero commitments.
- [ ] Carbon-saving claims for digital interventions state net figures and account for rebound and the technology's own footprint.
- [ ] Device refresh cycles are extended and end-of-life kit goes to certified reuse or recycling, not landfill.
- [ ] Procurement applies the Social Value Act and requires proportionate, credible carbon-reduction plans from significant suppliers.
- [ ] Supplier sustainability claims are verified, not taken on trust, and offsets are reported separately from real reductions.
- [ ] A small set of sustainability measures sits in your OKRs/KPIs with a named owner and regular review.
- [ ] Your public reporting is transparent about shortfalls as well as progress.
- [ ] Sustainability trade-offs are weighed alongside equity and digital-inclusion impacts, not against them.

## Key sources

- Greener NHS — *Delivering a Net Zero National Health Service*, NHS England — the founding strategy and the two-target framework.
- NHS Green Plan guidance, NHS England — expectations for local organisations, including ICS Green Plans.
- Public Services (Social Value) Act 2012 — statutory duty to consider social, economic, and environmental well-being in procurement.
- GHG Protocol Corporate Standard — the standard structure for Scope 1, 2, and 3 emissions accounting.
- NHS supplier carbon-reduction plan requirements (Procurement Policy Note on Carbon Reduction Plans) — supplier decarbonisation expectations in public procurement.
- Green Software Foundation — principles and practices for measuring and reducing software carbon.
- World Health Organization — guidance on climate change as a health threat and the co-benefits of greener care.

## References

1. Net-zero emissions — Wikipedia — https://en.wikipedia.org/wiki/Net-zero_emissions
2. Carbon footprint — Wikipedia — https://en.wikipedia.org/wiki/Carbon_footprint
3. GHG Protocol Corporate Standard — Wikipedia — https://en.wikipedia.org/wiki/GHG_Protocol_Corporate_Standard
4. Effects of climate change on human health — Wikipedia — https://en.wikipedia.org/wiki/Effects_of_climate_change_on_human_health
5. Green computing — Wikipedia — https://en.wikipedia.org/wiki/Green_computing
6. Data center — Wikipedia — https://en.wikipedia.org/wiki/Data_center
7. Electronic waste — Wikipedia — https://en.wikipedia.org/wiki/Electronic_waste
8. Circular economy — Wikipedia — https://en.wikipedia.org/wiki/Circular_economy
9. Sustainable procurement — Wikipedia — https://en.wikipedia.org/wiki/Sustainable_procurement
10. Public Services (Social Value) Act 2012 — Wikipedia — https://en.wikipedia.org/wiki/Public_Services_(Social_Value)_Act_2012
11. Greenwashing — Wikipedia — https://en.wikipedia.org/wiki/Greenwashing
12. Delivering a Net Zero National Health Service — NHS England (Greener NHS) — https://www.england.nhs.uk/greenernhs/publication/delivering-a-net-zero-national-health-service/
13. Greener NHS: national ambition and net-zero targets — NHS England — https://www.england.nhs.uk/greenernhs/a-net-zero-nhs/
14. Public Services (Social Value) Act 2012 — legislation.gov.uk (UK Government) — https://www.legislation.gov.uk/ukpga/2012/3/enacted
15. Greenhouse Gas Protocol — World Resources Institute & WBCSD — https://ghgprotocol.org/
16. Climate change and health — World Health Organization — https://www.who.int/news-room/fact-sheets/detail/climate-change-and-health
17. Green Software Foundation — https://greensoftware.foundation/
