# Chapter 19 — DevOps & Engineering Excellence

**In one sentence:** In clinical systems, disciplined engineering — automated pipelines, small reversible releases, infrastructure as code, and observability — is what makes change *safer*, not riskier, and treating "how we build and run software" as a safety, equity, and public-trust concern is the mark of a mature digital health organisation.

## Why this matters in health and care

The way you engineer and operate software is a clinical-safety control in its own right. When a district nurse cannot see a medication change, when an e-referral silently fails, or when an outage locks clinicians out of a shared care record, the harm is not abstract inconvenience — it is delayed treatment, a missed allergy, a safeguarding gap. The engineering practices in this chapter determine whether a needed fix reaches production in ten minutes or ten weeks, and whether a bad change can be reversed cleanly or leaves clinicians working around a broken system for days.

There is a persistent and dangerous myth in regulated domains that *change is risk*, so the safest system is the one you touch least. The evidence points the other way. Systems that are rarely changed accumulate unpatched vulnerabilities, brittle manual deployment steps, and undocumented tribal knowledge; when change finally becomes unavoidable — a security patch, a regulatory deadline, a supplier withdrawal — it arrives as a large, risky, poorly understood "big bang". Organisations that deploy small changes frequently, with automation and fast rollback, experience *fewer* failures and recover from them faster. In health and care, that difference is measured in patient safety.

Engineering excellence is also an equity and public-trust issue. Software that is not observable hides the fact that a service performs worse for users on older devices or in areas of poor connectivity. An insecure software supply chain puts confidential patient information at risk (see Chapter 7 — Information Governance, Data Protection & Cyber Security). And because this is public money and public data, the sector increasingly expects code to be built to open, inspectable standards — sometimes literally in the open. How you work is therefore not a private engineering matter; it is accountable to patients, clinicians, and the public.

## Core concepts

