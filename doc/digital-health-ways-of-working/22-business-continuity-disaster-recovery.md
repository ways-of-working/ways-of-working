# Chapter 22 — Business Continuity & Disaster Recovery

**In health and care, a major system outage is a patient-safety event before it is an IT problem, so your ability to keep delivering care while a system is down — and to recover it fully and quickly — is a core clinical and public-trust capability, not a technical footnote.**

## Why this matters in health and care

Care does not stop when the technology does. When an electronic patient record, an e-prescribing platform, or a laboratory results system fails across a hospital, clinicians do not get to pause treatment while engineers work. They must keep seeing patients, prescribing medicines, and making decisions — often without the allergy alerts, dose checks, and prior history that the failed system normally provides. That is why an outage is not measured only in downtime hours and service credits; it is measured in delayed diagnoses, missed interactions, cancelled operations, and the additional risk carried by every clinician working blind. Business continuity is the discipline of making sure that when the worst happens, care stays as safe as it can be.

The stakes are national and well-documented. The 2017 WannaCry ransomware attack disrupted around a third of NHS trusts in England, forced the cancellation of thousands of appointments and operations, diverted ambulances, and locked staff out of the very devices — including some imaging and pathology equipment — that they needed to treat people. It cost the NHS an estimated £92 million and, more importantly, showed that a cyber-attack on health infrastructure lands as a clinical crisis, not merely a data-security incident. Since then, resilience has moved from the server room to the board table, and rightly so.

This chapter extends the operational discipline of Chapter 21 — Service Management & Live Operations, but shifts the focus from everyday running to major disruption: the fire, flood, cyber-attack, supplier collapse, or regional outage that threatens to take a critical service down for hours or days. It connects tightly to Chapter 7 — Information Governance, Data Protection & Cyber Security (because ransomware recovery is now a central continuity scenario), to Chapter 23 — Technical Architecture, Cloud & Legacy (because resilience is designed in, not bolted on), and to Chapter 37 — Governance & Assurance (because someone must own, test, and be accountable for the plan). Get this right and disruption becomes a bad day; get it wrong and it becomes a public inquiry.

## Core concepts

