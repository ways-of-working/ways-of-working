# Chapter 24 — Identity & Access Management

**In health and care, controlling who can see and do what with a patient's record is not an IT housekeeping task but a front-line determinant of clinical safety, confidentiality, and public trust.**

## Why this matters in health and care

Every clinical decision rests on the assumption that the record in front of a clinician is the right record, belongs to the right patient, and has been reached by the right person. Identity and access management (IAM) is the machinery that makes those three assumptions true. When it works, a paramedic sees an allergy in time, a safeguarding note reaches only those who need it, and an audit trail can answer the question "who looked at this record and why?". When it fails, patients are harmed by records opened under the wrong name, staff snoop on relatives or celebrities, and confidence in the whole digital enterprise erodes.

Health and care raise the stakes above the ordinary corporate case in three ways. First, the data is among the most sensitive a person will ever generate — mental health, sexual health, substance use, gender identity, safeguarding concerns — so a confidentiality breach is not an inconvenience but a lasting harm. Second, the workforce is mobile, rotational, and multi-organisational: junior doctors rotate every few months, agency and locum staff arrive for a single shift, and integrated care means a district nurse may legitimately need a hospital record. Third, the duty of care is unforgiving of friction: an access control that is too slow at 3am in resuscitation is itself a safety hazard. IAM in this sector is therefore a constant negotiation between locking data down and letting the right person in fast.

This chapter deals with the access-control depth that sits beneath the broader duties covered in Chapter 7 — Information Governance, Data Protection & Cyber Security. Where that chapter sets the legal and organisational frame — the UK General Data Protection Regulation, the Data Security and Protection Toolkit, the confidentiality duty — this one is about the concrete mechanics of proving identity and granting the least access needed to do the job.

## Core concepts

