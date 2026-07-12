# Chapter 5.1 — Project-Led Work

**In one sentence:** Project-led work is the right tool when the job has a defined scope, a finite life, and a clear end state — a temporary, controlled endeavour delivered to agreed time, cost, and quality, then closed.

## Why this matters in health and care

Not everything is a living service. Some of the most important work in health and care is genuinely finite: [migrating](https://en.wikipedia.org/wiki/Data_migration) from one [electronic patient record](https://en.wikipedia.org/wiki/Electronic_health_record) to another, rolling out Wi-Fi across a hospital estate, replacing end-of-life servers, decommissioning a legacy system before a supplier contract ends, or delivering the digital element of a new hospital build. This work has a beginning, a middle, and a definite end. Managing it as an open-ended product would waste money and blur accountability; it needs the discipline of a project.

[Project management](https://en.wikipedia.org/wiki/Project_management) earns its keep here precisely because the stakes are high and the constraints are hard. A data-migration cutover has a fixed go-live weekend, a patient-safety risk if records are lost or corrupted, and a contractual cliff-edge if the old system switches off. Public money is committed against a business case, and Parliament, auditors, and boards will ask whether it was spent as approved. Project-led work provides the governance — a business case, stage gates, and a controlled close — that lets a board commit capital with confidence and stop the work cleanly if the justification falls away.

The danger is using this tool for the wrong job. Project-led governance applied to an evolving digital service produces the "build it and abandon it" pathology described in Chapter 5.0 — Product-Led Work. This chapter explains where project-led work is the right instrument, and where its limits begin. It sits alongside Chapter 5.2 — Programme-Led Work, which coordinates multiple projects, and Chapter 5.3 — Enterprise Portfolio & Project Management (EPPM), which chooses between these tools.

## Core concepts

**Project.** A temporary organization created to deliver one or more defined outputs to an agreed specification, within constraints of time, cost, and quality. The defining feature is that it is *temporary* — it exists to reach a defined end and then disband.

**The [iron triangle](https://en.wikipedia.org/wiki/Project_management_triangle) (scope, time, cost).** The classic constraint model: scope, schedule, and budget are interdependent, and quality is affected by how they are balanced. Change one and you change the others; project control is largely the discipline of managing this trade-off transparently.

**[PRINCE2](https://en.wikipedia.org/wiki/PRINCE2) (PRojects IN Controlled Environments).** The UK government's structured project method, widely used across the NHS and public sector. It is built on principles (continued business justification, defined roles, manage by stages, manage by exception, focus on products, learn from experience, tailor to the environment) and organizes work into controlled stages with a project board providing direction.

**PMI / PMBOK.** The [Project Management Institute](https://en.wikipedia.org/wiki/Project_Management_Institute)'s *[Guide to the Project Management Body of Knowledge](https://en.wikipedia.org/wiki/Project_Management_Body_of_Knowledge)* is the dominant international counterpart, framing project work around performance domains and principles rather than a prescribed staged process. PRINCE2 and PMBOK are complementary lenses on the same discipline.

**[Business case](https://en.wikipedia.org/wiki/Business_case).** The document that justifies the project: the problem, the options appraised, the expected benefits, the costs, and the risks. In PRINCE2 the business case is living — it is checked at every stage boundary, and if continued justification disappears, the right decision is to stop. In UK public bodies this is usually structured as [HM Treasury](https://en.wikipedia.org/wiki/HM_Treasury)'s Five Case Model (strategic, economic, commercial, financial, management).

**[Stage gates](https://en.wikipedia.org/wiki/Phase-gate_process).** A PRINCE2 project is divided into management stages separated by decision gates. At each boundary the project board makes a deliberate stop/proceed decision: it reviews progress and the business case, approves the next stage plan, and commits resources only for that stage. This is how a board keeps control and avoids throwing good money after bad.

**RAID log.** A single register of Risks, Assumptions, Issues, and Dependencies — the project manager's core control artefact. RAID makes uncertainty visible and manageable: risks are things that might happen, issues are things that have, assumptions are what the plan relies on, and dependencies are what the plan needs from elsewhere.

## Best practices

1. **Start with an honest business case and keep it alive.** Use a recognized structure (the Five Case Model in UK public bodies) to appraise real options, not a single predetermined answer. Then treat the business case as a living document reviewed at every stage gate — continued business justification is the first PRINCE2 principle, and losing it is a legitimate reason to stop.

2. **Define scope precisely and control changes to it.** The value of a project is a clear, bounded definition of "done". Agree the scope, baseline it, and run every proposed change through a change-control process so [scope creep](https://en.wikipedia.org/wiki/Scope_creep) does not quietly consume the budget and the timeline.

3. **Manage by stages with real decision gates.** Break the work into management stages and hold a genuine stop/proceed review at each boundary. A gate that always says "proceed" is theatre; the discipline only works if stopping or re-planning is a real option the board will exercise.

4. **Run a live RAID log and escalate by exception.** Maintain Risks, Assumptions, Issues, and Dependencies in one place, review it regularly, and use PRINCE2's "manage by exception" — the project manager runs within agreed tolerances and escalates to the board only when a tolerance is threatened. This keeps senior time focused on genuine decisions.

5. **Assign clear, single-point accountability.** PRINCE2 insists on defined roles: a project board with a senior responsible owner/executive owning the business case, a senior user representing those who will use the output, and a senior supplier. Ambiguous accountability is the most common cause of drift.

6. **Plan the transition to live service before you start.** A project delivers an output; someone must operate it afterwards. Agree the receiving team, the support model, and the clinical-safety handover (DCB0160 for deployment) as part of the project, so go-live is not a cliff-edge into an ownership vacuum.

7. **Bake in clinical safety, information governance, and testing.** For any system touching patient data, the clinical safety case, DPIA, and cutover/rollback testing are not optional extras — they are gating deliverables. A migration without a tested rollback plan is not ready to go live.

8. **Close the project deliberately and capture lessons.** A defined end means a defined close: confirm the outputs are accepted, hand over to operations, release the team, and record lessons learned (PRINCE2's lessons log). An un-closed project leaks resources and accountability indefinitely.

## Questions to discuss with your team

1. **Is the work in front of us genuinely finite with a defined end state, or are we reaching for project governance because it is the funding route we know?**
   This is the decisive question the chapter turns on, because project-led discipline is the right instrument only when the job truly has a beginning, a middle, and a definite end. In a health and care organization the pull toward project shape is strong — capital budgeting, business-case machinery, and board reporting are all built for it — so an evolving digital service can get dressed up as a project simply because that is how money is released, which then produces the build-it-and-abandon-it pathology. The debate should examine each candidate honestly: a pathology system replacement before a supplier withdraws support has a hard contractual cliff-edge and is unambiguously finite, whereas "improve the patient app" has no end state and belongs in Chapter 5.0. Consider whether there is a real go-live after which the team should disband, or whether someone will need to keep improving the thing indefinitely. A good answer resists using project governance as a habit, names the concrete end state and the event that defines "done", and is willing to say that some of what we currently run as projects should never have been projects at all.

2. **At our stage gates, would this board actually stop or re-plan a project that has lost its justification — and can we point to a time we did?**
   Stage gates are only a control if stopping is a genuine option the board will exercise; a gate that always says "proceed" is theatre, and continued business justification is the first PRINCE2 principle precisely because losing it should end the work. The tension in health and care is acute: halting a part-built EPR migration or a laboratory-system cutover feels like admitting failure, wasting sunk cost, and disrupting clinicians who have already changed their plans, so boards rationalize pressing on even as the business case quietly evaporates. Bring a real example to the discussion — a project where testing revealed the data-mapping risk was worse than assumed, or where benefits slipped — and ask whether the gate was used as designed or rubber-stamped. Consider what tolerances trigger escalation, who at the board has the standing to call a stop, and whether sunk-cost reasoning is named and challenged in the room. An honest answer admits where gates have been formalities, describes the conditions under which the board genuinely would halt or re-scope, and treats the authority to stop before a public write-off as the discipline's real value rather than a threat.

3. **Who receives each project's output as a live service, and how do we make clinical-safety handover and ongoing ownership a gating deliverable rather than a cliff-edge?**
   A project delivers an output; something finite ends, but the thing it produced must be operated, improved, and kept safe long after the team disbands — and the most common quiet failure is that no one owns it on the other side. In a system touching patient data this is not administrative tidiness: the DCB0160 deployment safety case, the DPIA, a tested rollback, and a named receiving team are what stand between a controlled go-live and an ownership vacuum where safety risks accumulate unmanaged. The debate should force clarity about the transition before the project starts, not at go-live weekend: which operational team takes it, what the support model is, and whether that team has the capacity and mode of work (product-led, per Chapter 5.0) to keep improving it. Consider concrete recent go-lives and whether the handover was planned or improvised, and whether "the project is done" was allowed to mean "and now it is nobody's job". A good answer names the receiving team and support model up front, treats the safety handover as a gate the project cannot pass without, and explicitly assigns the ongoing improvement of the live service to the right mode of work rather than leaving it to drift.

4. **When the iron triangle bites and scope, time, and cost collide, which constraint do we flex, and is patient safety ever allowed to be the variable that gives?**
   Every real project eventually hits the moment where the schedule, the budget, and the promised scope cannot all hold, and how the team resolves that squeeze reveals what it actually values. In health and care the trap is distinctive: because the end date is often a hard contractual cliff-edge — a supplier withdrawing support, a lease expiring, a data-centre closing — time frequently cannot move, so the pressure lands silently on quality, which in a clinical system means cutting testing, compressing validation, or shipping with known data-mapping defects. The discussion should name, in advance, which corner of the triangle the organization will protect and which it will sacrifice, and be explicit that clinical safety and information governance are not the release valve even when everything else is fixed. Look at a recent cutover and ask what quietly gave when the dates held: was it the rollback rehearsal, the clinical-validation window, the training? Consider who has the authority to move the go-live date rather than erode the safety margin, and whether that conversation happens openly at the board or by default on the ground. An honest answer states the priority order before the crunch, treats a slipped date or a re-planned stage as a legitimate outcome, and refuses to let unspoken schedule pressure convert into unlogged clinical risk.

5. **Is our RAID log a live instrument that changes what we do, or a document we maintain to look governed — and would it surface the risk that actually sinks the project?**
   A RAID log earns its place only if reviewing it changes decisions; the common pathology is a register written at kick-off, presented at boards, and never genuinely acted on while the risks that matter mature unwatched. In a migration or cutover the decisive risks are often specific and knowable — historical results that will not map cleanly to new reference ranges, a dependency on another team's firewall changes, an assumption that clinical validation resource will be free when it is needed — and the question is whether the log names those concretely or hides behind generic entries like "resource constraints". The debate should test whether escalation by exception is real: does the project manager run within agreed tolerances and raise the board's attention only when one is threatened, or does everything either stay silent or become a crisis? Consider whether near-misses and materialized issues feed back into how the next stage is planned, or simply get logged and forgotten. A good answer can point to a decision the RAID log actually changed, distinguishes the two or three risks that could genuinely stop the project from the long tail of minor ones, and treats the log as a working control rather than an artefact produced for assurance.

6. **After we close and disband, does anyone check whether the benefits in the business case actually materialized — and would we know if they did not?**
   The business case promises benefits to justify the spend, but project-led work naturally ends at go-live and team release, so the moment of truth — did the migration actually reduce risk, cut cost, or improve care — usually falls after everyone has moved on and no one is accountable for confirming it. This matters acutely in public health and care, where money is committed against a Five Case business case that Parliament, auditors, and boards were told would deliver specific outcomes, yet benefits realization is the step most often skipped because the project that would have owned it no longer exists. The discussion should decide who inherits benefits tracking when the project closes, over what period, and against which baseline measurements — which have to be captured before go-live or they are lost. Consider a recent completed project and ask plainly whether anyone has since checked its promised benefits, and whether a shortfall would ever reach the board that approved it. An honest answer assigns post-closure benefits ownership to a standing function rather than the disbanded team, captures the baseline while the project is still live, and is willing to record that a project delivered its output on time and to budget yet did not deliver the value that justified it.

## In practice: a health & care example

An acute trust must replace its ageing pathology laboratory information management system before the incumbent supplier withdraws support in 14 months. This is textbook project-led work: fixed end date, defined scope, a hard contractual cliff-edge, and acute patient-safety risk if results are lost in migration.

The trust writes a Five Case business case appraising three options (upgrade in place, procure a new system, share a regional instance), selects procurement, and stands up a PRINCE2 project with a clear board: an executive owning the business case, a senior user (the lead biomedical scientist), and the senior supplier. The work is split into management stages — procurement, build and configuration, data migration, testing, and go-live — each ending in a decision gate.

The project manager runs a RAID log. A key risk is that historical results may not map cleanly to the new system's reference ranges; a dependency is the network team's firewall changes; an assumption is that clinical validation resource will be available for testing. At the migration stage gate, testing reveals the data-mapping risk is worse than assumed, so the board uses the gate as designed: it does not blindly proceed, but approves a re-planned stage with an extended validation window and a tested rollback plan, protecting patient safety over the original schedule.

Go-live happens over a controlled weekend with the rollback plan on standby and a DCB0160 clinical-safety sign-off. The system is accepted, handed to the operations team who will run it, lessons are logged, and the project is formally closed. The team disbands — correctly, because the job is genuinely done. What comes next (continuous improvement of the live service) is a different mode of work, and the trust is careful not to keep a full project team running perpetually to do it.

## Sector lenses

### Startup

A small digital-health company rarely runs formal PRINCE2 projects, but genuinely finite work still appears — a one-off data migration onto a new cloud platform, a Cyber Essentials or DTAC certification push, pen-test remediation before a big NHS contract. The startup handles these as lightweight, time-boxed efforts with a named owner and a clear definition of done, borrowing the discipline (fixed scope, an end date, a go/no-go) without the ceremony (no formal project board, no five-stage gating). Funding is really founder attention and runway, so the risk is that finite work gets squeezed between product sprints and never actually closed. The corrective is naming a single owner and a hard deadline, and treating the certification or migration as done-and-dusted rather than perpetually "in progress".

### Small business

An established small provider — a GP practice, a community pharmacy, a care home, or a single-site clinic — meets project-led work as occasional but unavoidable events: switching clinical system supplier, migrating to a new practice-management platform, or replacing end-of-life devices before support lapses. The organization has real patients and ongoing operations but no dedicated project or IT function, so the "project team" is usually the practice manager or a registered manager doing this alongside the day job, often leaning on the incoming supplier to run the migration. The discipline that survives contact with this reality is the lightweight core: a clear end state, a baselined scope so the supplier does not quietly expand it, a named accountable person, and a tested rollback before any cutover that touches patient records. The trap is outsourcing not just the work but the judgement — accepting the supplier's go-live date and data-mapping assurances without independent checking — because the same clinical-safety and information-governance duties (DCB0160, a DPIA) apply regardless of how small the organization is. The corrective is to keep ownership of the go/no-go decision and the acceptance criteria in-house, even when every other pair of hands belongs to the vendor.

### Enterprise

A large NHS trust or integrated care system (ICS) is where project-led work is most at home: EPR replacements, estate-wide Wi-Fi, data-centre exits, and cutovers all carry hard contractual and patient-safety cliff-edges. Here the full apparatus is justified — a Five Case business case, a PRINCE2 board with a named executive/SRO, senior user and senior supplier, management stages with real gates, and a live RAID log — because the sums are large, the safety exposure is acute, and internal audit and the board will scrutinize the spend. The characteristic failure at this scale is applying the same governance indiscriminately to living services (Chapter 5.0 — Product-Led Work) and to finite work, so a portfolio view (Chapter 5.3 — Enterprise Portfolio & Project Management) that routes each piece of work to the right mode matters. Clinical safety (DCB0160) and a tested rollback are gating deliverables, not optional extras.

### Government

At national or major-project scale, project-led work sits inside the government's assurance regime: the Infrastructure and Projects Authority runs gateway reviews, HM Treasury's Green Book and Five Case Model govern the business case, and the largest projects enter the Government Major Projects Portfolio with published accountability to Parliament and the National Audit Office. Accountability is intensely public — the senior responsible owner is personally accountable and may be called before a select committee — so stage gates and options appraisals are statutory-grade control, not theatre. Funding is released tranche-by-tranche against approved business cases and the risk appetite is low, because failure becomes front-page news. The discipline's real value here is the authority to stop or re-scope a failing project before it becomes a public write-off.

## Common failure modes

- **Project-managing an evolving service.** Applying fixed-scope, disband-at-the-end governance to a living digital product produces the abandonment pathology. Fix: use product-led work (Chapter 5.0) where the service is ongoing.
- **The business case as a one-off ticket to funding.** Written once to unlock money, then never revisited. Fix: review it at every stage gate; be willing to stop.
- **Rubber-stamp stage gates.** Gates that never say "stop" provide no control. Fix: make stopping or re-planning a genuine board option and use it.
- **Scope creep with no change control.** Uncontrolled additions blow time and cost. Fix: baseline scope and route every change through change control.
- **No transition-to-service plan.** The project ends and no one owns the output. Fix: agree the receiving team and support model before go-live.
- **RAID as a filing cabinet.** A log that is written and never acted on. Fix: review RAID regularly and escalate by exception.
- **Never actually closing.** Zombie projects that consume resource with no end. Fix: a deliberate close with acceptance, handover, and lessons captured.

## Maturity model

| Dimension | Initiate | Develop | Standardize | Manage | Orchestrate |
|---|---|---|---|---|---|
| Justification | Funding sought without options appraisal | Business case written once, then shelved | Living business case (Five Case) reviewed at each gate | Business case tracked against quantified benefit targets and assured at each gate | Board routinely stops/re-plans projects that lose justification |
| Scope control | Scope vague; creep unmanaged | Scope defined but changes ad hoc | Scope baselined with formal change control | Change impact quantified; throughput and residual creep measured against baseline | Change control is fast, transparent, and trusted |
| Governance | No clear board or roles | Board exists but gates are formalities | PRINCE2 roles clear; real stop/proceed gates | Tolerances set and monitored; gate decisions evidenced by tracked metrics | Manage-by-exception frees senior time for real decisions |
| Risk & control | Risks tracked informally or not at all | RAID log exists but stale | Live RAID; escalation by exception | Risk exposure quantified and controls assured against agreed appetite | RAID drives decisions; near-misses feed lessons |
| Closure & transition | Projects drift, never formally closed | Handover ad hoc | Deliberate close; service transition planned | Closure and benefits realization measured post-handover against baseline | Lessons systematically reused across projects |

## Checklist

- [ ] Is the work genuinely finite with a defined scope and end state (not an ongoing service)?
- [ ] Is there a living business case (Five Case Model) reviewed at each stage gate?
- [ ] Is scope baselined, with a working change-control process?
- [ ] Are the work stages defined, each ending in a real stop/proceed decision gate?
- [ ] Are project board roles clear — executive/SRO, senior user, senior supplier?
- [ ] Is a live RAID log maintained, with escalation by exception?
- [ ] Are clinical safety (DCB0160), DPIA, and cutover/rollback testing gating deliverables?
- [ ] Is the receiving operations team and support model agreed before go-live?
- [ ] Is there a deliberate close: acceptance, handover, team release, lessons logged?
- [ ] Has the ongoing improvement of the live service been assigned to the right mode of work?

## Key sources

- AXELOS / PeopleCert — *Managing Successful Projects with PRINCE2* (7th edition) and the PRINCE2 principles, themes, and processes.
- Project Management Institute (PMI) — *A Guide to the Project Management Body of Knowledge (PMBOK Guide)* and *The Standard for Project Management*.
- HM Treasury — *Guide to Developing the Project Business Case* (the Five Case Model / Green Book).
- Infrastructure and Projects Authority (IPA), Cabinet Office — assurance and gateway review guidance for major projects.
- NHS Digital Clinical Safety standard DCB0160 (deployment of health IT systems).
- NHS England — NHS Service Manual and Digital Service Standard (for service-transition and user-need context).

## References

1. Project management — Wikipedia — https://en.wikipedia.org/wiki/Project_management
2. PRINCE2 — Wikipedia — https://en.wikipedia.org/wiki/PRINCE2
3. Project management triangle (iron triangle) — Wikipedia — https://en.wikipedia.org/wiki/Project_management_triangle
4. Project Management Institute — Wikipedia — https://en.wikipedia.org/wiki/Project_Management_Institute
5. Project Management Body of Knowledge — Wikipedia — https://en.wikipedia.org/wiki/Project_Management_Body_of_Knowledge
6. Business case — Wikipedia — https://en.wikipedia.org/wiki/Business_case
7. Phase-gate process (stage gates) — Wikipedia — https://en.wikipedia.org/wiki/Phase-gate_process
8. Scope creep — Wikipedia — https://en.wikipedia.org/wiki/Scope_creep
9. Data migration — Wikipedia — https://en.wikipedia.org/wiki/Data_migration
10. Electronic health record — Wikipedia — https://en.wikipedia.org/wiki/Electronic_health_record
11. HM Treasury — Wikipedia — https://en.wikipedia.org/wiki/HM_Treasury
12. *Managing Successful Projects with PRINCE2* (7th edition) — AXELOS / PeopleCert — https://www.peoplecert.org/browse-certifications/project-programme-and-portfolio-management/PRINCE-2-1005
13. *A Guide to the Project Management Body of Knowledge (PMBOK Guide)* — Project Management Institute — https://www.pmi.org/
14. *The Green Book* and *Guide to Developing the Project Business Case* (Five Case Model) — HM Treasury — https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-governent
15. Assurance and gateway review guidance for major projects — Infrastructure and Projects Authority, Cabinet Office — https://www.gov.uk/government/organisations/infrastructure-and-projects-authority
16. Clinical risk management standard DCB0160 — NHS England — https://digital.nhs.uk/services/clinical-safety
