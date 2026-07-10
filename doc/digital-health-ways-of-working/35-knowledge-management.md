# Chapter 35 — Knowledge Management & Documentation

**In one sentence:** In a safety-critical service, what your teams know but have never written down is a clinical risk, not just an inconvenience — so treat documentation as a first-class deliverable and knowledge continuity as a duty, not a nicety.

## Why this matters in health and care

Digital health teams are small, specialised, and often stitched together from permanent staff, contractors, and supplier engineers. The person who understands why the pathology interface retries three times before failing, or which flag in the electronic patient record suppresses a duplicate-allergy alert, is frequently one individual — and that individual moves on, retires, or is off sick the week the integration breaks at 2am. When the knowledge leaves with them, the system does not become merely harder to maintain; it becomes harder to operate *safely*. An undocumented workaround that a clinician relied on can silently disappear, and nobody left knows it was load-bearing.

The stakes are specific to the sector. A misunderstood configuration can produce a wrong-patient record, a missed alert, or a broken referral — harms measured in patient outcomes, not downtime tickets. Public bodies also carry statutory obligations: health records must be retained for defined periods, and decisions about care and about public money must be auditable years later and findable when a coroner, a regulator, or a Freedom of Information request comes calling. Good knowledge management is therefore part clinical safety, part governance, and part respect for the next person who has to keep the service running. It is inseparable from how you run live operations (see Chapter 14 — Service Management & Live Operations) and how you design teams (see Chapter 24 — Team Structures, Roles & Responsibilities).

## Core concepts