[Identity and access management](https://en.wikipedia.org/wiki/Identity_management) is the discipline and the set of technologies that ensure the right individuals have the right access to the right resources at the right time, and that this can be proven afterwards. It rests on a distinction that is easy to blur and dangerous to lose: the difference between authentication and authorization.

[Authentication](https://en.wikipedia.org/wiki/Authentication) answers "are you who you claim to be?". It is proven with factors: something you know (a password or PIN), something you have (a smartcard, a phone, a hardware token), and something you are (a fingerprint or face). [Authorization](https://en.wikipedia.org/wiki/Authorization) answers a different question — "now that we know who you are, what are you allowed to see and do?". A consultant and a receptionist may both authenticate perfectly well, but they are authorised to very different parts of a record. Confusing the two leads to systems that check identity strongly and then let everyone see everything.

Authorization in health and care is usually organised as [role-based access control](https://en.wikipedia.org/wiki/Role-based_access_control) (RBAC), where permissions attach to roles — "emergency department nurse", "GP", "medical secretary" — and people inherit permissions by holding a role, rather than being granted rights one by one. RBAC is governed by the [principle of least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege): each person, and each system account, should hold the minimum access needed to do the job and no more. Least privilege limits both accidental error and the blast radius of a compromised account.

Modern authentication strengthens the "prove who you are" step with [multi-factor authentication](https://en.wikipedia.org/wiki/Multi-factor_authentication) (MFA), combining two or more factors so that a stolen password alone is not enough. It reduces friction with [single sign-on](https://en.wikipedia.org/wiki/Single_sign-on) (SSO), where one authenticated session grants access to many applications without repeated logins — a genuine safety benefit when a clinician must move between a dozen systems in an hour. SSO across organisational boundaries relies on [federated identity](https://en.wikipedia.org/wiki/Federated_identity): one organisation vouches for a user so another can trust them without holding their credentials.

The plumbing of federation and modern authentication is built on open standards. [OAuth](https://en.wikipedia.org/wiki/OAuth) is a standard for delegated authorization — letting an application act on your behalf without handing over your password. [OpenID Connect](https://en.wikipedia.org/wiki/OpenID) layers authentication on top of OAuth so an application can learn who the user is, and the older XML-based [Security Assertion Markup Language](https://en.wikipedia.org/wiki/Security_Assertion_Markup_Language) (SAML) does a similar job for enterprise SSO. The lifecycle of an identity — the granting, changing, and revoking of access as people join, move, and leave — is handled by [provisioning](https://en.wikipedia.org/wiki/Provisioning_(technology)) processes, commonly called joiners/movers/leavers or JML.

The strategic direction of travel is [zero trust architecture](https://en.wikipedia.org/wiki/Zero_trust_architecture): the assumption that no user or device is trustworthy merely because it sits inside the network. Every request is authenticated, authorised, and checked against context — device health, location, sensitivity of the data — rather than relying on a hardened perimeter. In a sector where staff work from clinics, homes, ambulances, and partner sites, the perimeter has effectively dissolved, and zero trust names the honest response to that.

## Best practices

1. **Treat authentication and authorization as separate design decisions.** Decide first how strongly you must prove identity for a given system, and separately how finely you must control what each role can then do. Strong login on a system that gives everyone full access is a false comfort, and fine-grained permissions behind a weak password are equally hollow. Document both decisions explicitly for every clinical system, and revisit them when the data sensitivity or user population changes.

2. **Make role-based access control mirror real clinical roles, then keep it clean.** Design roles around how care is actually delivered — not around the org chart or the whims of a supplier's default configuration — and map each role to the minimum records and functions it needs. Over time RBAC decays into "role explosion", where hundreds of overlapping roles accumulate and no one can say what any of them grants. Schedule periodic role rationalisation, and resist the temptation to solve every access request by minting a new bespoke role.

3. **Apply least privilege to people and to machine accounts alike.** Least privilege is routinely applied to clinicians and then forgotten for the service accounts, integration engines, and reporting tools that often hold the widest access of all. An automated interface pulling data for a dashboard rarely needs write access or identifiable free text, yet frequently gets it. Inventory non-human identities, scope them down, and rotate their credentials on a schedule.

4. **Mandate multi-factor authentication for remote and privileged access, and choose factors that suit the setting.** Passwords alone are no longer defensible for anything reaching patient data from outside a trusted device, and MFA is now a baseline expectation across NHS systems. Choose factors that survive the clinical environment: phishing-resistant hardware tokens or platform authenticators for privileged and remote access, and be wary of SMS codes on wards where signal is poor and phones are shared. Balance the security gain against the reality that a clinician mid-resuscitation cannot fumble for a second factor.

5. **Use single sign-on to remove friction that pushes staff toward unsafe workarounds.** When staff must log in separately to ten systems, they write passwords on sticky notes, share smartcards, and leave sessions open — every one a safety and confidentiality risk. Well-implemented SSO, ideally combined with "tap in, tap out" proximity badges at shared clinical workstations, both improves security and gives clinicians time back. Treat SSO as a patient-safety intervention, not merely a convenience, and measure the login time you remove.

6. **Modernise NHS identity beyond the smartcard, without breaking what works.** The NHS Care Identity Service (formerly the Care Identity Service and, before that, the Registration Authority regime built on smartcards) authenticates NHS staff and drives access to national systems such as the Spine. National direction is now toward modern, standards-based authentication — CIS2 with MFA and OpenID Connect — reducing dependence on physical smartcards and card readers that fail, get shared, or block care. Plan your migration deliberately: keep the assurance and registration rigour of the smartcard model while adopting the flexibility of modern tokens.

7. **Run joiners/movers/leavers as a controlled, auditable process — especially leavers.** The single most common serious IAM failure in health and care is the account that outlives the person's need for it: the rotated junior doctor, the departed agency nurse, the contractor whose access was never revoked. Automate provisioning from an authoritative source (usually the electronic staff record) so that starting, changing, and ending a role triggers the matching access change within a defined, short window. Treat same-day revocation for leavers and for staff under investigation as a hard requirement, not an aspiration.

8. **Recertify access regularly and make managers accountable for it.** Access that was appropriate on day one drifts as people change teams and accumulate rights they no longer need — "privilege creep". Run periodic access reviews (recertification) in which the responsible manager or system owner actively confirms that each person still needs each right, with silence defaulting to removal rather than retention. Make the review meaningful by presenting it in plain clinical-role language, not raw permission codes that no manager can interpret.

9. **Govern privileged access as a category of its own.** Administrators, database owners, and infrastructure engineers can read or alter any record and disable the very controls that protect it, so their access needs stronger treatment than ordinary users. Implement privileged access management: separate admin identities from day-to-day accounts, grant elevated rights just-in-time and time-boxed rather than standing, and record privileged sessions for independent review. Never let a supplier or a "break-glass" account become a permanent, unmonitored master key.

10. **Make every access decision auditable, and actually read the audit.** Access control that cannot be reviewed afterwards is only half a control; the ability to answer "who accessed this record, when, and on what basis?" underpins both confidentiality investigations and patient safety. Configure comprehensive, tamper-evident audit logging, and — crucially — resource proactive audit, including alerts for self-lookups, lookups of colleagues or VIPs, and unusual access volumes. An audit trail no one examines deters no one.

11. **Design break-glass access so emergencies are served and abuse is caught.** Clinicians sometimes legitimately need a record they are not routinely authorised to see — an unconscious patient, a cross-organisational emergency. Provide an explicit "break-glass" path that grants emergency access with a required reason, immediate flagging, and mandatory after-the-fact review, rather than forcing staff to choose between the rules and the patient. The goal is to make the safe emergency action easy and the unjustified one visible.

12. **Adopt zero trust as a direction, and sequence it pragmatically.** Move from "trusted network, open inside" toward verifying every request against identity, device health, and context, so a compromised laptop on the corporate LAN is no longer automatically trusted. This is a multi-year journey through strong identity, device compliance, conditional access, and micro-segmentation — not a product you buy. Sequence it behind the fundamentals (MFA, least privilege, clean JML), and align it with the estate work in Chapter 23 — Technical Architecture, Cloud & Legacy.

## Questions to discuss with your team

1. **Where are we deliberately trading access friction against clinical safety, and who decided the balance?** Every additional login, second factor, or authorisation step protects confidentiality but costs seconds that, in an emergency, are themselves a safety risk. This question forces the team to name the specific places where security controls could delay care — the resus login, the shared ward workstation, the out-of-hours system — and to ask whether the current balance was chosen by people who understand both the clinical and the security consequences, or defaulted to a supplier's setting. Debate the tension honestly: an over-tight control drives sticky-note passwords and shared smartcards that are worse than the risk they address, while an over-loose one invites snooping and breaches. Look for concrete signals of a bad balance — staff sharing credentials, sessions left open, break-glass used routinely. A good answer identifies who owns each trade-off, shows that clinicians were in the room when it was set, and points to measured login times and workaround rates rather than assumptions. It also commits to revisiting the balance as roles, systems, and threats change.

2. **How confident are we that a leaver or a mover loses the right access, in the right timeframe, every time?** The account that outlives its need is the classic IAM failure, and in a rotational, multi-organisational health workforce the risk is acute. This question probes whether joiners/movers/leavers is a reliable, automated process driven from an authoritative source, or a set of manual emails that quietly fail when someone is busy. Discuss the hard cases: the junior doctor rotating between trusts, the agency nurse on one shift, the contractor, the member of staff suspended pending investigation. Consider what "the right timeframe" means for each — same-day revocation is non-negotiable for a suspension but may be softer for a routine internal move. A good answer can point to evidence, not intention: the last leaver-audit results, the number of dormant accounts found and closed, the time between someone leaving and their access ending. It is honest about the gaps and names who is accountable for closing them.

3. **When something goes wrong with a record, can we actually reconstruct who did what — and would we notice misuse without an incident prompting us?** Audit is the control that makes confidentiality and safety enforceable after the fact, but it only works if the logs are complete, protected, and genuinely reviewed. This question separates two things a team often conflates: the ability to investigate reactively when a complaint arrives, and the capability to detect misuse proactively before anyone complains. Explore what your logs actually capture, whether they can be altered, how long they are kept, and — the harder question — who looks at them when there is no incident. Consider the realistic threats: a staff member looking up a family member, a colleague, or a public figure; a compromised account exfiltrating records at scale. A good answer shows that audit is resourced as an active function with alerting, not a dormant archive, and can cite a real example of misuse the organisation detected and acted on. It also connects audit to fairness, ensuring reviews do not disproportionately target particular staff groups.

## In practice: a health & care example

Meadowvale Integrated Care System is rolling out a shared care record so that hospital, community, mental health, GP, and adult social care staff can see a unified view of each person. Early in discovery the programme realises that its real risk is not building the record but controlling access to it: a single view spanning five organisations multiplies both the safety benefit of the right clinician seeing the right information and the harm of the wrong person seeing something sensitive.

The team makes access control a first-class design stream. They agree a role model expressed in clinical language — "community nurse", "approved mental health professional", "care home manager" — and map each role to the least data it needs, with mental health and sexual health records subject to tighter, separately authorised access. Authentication is federated: each partner organisation authenticates its own staff through the NHS Care Identity Service or its local identity provider using OpenID Connect, and the shared record trusts those assertions rather than issuing its own credentials, so there is no new password to manage and joiners/movers/leavers stays with the employing organisation where the authoritative staff record lives.

Because a paramedic or an out-of-hours clinician will sometimes need a record they are not routinely authorised to see, the team builds an explicit break-glass path: emergency access is granted on entering a reason, flagged immediately to the record's home organisation, and reviewed within 48 hours. They stand up a small joint information governance and audit function that reviews break-glass events, runs alerts for self-lookups and lookups of flagged individuals, and reports quarterly to the ICS board.

Six months after go-live, an alert flags a care coordinator repeatedly opening the record of someone with no active involvement in their caseload. The audit function investigates, finds the access was personal rather than professional, and the employing organisation takes disciplinary action. No patient safety incident occurred, the breach was caught proactively, and — because the controls demonstrably worked — public confidence in the shared record held. The board notes that the same audit capability now doubles as evidence for its Data Security and Protection Toolkit submission (see Chapter 7 — Information Governance, Data Protection & Cyber Security).

## Three sector lenses

### Startup

A small digital-health company building, say, a remote monitoring app has the advantage of no legacy: it can adopt modern authentication, MFA, and standards-based federation from day one, and integrate with NHS login for citizens and CIS2 for clinicians rather than inventing its own identity system. The danger is speed outrunning discipline — hard-coded admin credentials, a shared "founder" superuser account, service accounts with god-mode access, and no leaver process because "everyone knows everyone". Least privilege and audit feel like overhead at ten people but become unrecoverable technical debt at a hundred. The pragmatic move is to buy identity as a managed service, enforce MFA and RBAC from the first commit, and treat DTAC (Digital Technology Assessment Criteria) requirements as the minimum bar for any NHS deployment.

### Enterprise

A large NHS trust or ICS runs dozens of clinical systems of wildly different ages, each with its own identity model, and its central challenge is integration and lifecycle at scale. Smartcards, SSO, "tap in, tap out" workflows, and a reliable JML pipeline from the electronic staff record all matter more here than any single clever control, because the failure modes are volume failures: thousands of dormant accounts, role explosion, and audit logs no one has the capacity to review. Privileged access management is critical given the number of administrators and suppliers touching the estate. Progress comes from an identity strategy that rationalises roles, federates across systems, and resources a standing audit function — not from point solutions bolted onto each application.

### Government

A national body such as NHS England operates identity as shared infrastructure for the whole system: the NHS Care Identity Service and CIS2 for staff, NHS login for citizens, and the standards and assurance regimes that let hundreds of organisations trust one another. Its decisions set the direction of travel — the move from smartcards to modern authentication, the adoption of OpenID Connect, the push toward zero trust — and its accountability is to Parliament and the public for both security and equitable access. The tension is between central standardisation and local flexibility: mandate too rigidly and you break local workflows, mandate too loosely and federation collapses into inconsistency. The government lens is therefore about setting interoperable standards (see Chapter 25 — Interoperability & Data Standards), providing trustworthy shared services, and assuring compliance without micromanaging every trust.

## Common failure modes

- **Orphaned and dormant accounts.** Leavers, rotated staff, and old contractors retain live access because JML relies on manual notification. The fix is automated deprovisioning from an authoritative source plus regular dormant-account sweeps.
- **Role explosion and privilege creep.** RBAC decays into hundreds of overlapping roles and individuals accumulate rights they no longer use. Counter with periodic recertification and scheduled role rationalisation.
- **Credential sharing and shared workstations.** Slow logins and clunky smartcards drive staff to share cards and leave sessions open. Address the root cause with SSO, proximity badges, and fast switching rather than by exhorting staff to behave.
- **Standing privileged access.** Administrators and suppliers hold permanent god-mode accounts that can disable the controls themselves. Move to just-in-time, time-boxed, recorded elevation.
- **Audit as decoration.** Logs are collected but never reviewed, so misuse is only ever found reactively. Resource proactive audit with alerting for self-lookups and VIP lookups.
- **Break-glass as a loophole.** Emergency access exists but is unmonitored, so it becomes the routine path of least resistance. Require a reason, flag every use, and review after the fact.
- **MFA theatre.** MFA is enabled but on weak, phishable factors, or waived for the busiest privileged users. Prefer phishing-resistant factors where the risk is highest.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimising |
|---|---|---|---|---|
| Authentication | Passwords only; sharing common | MFA on remote access; smartcards for national systems | MFA broad; SSO in place; modern auth (CIS2/OIDC) adopted | Phishing-resistant, risk-based auth; passwordless where safe |
| Authorization (RBAC & least privilege) | Ad hoc, everyone sees most things | Roles exist but broad and overlapping | Clean role model in clinical language; least privilege enforced | Attribute- and context-aware access; continuous minimisation |
| Joiners/movers/leavers | Manual, unreliable; dormant accounts common | Documented process, partly automated | Automated from authoritative source; same-day leaver revocation | Real-time provisioning; dormant accounts near zero, evidenced |
| Privileged access | Shared, standing admin accounts | Separate admin identities | Just-in-time, time-boxed, session-recorded | Zero standing privilege; continuous monitoring |
| Audit & review | Little logging; no review | Logs kept, reactive only | Comprehensive logs; scheduled recertification and audit | Proactive alerting and analytics; fair, evidenced enforcement |

## Checklist

- [ ] Authentication strength and authorization scope decided and documented separately for every clinical system.
- [ ] MFA enforced for all remote and privileged access, using factors appropriate to the clinical setting.
- [ ] Single sign-on and fast workstation switching deployed to remove login friction and credential sharing.
- [ ] Role model expressed in clinical language, mapped to least privilege, and rationalised on a schedule.
- [ ] Joiners/movers/leavers automated from an authoritative staff source, with same-day leaver and suspension revocation.
- [ ] Periodic access recertification run by accountable managers, with default-to-remove for unconfirmed access.
- [ ] Privileged access managed as a distinct category: separate identities, just-in-time elevation, session recording.
- [ ] Non-human and integration accounts inventoried, scoped to least privilege, and credential-rotated.
- [ ] Comprehensive, tamper-evident audit logging in place, with proactive alerting for self-, colleague-, and VIP lookups.
- [ ] Break-glass emergency access designed with mandatory reason, immediate flagging, and after-the-fact review.
- [ ] Migration from smartcards to modern NHS authentication (CIS2 / OpenID Connect) planned and sequenced.
- [ ] Zero trust roadmap agreed and aligned with the technical architecture strategy.

## Key sources

- NHS England — NHS Care Identity Service and Care Identity Service 2 (CIS2) guidance
- NHS England — Data Security and Protection Toolkit
- National Cyber Security Centre (NCSC) — Zero Trust Architecture Design Principles
- National Cyber Security Centre (NCSC) — Multi-factor authentication and identity/access management guidance
- NIST — Special Publication 800-207, Zero Trust Architecture
- NIST — Special Publication 800-63, Digital Identity Guidelines
- NHS England / NHS login — citizen identity verification service documentation
- DTAC — Digital Technology Assessment Criteria for health and social care
- Caldicott Principles and the common law duty of confidentiality (UK)

## References

1. Identity management (identity and access management) — Wikipedia — https://en.wikipedia.org/wiki/Identity_management
2. Authentication — Wikipedia — https://en.wikipedia.org/wiki/Authentication
3. Authorization — Wikipedia — https://en.wikipedia.org/wiki/Authorization
4. Role-based access control — Wikipedia — https://en.wikipedia.org/wiki/Role-based_access_control
5. Principle of least privilege — Wikipedia — https://en.wikipedia.org/wiki/Principle_of_least_privilege
6. Multi-factor authentication — Wikipedia — https://en.wikipedia.org/wiki/Multi-factor_authentication
7. Single sign-on — Wikipedia — https://en.wikipedia.org/wiki/Single_sign-on
8. Federated identity — Wikipedia — https://en.wikipedia.org/wiki/Federated_identity
9. OAuth — Wikipedia — https://en.wikipedia.org/wiki/OAuth
10. OpenID (and OpenID Connect) — Wikipedia — https://en.wikipedia.org/wiki/OpenID
11. Security Assertion Markup Language (SAML) — Wikipedia — https://en.wikipedia.org/wiki/Security_Assertion_Markup_Language
12. Provisioning (technology) — Wikipedia — https://en.wikipedia.org/wiki/Provisioning_(technology)
13. Zero trust architecture — Wikipedia — https://en.wikipedia.org/wiki/Zero_trust_architecture
14. NHS Care Identity Service 2 (CIS2) — NHS England — https://digital.nhs.uk/services/care-identity-service
15. Data Security and Protection Toolkit — NHS England — https://www.dsptoolkit.nhs.uk/
16. Zero Trust Architecture Design Principles — National Cyber Security Centre — https://www.ncsc.gov.uk/collection/zero-trust-architecture
17. Special Publication 800-207: Zero Trust Architecture — National Institute of Standards and Technology (NIST) — https://csrc.nist.gov/pubs/sp/800/207/final
18. Special Publication 800-63: Digital Identity Guidelines — National Institute of Standards and Technology (NIST) — https://pages.nist.gov/800-63-3/
19. Digital Technology Assessment Criteria (DTAC) — NHS England — https://www.nhs.uk/digital-technology-assessment-criteria-dtac/
20. NHS login — NHS England — https://www.nhs.uk/nhs-services/online-services/nhs-login/
