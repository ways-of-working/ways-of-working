# Chapter 17 — Testing & Quality Assurance

**In one sentence:** In health and care, [testing](https://en.wikipedia.org/wiki/Software_testing) and [quality assurance](https://en.wikipedia.org/wiki/Quality_assurance) are not a phase you do before release but a continuous discipline that provides much of the evidence a service is clinically safe, accessible, secure, and fit to touch a patient's care.

## Why this matters in health and care

Every digital service carries defects; the only questions are how many, how serious, and whether you find them before or after a patient is affected. In a consumer app an undetected bug wastes a user's afternoon. In a clinical system it can display the wrong patient's allergies, round a paediatric drug dose incorrectly, or silently drop a referral into a queue no one monitors. Testing is the organised effort to find those defects early, and quality assurance is the wider system of controls that keeps quality from depending on luck or heroics.

This is why testing in health IT is inseparable from clinical safety. The hazards recorded in a DCB0129/0160 hazard log (see Chapter 5 — Clinical Safety & Risk Management) are only genuinely mitigated when a test proves the mitigation works and keeps working after every subsequent change. A safety case that claims "the system prevents duplicate prescriptions" without a repeatable test behind it is an assertion, not assurance. Testing is the evidence base beneath the clinical safety argument.

The stakes are also about equity and public trust. A service that has never been tested against accessibility standards will exclude disabled users by default (see Chapter 8 — Digital Inclusion & Accessibility). A service tested only with copies of live patient records risks a data breach that erodes the trust the NHS depends on. And the money is not trivial: reworking a defect found in live operation costs many times more than catching it in design, and a serious clinical incident costs far more than either. Inadequate testing is not a saving; it is a deferred and inflated bill, sometimes paid in harm.

## Core concepts

**Testing versus quality assurance.** *Testing* is the act of exercising a system to find defects and confirm behaviour. *Quality assurance* is the broader set of processes — standards, reviews, definitions of done, gates — that build quality in rather than inspecting it in at the end. Testing tells you whether this build works; QA is why your builds tend to work at all. Both matter, and leaders often fund the first while neglecting the second.

**The test pyramid and shift-left.** A healthy test strategy has many fast, cheap [unit tests](https://en.wikipedia.org/wiki/Unit_testing) (checking individual functions), fewer [integration tests](https://en.wikipedia.org/wiki/Integration_testing) (checking components work together), and a small number of slow, expensive end-to-end tests (checking whole user journeys). This "test pyramid" keeps feedback fast and maintenance affordable. It pairs with [shift-left testing](https://en.wikipedia.org/wiki/Shift-left_testing) — moving testing earlier in the lifecycle, so defects are designed out cheaply rather than found in a frantic pre-release scramble. An inverted pyramid (mostly manual end-to-end tests) is slow, brittle, and a warning sign.

**Functional and non-functional testing.** *Functional testing* asks "does the system do what it should?" — correct calculations, correct workflows, correct data. [Non-functional testing](https://en.wikipedia.org/wiki/Non-functional_testing) asks "how well does it behave?" — performance and load (does it stay responsive when the whole trust logs on at 08:00?), security (can it be breached?), reliability, and accessibility. In health and care, non-functional failures are often the most dangerous: a system that is functionally perfect but times out during a resus call has failed clinically.

**Regression testing.** [Regression testing](https://en.wikipedia.org/wiki/Regression_testing) re-runs existing tests after a change to confirm that fixing or adding one thing has not broken another. In live clinical systems this is the single most important safety habit: most clinical software incidents come not from new features but from changes that quietly broke working behaviour. A trustworthy regression suite is what lets you change a live system without holding your breath.

**Test automation and continuous integration.** [Test automation](https://en.wikipedia.org/wiki/Test_automation) uses software to run tests repeatably, so a large suite executes in minutes on every change. Combined with [continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) — merging and automatically testing changes frequently — this turns testing from an occasional event into a constant safety net (see Chapter 16 — Delivery Lifecycles). Automation does not replace human judgement; it frees humans to do the exploratory and clinical testing machines cannot.

**Acceptance testing.** [Acceptance testing](https://en.wikipedia.org/wiki/Acceptance_testing), and specifically *user acceptance testing (UAT)*, is where real clinicians and users confirm the system works in their actual context before it goes live. Operational acceptance testing (OAT) confirms the service can be run, backed up, and recovered. UAT with genuine end users catches the workflow mismatches that no developer test will.

**Test environments and safe test data.** A [deployment environment](https://en.wikipedia.org/wiki/Deployment_environment) is a system where software runs — typically development, test, staging, and production tiers. Testing needs environments that resemble production but must never casually use live patient data. Safe practice uses [synthetic data](https://en.wikipedia.org/wiki/Synthetic_data) (artificially generated) or properly anonymised data, so that testing a referral form cannot leak a real citizen's diagnosis.

**Quality gates, definition of done, and defect management.** A *definition of done* states what "finished" means (tested, accessible, documented, safety-reviewed) so quality is not negotiable per feature. *Quality gates* are checkpoints a change must pass to progress. *Defect triage* is the disciplined process of assessing found defects for severity and clinical impact, and deciding what to fix, when, and what may ship as a known issue.

## Best practices

1. **Build the pyramid and shift testing left.** Invest in a broad base of fast automated unit and integration tests, run on every change, so defects surface within minutes of being written rather than weeks later in UAT. Reserve slow end-to-end tests for the handful of critical journeys — the prescription, the referral, the identity match. This makes testing cheaper and faster, which is what actually makes teams do more of it.

2. **Treat regression testing as a clinical safety control.** Before any change reaches a live clinical system, an automated regression suite must confirm that existing, safety-relevant behaviour still works. Map your highest hazards from the DCB0129/0160 hazard log directly to named regression tests, so a change that would reintroduce a known hazard fails the build automatically. This is the mechanism that lets you iterate on live systems without accumulating silent clinical risk.

3. **Never test with live patient data by default.** Provision test and staging environments with synthetic or robustly anonymised data, governed by the same information governance and DPIA discipline as production (see Chapter 6 — Information Governance, Data Protection & Cyber Security). If a specific test genuinely requires production-like data, treat it as a controlled exception with a documented lawful basis, minimisation, and audit — not as routine convenience. A test database is still a patient database.

4. **Test the non-functional requirements as seriously as the functional ones.** Run performance and load tests against realistic peak demand — shift handovers, Monday-morning logins, a regional outage rerouting traffic — because a clinical system that slows to a crawl under load has failed when it matters most. Include security testing and accessibility testing against the [Web Content Accessibility Guidelines](https://en.wikipedia.org/wiki/Web_Content_Accessibility_Guidelines) (WCAG) as standing, non-optional test types. Non-functional defects are easy to defer and expensive to discover in production.

5. **Automate accessibility testing, then verify it with people.** Automated WCAG checks catch a meaningful fraction of issues (missing labels, poor contrast, structure) cheaply on every build, but they miss the ones that matter most to real users of assistive technology. Pair automated scanning with manual testing by people using screen readers, keyboard-only navigation, and magnification. Accessibility is a legal duty for public bodies and a clinical-safety issue when the excluded user is a clinician or a patient managing their own care.

6. **Run user acceptance testing with real clinicians in realistic conditions.** Schedule UAT with the actual people who will use the system — nurses, GPs, administrators, pharmacists — exercising real workflows, ideally in a setting that mirrors the ward or clinic, not a quiet meeting room. Their feedback catches dangerous workflow mismatches (a warning shown at the wrong moment, a default that invites error) that unit tests cannot. Budget clinical backfill time so UAT is done properly, not squeezed into goodwill.

7. **Make the definition of done and quality gates explicit and enforced.** Agree what "done" means for your context — passing tests, accessibility conformance, security scan clear, clinical safety review complete, documentation updated — and enforce it as a gate, not a wish. A definition of done that is written but routinely waived under deadline pressure is worse than none, because it launders unsafe work as complete. Gates should be automated where possible so they cannot be quietly skipped.

8. **Triage and manage defects with clinical severity front of mind.** Assess every defect not only for technical severity but for clinical impact and likelihood, using the same risk lens as your hazard log. A cosmetic bug can wait; a defect that could contribute to a wrong dose blocks release regardless of the go-live date. Maintain a visible defect register, and be honest about known issues shipped as accepted, mitigated risks rather than hidden ones.

9. **Integrate testing into the delivery pipeline, not after it.** Wire automated tests, security scanning, and accessibility checks into the continuous integration and delivery pipeline so every change is tested before it can progress (see Chapter 16 — Delivery Lifecycles). This makes quality continuous and cheap, and it means the ability to deploy a tested fix quickly — itself a safety control — is always available. Manual, end-of-project test phases are slow, late, and the first thing sacrificed when time runs short.

## Questions to discuss with your team

1. **If we change one thing in our live clinical system tomorrow, how confident are we that we would find out — before a patient does — if it broke something else?**
   This question probes the maturity of your regression testing and the honesty of your safety claims. Most serious clinical software incidents are not exotic new failures but regressions: a change that quietly broke behaviour everyone assumed was stable, discovered only when a clinician or patient hit it. A good discussion traces a recent real change through to the tests that would have caught a regression, and asks whether the highest hazards in the DCB0129/0160 hazard log are each backed by an automated test that fails when the hazard reappears. The tension to surface is between the pressure to ship fixes fast and the discipline of proving nothing else broke — and whether your pipeline makes that proof automatic or leaves it to someone remembering to check. Consider how long your test suite takes to run, whether it runs on every change, and whether anyone has quietly disabled failing tests to hit a deadline. An honest answer distinguishes "we have a regression suite tied to our clinical hazards and trust it" from "we test the change we made and hope for the best". If the answer is the latter, you are carrying clinical risk you cannot see.

2. **Where does our test data come from, and could a test ever expose a real patient's information?**
   Test environments are a common and under-examined route to a data breach, because teams under pressure reach for the easiest realistic data — a copy of production — and the resulting patient records then sit in less-protected test systems, laptops, or supplier environments. This question asks the team to trace every test and staging environment back to its data source, and to confront honestly whether "just this once" copies of live data have become routine. The trade-off to debate is realism versus safety: synthetic and anonymised data are safer but can miss the messy edge cases real data contains, while live data is realistic but a governance and breach liability, and true anonymisation is harder than it looks because records can be re-identified when combined. Concrete angles include who can access test environments, whether test databases are encrypted and audited like production, and whether your suppliers' test environments meet the same bar. A strong answer describes a deliberate strategy — synthetic data by default, anonymisation done properly, live data only as a documented, minimised, time-limited exception — rather than an accident waiting for an information governance investigation.

3. **When the go-live date and the quality bar collide, what actually gives — and who decides?**
   Every delivery eventually faces the moment when testing is not finished, a defect is unresolved, or accessibility conformance is incomplete, and the launch date is looming; how your organisation behaves in that moment reveals whether quality is a genuine control or merely aspirational. This question asks the team to recall the last time it happened and describe honestly what was cut: was it the cosmetic backlog, or was it regression testing, UAT, or the accessibility audit? The tension is real and should not be waved away — dates matter, funding cycles are unforgiving, and endless testing can itself be a failure mode — but the resolution must be governed by clinical and equity risk, not by whoever shouts loudest. Discuss who has the authority to hold a launch on quality grounds without career risk, whether your definition of done is ever formally waived and by whom, and whether known defects shipped at go-live are recorded as accepted risks or quietly buried. A good answer shows a clear, named decision route, a bright line below which a defect blocks release regardless of date (anything that could contribute to patient harm), and a culture where saying "not yet, it isn't safe" is rewarded rather than punished.

## In practice: a health & care example

An acute NHS trust is rolling out a new electronic observations and early-warning-score (EWS) module within its electronic patient record, replacing paper charts on which nurses record vital signs and the system calculates a deterioration score. The clinical hazard is obvious: a wrong score could mean a deteriorating patient is not escalated.

The team builds the pyramid from the start. Unit tests cover the EWS calculation against the national scoring rules, including boundary cases (the exact thresholds where a score tips into escalation) and awkward inputs (missing respiratory rate, a patient on supplemental oxygen). Integration tests confirm the score flows correctly to the escalation alert and the nursing task list. A small set of end-to-end tests exercises the full journey from bedside entry to a triggered alert. Each hazard in the DCB0160 hazard log is mapped to named tests, and the whole suite runs automatically on every change in the continuous integration pipeline.

Test environments are provisioned with synthetic patients — realistic vital-sign patterns including deteriorating trajectories — so no real record ever leaves production. Performance testing simulates a full ward round at shift handover, confirming alerts fire within seconds under peak load. Accessibility testing, automated on every build and verified manually with a nurse using screen magnification, catches a low-contrast alert banner.

UAT on a pilot ward, with real nurses working through simulated scenarios, surfaces a workflow flaw no developer had seen: the confirmation dialogue appeared after the score, tempting staff to dismiss it reflexively. The team redesigns the flow and adds a regression test. At go-live, three cosmetic defects ship as documented, accepted issues; two that touched the calculation were fixed and blocked release until they passed, and the safety case cites the test evidence directly. Six months into live operation, a routine change to the task list trips a regression test that would, undetected, have suppressed an escalation alert — caught in the pipeline, fixed before deployment, never reaching a ward.

## Three sector lenses

### Startup

A small digital-health company has the advantage of building automated testing and continuous integration into its DNA from day one, with no legacy manual test process to unwind, and can achieve fast, safe iteration a large trust would envy. The danger is treating testing as a luxury to defer while chasing product-market fit, and skimping on the non-functional and clinical-safety testing no early customer is yet demanding. The founder must remember that DCB0129 obligations attach to the manufacturer regardless of company size, so the regression evidence behind a safety claim is not optional even pre-revenue. Synthetic test data is also a startup's friend: it avoids the governance burden of handling real patient data before the company has the controls to do so safely.

### Enterprise

An NHS trust or major supplier runs testing at scale and under full assurance: dedicated test environments, formal UAT with clinical backfill, operational acceptance testing, security penetration testing, and change advisory boards gating releases to live clinical systems. The characteristic challenge is legacy — large, old systems with thin automated test coverage, where every change is feared because no one is confident what it might break, producing slow, expensive, manual regression cycles. The strategic move is to invest steadily in automated test coverage around the highest-risk areas, converting fear into confidence and slow releases into fast, safe ones. Enterprises also carry the coordination burden of testing across integrated systems, where a change in one supplier's product can break another's.

### Government

A national body delivers testing under the Service Standard, published service assessments, and the highest bar of public accountability, where a testing failure in a nationwide system can affect millions and reach Parliament. Accessibility testing against WCAG is a legal duty enforced for public sector bodies, and non-functional testing at national scale — load, resilience, security — is existential rather than optional. The challenge is coordinating quality assurance across many suppliers and integrated services, and holding a consistent definition of done across a sprawling programme. National services also shape the ecosystem: the test data, tools, and standards a government body mandates or publishes become the norm suppliers build to.

## Common failure modes

- **The inverted pyramid.** Testing is mostly slow, manual, end-to-end checks; feedback is slow, coverage is thin, and regression testing is skipped under time pressure. Antidote: invest in a broad base of fast automated unit and integration tests.
- **Testing as an end-phase.** Testing is a stage crammed in before go-live and the first thing cut when the schedule slips. Antidote: shift left and wire testing into the continuous integration pipeline so it is continuous and cheap.
- **Live data in test environments.** Real patient records are copied into less-protected test systems for realism, creating a breach waiting to happen. Antidote: synthetic and anonymised data by default; live data only as a governed exception.
- **Green build, no confidence.** Tests pass but cover trivia while the real clinical hazards are untested. Antidote: map tests explicitly to the hazard log and highest-risk journeys.
- **Accessibility as an automated tick-box.** A passing automated scan is treated as conformance while real assistive-technology users are never involved. Antidote: pair automated checks with manual testing by disabled users.
- **The waived definition of done.** "Done" is defined but routinely overridden under deadline pressure, launching unsafe work as complete. Antidote: automate gates and give someone the authority to hold a launch on quality grounds.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Test strategy | Ad-hoc manual testing before release | Some automated tests; inverted pyramid | Test pyramid with automation across levels | Shift-left culture; fast, trusted feedback on every change |
| Regression & safety link | No systematic regression testing | Manual regression cycles, incomplete | Automated regression suite mapped to hazard log | Hazard-linked tests gate every release automatically |
| Test data | Live patient data copied casually | Mix of live and anonymised, ungoverned | Synthetic/anonymised by default, governed | Robust synthetic data with realistic edge cases; live data never used |
| Non-functional testing | None or afterthought | Occasional load/security checks | Performance, security, accessibility tested routinely | Continuous non-functional testing at realistic peak scale |
| Defects & done | No defined "done"; defects untracked | "Done" defined but often waived | Enforced gates; defects triaged by clinical severity | Quality built in; releases boring and reversible |

## Checklist

- [ ] A test pyramid exists: broad automated unit/integration coverage, few end-to-end tests, all run in continuous integration.
- [ ] The highest hazards in the DCB0129/0160 hazard log are each mapped to named, automated regression tests.
- [ ] A regression suite runs and must pass before any change reaches a live clinical system.
- [ ] Test and staging environments use synthetic or anonymised data; live patient data is never used casually.
- [ ] Performance and load testing is run against realistic peak demand for critical clinical journeys.
- [ ] Security testing and WCAG accessibility testing (automated plus manual with assistive-technology users) are standing test types.
- [ ] User acceptance testing is run with real clinicians in realistic conditions, with backfill time budgeted.
- [ ] A definition of done and enforced quality gates exist and are not quietly waived under deadline pressure.
- [ ] Defects are triaged by clinical impact, and known issues shipped at go-live are recorded as accepted, mitigated risks.
- [ ] Test evidence is cited directly in the clinical safety case report.

## Key sources

- NHS England Digital — DCB0129 and DCB0160 clinical risk management standards; hazard log and clinical safety case report.
- NHS England — NHS Service Standard and NHS Digital Service Manual (accessibility, testing, and operating a reliable service).
- GOV.UK Service Manual (Government Digital Service) — testing, test data and environments, accessibility, and continuous delivery guidance.
- W3C Web Accessibility Initiative — Web Content Accessibility Guidelines (WCAG) 2.2 and testing techniques.
- NHS England — Digital Technology Assessment Criteria (DTAC), including clinical safety, technical assurance, and usability/accessibility.
- ISTQB (International Software Testing Qualifications Board) — foundational testing terminology and test levels.
- Public Sector Bodies (Websites and Mobile Applications) Accessibility Regulations 2018.
- Mike Cohn — the test pyramid concept; Martin Fowler / Continuous Delivery (Humble & Farley) — test automation and CI/CD practice.

## References

1. Software testing — Wikipedia — https://en.wikipedia.org/wiki/Software_testing
2. Quality assurance — Wikipedia — https://en.wikipedia.org/wiki/Quality_assurance
3. Unit testing — Wikipedia — https://en.wikipedia.org/wiki/Unit_testing
4. Integration testing — Wikipedia — https://en.wikipedia.org/wiki/Integration_testing
5. Shift-left testing — Wikipedia — https://en.wikipedia.org/wiki/Shift-left_testing
6. Non-functional testing — Wikipedia — https://en.wikipedia.org/wiki/Non-functional_testing
7. Regression testing — Wikipedia — https://en.wikipedia.org/wiki/Regression_testing
8. Test automation — Wikipedia — https://en.wikipedia.org/wiki/Test_automation
9. Continuous integration — Wikipedia — https://en.wikipedia.org/wiki/Continuous_integration
10. Acceptance testing — Wikipedia — https://en.wikipedia.org/wiki/Acceptance_testing
11. Web Content Accessibility Guidelines — Wikipedia — https://en.wikipedia.org/wiki/Web_Content_Accessibility_Guidelines
12. Deployment environment — Wikipedia — https://en.wikipedia.org/wiki/Deployment_environment
13. Synthetic data — Wikipedia — https://en.wikipedia.org/wiki/Synthetic_data
14. Clinical risk management standards DCB0129 and DCB0160 — NHS England (Clinical Safety) — https://digital.nhs.uk/services/clinical-safety
15. NHS service standard and NHS digital service manual — NHS England — https://service-manual.nhs.uk/
16. Testing your service, and test data and environments — Government Digital Service, GOV.UK Service Manual — https://www.gov.uk/service-manual/technology
17. Web Content Accessibility Guidelines (WCAG) 2.2 — W3C Web Accessibility Initiative — https://www.w3.org/WAI/standards-guidelines/wcag/
18. Digital Technology Assessment Criteria (DTAC) — NHS England — https://www.nhs.uk/digital-tools/digital-technology-assessment-criteria-dtac/
19. Public Sector Bodies (Websites and Mobile Applications) Accessibility Regulations 2018 — UK Government / GOV.UK — https://www.legislation.gov.uk/uksi/2018/952/contents/made
20. Continuous Delivery — Jez Humble and David Farley — https://continuousdelivery.com/
