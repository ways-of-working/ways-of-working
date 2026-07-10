# Chapter 14 — Service Management & Live Operations

**In health and care, most of a service's life, cost, and clinical risk sits after go-live — so how you run, monitor, and support a live service is a patient-safety decision, not a back-office afterthought.**

## Why this matters in health and care

The launch is the beginning, not the end. A digital service spends a few months being built and, if it succeeds, years or decades being run — and the running is where most of the money goes and where the harm actually happens. A shared care record, an e-prescribing system, or a maternity notes platform delivers its value only while it is up, correct, and responsive. When it degrades or fails, the consequences are not inconvenience but delayed treatment, missed allergies, cancelled clinics, and clinicians reverting to unfamiliar paper workarounds under pressure.

Health and care runs 24 hours a day, seven days a week, and cannot pause. When a supermarket's checkout system fails, customers wait; when a hospital's patient administration system fails, ambulances may be diverted and elective lists postponed. This gives live operations a distinctive weight: downtime is a clinical-safety event, and the plan for how you detect, escalate, communicate, and recover from it is part of your duty of care. The 2017 WannaCry ransomware attack — which forced the cancellation of thousands of NHS appointments and operations — is the reference case for how an operational failure becomes a patient-safety and public-trust crisis (see Chapter 5 — Information Governance, Data Protection & Cyber Security).

Leaders also need to fund and staff live operations honestly. The persistent failure in health-tech is to celebrate a go-live, disband the team, and treat the running service as "finished". A live service with no standing team, no monitoring, and no on-call cover is not saving money — it is quietly accruing clinical risk until the day it fails loudly. Service management is the discipline that keeps a live service safe, and it deserves the same rigour as the build.

## Core concepts