**[DevOps](https://en.wikipedia.org/wiki/DevOps).** DevOps is a culture and set of practices that break down the traditional wall between the developers who *build* software and the operations staff who *run* it. Instead of "throwing code over the wall" to a separate team, the same people share ownership of a service from design through to live operation, supported by automation and fast feedback. It is primarily a way of working — shared responsibility, blameless learning, small batches — enabled by tooling, not a tool you buy.

**[Continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) and [continuous delivery](https://en.wikipedia.org/wiki/Continuous_delivery) ([CI/CD](https://en.wikipedia.org/wiki/CI/CD)).** Continuous integration (CI) means every developer merges small changes into a shared main branch frequently, each triggering an automated build and test run so problems surface within minutes. Continuous delivery (CD) extends this so that software is always in a releasable state and can be deployed to production through an automated, repeatable pipeline. *Continuous deployment* goes one step further, releasing every change that passes the pipeline automatically. Testing is the substance of the pipeline's gates — covered in depth in Chapter 20 — Testing & Quality Assurance.

**Trunk-based development and small, reversible releases.** Trunk-based development keeps everyone working close to a single main line in [version control](https://en.wikipedia.org/wiki/Version_control), integrating many times a day rather than nursing long-lived branches that drift apart and merge painfully. The paired discipline is to ship small, frequent, independently reversible changes. A small change is easy to review, easy to test, and — crucially in a clinical system — easy to roll back cleanly if something goes wrong.

**[Infrastructure as code](https://en.wikipedia.org/wiki/Infrastructure_as_code) (IaC).** Rather than configuring servers by hand, you define infrastructure in machine-readable files kept under version control. The environment becomes reproducible, reviewable, and auditable: you can rebuild it identically, see who changed what and why, and prove that test and production match. This is the foundation for reliable environments (see Chapter 24 — Technical Architecture, Cloud & Legacy).

**[Platform engineering](https://en.wikipedia.org/wiki/Platform_engineering) and developer experience.** Platform engineering treats the internal tools, pipelines, and environments that delivery teams depend on as a *product*, with the teams as its users. A well-built internal platform gives teams a "paved road" — secure defaults, pre-approved patterns, one-click deployment — so they can move quickly *and* safely without each reinventing compliance. Good developer experience is not indulgence; it is how you make the safe path the easy path.

**The [DORA](https://en.wikipedia.org/wiki/DevOps_Research_and_Assessment) metrics.** DevOps Research and Assessment (DORA) identified four measures that distinguish high-performing teams: *deployment frequency* (how often you release), *lead time for changes* (how long from commit to production), *change-failure rate* (what proportion of changes cause a problem), and *time to restore service* (how fast you recover). Together they reveal that speed and stability rise together — the teams that deploy most often also fail least and recover fastest.

**"You build it, you run it," SRE, and observability.** Popularised at Amazon, "you build it, you run it" means the team that writes a service also operates it, carries the pager, and feels its failures — closing the feedback loop between engineering choices and operational reality (see Chapter 21 — Service Management & Live Operations). [Site reliability engineering](https://en.wikipedia.org/wiki/Site_reliability_engineering) (SRE) is a specific implementation that applies engineering to operations, with explicit reliability targets and error budgets. [Observability](https://en.wikipedia.org/wiki/Observability_(software)) — the ability to understand a system's internal state from its outputs (metrics, logs, traces) — is what lets you detect and diagnose problems before patients and clinicians do.

**Secure software supply chain.** Modern software is assembled from many third-party components and dependencies. A [supply chain attack](https://en.wikipedia.org/wiki/Supply_chain_attack) exploits a trusted component to compromise everything that depends on it. Managing dependencies, scanning for known vulnerabilities, and maintaining a software bill of materials is core engineering hygiene, not an optional security extra.

**Coding in the open and [open-source software](https://en.wikipedia.org/wiki/Open-source_software).** UK government policy — expressed in the GDS Service Standard and the NHS Service Standard — asks teams to make new source code open by default and to use open standards. For publicly funded health software this improves scrutiny, reuse, and trust, provided patient data and genuine secrets are rigorously kept out of public repositories.

## Best practices

1. **Build a CI/CD pipeline before you build the service.** Establish automated build, test, and deployment from the first week, so every change flows through the same repeatable, auditable path to production. The pipeline is where your clinical-safety, security, and accessibility gates live as automated checks, giving you a documented, tamper-evident record of exactly what was deployed and when. In a regulated system this audit trail is not overhead — it is evidence for your clinical safety case (see Chapter 6 — Clinical Safety & Risk Management).

2. **Deploy small, frequent, reversible changes.** Prefer many small releases over occasional large ones, and design every change so it can be rolled back or disabled quickly. A tiny change that fails is easy to understand and reverse; a quarterly mega-release that fails is a clinical incident with a hundred suspects. Techniques such as feature flags, canary releases, and blue-green deployment let you expose change gradually and pull it back instantly — turning deployment from a feared event into a routine, low-drama act.

3. **Make fast, clean rollback a first-class safety control.** Rehearse rollback the way you rehearse a fire drill, and measure how long it actually takes. In a clinical system the single most valuable operational capability is the ability to return to a known-good state within minutes when a change causes harm. Rollback that has never been tested is a hope, not a control; prove it works and keep proving it.

4. **Treat infrastructure and configuration as code.** Define environments, networking, and configuration declaratively, under version control, and provision them automatically. This gives you reproducible environments, peer-reviewed changes, and the ability to rebuild after a failure or disaster (see Chapter 22 — Business Continuity & Disaster Recovery). Manual, hand-tuned "snowflake" servers are unrepeatable, undocumented, and the usual cause of "it worked in test but not in production".

5. **Use the DORA metrics to have honest conversations, not to rank people.** Track deployment frequency, lead time, change-failure rate, and time to restore as a system-level health signal, and watch them move together toward faster-and-safer. Resist turning them into individual or team league tables — DORA's own authors caution against this, because it drives gaming and hidden risk. The right use is diagnostic: a rising change-failure rate is telling you something about test coverage or batch size that a board should want to hear.

6. **Adopt "you build it, you run it," backed by observability.** Give delivery teams genuine ownership of their services in production, including on-call responsibility, so the people who make design choices live with the operational consequences. Underpin this with observability — metrics, structured logs, and traces, plus meaningful alerting tied to user impact — so teams find problems before clinicians report them. This closes the feedback loop that makes engineering choices better over time and connects directly to service management (Chapter 21).

7. **Secure the software supply chain continuously.** Maintain an inventory of dependencies, scan automatically for known vulnerabilities, pin and verify versions, and keep a software bill of materials so you can answer "are we affected?" within hours of the next widely publicised flaw. Restrict who and what can push to production, and protect secrets and credentials rigorously (see Chapter 25 — Identity & Access Management). In health and care a compromised dependency is a route to confidential patient data, so supply-chain hygiene is patient-safety and information-governance work.

8. **Set and enforce engineering standards, and manage technical debt deliberately.** Agree coding standards, automated linting, code review, and a clear "definition of done", so quality is built in rather than inspected in later. Track technical debt explicitly and pay it down as planned work, because unmanaged debt in a clinical system silently raises the cost and risk of every future change. Standards make code legible to the next engineer — and to the auditors, safety officers, and open-source reviewers who may need to read it.

9. **Code in the open where you safely can.** Follow the GDS and NHS expectation to make new source code open by default and reuse open standards, keeping patient data and secrets strictly out of public repositories through disciplined secrets management. Open code invites scrutiny that improves quality and security, enables reuse across a cash-strapped system, and builds public trust that software spending public money is doing what it claims. Where code genuinely cannot be opened (for example, some security-sensitive components), document the reason rather than defaulting to closed out of habit.

## Questions to discuss with your team

1. **Do we actually believe that changing our clinical systems more often makes them safer — and does our behaviour match that belief?**
   This question forces a team to confront the gap between the evidence and the instinct. The DORA research is clear that teams deploying small changes frequently have *lower* failure rates and recover faster, yet many health organisations still batch changes into rare, heavily gated releases in the name of safety, unintentionally making each one larger and riskier. Debate where your change-advisory processes genuinely reduce risk versus where they merely add delay that pushes teams toward big-bang releases. Look honestly at your last few incidents: were they caused by frequent small changes, or by rare large ones and unpatched neglect? Consider whether your rollback capability is real and rehearsed, because the case for frequent change rests entirely on being able to reverse it fast. A good answer is not ideological; it names the specific controls — automated testing, canary releases, tested rollback — that would let you increase change frequency *and* satisfy your clinical-safety and assurance obligations at the same time.

2. **Who runs our services in production at 2am, and what does that tell us about our engineering choices?**
   "You build it, you run it" is easy to endorse and hard to live. This question surfaces whether the people making architectural and delivery decisions actually feel the operational consequences, or whether pain is offloaded to a separate operations or service-desk team who cannot fix root causes. Explore the state of your observability: when a shared care record slows down, do you learn it from dashboards and alerts, or from an angry clinician? Discuss the human cost too — on-call must be humane, funded, and shared, or it becomes a burnout and retention problem, which in a workforce-constrained NHS is a serious risk (see Chapter 40 — Workforce Planning). There is a real trade-off between full team ownership and the reality that some smaller organisations and suppliers genuinely need a shared platform or managed service to run things reliably. A strong answer connects operational responsibility back to design: it identifies where the feedback loop between building and running is broken, and what you would change so that engineering choices are informed by the reality of live operation.

3. **How much of our code, and our engineering practice, could withstand being made public — and what does the answer reveal?**
   Government and NHS policy asks teams to code in the open by default, and this question uses that lens as a diagnostic even where full openness is not yet possible. If the prospect of publishing your repositories provokes anxiety, ask precisely why: is it hard-coded secrets, embedded patient data, absent tests, undocumented decisions, or simply unfamiliarity? Each of those is a real engineering-quality or information-governance problem that being closed merely hides rather than solves. Debate the genuine constraints — some security-sensitive code should stay closed, and getting secrets management right is a prerequisite — against the benefits of scrutiny, reuse across a cash-strapped system, and public trust in how health software spending is used. Consider the reputational and safety value of external eyes finding a flaw before an attacker does. A good, honest answer distinguishes code that is closed for a defensible, documented reason from code that is closed out of habit or embarrassment, and commits to fixing the underlying quality and hygiene issues either way.

## In practice: a health & care example

An integrated care system (ICS) runs a shared "single point of access" service that routes urgent community-care referrals to the right team. In its first two years the service was deployed by hand roughly once a quarter: a developer followed a wiki page of manual steps late on a Friday, and each release was a tense, all-hands event. When a referral-routing bug surfaced — occasionally sending complex-needs referrals to the wrong team — the fix sat in a queue for six weeks waiting for the next release window, and clinicians managed the risk with manual workarounds.

The new engineering lead reframes this as a clinical-safety problem, not merely an efficiency one. The team introduces a CI/CD pipeline: every change is small, peer-reviewed, and automatically built and tested, with accessibility and security checks and a clinical-safety sign-off step encoded as pipeline gates that produce an auditable record for the hazard log. Infrastructure is moved to code, so test and production environments finally match. Deployments move from quarterly to several times a week, released first to a single locality as a canary, with a tested rollback that returns to the last known-good state in under five minutes.

Six months on, the DORA metrics tell the story to the board in plain terms: lead time for a fix has fallen from six weeks to under a day, deployment frequency is up tenfold, and the change-failure rate has *dropped* because changes are now small and observable. When a subtle routing error recurs, observability dashboards flag the anomaly within minutes, the team rolls back before any referral is misrouted, ships a fix the next morning, and records a blameless post-incident review. The team also publishes the non-sensitive routing-rules engine as open source under the NHS Service Standard, and a neighbouring ICS reuses it. Changing the system more often has made it demonstrably safer.

## Three sector lenses

### Startup

A digital-health startup can adopt modern engineering practice from day one, with no legacy operations team to negotiate with — trunk-based development, CI/CD, and infrastructure as code are essentially free defaults in a small, greenfield team, and this is a genuine advantage. The risk is that "move fast" quietly drops the disciplines that health demands: automated tests, tested rollback, secrets management, and dependency scanning feel like friction when there is no regulator yet watching. The founders must recognise that clinical-safety and supply-chain obligations attach regardless of company size, and that one leaked patient dataset or unmanaged dependency can end the company. The pragmatic path is to lean on managed cloud platforms and a small, opinionated "paved road" so that a tiny team gets safety-by-default without building a platform group it cannot yet afford.

### Enterprise

A large NHS trust or major health-tech supplier has the resources to do platform engineering, observability, and "you build it, you run it" properly, but is held back by legacy systems, siloed development-and-operations teams, and change-advisory processes built for a slower era. The characteristic failure is a heavyweight change board that, in trying to control risk, forces large batched releases that are *more* dangerous than the frequent small ones it fears. The opportunity is to invest in an internal developer platform that bakes compliance, security, and clinical-safety gates into a paved road, so dozens of teams inherit good practice instead of each negotiating it. Scale here is the double-edged sword: the blast radius of a bad deployment is enormous, which is exactly why automation, canary releases, and tested rollback are essential rather than optional.

### Government

A national body such as NHS England or a devolved health department sets the standards others follow — the NHS and GDS Service Standards, the spend controls, the expectation to code in the open — and is accountable to Parliament and the public for how software is built and run. Its engineering choices ripple across the system: a well-run national platform, published open-source components, and clear supply-chain guidance raise the floor for every trust and supplier. The constraints are real — multi-year funding, procurement rules, and the sheer scale and sensitivity of national data mean deployment cadence is more measured than in a startup. The government lens must balance exemplary transparency and reuse against the security of nationally critical systems, deciding deliberately what is opened and what is protected, and documenting the reasoning either way.

## Common failure modes

- **"Change is risk" paralysis.** Deploying rarely to feel safe, which produces large, dangerous, poorly understood releases and unpatched neglect. Antidote: small, frequent, reversible changes with tested rollback.
- **The wall between dev and ops.** Developers "throw code over the wall" to a separate operations team that cannot fix root causes; nobody owns the whole loop. Antidote: shared ownership and "you build it, you run it", supported humanely.
- **Manual, snowflake deployments.** Releases depend on one person and a wiki page; environments drift and "works in test, breaks in production" is routine. Antidote: CI/CD plus infrastructure as code.
- **Metrics as a stick.** DORA numbers used to rank teams, driving gaming and hidden risk. Antidote: use them as a system-level diagnostic, per DORA's own guidance.
- **Alert-blind operations.** No observability, so patients and clinicians discover failures first. Antidote: metrics, logs, traces, and user-impact alerting.
- **Neglected supply chain.** Unpatched dependencies and unscanned components become the breach. Antidote: continuous scanning, a software bill of materials, and protected pipelines.
- **Accidental exposure.** Coding in the open done carelessly, leaking secrets or patient data. Antidote: rigorous secrets management and pre-publication scanning, not a retreat to closed-by-default.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Build & release | Manual, infrequent, one-person deployments | Partial automation; releases still batched and feared | CI/CD pipeline with automated tests and gates | Continuous delivery of small changes; deployment is routine |
| Change & rollback | No rollback plan; failures linger | Rollback exists on paper, rarely tested | Tested rollback; canary/feature-flag releases | Fast rollback as a proven, drilled clinical-safety control |
| Infrastructure | Hand-configured snowflake servers | Some scripting; environments drift | Infrastructure as code, version-controlled | Fully reproducible, self-service, disaster-recoverable |
| Run & observe | Separate ops team; failures found by users | Basic monitoring; reactive firefighting | Team runs its service; metrics, logs, traces, alerting | "You build it, you run it" with SLOs and blameless learning |
| Supply chain & openness | Dependencies unmanaged; all code closed | Occasional manual scanning; openness ad hoc | Automated scanning, SBOM; open where safe | Continuous supply-chain assurance; open-by-default with reuse |

## Checklist

- [ ] A CI/CD pipeline builds, tests, and deploys every change through one auditable path, with safety/security/accessibility gates encoded.
- [ ] Changes are small, frequent, and independently reversible (feature flags, canary or blue-green releases).
- [ ] Rollback to a known-good state is tested regularly and completes within a documented, short time.
- [ ] Infrastructure and configuration are defined as version-controlled code; test and production environments match.
- [ ] The four DORA metrics are tracked as a system-level signal, not used to rank individuals or teams.
- [ ] Delivery teams own their services in production, with humane, funded on-call and meaningful observability (metrics, logs, traces, alerting).
- [ ] Dependencies are inventoried and scanned automatically; a software bill of materials exists and secrets are protected.
- [ ] Engineering standards, code review, and a definition of done are agreed; technical debt is tracked and paid down as planned work.
- [ ] New source code is open by default where safe, with rigorous checks that no patient data or secrets are exposed.
- [ ] Engineering practice is documented so a new engineer, auditor, or safety officer can understand what runs and why (see Chapter 57).

## Key sources

- Nicole Forsgren, Jez Humble & Gene Kim, *Accelerate: The Science of Lean Software and Development and DevOps* — the DORA research and the four key metrics.
- DORA (DevOps Research and Assessment) — annual State of DevOps reports and capability catalogue — dora.dev.
- Jez Humble & David Farley, *Continuous Delivery* — the deployment pipeline and release automation.
- Betsy Beyer et al. (eds.), *Site Reliability Engineering* — Google's SRE book on running production systems.
- NHS England — NHS Service Standard and NHS Digital Service Manual (including coding in the open and open standards).
- GOV.UK Service Manual / Government Service Standard (GDS) — "make new source code open", continuous delivery, and operating a service.
- National Cyber Security Centre (NCSC) — guidance on secure software development and supply chain security.
- NHS England — Clinical risk management standards DCB0129 and DCB0160 (engineering change as part of the clinical safety case).

## References

1. DevOps — Wikipedia — https://en.wikipedia.org/wiki/DevOps
2. CI/CD — Wikipedia — https://en.wikipedia.org/wiki/CI/CD
3. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
4. Continuous delivery — Wikipedia — https://en.wikipedia.org/wiki/Continuous_delivery
5. Version control — Wikipedia — https://en.wikipedia.org/wiki/Version_control
6. Infrastructure as code — Wikipedia — https://en.wikipedia.org/wiki/Infrastructure_as_code
7. Platform engineering — Wikipedia — https://en.wikipedia.org/wiki/Platform_engineering
8. DevOps Research and Assessment (DORA) — Wikipedia — https://en.wikipedia.org/wiki/DevOps_Research_and_Assessment
9. Site reliability engineering — Wikipedia — https://en.wikipedia.org/wiki/Site_reliability_engineering
10. Observability (software) — Wikipedia — https://en.wikipedia.org/wiki/Observability_(software)
11. Supply chain attack — Wikipedia — https://en.wikipedia.org/wiki/Supply_chain_attack
12. Open-source software — Wikipedia — https://en.wikipedia.org/wiki/Open-source_software
13. Accelerate: The Science of Lean Software and DevOps — Nicole Forsgren, Jez Humble & Gene Kim (IT Revolution) — https://itrevolution.com/product/accelerate/
14. DORA — DevOps Research and Assessment — Google Cloud / DORA — https://dora.dev/
15. Continuous Delivery — Jez Humble & David Farley — https://continuousdelivery.com/
16. Site Reliability Engineering — Google (O'Reilly) — https://sre.google/books/
17. NHS Service Standard — NHS England — https://service-manual.nhs.uk/standards-and-technology/service-standard-points
18. Making source code open and reusable — Government Digital Service, GOV.UK Service Manual — https://www.gov.uk/service-manual/technology/making-source-code-open-and-reusable
19. Secure software development and supply chain security — National Cyber Security Centre (NCSC) — https://www.ncsc.gov.uk/collection/developers-collection
20. Clinical risk management standards DCB0129 and DCB0160 — NHS England — https://digital.nhs.uk/services/clinical-safety
