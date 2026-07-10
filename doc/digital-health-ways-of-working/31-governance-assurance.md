# Chapter 31 — Governance & Assurance

**Governance exists to help you make good, fast, safe decisions and to prove — to yourself, your board, and the public — that a digital service is being run responsibly, so treat it as an enabler of delivery rather than a tax on it.**

## Why this matters in health and care

In most sectors, weak governance costs money and reputation. In health and care it can cost lives, entrench inequity, and erode the public trust on which the whole system depends. A poorly governed change to a clinical system can propagate a dosing error to thousands of patients before anyone notices; an ungoverned data flow can breach the confidentiality of the most vulnerable people you serve; an unassured go-live can lock in a service that quietly excludes those who most need care. The stakes are why "how you work" is a clinical-safety, equity, and trust issue, not merely an efficiency one.

At the same time, governance in health and care has a well-earned reputation for being slow, ritualistic, and disconnected from delivery. Teams sit through board meetings that rubber-stamp decisions already made, complete templates nobody reads, and watch amber risks turn green the week before a review only to fail spectacularly afterwards. This is the paradox you must resolve. The answer is not less governance or more; it is *proportionate* governance that scales with risk and value, gives clear people clear accountability, and produces honest information fast enough to act on. This chapter shows you how to build that, and how to layer independent assurance on top so that the people accountable — and the public — can be confident the controls actually work. It connects tightly to Chapter 5 — Clinical Safety & Risk Management, Chapter 6 — Information Governance, Data Protection & Cyber Security, Chapter 26 — EPPM, and Chapter 48 — Visibility for the CEO & Senior Leaders.

## Core concepts