**Service management and the "Live" phase.** [IT service management](https://en.wikipedia.org/wiki/IT_service_management) (ITSM) is the set of practices for designing, running, supporting, and improving IT services across their whole life. In the GOV.UK and NHS phase model, **Live** is the phase where a service runs in continuous operation — still iterating, still funded, still owned — until it is retired (see Chapter 12 — Delivery Lifecycles). Live is not a resting state; it is the longest and most expensive part of the lifecycle.

**ITIL 4.** [ITIL](https://en.wikipedia.org/wiki/ITIL) is the most widely used ITSM framework. Its current edition, ITIL 4, reframes older process-heavy versions around a "service value system" and flexible practices, and is designed to sit alongside Agile, DevOps, and Lean rather than compete with them. Treat ITIL as a vocabulary and a checklist of practices to adopt proportionately — not a bureaucracy to import wholesale.

**Incident, problem, and change management.** [Incident management](https://en.wikipedia.org/wiki/Incident_management) restores normal service as quickly as possible after an unplanned disruption — the priority is recovery, not diagnosis. *Problem management* investigates the underlying cause of one or many incidents to stop recurrence, and maintains a record of known errors and workarounds. [Change management](https://en.wikipedia.org/wiki/Change_management_(ITSM)) (in the ITSM sense) controls how changes to the live estate are assessed, approved, and released so that fixing one thing does not break another. These three practices are the operational core, and they interlock: an incident may raise a problem, whose fix is delivered as a change.

**Major incident management and business continuity.** A *major incident* is a high-impact event — a clinical system down across a trust — that needs a declared, coordinated response with a defined incident commander, communications, and clinical leadership. [Business continuity planning](https://en.wikipedia.org/wiki/Business_continuity_planning) (BCP) is the broader capability to keep delivering care at acceptable levels during disruption, including tested clinical downtime procedures (the safe paper fallback) and disaster recovery. In health and care these are not optional: keeping patients safe while the system is down is the whole point.

**Site reliability engineering, SLIs, SLOs, SLAs, and error budgets.** [Site reliability engineering](https://en.wikipedia.org/wiki/Site_reliability_engineering) (SRE), originated at Google, applies software-engineering discipline to operations. It measures reliability with a [service level indicator](https://en.wikipedia.org/wiki/Service_level_indicator) (SLI) — a metric such as availability or latency — against a [service-level objective](https://en.wikipedia.org/wiki/Service-level_objective) (SLO), an internal target for that metric. A [service-level agreement](https://en.wikipedia.org/wiki/Service-level_agreement) (SLA) is the external, often contractual, promise, usually set looser than the internal SLO. The gap between 100% and your SLO is the *error budget*: the amount of unreliability you can spend before you must stop shipping features and stabilise. In clinical systems, SLOs must be set with clinicians, because "acceptable" downtime is a safety judgement, not just an engineering one.

**Observability and monitoring.** [Observability](https://en.wikipedia.org/wiki/Observability_(software)) is the ability to understand a system's internal state from its external outputs — logs, metrics, and traces — so you can detect and diagnose problems, ideally before users do. Monitoring and alerting turn that data into timely signals for the people on call. You cannot run a service safely that you cannot see.

**On-call, rotas, and the service desk.** *On-call* rotas ensure a competent human can respond to alerts around the clock; in a 24/7 care setting they are essential, and they must be humane and sustainable. A *service desk* (or [help desk](https://en.wikipedia.org/wiki/Help_desk)) is the single point of contact for end users — the clinician who cannot log in, the receptionist whose booking screen has frozen — providing support, logging incidents, and routing them onward.

**DevOps, configuration management, and the CMDB.** [DevOps](https://en.wikipedia.org/wiki/DevOps) and the SRE principle "you build it, you run it" put the team that builds a service in charge of running it, closing the gap between development and operations. *Configuration management* keeps an accurate record of the components that make up a service and their relationships, often in a *configuration management database* ([CMDB](https://en.wikipedia.org/wiki/Configuration_management_database)); without it, no one can safely answer "what will this change affect?" during an incident.

**Run-versus-build and decommissioning.** Organisations separate *build* funding (creating new capability) from *run* funding (operating what exists). Underfunding run is the structural root of most operational failure. And every service eventually reaches *decommissioning* — safe retirement, with data migrated or archived under retention law and users redirected — which is an operational discipline in its own right.

## Best practices

1. **Fund and staff "run" as a first-class commitment, not a leftover.** Budget for the operational life of the service — monitoring, on-call, service desk, security patching, and continuous iteration — before go-live, and protect it from raids by the next shiny build. The industry rule of thumb that running a system costs far more over its life than building it holds in health too. A service with build funding and no run funding is a clinical risk with a launch date.

2. **Avoid the "throw it over the wall to ops" anti-pattern.** Do not let a project team build a service and hand it to a separate operations team that never saw it made. Apply "you build it, you run it": keep the team that understands the service accountable for its reliability, or at minimum run a deliberate, documented service-transition with shared on-call and a warranty period. The wall between build and run is where knowledge, ownership, and safety fall through.

3. **Set SLOs with clinicians and manage an error budget.** Define what "reliable enough" means for each service as measurable SLIs and SLOs, and set them jointly with the clinicians who bear the consequences — availability targets for an emergency-department system are not a purely technical choice. Use the error budget to arbitrate the eternal tension between shipping features and staying stable: when reliability is spent, stop and stabilise. Keep external SLAs looser than internal SLOs so you have room to act before you breach a promise.

4. **Make the service observable before you make it bigger.** Instrument logging, metrics, and tracing, and build dashboards and alerts that reflect the user's and clinician's experience, not just server health. Alert on symptoms that matter (patients cannot be booked) rather than every underlying blip, to avoid alert fatigue that trains responders to ignore pages. You cannot keep safe a service whose failures you learn about from angry clinicians.

5. **Run disciplined incident, problem, and change management — proportionately.** Give incidents clear severity levels, response targets, an incident commander for major ones, and a single source of truth during the response. Feed serious incidents into blameless post-incident reviews and a problem-management process that fixes root causes rather than repeatedly restarting the server. Control changes through a right-sized process — lightweight, standard, pre-approved changes for routine low-risk work; a change advisory review only for genuinely risky changes — so governance protects safety without becoming a bottleneck that tempts people to bypass it.

6. **Rehearse major incidents and clinical downtime, do not just document them.** Write, test, and regularly exercise business-continuity and clinical downtime procedures: how care continues on paper, how staff are told the system is down, how data is reconciled on recovery, and who declares and commands a major incident. Untested plans fail on the day. Link this explicitly to your clinical risk management and hazard log (see Chapter 4 — Clinical Safety & Risk Management), because downtime is a clinical hazard with a mitigation you can rehearse.

7. **Treat post-incident learning as blameless and systemic.** After every significant incident, run a review that asks how the system allowed the failure, not who to blame — because blame drives reporting underground and repeats the harm. Capture actions, assign owners, and track them to closure; feed patterns into problem management and design. A learning culture is a patient-safety control, mirroring the "just culture" of clinical incident reporting.

8. **Keep an accurate configuration record and manage the whole estate.** Maintain a CMDB or equivalent inventory of what runs, what depends on what, which versions are deployed, and who owns each service, so that during an incident you can answer "what does this affect?" in minutes. This underpins safe change, security patching, and licensing, and it is where most large NHS estates are weakest. An unknown, unpatched system is both an outage and a cyber-security incident waiting to happen (see Chapter 5).

9. **Make on-call sustainable and support human.** Design on-call rotas that are adequately staffed, fairly compensated, and humane, with clear escalation and realistic expectations — burned-out responders make slow, error-prone decisions in exactly the moments that matter most. Resource the service desk to the real demand of a 24/7 clinical workforce, and give front-line staff a fast, respected route to report problems. The quality of your support is the quality of care staff experience from your service.

10. **Plan decommissioning as a controlled operation.** Decide, while the service is live, how it will eventually be retired: data migration or archival under records-retention law, user redirection, clinician notification, and preservation of the hazard log and audit trail. An unplanned retirement strands data and users and can breach statutory retention duties. A planned one is an auditable operational project, not a scramble when the replacement arrives.

## Questions to discuss with your team

1. **When a critical clinical system goes down at 3am on a bank holiday, exactly who does what — and have we ever tested it?**
   This question forces the difference between a documented plan and a real capability. In health and care, downtime is a clinical event: the practical questions are who is paged, how fast they respond, who has authority to declare a major incident, how clinical staff are told to switch to downtime procedures, how patients stay safe on paper, and how data is reconciled on recovery. Debate whether your on-call rota actually has competent cover at unsociable hours and holidays, or whether it thins out to a single exhausted person when the risk is highest. Consider whether clinicians know the downtime procedure and have ever rehearsed it, or whether it lives in a binder no one has opened. A good, honest answer describes a tested response — with named roles, a real exercise in the last year, and lessons acted upon — not a policy document that has never met an outage. Where the honest answer is "we don't really know", that is itself the most important finding to surface to the board.

2. **Are we genuinely funding and staffing the "run", or did we celebrate go-live and quietly walk away?**
   Most of a service's cost and clinical risk lives after launch, yet funding models reward building new things and starve the running of old ones. The tension to debate is the structural pull of build funding versus the unglamorous, essential work of monitoring, patching, supporting, and iterating a live service for years. Look honestly at your live estate: how many services have a named owner, a funded team, current security patches, and working monitoring — and how many are orphaned, running on unsupported software, with no one accountable? Consider the "throw it over the wall to ops" pattern and whether the people running each service understand how it was built. A good answer can point to protected run budgets, named service owners for the operational life, and a deliberate service-transition rather than an abandonment, and it can name the orphaned services honestly so they can be adopted, replaced, or retired rather than left to fail.

3. **How do we decide what "reliable enough" means — and who gets a say?**
   Reliability is not free, and chasing an extra nine of availability can cost more than the harm it prevents; but in clinical systems, "acceptable" downtime is a safety judgement that engineers cannot make alone. This question asks whether you have explicit SLIs and SLOs, whether they were set with the clinicians and operational leaders who bear the consequences, and whether you use something like an error budget to balance shipping improvements against staying stable. Debate the difference between the internal target you manage to and the external SLA you promise, and whether your monitoring measures what clinicians actually experience or just what servers report. Consider whether "we aim for 99.9%" has any teeth — a defined measurement, a consequence when breached, an owner who acts. A good answer connects a reliability target to a clinical-safety rationale, shows the metric is measured and owned, and describes what the team does differently when the budget is spent, rather than a number in a slide no one manages to.

## In practice: a health & care example

An integrated care system (ICS) runs a shared care record used by hospital clinicians, GPs, community teams, and out-of-hours services across a region. It went live two years ago; the build programme has closed and a standing product-and-operations team now owns it. That team learned service management the hard way.

Early on, the record had monitoring only of server uptime. One winter evening, the servers were "green" while a failing integration silently stopped GP medication updates from flowing through — so hospital clinicians saw stale medication lists for several hours before a pharmacist noticed and phoned the service desk. The post-incident review was blameless and systemic: it found the real problem was the absence of an SLI reflecting the clinician's experience. The team added end-to-end observability, an SLO for data freshness agreed jointly with a clinical safety officer, and an alert that pages on-call when updates lag beyond the safety threshold. This hazard was added to the clinical risk hazard log (Chapter 4).

They then right-sized their practices. Routine, low-risk configuration updates became standard pre-approved changes shipped through an automated pipeline with fast rollback; only genuinely risky changes go to a weekly change review with clinical representation. A humane on-call rota covers nights and holidays, backed by a service desk resourced to the real 24/7 demand. Crucially, they wrote and now twice-yearly rehearse a clinical downtime procedure: a read-only cached copy of key records, a paper fallback, an SMS cascade to tell clinicians the system is degraded, and a reconciliation step on recovery. When a data-centre power fault took the primary system offline for forty minutes last spring, care continued on the tested fallback, the incident commander ran a calm coordinated response, and no patient was harmed. The board saw a reliability report tied to clinical-safety measures, not a vague reassurance — and the service's ownership through to eventual decommissioning is named and funded.

## Three sector lenses

### Startup

A small health-tech company often has no separate operations function, so "you build it, you run it" is the default rather than an aspiration — the same engineers who wrote the code carry the pager. The advantage is fast feedback and no wall to throw work over; the danger is a two-person on-call rota that is neither sustainable nor safe, and monitoring that stops at "is the server up?". Startups should adopt SLOs, basic observability, blameless post-incident reviews, and a written downtime procedure from the first NHS customer, because a clinical outage can end both the contract and the company. Even without ITIL ceremony, the intent — see the service, respond fast, learn systemically, keep patients safe when it fails — is non-negotiable in health.

### Enterprise

An NHS trust or large supplier runs service management in its fullest form: a formal service desk, ITIL-aligned incident/problem/change practices, change advisory boards, major-incident and business-continuity plans, and often a 24/7 operations centre. The characteristic challenge is a sprawling legacy estate with weak configuration records, unpatched systems, and unclear ownership — the conditions that turned WannaCry into a crisis. The classic failures are change processes so heavy that staff bypass them, and "run" perpetually starved to fund the next build. The enterprise has the resources to do observability, sustainable on-call, and tested continuity properly, so the task is to keep the practices proportionate and genuinely clinically owned rather than a paperwork ritual that gives false assurance.

### Government

A national body operates services that may touch millions, so an outage is a national incident with parliamentary and public-trust consequences, and reliability targets are matters of public accountability. Government delivery couples ITSM with the GOV.UK Service Manual's expectation that live services are properly operated, monitored, and iterated — not frozen at launch — and with statutory duties around records retention and cyber-security (NCSC, DSPT). Spend controls and multi-year funding settlements shape what "run" funding looks like, and the sheer scale raises the stakes on business continuity, coordinated major-incident response, and the safe decommissioning of legacy national systems with decades of records. The trade-off is assurance and resilience versus speed and cost, resolved in the open under scrutiny.

## Common failure modes

- **Throw it over the wall to ops.** A build team hands a service to an operations team that never saw it made; knowledge, ownership, and safety fall through the gap. Antidote: "you build it, you run it", or a deliberate transition with a warranty period and shared on-call.
- **The orphaned live service.** The project closes, the team disbands, run funding evaporates; the service rots, goes unpatched, and accrues clinical and cyber risk silently. Antidote: named service owner and protected run budget for the operational life.
- **Monitoring the servers, not the service.** Everything is "green" while clinicians see stale or missing data. Antidote: SLIs that reflect the user's and clinician's experience, with alerting on symptoms that matter.
- **Untested continuity plans.** A clinical downtime procedure exists on paper but has never been rehearsed, so it fails on the day. Antidote: exercise major-incident and downtime plans regularly and fix what breaks.
- **Blame-driven incident reviews.** Fault-finding drives reporting underground and repeats the harm. Antidote: blameless, systemic post-incident learning with tracked actions.
- **Change process theatre.** A change board so heavy that teams route around it, or so light that risky changes ship unchecked. Antidote: right-size — pre-approve standard changes, reserve review for genuinely risky ones.
- **No configuration record.** No one can answer "what will this change affect?" during an incident. Antidote: maintain a CMDB or equivalent with ownership and dependencies.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Run funding & ownership | No run budget; services orphaned at go-live | Run funded ad-hoc; ownership unclear | Named owners; protected run budget for operational life | Whole-life ownership; run and build balanced deliberately |
| Reliability targets | None; "up or down" only | Uptime measured but no agreed targets | SLIs/SLOs set, some with clinicians; SLAs defined | Error budgets manage feature-vs-stability; SLOs clinically owned |
| Observability & alerting | Little visibility; users report outages first | Server monitoring only; noisy or ignored alerts | Logs/metrics/traces; symptom-based alerts on user experience | Predictive detection; alerts tuned; near-misses caught early |
| Incident/problem/change | Firefighting; no post-incident learning | Incidents logged; root causes rarely fixed | Severity levels, blameless reviews, right-sized change control | Systemic learning feeds design; recurrence steadily falls |
| Continuity & major incident | No tested downtime plan | Plans documented but never exercised | Downtime and major-incident plans rehearsed periodically | Continuity proven in real events; drills routine and improving |

## Checklist

- [ ] Every live service has a named owner and a protected run budget for its operational life.
- [ ] The team that runs each service understands how it was built (or a documented transition with warranty and shared on-call exists).
- [ ] SLIs and SLOs are defined, and clinical systems' targets were set with clinicians; external SLAs are looser than internal SLOs.
- [ ] Observability (logs, metrics, traces) and symptom-based alerting reflect the clinician's and user's experience, not just server health.
- [ ] Incident management has severity levels, response targets, an incident-commander role, and a single source of truth during response.
- [ ] Problem management fixes root causes; post-incident reviews are blameless and their actions are tracked to closure.
- [ ] Change management is right-sized: standard changes pre-approved and automated; only risky changes reviewed, with clinical input.
- [ ] Business-continuity and clinical downtime procedures are written, linked to the hazard log, and rehearsed at least annually.
- [ ] On-call rotas are adequately staffed, humane, and fairly compensated; the service desk is resourced to real 24/7 demand.
- [ ] A configuration record (CMDB or equivalent) lists components, dependencies, versions, and owners, and supports security patching.
- [ ] A decommissioning plan covers data migration/archival under retention law, user redirection, and preservation of safety and audit records.

## Key sources

- ITIL 4 — the service value system and management practices (incident, problem, change, service desk, service level management) — PeopleCert / AXELOS.
- Google — *Site Reliability Engineering* and *The Site Reliability Workbook* (SLIs, SLOs, error budgets, on-call, blameless post-mortems).
- GOV.UK Service Manual — operating and iterating a live service; monitoring the status of a service; maintaining a service after launch.
- NHS England — clinical risk management standards DCB0129/DCB0160 and the treatment of system downtime as a clinical hazard (see Chapter 4).
- NHS England / NCSC — cyber-security operations, the Data Security and Protection Toolkit (DSPT), and lessons from the 2017 WannaCry incident (see Chapter 5).
- ISO/IEC 20000 (IT service management) and ISO 22301 (business continuity management systems).
- DevOps Research and Assessment (DORA) — capabilities linking delivery and operational performance (monitoring, change, reliability).
- OKRs and KPIs for operational and reliability reporting to leadership (see Chapter 34 — OKRs & KPIs).

## References

1. IT service management — Wikipedia — https://en.wikipedia.org/wiki/IT_service_management
2. ITIL — Wikipedia — https://en.wikipedia.org/wiki/ITIL
3. Incident management — Wikipedia — https://en.wikipedia.org/wiki/Incident_management
4. Change management (ITSM) — Wikipedia — https://en.wikipedia.org/wiki/Change_management_(ITSM)
5. Business continuity planning — Wikipedia — https://en.wikipedia.org/wiki/Business_continuity_planning
6. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
7. Service-level agreement — Wikipedia — https://en.wikipedia.org/wiki/Service-level_agreement
8. Service-level objective — Wikipedia — https://en.wikipedia.org/wiki/Service-level_objective
9. Service level indicator — Wikipedia — https://en.wikipedia.org/wiki/Service_level_indicator
10. Observability (software) — Wikipedia — https://en.wikipedia.org/wiki/Observability_(software)
11. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
12. Configuration management database — Wikipedia — https://en.wikipedia.org/wiki/Configuration_management_database
13. Help desk — Wikipedia — https://en.wikipedia.org/wiki/Help_desk
14. Site Reliability Engineering (SRE book) — Betsy Beyer, Chris Jones, Jennifer Petoff, Niall Richard Murphy (eds.), Google — https://sre.google/books/
15. ITIL 4 Foundation and service management practices — PeopleCert / AXELOS — https://www.peoplecert.org/browse-certifications/it-governance-and-service-management/ITIL-1/itil-4-foundation-2565
16. Service Manual: operating a service and monitoring its status — Government Digital Service, GOV.UK — https://www.gov.uk/service-manual/technology/monitoring-the-status-of-your-service
17. Clinical risk management standards DCB0129 and DCB0160 — NHS England (Clinical Safety) — https://digital.nhs.uk/services/clinical-safety
18. Investigation: WannaCry cyber attack and the NHS — National Audit Office — https://www.nao.org.uk/reports/investigation-wannacry-cyber-attack-and-the-nhs/
19. ISO/IEC 20000-1 — IT service management systems — International Organization for Standardization — https://www.iso.org/standard/70636.html
20. ISO 22301 — Security and resilience: business continuity management systems — International Organization for Standardization — https://www.iso.org/standard/75106.html
21. DevOps Research and Assessment (DORA) capabilities — Google Cloud / DORA — https://dora.dev/
