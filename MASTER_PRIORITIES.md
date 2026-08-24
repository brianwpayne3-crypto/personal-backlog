# Master Priorities

_Last groomed: 2026-08-23 — refreshed against current repository/issues after today's work_

This is the authoritative portfolio-level priority layer above all project repositories, issues, and idea backlogs.

Its purpose is to answer one question:

> **Of everything I could work on, what should I work on now?**

Detailed requirements, decisions, and implementation work remain in their project repos/issues. `PROJECT_INDEX.md` describes the body of work. This file governs **what is allowed to consume attention now**.

## Core rule: capture is not commitment

> **Creating or capturing an issue does not make it active work. New ideas are PARKED by default. Work may only enter ACTIVE through portfolio grooming.**

A good idea is not automatically a priority. The existence of a GitHub issue is permission to stop remembering the idea — not an obligation to work on it.

## WIP limit

**Maximum: 3 active portfolio priorities.**

Do not add a fourth active priority. Something must leave ACTIVE first.

Administrative/risk work that is small and bounded may happen alongside the active three without becoming another software/product workstream.

## ACTIVE

### 1. Max's AIM → Square cutover — PRIMARY

**Why now:** Real operating business, Aug. 30 latest target cutover, substantial momentum, and the migration is now past much of the catalog/data-preparation work and into production validation/cutover readiness.

**Current reality from the Max's repo:**
- Current physical bike inventory has been captured and imported into Square production.
- Bike catalog structure has been validated around Size / Frame Style / Color options.
- Known manufacturer SKU/GTIN data is being preserved correctly rather than misusing serial numbers as SKU.
- AIM customer migration source was prepared/cleaned and customers imported into Square.
- Production service items/prices exist and launch tax policy has been decided.
- Production Sales and Service locations are established.
- The main remaining work is no longer "build the inventory/catalog." It is **prove the real day-one operation, settle hardware/payment choices, reconcile data, and cut over.**