[Governance](https://en.wikipedia.org/wiki/Governance) is the system of decision rights, accountability, and oversight through which an organisation directs and controls what it does. In digital health and care you are really managing three overlapping governance domains at once. [Corporate governance](https://en.wikipedia.org/wiki/Corporate_governance) covers the board's stewardship of the organisation as a whole — finance, strategy, risk, and legal duties. [Clinical governance](https://en.wikipedia.org/wiki/Clinical_governance) is the framework through which health organisations are accountable for continuously improving the quality and safety of care. [Information governance](https://en.wikipedia.org/wiki/Information_governance) covers how the organisation handles data lawfully, securely, and ethically. A digital service touches all three; if you govern only one, you will be blindsided by the others.

Single-point accountability is the spine of good governance. The [Senior Responsible Owner](https://en.wikipedia.org/wiki/Senior_responsible_owner) (SRO) is the one named individual personally accountable for a programme or major project achieving its objectives and realising its benefits — a role popularised by UK government but universally useful. Decision rights below the SRO are made explicit through a [responsibility assignment matrix](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix), commonly the RACI (responsible, accountable, consulted, informed) form, which prevents the two classic failures of "everyone thought someone else owned it" and "everyone tried to own it".

[Assurance](https://en.wikipedia.org/wiki/Assurance_services) is distinct from governance. Governance is the act of directing and deciding; assurance is independent, objective confirmation that the governance and controls are actually working as intended. The dominant mental model is the "three lines of defence": the first line is operational management who own and manage risk day-to-day; the second line is oversight functions (risk, compliance, clinical safety, information governance) that set policy and challenge; and the third line is [internal audit](https://en.wikipedia.org/wiki/Internal_audit), independent of both, reporting to the board. External regulators and auditors form a de facto fourth line.

Two further concepts hold the system together. [Risk appetite](https://en.wikipedia.org/wiki/Risk_appetite) is the amount and type of risk the organisation is willing to accept in pursuit of its objectives; without it, escalation is arbitrary. And the risk log — often extended to a RAID log (risks, assumptions, issues, dependencies) built on the same discipline as a [risk register](https://en.wikipedia.org/wiki/Risk_register) — is the working record that keeps a delivery honest. Review points are provided by staged assurance such as a [phase-gate process](https://en.wikipedia.org/wiki/Phase-gate_process) and, in UK government, gateway-style reviews run by the [Infrastructure and Projects Authority](https://en.wikipedia.org/wiki/Infrastructure_and_Projects_Authority) (IPA).

## Best practices

1. **Name one accountable SRO and mean it.** Appoint a single, sufficiently senior individual who is personally accountable for the outcome, has the authority to make decisions, and stays with the programme long enough to be held to account. Write their accountability into the terms of reference and their objectives. Resist the temptation to spread accountability across a committee — committees advise and decide collectively, but they cannot be accountable, because accountability that is shared is accountability that is absent.

2. **Design governance to fit the risk and value, not the calendar.** A small, low-risk internal tool does not need the same board, gates, and paperwork as a region-wide electronic patient record. Set tiers so that low-risk, low-value work flows through lightweight team-level governance, while high-risk or high-value work attracts formal boards and independent review. Publish the thresholds so teams know which tier they are in and can self-serve. Proportionality is what keeps governance from becoming a bottleneck that teams route around.

3. **Write terms of reference that clarify decision rights.** Every board should have a short terms-of-reference document stating its purpose, membership, quorum, what decisions it can make, what it can only recommend, and what must escalate above it. Pair this with a RACI so that recurring decision types — architecture choices, clinical sign-off, budget release, go-live approval — have a named accountable owner. Ambiguous decision rights are the single most common cause of governance drift, where meetings multiply because no one is sure who can actually say yes.

4. **Separate assurance from governance and use the three lines.** Do not let the people delivering a programme be the only people who assure it is safe. Ensure the second line — clinical safety officers, information governance leads, cyber security — has an independent voice and can escalate over the SRO's head when needed, and that internal audit periodically tests the whole system. This separation is what turns optimistic self-reporting into credible assurance, and it is a regulatory expectation in most health systems, not a nicety.

5. **Use integrated assurance and staged review points.** Rather than commissioning uncoordinated reviews, plan an integrated assurance and approval schedule that aligns clinical safety, information governance, technical, and commercial reviews to the same decision points. Adopt gateway-style reviews at the transitions that matter — before committing money, before build, before go-live — modelled on IPA gateway reviews and, for public-facing digital services, the service assessments pioneered by the Government Digital Service (GDS) and adapted by NHS. A good gate is a supportive challenge that de-risks the next phase, not an exam to be gamed.

6. **Make risk appetite explicit and let it drive escalation.** Agree, at board level, how much risk you are willing to carry in each domain — patient safety, data, delivery, finance, reputation — and express it concretely enough that a team can tell whether a given risk sits inside or outside appetite. Then wire escalation to appetite: anything outside appetite goes up automatically, with a named owner and a decision deadline. This stops the two failure modes of trivia clogging the board and serious risks quietly sitting in a spreadsheet.

7. **Run a living RAID log and a Board Assurance Framework.** Maintain a RAID log that is reviewed every delivery cycle, with each entry owned, dated, scored, and actively worked — not a graveyard of stale amber items. At organisational level, maintain a Board Assurance Framework (BAF) that maps your principal strategic risks to the controls in place and the assurance you have that those controls work, exposing gaps where you are relying on hope. The BAF is what lets a board see, on one page, whether its most important objectives are actually protected.

8. **Report honestly and kill governance theatre.** Insist on candid status reporting that surfaces bad news early, and protect the people who raise it. Watch for "watermelon reporting" — green on the outside, red on the inside — where dashboards stay green until the moment of failure; counter it by having assurance functions and delivery leads report on the same facts. Cut any meeting, template, or report that does not change a decision. Governance that produces documents nobody acts on is not caution, it is waste dressed as diligence.

## Questions to discuss with your team

1. **Where is single-point accountability genuinely clear on our most important digital work, and where is it a comfortable fiction?** Walk through your top three initiatives and ask, for each, who would personally answer to the board if it failed. If the honest answer is "the board", "the programme", or a name that keeps changing, you have a gap. Test whether the named SRO actually has the authority and time the role demands, or whether they are a figurehead while real decisions happen elsewhere. Consider whether accountability is undermined by a matrix in which the SRO cannot direct the people delivering. Discuss how continuity is protected when SROs move on, since accountability that resets every reorganisation is no accountability at all. The aim is not to blame individuals but to make sure that when something goes wrong, one empowered person owns putting it right.

2. **Is our governance proportionate, or are we applying heavyweight process to low-risk work and vice versa?** Map your current boards, gates, and approval steps against the actual risk and value of what passes through them. Look for the low-risk change that waited six weeks for a board that meets monthly, and the high-risk clinical change that slipped through on a team's own say-so. Ask whether teams are routing around governance because it is too slow, which is itself a serious risk signal. Consider whether you have published clear tiers and thresholds, or whether everything defaults to maximum ceremony out of caution. Debate where you could delegate decisions safely to move faster, and where you have been dangerously light. The goal is a system where the weight of governance visibly tracks the weight of the risk.

3. **How would we know if our reporting is telling us the truth?** Discuss concrete recent examples where a status went from green to red with little warning, and ask what the early signals were and why they did not surface. Explore whether delivery leads and assurance functions report from the same facts or from separate, conveniently divergent versions. Consider what happens, socially and professionally, to someone who reports a red status here — are they thanked or punished? Ask whether your board sees independent assurance alongside management's own account, or only the latter. Examine whether your dashboards measure things that predict problems or only things that are easy to make green. The purpose is to build a culture where honest bad news travels fast, because a governance system that cannot hear bad news cannot govern.

## In practice: a health & care example

An integrated care system (ICS) is rolling out a shared care record that lets clinicians across hospitals, general practice, and social care see a unified view of each patient. It is high-value and high-risk: it touches clinical decisions, links sensitive data across organisations, and serves a population with wide variation in digital access.

Early on, accountability is muddy. Three chief information officers each feel partly responsible, a supplier is driving the timeline, and the programme board of eighteen people spends its meetings receiving updates rather than deciding. Reporting is green. Then a near-miss surfaces: a medication allergy recorded in one system is not displaying in another, and a clinician nearly prescribes a drug the patient is allergic to.

The chief executives use this as a turning point and rebuild the governance. They appoint one SRO — a chief medical officer with the seniority to direct the programme and the standing to challenge the supplier. They rewrite the board's terms of reference, cut it to the decision-makers, and attach a RACI so clinical safety sign-off, information governance approval, and go-live authorisation each have a named accountable owner. Risk appetite is made explicit: zero appetite for undetected clinical-safety defects, limited appetite for schedule slippage. That single statement reorders everything.

Assurance is separated from delivery. The clinical safety officer and the information governance lead report independently and can escalate over the SRO to the chief executives; the shared-record work is added to each partner's Board Assurance Framework. An integrated assurance schedule sets three gates — before further build, before pilot, before full roll-out — each combining clinical safety, information governance, technical, and accessibility reviews, in the spirit of IPA gateway reviews and NHS service assessments. The RAID log is reviewed fortnightly, with the allergy-display defect logged as a red issue owned by name with a fixed resolution date.

The first gate is uncomfortable: the review team finds the clinical-safety case is thinner than the green reports implied, and the roll-out is paused four weeks. It is exactly the watermelon the old reporting had hidden. Because the pause happens before pilot rather than after go-live, no patient is harmed, the supplier fixes the data-mapping, and the eventual roll-out is slower to start but far safer and more trusted. Governance did not slow delivery; it prevented a failure that would have stopped it altogether.

## Three sector lenses

### Startup

A health-tech startup rarely needs boards and gateway reviews, but it does need the essentials early, because regulators, buyers, and investors will ask. Name one accountable founder or executive for clinical safety and one for data protection, keep a lightweight RAID log, and write down your risk appetite even if it is a single page. The trap is treating governance as something to bolt on later; retrofitting evidence of safe, lawful decisions across a fast-moving product is painful and sometimes impossible. Build the minimum viable governance that a serious NHS buyer would recognise, and let it grow with you rather than lurching from nothing to bureaucracy overnight.

### Enterprise

A large provider or supplier already has boards, audit committees, and internal audit, so the enterprise risk is the opposite of the startup's: too much governance, poorly integrated, generating theatre. Consolidate overlapping boards, publish proportionality tiers, and integrate clinical, information, technical, and commercial assurance into a single schedule so teams face one coherent set of gates rather than a dozen uncoordinated reviews. Make sure the three lines of defence are genuinely independent and that internal audit periodically tests digital delivery, not just finance. The prize is turning an existing, expensive governance machine into one that actually accelerates safe decisions.

### Government

National and regional bodies — NHS England, ICBs, arms-length bodies — operate under statutory accountability, public spending controls, and formal assurance regimes such as IPA gateway reviews and the government's spend-control and service-assessment processes. Here the SRO role is codified and personally accountable to Parliament or its equivalents, and transparency is a duty, not a choice. The discipline is to make this mandated governance proportionate and to align the many external assurance demands so they inform delivery rather than merely audit it after the fact. Done well, public-sector governance is a model of accountability; done badly, it is the origin of the "governance theatre" the whole sector fears.

## Common failure modes

- **Accountability by committee.** No single SRO, so when things go wrong everyone points sideways and nothing is owned.
- **Governance theatre.** Boards that receive rather than decide, templates nobody reads, and gates that are exams to be passed rather than genuine de-risking.
- **Watermelon reporting.** Status stays green until the moment of failure because bad news is unwelcome and delivery reports go unchallenged by assurance.
- **One-size-fits-all process.** Heavyweight governance applied to trivial work, driving teams to route around it, while genuinely risky work slips through lightly.
- **Assurance captured by delivery.** The people building the service are the only people confirming it is safe, so optimism goes unchecked.
- **Stale RAID logs.** Risks logged once and never worked; amber items that quietly turn green before a review with no change underneath.
- **Domain blindness.** Governing the delivery well but missing the clinical-safety, information-governance, or equity dimension until it becomes a crisis.
- **Gate theatre without teeth.** Review points that never actually stop or reshape work, so failing programmes sail through every gate.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Accountability | No clear owner; decisions diffuse | SRO named but under-empowered | Empowered SRO with clear terms of reference and RACI | Accountability continuous through change; SROs supported and held to account |
| Proportionality | Ad hoc; process by habit | Some tiering, inconsistently applied | Published tiers scale with risk and value | Tiers actively tuned; teams self-serve the right level |
| Assurance | Self-reported only | Second line exists but weak voice | Three lines operating; integrated assurance schedule | Assurance shapes delivery; findings routinely improve the system |
| Risk & escalation | Risks in scattered lists | RAID log kept but stale | Risk appetite explicit; escalation wired to it; BAF live | Predictive, appetite-driven; near-misses drive learning |
| Reporting | Green until failure | Reports exist but unchallenged | Delivery and assurance report on shared facts | Honest reporting is cultural; bad news travels fast and safely |

## Checklist

- [ ] Every major initiative has one named, sufficiently senior, empowered SRO.
- [ ] Each board has current terms of reference stating its decision rights, quorum, and escalation.
- [ ] A RACI assigns a named accountable owner to each recurring decision type.
- [ ] Governance tiers scale with risk and value, and the thresholds are published.
- [ ] The three lines of defence are in place, with an independent second-line voice that can escalate.
- [ ] An integrated assurance schedule aligns clinical, information-governance, technical, and commercial reviews to staged gates.
- [ ] Risk appetite is written down per domain and escalation is wired to it.
- [ ] A living RAID log is reviewed each delivery cycle, with every entry owned and dated.
- [ ] A Board Assurance Framework maps principal risks to controls and to the assurance those controls work.
- [ ] Delivery and assurance report from the same facts, and raising bad news is safe.
- [ ] Every meeting, template, and report you keep changes a real decision.

## Key sources

- Infrastructure and Projects Authority (IPA), *Principles for Project Success* and the gateway/assurance review guidance — UK Cabinet Office / HM Treasury.
- NHS England, *Clinical Risk Management Standards* (DCB0129 and DCB0160) — for clinical governance of health IT (see also Chapter 5).
- Institute of Internal Auditors (IIA), *The IIA's Three Lines Model* (2020 update) — the authoritative statement of the three-lines approach.
- HM Treasury, *The Orange Book: Management of Risk — Principles and Concepts* — risk appetite, controls, and assurance in UK public bodies.
- NHS England / former Government Digital Service, *Service Standard* and service-assessment guidance — assurance of public-facing digital services.
- UK Corporate Governance Code — Financial Reporting Council — board accountability and internal control.

## References

1. Governance — Wikipedia — https://en.wikipedia.org/wiki/Governance
2. Corporate governance — Wikipedia — https://en.wikipedia.org/wiki/Corporate_governance
3. Clinical governance — Wikipedia — https://en.wikipedia.org/wiki/Clinical_governance
4. Information governance — Wikipedia — https://en.wikipedia.org/wiki/Information_governance
5. Senior responsible owner (Executive sponsor) — Wikipedia — https://en.wikipedia.org/wiki/Senior_responsible_owner
6. Responsibility assignment matrix (RACI) — Wikipedia — https://en.wikipedia.org/wiki/Responsibility_assignment_matrix
7. Assurance services — Wikipedia — https://en.wikipedia.org/wiki/Assurance_services
8. Internal audit (Three Lines model) — Wikipedia — https://en.wikipedia.org/wiki/Internal_audit
9. Risk appetite — Wikipedia — https://en.wikipedia.org/wiki/Risk_appetite
10. Risk register — Wikipedia — https://en.wikipedia.org/wiki/Risk_register
11. Phase-gate process — Wikipedia — https://en.wikipedia.org/wiki/Phase-gate_process
12. Infrastructure and Projects Authority — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_and_Projects_Authority
13. The IIA's Three Lines Model — Institute of Internal Auditors — https://www.theiia.org/en/content/position-papers/2020/the-iias-three-lines-model-an-update-of-the-three-lines-of-defense/
14. The Orange Book: Management of Risk — Principles and Concepts — HM Treasury — https://www.gov.uk/government/publications/orange-book
15. Clinical Risk Management: its Application in the Deployment and Use of Health IT Systems (DCB0160) — NHS England — https://digital.nhs.uk/services/clinical-safety
16. Service Standard — Government Digital Service / GOV.UK — https://www.gov.uk/service-manual/service-standard
17. The UK Corporate Governance Code — Financial Reporting Council — https://www.frc.org.uk/library/standards-codes-policy/corporate-governance/uk-corporate-governance-code/
