# Master Priorities

_Last groomed: 2026-08-23_

This is the authoritative portfolio-level priority layer above all project repositories, issues, and idea backlogs.

Its purpose is to answer one question:

> **Of everything I could work on, what should I work on now?**

Detailed requirements, decisions, and implementation work remain in their project repos/issues. `PROJECT_INDEX.md` describes the body of work. This file governs **what is allowed to consume attention now**.

## Core rule: capture is not commitment

> **Creating or capturing an issue does not make it active work. New ideas are PARKED by default. Work may only enter ACTIVE through portfolio grooming.**

A good idea is not automatically a priority.

The existence of a GitHub issue is permission to stop remembering the idea — not an obligation to work on it.

## WIP limit

**Maximum: 3 active portfolio priorities.**

Do not add a fourth active priority. Something must leave ACTIVE first.

Administrative/risk work that is small and bounded may happen alongside the active three without becoming another software/product workstream.

## ACTIVE

### 1. Max's AIM → Square cutover — PRIMARY

**Why now:** Real operating business, active migration, near-term cutover target, substantial work already invested, and finishing it unlocks cleaner downstream operations.

Current focus:
- Finish minimum Square catalog/inventory needed for cutover.
- Convert the clean physical bike inventory into the Square-ready import/model.
- Validate required real transaction scenarios in production/native Square.
- Complete customer migration/dedupe plan.
- Handle final AIM delta.
- Execute controlled cutover and stabilize.

**Scope rule:** Do not use the Square migration as an excuse to build custom applications on top of Square. Prefer native Square capabilities at cutover. Manual operator work is acceptable initially.

**Exit ACTIVE when:** Square is the functioning transaction source of truth and the immediate cutover/stabilization work is complete.

---

### 2. Engineering job search / positioning — PROTECTED LANE

**Why now:** This directly supports the next full-time engineering leadership role and has external timing that cannot wait behind side projects.

Current focus:
- Applications and recruiter/hiring-manager follow-ups.
- Interview preparation when an interview is scheduled.
- Maintain a coherent engineering-leadership narrative connecting corporate leadership experience with current hands-on/agentic work.
- Build the `brianwpayne.com/engineering` deep-dive page when it is the highest-leverage positioning task.

**Critical page principle:** `/engineering` is not a web résumé. It should provide the layer beneath the résumé: technical/product judgment, architecture reasoning, build-vs-buy decisions, ambiguity, systems thinking, agentic engineering practice, and current technical credibility.

**Override:** Time-sensitive interview/application work wins over other planned work.

**Exit ACTIVE when:** Full-time career search is intentionally paused or a role is secured. Until then this remains a protected lane, though its weekly effort may vary.

---

### 3. BCBG hosted operational pilot — NEXT BUILD

**Why now:** A substantial service workflow already exists. The highest-value next step is not more features; it is getting the existing system onto a durable hosted foundation and using it for real repairs.

Sequence:
1. Persistence parity / durable database.
2. Private/durable photo storage.
3. Authentication / shop protection.
4. Recovery, backup, and cost controls.
5. Deploy protected operational pilot.
6. Run real repairs through it.
7. Let real-world friction determine the next feature work.

**Scope rule:** Do not add search, filters, dashboards, Kanban, AI, visual polish, or speculative workflow features merely because they are in the backlog. Production use earns those features.

**Exit ACTIVE when:** The hosted protected application is being used reliably for actual BCBG repairs and the immediate pilot defects are under control.

## OVERRIDE RULES

These rules resolve priority without requiring a new grooming session every day.

1. **Scheduled interview / application deadline / recruiter commitment → career work wins.**
2. **Production failure affecting a real customer/business → fix or contain it.**
3. **Explicit customer commitment with a real deadline → honor the commitment.**
4. **Safety, legal, insurance, financial, or material business-risk issue → may interrupt normal priority order.**
5. Otherwise, **Square is the primary workstream until cutover.**
6. After Square exits ACTIVE, **BCBG hosted pilot becomes the primary build.**
7. A new exciting idea does **not** qualify as an override.

## SMALL / BOUNDED RISK & ADMIN WORK

These may be completed without promoting them into a major active product workstream, provided they stay bounded.

### BCBG business liability insurance

Get appropriate quotes/coverage for the real bicycle-repair operation, including completed-operations and care/custody/control considerations. This has high downside reduction relative to the effort required.

Do not postpone this because software work is more interesting.

## NEXT

Work here is eligible to enter ACTIVE **only when capacity opens**.

### Max's customer fulfillment / bike lifecycle

Treat the scattered paid-order, arrival, serial, build, accessory, notification, and fulfillment issues as one operational problem:

> **We took someone's money. What do we still owe them?**

Likely lifecycle:

Paid/order → ordered bike arrives → serial captured → build/accessories/commitments → ready/customer communication → fulfilled.

This should be the next major Max's operational problem after Square stabilizes because forgotten customer obligations create direct business/customer risk.

### Consulting client acquisition

Keep this lightweight and outward-facing:
- Publish already-prepared local/Facebook outreach rather than building more consulting infrastructure.
- Use consulting cards/network conversations.
- Follow up on real leads.

Do not substitute website/tooling/methodology work for talking to potential clients.

## MAINTENANCE ONLY

### Max's Test Ride application