**Business continuity and disaster recovery.** [Business continuity planning](https://en.wikipedia.org/wiki/Business_continuity_planning) (BCP) is the capability to keep delivering products or services — in your case, safe care — at pre-defined acceptable levels during and after a disruptive incident. [IT disaster recovery](https://en.wikipedia.org/wiki/IT_disaster_recovery) (DR) is the narrower, technical subset concerned with restoring the systems, data, and infrastructure that underpin those services. Business continuity is the wider promise ("patients keep being treated"); disaster recovery is one of the means ("the results system is back within four hours"). You need both, and you must not confuse a restored server with a restored service.

**Business continuity management and business impact analysis.** *Business continuity management* (BCM) is the ongoing management process — not a one-off document — that identifies threats and builds organisational resilience. Its foundation is the *business impact analysis* (BIA): a structured assessment of each service that asks how quickly its loss causes unacceptable harm, what it depends on, and how far back in time you can afford to lose data. The BIA is where clinical judgement enters engineering: clinicians, not just technologists, must define what "unacceptable" means for a maternity system versus a staff intranet.

**Recovery time objective and recovery point objective.** Two numbers anchor every recovery plan. The *recovery time objective* (RTO) is the maximum acceptable time to restore a service after failure. The *recovery point objective* (RPO) is the maximum acceptable amount of data loss, expressed as time — an RPO of fifteen minutes means you can tolerate losing at most the last fifteen minutes of entries. For a critical clinical system these may be minutes; for a reporting warehouse they may be days. Setting them honestly, per service, is the single most useful continuity decision you will make.

**Backups and tested restores.** A [backup](https://en.wikipedia.org/wiki/Backup) is a copy of data stored elsewhere so the original can be restored after loss. The industry baseline is the *3-2-1 rule*: three copies, on two types of media, with one held off-site (and, in the ransomware era, one held immutable or offline). Crucially, a backup you have never restored is a hope, not a control. Ransomware routinely encrypts backups that are reachable from the network, and untested restores routinely fail on the day. The discipline is not "do we back up?" but "when did we last successfully restore, end to end, and how long did it take?"

**High availability, redundancy, and failover.** [High availability](https://en.wikipedia.org/wiki/High_availability) (HA) is a design property that keeps a system running through component failure, usually measured in "nines" of uptime. It is achieved through [redundancy](https://en.wikipedia.org/wiki/Redundancy_(engineering)) — the deliberate duplication of critical components — and [failover](https://en.wikipedia.org/wiki/Failover), the automatic switch to a standby component or site when the primary fails. High availability reduces the frequency of outages; disaster recovery handles the ones that get through. They are complementary, not alternatives, and confusing them leaves dangerous gaps.

**Single points of failure and critical dependencies.** A [single point of failure](https://en.wikipedia.org/wiki/Single_point_of_failure) (SPOF) is any component whose failure stops the whole service — one network link, one authentication service, one supplier, one database, or one person who alone knows how something works. Mapping SPOFs and *critical dependencies* (the upstream services and third parties your service silently relies on) is the analytical heart of resilience. In modern health IT, dependencies are rarely local: a single-sign-on service, a national spine connection, or a cloud region can take down many systems at once.

**Clinical downtime and business-continuity procedures.** Health and care has a distinctive control that generic IT lacks: the *clinical downtime procedure*, a rehearsed, safe fallback — usually paper — for delivering care when a digital system is unavailable, plus the *re-entry* process for reconciling that paper record back into the system once it returns. This is business continuity made concrete at the bedside, and it is where continuity plans most often meet reality.

**Ransomware and cyber-recovery.** [Ransomware](https://en.wikipedia.org/wiki/Ransomware) encrypts your data and demands payment, and it has become the defining continuity threat for health systems. The [WannaCry ransomware attack](https://en.wikipedia.org/wiki/WannaCry_ransomware_attack) of 2017 is the reference case: it is why cyber-recovery — isolating, rebuilding from clean backups, and validating integrity before reconnecting — is now a first-class scenario in every serious plan.

**The continuity standard.** [ISO 22301](https://en.wikipedia.org/wiki/ISO_22301) is the international standard for business continuity management systems. It provides a recognised structure — context, leadership, planning, support, operation, evaluation, improvement — for building and auditing continuity capability, and it is a useful backbone whether or not you seek formal certification.

## Best practices

1. **Start from a business impact analysis owned by clinicians, not IT alone.** Rank every service by the clinical harm caused when it fails and by how quickly that harm becomes intolerable, then assign each a specific RTO and RPO. Do this with the clinicians and operational managers who bear the consequences, because "how long can we run without this safely?" is a care question, not an infrastructure one. The output is a prioritised list that tells you where to spend your finite resilience budget first.

2. **Design resilience proportionate to criticality.** Match the engineering to the impact: mission-critical systems (emergency department, patient administration, e-prescribing) warrant high availability, geographic redundancy, and automatic failover; lower-criticality systems can accept longer recovery and simpler backups. Resist both under-engineering critical systems and gold-plating trivial ones. Architecture and continuity must be designed together (see Chapter 23 — Technical Architecture, Cloud & Legacy), because you cannot bolt resilience onto a fragile design after the fact.

3. **Hunt down single points of failure and hidden dependencies.** Systematically map each critical service's dependencies — network, authentication, DNS, national connections, power, cooling, key suppliers, and key people — and identify where one failure cascades. Pay particular attention to shared services such as single sign-on or a common integration engine, whose failure takes down many systems at once. A dependency you have not mapped is a dependency you will discover during the outage.

4. **Back up to survive ransomware, and prove restores by testing them.** Follow the 3-2-1 rule and keep at least one backup copy immutable or physically offline, so an attacker who reaches your network cannot encrypt your last line of defence. Then test restores on a schedule, timing them against your RTO and validating data integrity against your RPO — a restore that takes two days against a four-hour objective is a failed control you have simply not noticed yet. Treat "last successful full restore" as a metric you report, not a task you assume.

5. **Write, resource, and rehearse clinical downtime procedures.** For every critical clinical system, maintain a tested paper (or offline) fallback that lets staff keep delivering safe care during an outage, plus a clear process for re-entering that data afterwards without loss or duplication. Store downtime forms where they can be reached when the network and the printers are also down. Rehearse them with frontline staff, because a procedure that lives only in a folder will not be found, understood, or trusted at 3 a.m. during a crisis.

6. **Maintain a disaster recovery plan with real site failover.** Document, for each critical system, exactly how it recovers: what runs where, in what order, who decides to invoke it, and how you fail back afterwards. Where the impact justifies it, run a genuinely separate recovery site or cloud region and prove you can switch to it — recovery order matters, because systems have dependencies that dictate sequence. An untested DR site is an expensive assumption.

7. **Exercise the plan; a plan never tested is a plan that fails.** Run regular exercises across a spectrum: desktop tabletop walk-throughs of scenarios, technical failover tests, and occasional full live simulations including the clinical fallback. Exercises expose the gaps — the out-of-date contact list, the recovery step that needs a password no one has, the assumption that staff know the paper process — while it is safe to find them. Capture the lessons, fix them, and re-test; an exercise with no follow-up is theatre.

8. **Extend continuity to your suppliers and cloud.** Your resilience is only as strong as the third parties your critical services depend on, so make continuity a contractual and assurance matter: require suppliers to evidence their own RTO/RPO, DR testing, and cyber-recovery, and understand your cloud provider's shared-responsibility model — availability zones and regions protect against some failures but not against a mis-configuration or account compromise that you own. Plan for supplier failure itself, including the scenario where a key supplier is the one hit by ransomware (see Chapter 36 — Procurement & Commercial).

9. **Adopt a recognised standard and put continuity under governance.** Use ISO 22301 as a structured backbone and NHS and national guidance as the sector overlay, and give a named executive accountability for business continuity, reporting to the board. Continuity that no one owns, funds, or reviews decays quietly until the incident reveals it. Wire it into your assurance framework (see Chapter 37 — Governance & Assurance) so plans are maintained, tested, and improved as a matter of routine, not rediscovered in a crisis.

## Questions to discuss with your team

1. **For each of our critical clinical systems, what RTO and RPO have we actually agreed with clinicians — and can we currently meet them?** This question forces the gap between aspiration and capability into the open. Many organisations have never set explicit recovery objectives, or set them in IT without clinical input, so the "acceptable" downtime is really just whatever the current architecture happens to deliver. Debate where clinical need (minutes for an emergency system) collides with what your backups and DR can actually achieve (perhaps a day), because that gap is unmanaged clinical risk you are carrying whether you name it or not. Look concretely at your last real or tested recovery: how long did it take, how much data would you have lost, and who signed off that this is safe? A good, honest answer names specific numbers per system, admits where you cannot yet meet them, and turns each gap into a funded action rather than a comfortable silence.

2. **If ransomware encrypted our core systems and our backups tonight, how would we keep patients safe tomorrow — and how long until we are fully recovered?** This is the scenario that has hit real health systems, so it deserves a concrete, unflinching walk-through rather than reassurance. Explore both halves honestly: the immediate clinical continuity (are the downtime procedures rehearsed, resourced, and trusted enough to run a whole hospital on paper for days?) and the technical recovery (are backups immutable and offline, have you tested rebuilding from clean copies, and do you know the recovery order?). Surface the uncomfortable dependencies — if single sign-on, the integration engine, or a key supplier is down, how much else falls with it? Consider who declares the major incident, who talks to staff, patients, and the media, and who decides that a system is safe to reconnect. A strong answer describes a rehearsed plan with named roles and tested restores; a weak one assumes the backups are fine and the paper process will simply work.

3. **When did we last test our continuity and disaster recovery plans end to end, and what did we learn?** The purpose here is to distinguish a living capability from a shelf document. A plan that has not been exercised is untested, and untested plans routinely fail on contact with reality — the contact list is stale, the recovery step needs credentials no one has, the downtime forms are stored on the system that is down. Discuss the range of exercising you actually do: tabletop scenarios, technical failover tests, and full simulations that include the frontline clinical fallback, not just the server restore. Probe whether lessons from past incidents and exercises were actually fixed and re-tested, or logged and forgotten. A good answer shows a regular exercise calendar, evidence of gaps found and closed, and honesty about which parts of the plan remain unproven.

## In practice: a health & care example

Meadowvale NHS Foundation Trust runs a 600-bed acute hospital. On a Tuesday morning, staff arrive to find their electronic patient record (EPR), pathology, and radiology systems locked by a ransom note; the attackers had entered through a supplier's remote-access account ten days earlier. The chief information officer declares a major incident within the hour, and the trust's business continuity plan activates.

Because the trust had done its business impact analysis, it knew the EPR and pathology were its highest-criticality systems, with agreed recovery objectives, while its downtime procedures had been rehearsed the previous autumn. Wards switch to paper drug charts and pre-printed observation forms — stored deliberately in physical cabinets on each ward, not on a shared drive — and the emergency department reverts to its paper pathway. Elective operations for the week are postponed and communicated to patients; ambulances are diverted from the busiest periods. Care continues, degraded but safe, because staff had practised working this way.

Recovery is harder than restoration. The security team isolates the network to stop the spread, then rebuilds critical systems from immutable backups held offline — copies the attackers could not reach. Those backups had been restore-tested quarterly, so the team knew the process worked and roughly how long it took; the EPR is back within its RTO of eight hours, though pathology, with more complex dependencies, takes two days. The RPO of fifteen minutes means only a short window of data was lost, and staff reconcile the paper records back into the system under a controlled re-entry process, double-checking medications and results.

In the debrief, the trust finds real gaps: single sign-on was a single point of failure that delayed clinician access during recovery, and the supplier's remote access had not been covered by the trust's own continuity assurance. Both go onto the board's risk register with owners and dates, and the next full exercise is scheduled. It was a bad week — but not a catastrophe, because the plan existed, was resourced, and had been tested.

## Three sector lenses

### Startup

A digital-health startup rarely has a spare data centre, so its continuity strategy leans almost entirely on cloud-native resilience and disciplined backups. Use managed services with built-in high availability across availability zones, automate backups with immutable, off-account copies to survive both ransomware and a compromised cloud account, and actually rehearse a restore into a clean environment. Your customers — NHS trusts and integrated care systems — will increasingly demand evidence of RTO, RPO, and DR testing through frameworks like DTAC and supplier assurance, so treat continuity as a sales asset, not overhead. The existential risk for a small supplier is that a single incident, or the founder who alone understands the deployment, becomes your single point of failure.

### Enterprise

A large NHS trust, an integrated care system, or a big health-tech vendor carries a sprawling, interdependent estate where the hardest problem is mapping dependencies and shared services, not any single system. Invest in a formal BCM programme aligned to ISO 22301, a maintained dependency map, DR sites or regions for critical systems, and a rolling calendar of exercises that includes the clinical fallback. The scale means SPOFs are often shared services — identity, integration engines, network cores — whose failure cascades across dozens of systems. Governance is the binding constraint: with many teams and suppliers, continuity only holds if a named executive owns it and the board reviews tested assurance, not paper plans.

### Government

A national body — NHS England, a devolved health department, or UKHSA — must think about resilience at population and systemic scale, where the failure of a national service or a widely used supplier is itself a continuity event for the whole sector. Set standards and expectations (recovery objectives, cyber-recovery, mandatory exercising), fund shared protective capabilities, and coordinate the sector-wide response to major incidents such as a national ransomware campaign. The WannaCry response reshaped national policy precisely because the impact crossed hundreds of organisations at once, exposing common weaknesses. Accountability here is public and parliamentary, so transparency about known risks, and honest reporting of preparedness, matter as much as the technical controls themselves.

## Common failure modes

- **Backups that have never been restored.** Confusing "we back up nightly" with "we can recover." Untested restores routinely fail or blow the RTO; measure and report successful end-to-end restores, not backup completion.
- **Ransomware-reachable backups.** Keeping every backup online and network-connected, so an attacker encrypts them along with production. Hold at least one immutable or offline copy.
- **DR that protects servers, not services.** Restoring a database but not the dependencies, integrations, and access that make it a usable clinical service. Recover and test whole services, in dependency order.
- **Downtime procedures that exist only on paper about paper.** Fallback plans that are never rehearsed, stored on the system that fails, or unknown to frontline staff. Rehearse them where care actually happens.
- **Unmapped dependencies and shared SPOFs.** Discovering during the outage that single sign-on, DNS, or one supplier underpinned everything. Map dependencies before, not during, the incident.
- **A plan written for the auditor, never exercised.** Continuity as a compliance document that decays untested until the day it is needed. A plan never tested is a plan that fails.
- **Ignoring supplier and cloud continuity.** Assuming your third parties are resilient without evidence, and forgetting the shared-responsibility model. Make continuity contractual and assured.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
| --- | --- | --- | --- | --- |
| Recovery objectives | No RTO/RPO set; recovery is whatever the kit allows | RTO/RPO set for a few systems, by IT alone | RTO/RPO agreed with clinicians for all critical systems | Objectives evidenced by regular tests and continually tuned |
| Backups & restores | Backups run, restores never tested | Occasional ad-hoc restore tests | Scheduled restore tests, some immutable/offline copies | Immutable backups with automated, timed, integrity-checked restores |
| Clinical downtime | No documented fallback | Paper procedures exist but unrehearsed | Rehearsed downtime and re-entry for critical systems | Frequent drills; staff fluent, forms and access assured |
| Disaster recovery | No DR plan; hope and heroics | DR plan documented but untested | DR site/region tested for critical systems | Regular failover tests, dependency-ordered, cyber-recovery included |
| Governance & exercising | No owner, no exercises | Owner named, exercises rare | Executive-owned BCM aligned to ISO 22301, regular exercises | Board-assured, continuous improvement from every incident and drill |

## Checklist

- [ ] A business impact analysis, owned with clinicians, ranks every service and sets an explicit RTO and RPO for each critical system.
- [ ] Critical systems have high availability and redundancy proportionate to their clinical criticality.
- [ ] Single points of failure and critical dependencies (including shared services and suppliers) are mapped and mitigated.
- [ ] Backups follow the 3-2-1 rule with at least one immutable or offline copy that ransomware cannot reach.
- [ ] Restores are tested on a schedule and timed against RTO/RPO, with "last successful restore" reported as a metric.
- [ ] Every critical clinical system has a rehearsed downtime procedure and a controlled data re-entry process.
- [ ] A disaster recovery plan defines recovery steps, order, decision authority, and failback, and the DR site/region is tested.
- [ ] A cyber-recovery scenario (isolate, rebuild from clean backups, validate, reconnect) is documented and exercised.
- [ ] Supplier and cloud continuity is contractually required, evidenced, and assured, including the shared-responsibility model.
- [ ] Continuity is aligned to ISO 22301, owned by a named executive, exercised on a calendar, and reported to the board.

## Key sources

- NHS England — *Business Continuity Management Toolkit* and Emergency Preparedness, Resilience and Response (EPRR) Framework and Core Standards.
- National Cyber Security Centre (NCSC) — guidance on offline/immutable backups, ransomware mitigation, and incident response.
- ISO 22301:2019 — *Security and resilience — Business continuity management systems — Requirements* (International Organization for Standardization).
- ISO/IEC 27031 — *Guidelines for information and communication technology readiness for business continuity*.
- Business Continuity Institute (BCI) — *Good Practice Guidelines*.
- National Audit Office — *Investigation: WannaCry cyber attack and the NHS* (2017) and Department of Health lessons-learned review.
- NHS England / Data Security and Protection Toolkit (DSPT) — data security standards including business continuity and incident response.
- GOV.UK Service Manual — resilience, monitoring, and recovery guidance for live services.

## References

1. Business continuity planning — Wikipedia — https://en.wikipedia.org/wiki/Business_continuity_planning
2. IT disaster recovery — Wikipedia — https://en.wikipedia.org/wiki/IT_disaster_recovery
3. ISO 22301 — Wikipedia — https://en.wikipedia.org/wiki/ISO_22301
4. Backup — Wikipedia — https://en.wikipedia.org/wiki/Backup
5. High availability — Wikipedia — https://en.wikipedia.org/wiki/High_availability
6. Redundancy (engineering) — Wikipedia — https://en.wikipedia.org/wiki/Redundancy_(engineering)
7. Failover — Wikipedia — https://en.wikipedia.org/wiki/Failover
8. Single point of failure — Wikipedia — https://en.wikipedia.org/wiki/Single_point_of_failure
9. Ransomware — Wikipedia — https://en.wikipedia.org/wiki/Ransomware
10. WannaCry ransomware attack — Wikipedia — https://en.wikipedia.org/wiki/WannaCry_ransomware_attack
11. ISO 22301:2019 Security and resilience — Business continuity management systems — Requirements — International Organization for Standardization — https://www.iso.org/standard/75106.html
12. Investigation: WannaCry cyber attack and the NHS — National Audit Office — https://www.nao.org.uk/reports/investigation-wannacry-cyber-attack-and-the-nhs/
13. Emergency Preparedness, Resilience and Response (EPRR) — NHS England — https://www.england.nhs.uk/ourwork/eprr/
14. Offline backups in an online world — National Cyber Security Centre — https://www.ncsc.gov.uk/blog-post/offline-backups-in-an-online-world
15. Data Security and Protection Toolkit — NHS England — https://www.dsptoolkit.nhs.uk/