**Knowledge management as a discipline.** [Knowledge management](https://en.wikipedia.org/wiki/Knowledge_management) is the set of practices by which an organisation creates, captures, shares, and reuses what it knows. It balances three components — people and culture, processes and structure, and technology — and fails whenever leaders treat it as a tool-purchase rather than a habit. The "knowledge" ranges from how a clinical pathway actually works in a given trust to how a specific integration engine is configured.

**Tacit versus explicit knowledge.** [Tacit knowledge](https://en.wikipedia.org/wiki/Tacit_knowledge) is what lives in people's heads and hands — the judgement, intuition, and hard-won "you have to know that this trust codes discharge differently" that is hard to write down. [Explicit knowledge](https://en.wikipedia.org/wiki/Explicit_knowledge) is what has been articulated and codified into documents, diagrams, and runbooks. Most of the knowledge that keeps a service safe starts tacit; the work of knowledge management is to convert enough of it to explicit form that the service does not depend on any one head.

**The SECI knowledge-conversion model.** The [SECI model](https://en.wikipedia.org/wiki/SECI_model_of_knowledge_dimensions) (Socialisation, Externalisation, Combination, Internalisation), from Nonaka and Takeuchi, describes how knowledge moves between tacit and explicit forms: sharing by working alongside each other (socialisation), writing tacit knowledge down (externalisation), combining explicit pieces into larger documents (combination), and absorbing documented knowledge back into fluent practice (internalisation). It is useful because it reminds you that documentation alone is not enough — pairing, shadowing, and communities matter just as much as the wiki.

**Key-person dependency and the bus factor.** The [bus factor](https://en.wikipedia.org/wiki/Bus_factor) is the number of people who would have to be lost before a service stalls for lack of anyone who understands it. A bus factor of one is the default state of most small digital teams and a serious operational risk in a service people's health depends on. High staff turnover, heavy contractor use, and single-supplier lock-in all push the number down; deliberate documentation, cross-training, and pairing push it back up.

**Documentation as a first-class deliverable.** Treat documents as products, not by-products. A service manual describes what the service is and how it behaves; a [runbook](https://en.wikipedia.org/wiki/Runbook) (or playbook) gives step-by-step procedures for starting, stopping, and recovering it; an [architecture decision record](https://en.wikipedia.org/wiki/Architectural_decision) (ADR) captures *why* a significant choice was made, so future maintainers do not unpick it without knowing the reasons. A [single source of truth](https://en.wikipedia.org/wiki/Single_source_of_truth) means each fact is mastered in exactly one place, so people are not chasing contradictory copies of "the current architecture".

**Docs-as-code.** Keeping documentation in the same version-controlled repository as the work — written in plain text or Markdown, reviewed like code, published automatically — keeps docs close to the thing they describe and far more likely to stay current. When the diagram lives next to the code and changes in the same pull request, it rots more slowly.

**Communities of practice.** A [community of practice](https://en.wikipedia.org/wiki/Community_of_practice) (sometimes called a guild) is a cross-team group that shares a craft — clinical safety officers, front-end engineers, information governance leads — and improves it together. Communities spread tacit knowledge horizontally across an organisation that vertical team boundaries would otherwise trap.

**Records management and retention.** [Records management](https://en.wikipedia.org/wiki/Records_management) governs information through its lifecycle, including how long it must be kept and when it may be destroyed. In health this is partly statutory: clinical records carry defined retention periods under the NHS Records Management Code of Practice. This is distinct from team documentation, and conflating the two causes real errors — a point we return to below.

**Information architecture and findability.** [Information architecture](https://en.wikipedia.org/wiki/Information_architecture) is the structural design of an information space so that people can find what they need. A wiki with ten thousand pages and no structure is not documentation; it is a landfill. Findability is the difference between knowledge that exists and knowledge that is used.

## Best practices

1. **Make documentation a definition-of-done, not an afterthought.** A feature, integration, or configuration change is not "done" until its runbook entry, its ADR (if a significant decision was made), and its service-manual update exist. Bake this into your ways of working so it is written while the knowledge is fresh, by the person who has it. Retro-documenting a system six months later, from memory, is where inaccuracies and dangerous gaps are born.

2. **Keep a single source of truth and link outward from it.** Decide, per domain, where the authoritative version of each fact lives — the architecture, the on-call rota, the data-flow diagram — and make everything else point to it rather than copy it. Duplicated documentation drifts, and in a clinical context a stale copy that says "the allergy check is on" when it is off is worse than no document at all. Ruthlessly delete or redirect the stale duplicates you already have.

4. **Adopt docs-as-code and keep documentation next to the work.** Store runbooks, ADRs, and service manuals in version control alongside the systems they describe, review documentation changes in the same pull request as the code change, and publish automatically. This makes updates cheap, changes reviewable, and history auditable — and it means the person changing the system is nudged to change the docs in the same breath.

5. **Write runbooks a stressed stranger could follow at 3am.** A runbook should assume the reader is tired, unfamiliar with the system, and under pressure — because during a major incident they will be. Use numbered, literal steps, name the exact screens and commands, and state the expected result of each step and what to do if it fails. Test them by having someone who did not write them execute a recovery in a drill.

6. **Capture the "why", not just the "what", with architecture decision records.** A short ADR — context, decision, consequences — preserves the reasoning behind significant choices so that future maintainers do not reverse a decision without understanding the constraint that drove it. In health this matters acutely: a configuration that looks odd may exist because of a clinical-safety hazard analysis or an information-governance ruling. Recording the reason prevents a well-meaning "clean-up" from reintroducing a known risk.

7. **Deliberately raise the bus factor on every critical system.** Identify the systems with a bus factor of one and treat that as a risk on your register with a named owner and a plan. Pair people, rotate on-call knowledge, run "teach-back" sessions where the expert documents while a colleague follows along, and forbid any single person being the only one who can deploy or recover a safety-critical service. This is cheaper than discovering the gap during an outage.

8. **Run post-incident reviews that change practice, not blame people.** After any significant incident, run a blameless [post-incident review](https://en.wikipedia.org/wiki/Postmortem_documentation) that produces documented, owned, time-bound actions — and then actually close them. Lessons-learned that are filed and never revisited are theatre; the test of the process is whether a later incident of the same shape is prevented. Feed the findings straight back into runbooks and the clinical-safety case (see Chapter 14 — Service Management & Live Operations).

9. **Invest in information architecture and findability.** Structure your knowledge base so a new joiner can find the on-call runbook in under a minute, and prune aggressively — an out-of-date page is a liability, not an asset. Agree naming conventions, a clear hierarchy, and an owner for each area, and put a "last reviewed" date on pages that matter so readers can judge freshness. Search is not a substitute for structure; it is a complement to it.

10. **Grow communities of practice to spread tacit knowledge.** Stand up cross-team guilds for the crafts that matter — clinical safety, security, front-end, data engineering — with a light remit: share what you are learning, agree common patterns, mentor newcomers. These forums move the tacit knowledge that no document captures, and they reduce duplicated mistakes across teams (see Chapter 27 — People & Organisational Development). Give them time in the working week, or they wither.

11. **Separate team documentation from statutory records — and manage both.** Be explicit about what is *team knowledge* (runbooks, ADRs, wikis) versus what is a *record* subject to legal retention (clinical records, care decisions, financial approvals, information-governance decisions). Apply the NHS Records Management Code of Practice retention schedules to the latter, and do not let casual wiki deletion destroy something you were legally required to keep. Equally, do not hoard everything forever "to be safe" — over-retention is its own governance and data-protection risk.

12. **Make onboarding a test of your documentation.** Treat every [onboarding](https://en.wikipedia.org/wiki/Onboarding) as a live audit: if a competent new engineer or clinician cannot get productive from your written material plus a little pairing, your documentation has failed, and the gaps they hit are your backlog. Ask new joiners to fix the first thing that confused them as their first contribution. This turns onboarding from a one-way cost into a continuous improvement loop for knowledge continuity.

## Questions to discuss with your team

1. **If the one person who understands our most critical integration left tomorrow, how long until we were exposed — and what specifically would we not know?**
   This turns the abstract idea of a bus factor into a concrete stress test of your most important systems. Work through a real example — the pathology feed, the single-sign-on configuration, the shared care record's matching logic — and ask honestly who else could operate, change, and recover it without that person. The tension to surface is that the deepest knowledge usually sits with your busiest, most trusted individual, and the pressures of delivery make it rational for them never to stop and write it down. Distinguish knowledge that is genuinely tacit and hard to codify from knowledge that simply has never been captured because nobody made time. A good, honest answer names your bus-factor-one systems out loud, admits which gaps are real, and produces a costed plan — pairing, documentation sprints, cross-training — rather than a vague reassurance that "it's all in people's heads and that's fine". If the conversation is comfortable, you have not been specific enough.

2. **When we write something down, how do we know anyone will ever find it, trust it, and keep it current — and where is our documentation already lying to us?**
   Documentation that is out of date is not neutral; in a safety-critical setting it actively misleads a stressed operator into the wrong action. The discussion should confront the difference between *having* documents and having documents people can find, trust, and act on — a question of information architecture, ownership, and freshness, not volume. Debate whether your knowledge base has a real structure or has become a sprawl nobody navigates, and whether docs live close enough to the work (docs-as-code) to stay current or drift in a separate tool nobody updates. Ask each person when they last relied on an internal document and found it wrong, and what that cost. A strong answer identifies specific pages you know to be stale, assigns owners and review dates, and agrees a single source of truth for the facts that matter most — and it is willing to delete more than it adds.

3. **After our last serious incident, what actually changed in how we work — and if the answer is "not much", why do we keep running reviews?**
   Post-incident reviews are common; reviews that change practice are rare, and the gap between the two is where the same failures recur. This tests whether your lessons-learned process is a genuine feedback loop or a ritual that produces a document and no change. Explore the cultural conditions honestly: reviews only surface the truth if they are blameless, and people will hide the real cause if the process punishes them, so psychological safety is a precondition, not a nicety (see Chapter 29 — Change Management). Look at your last few incidents and trace each action to whether it was completed and whether it prevented recurrence. A good answer can point to a concrete change — a rewritten runbook, a new alert, a design fix — that a past review produced, and is candid about actions that were logged and quietly abandoned, with a plan to close that loop.

## In practice: a health & care example

An integrated care system (ICS) runs a shared care record that pulls data from three acute trusts, community services, and a social-care case-management system. The integration was built two years ago largely by one contract engineer, "Dev", who understood every quirk of the matching logic that decides when two records refer to the same person. Dev's contract ends in six weeks. There is a wiki, but it was last meaningfully updated during the build.

The delivery lead treats this as a bus-factor-one risk and puts it on the programme risk register with her own name against it. Over the six weeks, she funds a small "knowledge continuity" effort: Dev pairs each morning with two permanent engineers, and instead of a farewell brain-dump they externalise as they go — writing runbooks for the failure modes Dev knows by heart, and ADRs explaining *why* the matching logic tolerates certain mismatches (it turns out one apparently sloppy rule exists to avoid a known patient-safety hazard flagged in the original clinical-safety case). The docs go into the same Git repository as the integration code, reviewed in pull requests, so they are versioned and current.

Two months after Dev leaves, the feed from one acute trust starts producing duplicate patient records overnight. The on-call engineer — who never met Dev — opens the runbook, follows the numbered steps, confirms the expected result at each stage, and restores correct matching within the hour. In the blameless post-incident review the team finds the trigger (an upstream change to how the trust codes NHS numbers) and turns it into a monitoring alert and a runbook update. What would have been a multi-day, high-risk scramble — and a genuine patient-safety incident — became a documented, one-hour recovery, because tacit knowledge was made explicit while the person who held it was still there.

## Three sector lenses

### Startup

A digital-health startup lives with the highest bus-factor risk and the least slack to address it: a handful of engineers, deep knowledge in each head, and a culture that prizes shipping over writing. The pragmatic move is lightweight, cheap documentation embedded in the workflow — ADRs as short Markdown files in the repo, runbooks written the first time something breaks, docs-as-code from day one so the habit forms before scale makes it hard. Founders should resist the temptation to defer all documentation until "after product-market fit", because an outage in a clinical product, or a failed clinical-safety or DTAC (Digital Technology Assessment Criteria) assessment for want of evidence, can be existential. The goal is not a polished knowledge base but ensuring no single departure can sink the company.

### Enterprise

A large NHS trust, ICS, or health-tech supplier faces the opposite failure: too much documentation, scattered across SharePoint, Confluence, network drives, and email, with no single source of truth and poor findability. The enterprise challenge is information architecture, ownership, and pruning — deciding where each fact is mastered, assigning owners, retiring duplicates, and connecting knowledge management to service management and change control. Communities of practice earn their keep here, spreading patterns across dozens of teams that would otherwise each learn the same lesson painfully. The risk to manage is heavy contractor and multi-supplier use, where knowledge walks out of the door at the end of every contract unless capture is a contractual and cultural expectation.

### Government

A national or local public body — NHS England, DHSC, UKHSA, or a local authority — operates under statutory records-management duties, Freedom of Information obligations, and public-audit scrutiny, so knowledge management is partly a matter of law and public accountability. Decisions about services, money, and policy must be documented, retained for defined periods, and findable years later for select committees, National Audit Office reviews, and public inquiries; the recent history of major inquiries shows how poor record-keeping becomes a scandal in its own right. Government must hold the line between statutory records (retained and disposed of by schedule) and working knowledge (managed for currency), applying the NHS Records Management Code of Practice with discipline. Transparency is the watchword: the working assumption should be that documentation may one day be read by the public.

## Common failure modes

- **The hero and the bus factor of one.** Celebrating the individual who "just knows" the system while never funding the work to spread that knowledge. It feels efficient until the day they are unavailable and a safety-critical service has no one who can operate it.
- **Write-once documentation.** Documents created during a build and never touched again, drifting into confident falsehood. Stale docs are more dangerous than none, because people act on them.
- **The wiki landfill.** Thousands of pages, no structure, no owners, no review dates — knowledge that technically exists but cannot be found or trusted. Volume mistaken for value.
- **Docs far from the work.** Documentation in a separate tool nobody opens while coding, guaranteeing it diverges from reality. Docs-as-code is the antidote.
- **Lessons-learned theatre.** Post-incident reviews that produce a document and a list of actions that are never closed, so the same incident recurs. The process becomes ritual, not improvement.
- **Confusing records with notes.** Either deleting something you were legally required to retain, or hoarding everything forever and creating a data-protection and findability liability. Both stem from not distinguishing statutory records from team documentation.
- **Blame in the review room.** Reviews that punish the person nearest the failure, which teaches everyone to hide the real cause and destroys the honesty the process depends on.

## Maturity model

| Dimension | Initial | Developing | Defined | Optimizing |
|---|---|---|---|---|
| Knowledge capture | In people's heads; nothing written | Some docs written during builds, then abandoned | Docs are a definition-of-done, kept in version control | Capture is continuous; tacit knowledge routinely externalised via pairing and ADRs |
| Bus factor | Critical systems depend on one person | Risk acknowledged, no plan | Bus-factor-one systems on the risk register with owners and cross-training | No safety-critical system depends on a single individual; resilience is designed in |
| Findability | No structure; ad-hoc files everywhere | Central wiki exists but sprawling | Clear information architecture, owners, review dates, single source of truth | Knowledge is discoverable in seconds; onboarding tests and improves it |
| Incident learning | No reviews, or blame-driven | Reviews happen, actions rarely closed | Blameless reviews with owned, tracked actions feeding runbooks | Demonstrable prevention of recurrence; learning changes design and practice |
| Records & retention | No distinction; delete or hoard at random | Aware of duties, applied inconsistently | Statutory records and team docs separated; retention schedules applied | Lifecycle managed end-to-end; retention and disposal audited and defensible |

## Checklist

- [ ] Every critical system has a service manual, an up-to-date runbook, and ADRs for its significant decisions.
- [ ] Documentation is part of your definition-of-done and reviewed in the same pull request as the change.
- [ ] Each domain has a named single source of truth; known duplicates are deleted or redirected.
- [ ] Bus-factor-one systems are on the risk register with owners and an active cross-training plan.
- [ ] Runbooks have been tested by someone who did not write them, in a drill or a real incident.
- [ ] Post-incident reviews are blameless and produce owned, time-bound actions that get closed.
- [ ] The knowledge base has a clear structure, page owners, and review dates; stale pages are pruned.
- [ ] At least one active community of practice exists for a craft that spans teams, with time protected for it.
- [ ] Statutory records are distinguished from team documentation and managed to the correct retention schedule.
- [ ] New joiners are asked to fix the first documentation gap they hit as an early contribution.

## Key sources

- NHS England / NHSX, *Records Management Code of Practice 2021* — statutory retention schedules and lifecycle duties for health and care records.
- GOV.UK Service Manual (Government Digital Service) — guidance on writing for and running digital services, including documentation and operating a service.
- NHS Digital Service Standard — expectations for building and maintaining sustainable, well-documented digital services.
- Michael Nygard, "Documenting Architecture Decisions" (2011) — the originating pattern for architecture decision records (ADRs).
- Google, *Site Reliability Engineering* — blameless post-incident reviews (postmortems), runbooks, and reducing operational key-person risk.
- Etienne Wenger, *Communities of Practice: Learning, Meaning, and Identity* (1998) — the foundational text on communities of practice.
- Nonaka & Takeuchi, *The Knowledge-Creating Company* (1995) — the SECI model of tacit-to-explicit knowledge conversion.
- The Write the Docs community — practitioner guidance on docs-as-code and treating documentation as a product.

## References

1. Knowledge management — Wikipedia — https://en.wikipedia.org/wiki/Knowledge_management
2. Tacit knowledge — Wikipedia — https://en.wikipedia.org/wiki/Tacit_knowledge
3. Explicit knowledge — Wikipedia — https://en.wikipedia.org/wiki/Explicit_knowledge
4. SECI model of knowledge dimensions — Wikipedia — https://en.wikipedia.org/wiki/SECI_model_of_knowledge_dimensions
5. Bus factor — Wikipedia — https://en.wikipedia.org/wiki/Bus_factor
6. Runbook — Wikipedia — https://en.wikipedia.org/wiki/Runbook
7. Architectural decision — Wikipedia — https://en.wikipedia.org/wiki/Architectural_decision
8. Single source of truth — Wikipedia — https://en.wikipedia.org/wiki/Single_source_of_truth
9. Community of practice — Wikipedia — https://en.wikipedia.org/wiki/Community_of_practice
10. Records management — Wikipedia — https://en.wikipedia.org/wiki/Records_management
11. Information architecture — Wikipedia — https://en.wikipedia.org/wiki/Information_architecture
12. Postmortem documentation — Wikipedia — https://en.wikipedia.org/wiki/Postmortem_documentation
13. Onboarding — Wikipedia — https://en.wikipedia.org/wiki/Onboarding
14. Records Management Code of Practice 2021 — NHS England / NHSX — https://www.nhsx.nhs.uk/information-governance/guidance/records-management-code/
15. Service manual — Government Digital Service (GOV.UK) — https://www.gov.uk/service-manual
16. Documenting Architecture Decisions — Michael Nygard — https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions
17. Site Reliability Engineering — Google — https://sre.google/books/
18. Write the Docs — docs-as-code guidance — https://www.writethedocs.org/guide/docs-as-code/
</content>
</invoke>