The application is already live and useful.

Allowed now:
- Real production bugs.
- Security/reliability problems.
- Small changes required for continued real-world operation.

Not active now:
- Postgres migration simply because it would be architecturally cleaner.
- Reporting/dashboard expansion.
- Shopping-party model.
- Broad new feature development.

Production reality can promote a specific issue if it becomes materially important.

## VISION / REQUIREMENTS CAPTURE ONLY

### General Manager AI / Small Retail Operations

This is an important long-term vision, **not a current standalone build**.

The GM AI sits above coherent operating layers and helps a small retail owner run the business based on how it actually works. Max's is the proving ground.

For now:
- Capture management questions and decisions that emerge from real operations.
- Improve the underlying operating layers.
- Notice what information the owner repeatedly needs.
- Capture examples of obligations, exceptions, waiting states, priorities, and decisions.

Do not build the AI layer prematurely. The operating context beneath it is the current work.

## CREATIVE TIMEBOX

### YourBikeSucks.com

This is the one explicitly allowed small creative side project.

Purpose:
- Enjoyable design/brand experiment.
- AI-assisted visual-design learning.
- Potential tiny web/merch artifact.

Constraint:

> **Creative break, not active program.**

Allowed scope:
- Sticker/identity exploration.
- Tiny indexable V0 site.
- Optional tiny bicycle-adjudication interaction with incremental case number.

Do not allow it to expand into accounts, social networking, elaborate submissions, AI bicycle analysis, merch infrastructure, or a large software project.

If it starts competing with ACTIVE work, stop.

## PARKED

These are deliberately preserved but are **not currently allowed to compete for execution**:

- BikeStories.bike.
- DeLinkedIn.
- BustedJeep.com reboot.
- Zero-effort small-business content inbox / automated GBP posting product.
- Test Ride Postgres migration and architecture expansion.
- Test Ride reporting/dashboard work.
- Test Ride linked shopping parties.
- Max's digital assembly checklist as a standalone project.
- Max's service-system expansion.
- AI mechanic assistant.
- BCBG Kanban/dashboard/reporting expansion.
- General Manager AI implementation.
- Résumé single-source generator / elaborate résumé infrastructure.
- Historical health/workout-data import.
- Consulting starter guide.
- Consulting workspace-launcher/tooling standards.
- brianwpayne.com Carrd → Git migration.
- Elaborate consulting-methodology packaging/branding.
- Other captured personal/project ideas unless explicitly promoted during grooming.

**Parked does not mean rejected.** It means the idea is safely stored and does not get to consume current attention.

## THOUGHT LEADERSHIP / CONTENT

Ideas such as agentic engineering, speed-to-production, engineering rigor, ambient idea capture, customer journeys, and writing in the AI era should remain **capture-first**.

Allowed:
- Capture a thought when it occurs.
- Develop/publish a post when it naturally feels ready and the effort is small.

Avoid:
- Turning content production into another large project.
- Building elaborate publishing infrastructure before there is a real need.
- Allowing a post idea to displace ACTIVE operational/career work.

## PORTFOLIO GROOMING PROCESS

When grooming the entire body of work, use this sequence:

### 1. Read current reality
Review:
- `MASTER_PRIORITIES.md`
- `PROJECT_INDEX.md`
- Open issues across active repositories.
- Any real deadlines, interviews, customer commitments, production incidents, or business risks.

### 2. Challenge ACTIVE
For each active priority ask:
- Is it still materially important?
- Is there a real reason it must happen now?
- Has its exit condition been met?
- Has another item become more urgent/valuable?

### 3. Enforce WIP = 3
Never solve overload by adding another ACTIVE item.

If something new deserves ACTIVE status, explicitly demote, complete, or pause something else.

### 4. Promote based on evidence, not excitement
Prefer work with:
- External deadlines.
- Real customers/users.
- Revenue/career impact.
- Risk reduction.
- Strong dependency/unblocking value.
- Existing momentum close to a useful outcome.

Penalize work that is primarily:
- Novel.
- Fun but expanding rapidly.
- Infrastructure without an immediate consumer.
- Speculative architecture.
- A solution looking for a problem.
- Another way to avoid finishing something already underway.

### 5. Reorder NEXT/PARKED as needed
It is fine for PARKED to contain many good ideas. Do not groom it into a fake ordered queue unless something is realistically approaching execution.

### 6. Record the decision here
Update the date, ACTIVE priorities, NEXT items, and any relevant rules. Do not duplicate detailed project status that belongs in underlying issues.

## Default answer to “What should I work on?”

Until this file is groomed again:

1. **If there is time-sensitive engineering job-search work, do that.**
2. Otherwise **work on the Max's Square cutover.**
3. If Square work is blocked or complete, **advance the BCBG hosted operational pilot.**
4. Handle bounded BCBG insurance/risk work promptly.
5. Do not start another project because it sounds interesting.

## Relationship to other portfolio files

- **`MASTER_PRIORITIES.md`** — What deserves attention now?
- **`PROJECT_INDEX.md`** — What projects/ideas exist, what state are they in, and what is their story?
- **Project repos/issues** — What exactly needs to be done and what decisions/history belong to that project?

Together these form the portfolio operating system:

> **Capture broadly. Understand the portfolio. Execute narrowly.**