**Immediate next actions — use the detailed Max's issues/checklists as source of truth:**
1. **Transaction validation (#16 / #28):** run representative bike-sale and service workflows in a supported Square POS environment, including imported/new customer, correct bike variation, price/tax, required $199 Service Plan, accessory/manual merchandise, payment/receipt, and inventory decrement behavior.
2. **Checkout hardware decision (#30):** compare Square Terminal + Hub against new iPad + Square Stand + compatible thermal printer as complete systems; finish cash-drawer and Code CR950 scanner compatibility checks; discuss the actual counter workflow with John. Virtual Terminal remains useful for browser-side testing but is not the full retail POS test.
3. **Customer verification/integration (#28/#29):** export/reconcile Square customers against the cleaned migration source, spot-check imported records, prove new-customer creation/lookup, and define the minimum safe Square ↔ HubSpot ↔ Smartwaiver identity flow without building a broad CRM sync platform.
4. **Catalog/transaction cleanup (#28):** verify tax at checkout, service items at intended locations, Manual Merchandise fallback, minimum day-one accessory seed list, and any small missing service/catalog items such as the $50 rack build/install service.
5. **Bike serial/receiving operating rule:** preserve the decision that serial capture belongs at receiving/intake, not checkout; collect/add known serials as physical bikes are validated without allowing perfect serial coverage to block cutover.
6. **Pre-cutover reconciliation:** immediately before launch physically recount bikes and reconcile Square against what is actually on hand; account for bikes received/sold/returned since the initial import.
7. **AIM cutoff (#17):** choose explicit cutoff, rerun/preserve final AIM Sales Journal delta from the Aug. 16 baseline, stop new AIM transactions, start all new transactions in Square, validate first live transactions, then retain AIM read-only briefly before sunset.

**Scope rule:** Do not turn Phase 1 into custom Square software. Native Square + safe manual processes are acceptable. Do not let perfect accessories, automated serial workflows, build sheets, fulfillment systems, or broad CRM synchronization delay a safe transaction cutover unless testing proves one is genuinely blocking.

**Exit ACTIVE when:** Square is the functioning transaction source of truth, the first live workflows are stable, and AIM has moved into read-only/sunset validation.

---

### 2. Engineering job search / positioning — PROTECTED LANE

**Why now:** This directly supports the next full-time engineering leadership role and has external timing that cannot wait behind side projects.

Current focus:
- Applications and recruiter/hiring-manager follow-ups.
- Interview preparation when an interview is scheduled.
- Maintain the engineering-leadership narrative connecting corporate leadership scale with current operator/agentic work.
- **Consulting #16:** build `brianwpayne.com/engineering` when it is the highest-leverage positioning task. It should be the layer beneath the résumé, not a web résumé: architecture/product judgment, ambiguity, systems of record, build-vs-buy, migration/cutover thinking, agentic engineering practice, and current technical credibility.
- Continue developing the reusable interview backbone/system-design reasoning only when it directly supports an upcoming interview or materially improves readiness.

**Override:** Scheduled interview, application deadline, or recruiter commitment wins over planned side-project work.

**Exit ACTIVE when:** Full-time career search is intentionally paused or a role is secured.

---

### 3. BCBG hosted operational pilot — NEXT BUILD

**Why now:** The local V1 workflow already works end-to-end. The useful next milestone is durable hosted real-world use, not more speculative feature development.

**Current reality from the BCBG repo:**
- Local operator workflow through Closed has been proven.
- Database/repository foundation **#36 is complete**.
- The controlled hosted sequence is now:
  1. **#37 — prove hosted workflow persistence parity** — NEXT.
  2. **#38 — private object/photo storage.**
  3. **#39 — minimal authentication + Shop access protection.**
  4. **#40 — recovery, backup, and cost controls.**
  5. **#43 — review/remediate current Next.js dependency advisories before production deployment.**
  6. **#35 — deploy and validate the protected hosted pilot on the iPad.**
  7. Run real BCBG repairs through it and let usage drive the next backlog.

**Important sequencing decision:** BCBG Square customer lookup/create (#47), search/filter polish (#44/#45), service-line UX fixes (#41/#42), feedback UI, dashboards/Kanban, AI, and other enhancements do **not** outrank getting the existing workflow safely hosted unless they become actual deployment/real-use blockers.

**Scope rule:** Preserve the tested workflow and one maintained codebase. Build only the minimum Shop ownership/security foundation needed for BCBG now while keeping a cheap path to Max's later. Do not turn this into a generic SaaS platform.

**Exit ACTIVE when:** The protected hosted app is being used reliably for actual BCBG repairs and immediate pilot defects are under control.

## OVERRIDE RULES

1. **Scheduled interview / application deadline / recruiter commitment → career work wins.**
2. **Production failure affecting a real customer/business → fix or contain it.**
3. **Explicit customer commitment with a real deadline → honor it.**
4. **Safety, legal, insurance, financial, or material business-risk issue → may interrupt normal priority order.**
5. Otherwise, **Square is the primary workstream until cutover.**
6. After Square exits ACTIVE, **BCBG hosted pilot becomes the primary build.**
7. A new exciting idea does **not** qualify as an override.

## SMALL / BOUNDED RISK & ADMIN WORK

### BCBG business liability insurance

**BCBG #26 remains a real risk item.** Get quotes/coverage appropriate to the home-based bicycle/e-bike repair operation, explicitly including general liability, products/completed operations, customer bikes in care/custody/control, and test-riding where applicable. Also investigate whether a future Max's-branded home service arrangement could be explicitly covered by Max's policy.

This should be handled promptly as bounded risk reduction without becoming a fourth software workstream.

## NEXT

Work here may enter ACTIVE only when capacity opens.

### Max's customer fulfillment / serialized bike lifecycle

After Square stabilizes, treat Max's #18, #19, #22, and #26 as related parts of one operating problem:

> **We took someone's money or accepted a physical bike/item. What do we still owe them, and where is it now?**

The emerging lifecycle includes paid special orders, arrival, receiving/serial capture, assembly/build requirements, customer accessories/parts still owed, readiness, notification, and final fulfillment.

The Aug. 23 serial decision is important: **capture the serial when the bike physically arrives**, then let assembly/readiness/customer fulfillment attach to that serialized physical unit. Do not build this as disconnected reminder/checklist apps.

### Consulting client acquisition

Keep this outward-facing and lightweight:
- Follow up on real leads/conversations.
- Use consulting cards/networking when useful.
- Use the small-business discovery guide when actual conversations occur.

Do not let Carrd migration, website polish, playbook packaging, or internal consulting infrastructure substitute for talking to potential clients.

## MAINTENANCE ONLY

### Max's Test Ride application

The application is already live/useful. Allowed now: production bugs, security/reliability problems, or small changes required for continued real-world operation.

The Square migration checkpoint that also exists in the Test Ride repo is **not a separate portfolio workstream**; `maxs-operations` is the authoritative operating/cutover source going forward. Avoid maintaining two competing migration plans.

The date-specific Smartwaiver repeat-signing requirement has a workable manual process and remains deferred unless real volume/friction changes that decision.

## CREATIVE TIMEBOX / WAITING

### YourBikeSucks.com

**Current reality:** V0 is no longer hypothetical. It is built, deployed on Vercel, live at `https://yourbikesucks.com`, mobile/desktop reviewed, connected to the Namecheap domain, technically SEO-ready, submitted to Google Search Console, sitemap submitted, and homepage indexing requested. V0/domain issues are closed.

Open work:
- **#4 serialized physical sticker fulfillment — WAITING ON VENDORS.** Prodigi and Midwest Label Supply were contacted on Aug. 23. Do not build commerce/fulfillment infrastructure until a vendor proves the physical sticker requirements and economics.
- Gelato remains a secondary vendor check only if needed.
- **#2 V1 adjudication/global case counter** remains an optional creative increment, not an active obligation.

Constraint remains:

> **Creative break, not active program.**

The project has reached a natural stopping point. Vendor responses can be evaluated when they arrive without promoting the project into ACTIVE. Do not let the fun/novelty of the Bureau concept displace Square, career work, or BCBG hosting.

## VISION / REQUIREMENTS CAPTURE ONLY

### General Manager AI / Small Retail Operations

Important long-term direction, not a standalone build. Continue capturing management questions, obligations, waiting states, exceptions, and decisions that emerge from Max's/BCBG. Improve the operating layers first. The AI layer earns priority only when trustworthy operational context beneath it exists and a concrete management use case is ready.

## PARKED

Preserved but not currently allowed to compete for execution:
- BikeStories.bike.
- DeLinkedIn.
- BustedJeep.com reboot.
- Zero-effort small-business content inbox / automated GBP product.
- Test Ride Postgres/reporting/shopping-party expansion.
- Max's service-system expansion beyond the current cutover/fulfillment sequencing.
- AI mechanic assistant.
- BCBG Kanban/dashboard/reporting expansion.
- General Manager AI implementation.
- Résumé single-source generator.
- Historical health/workout-data import.
- Consulting starter guide/workspace-launcher standards.
- brianwpayne.com Carrd → Git migration unless it becomes necessary to deliver a high-leverage career/consulting page.
- Elaborate consulting methodology packaging/branding.
- Other captured ideas unless explicitly promoted during grooming.

**Parked does not mean rejected.** It means the idea is safely stored and does not get to consume current attention.

## THOUGHT LEADERSHIP / CONTENT

Agentic engineering, delivery cadence, engineering rigor, customer journeys, human writing/AI content, and related ideas remain capture-first. Develop/publish when something naturally feels ready and the effort is small. Do not create another content-production workstream.

## PORTFOLIO GROOMING PROCESS

When grooming the body of work:
1. Read `MASTER_PRIORITIES.md`, `PROJECT_INDEX.md`, and **current repo issues/checkpoints**, not just this file's previous status text.
2. Check real deadlines, interviews, customer commitments, production incidents, and business risks.
3. Challenge each ACTIVE item against current repo reality and its exit condition.
4. Enforce WIP = 3.
5. Promote based on external timing, real users/revenue/career impact, risk reduction, dependency value, and momentum toward a useful outcome — not novelty.
6. Update this file with portfolio decisions and immediate project-level next steps, while leaving detailed requirements/history in the project repos.

## Default answer to “What should I work on?”

As of this grooming:

1. **If there is time-sensitive engineering job-search work, do that.**
2. Otherwise **continue Square cutover readiness — specifically transaction/hardware/customer validation, not more inventory capture.**
3. If Square work is blocked by needing shop hardware/John/in-person access, **advance BCBG #37 persistence parity** rather than inventing another project.
4. Handle BCBG insurance as bounded risk work.
5. Evaluate YourBikeSucks vendor replies when they arrive; otherwise leave it waiting.
6. Do not start another project because it sounds interesting.

## Relationship to other portfolio files

- **`MASTER_PRIORITIES.md`** — What deserves attention now?
- **`PROJECT_INDEX.md`** — What projects/ideas exist, what state are they in, and what is their story?
- **Project repos/issues** — What exactly needs to be done and what decisions/history belong to that project?

Together:

> **Capture broadly. Understand the portfolio. Execute narrowly.**
