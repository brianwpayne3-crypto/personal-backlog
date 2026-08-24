# Master Priorities

_Last groomed: 2026-08-23 — refreshed against current repository/issues and separated by life/work lane_

This is the authoritative portfolio-level priority layer above all project repositories, issues, and idea backlogs.

It answers two related but different questions:

> **What matters most overall?**
>
> **Given the time/context I am in right now, what should I work on?**

Detailed requirements, decisions, and implementation work remain in project repos/issues. `PROJECT_INDEX.md` describes the body of work. This file governs attention and sequencing.

## Core principles

### Capture is not commitment

> **Creating or capturing an issue does not make it active work. New ideas are PARKED by default. Work may only enter ACTIVE through portfolio grooming.**

A GitHub issue is permission to stop remembering an idea — not an obligation to execute it.

### Explore is not execute

> **Design exercises, prototypes, mood boards, sketches, product thinking, and experiments do not automatically promote a project into ACTIVE execution.**

Exploration is allowed across active and parked projects when it is bounded and useful. It can clarify whether an idea is compelling before implementation commitment.

Examples of legitimate exploration:
- visual language / mood boards;
- core screen concepts and information hierarchy;
- workflow sketches;
- brand/identity experiments;
- small prototypes intended to learn rather than launch.

Exploration should have a stopping point. If it turns into sustained implementation, infrastructure, launch planning, or an expanding feature backlog, it has become execution and must compete for ACTIVE capacity.

### Human design collaboration still matters

AI-assisted design exploration is useful for getting unstuck, generating directions, articulating constraints, creating rough concepts, and preparing material for critique. It is **not assumed to replace a skilled human designer**.

For projects where design quality materially matters, a strong pattern is:

> **AI-assisted exploration → clearer brief/options → human designer critique/collaboration → implementation.**

This is especially relevant to BCBG/service intake, BikeStories, and personal/consulting brand work.

## Work lanes

A single global ranking is insufficient because not every project belongs in every block of time.

### PAID / MAX'S
Work performed for Max's should primarily consume Max's paid work time or deliberately agreed Max's project time. Being the highest operational priority does not mean it should automatically consume days off.

### CAREER
Job search, recruiter follow-up, interviews, engineering positioning, and directly useful portfolio material. External deadlines can override other lanes.

### OWNED / PERSONAL BUSINESS & PRODUCT
BCBG, consulting business development, personal brand, and other work the user owns. This is the main execution pool during discretionary project time when paid Max's work is not in context.

### CREATIVE / EXPLORATION
Bounded design/product/brand exploration, including parked ideas. This lane is intentionally allowed because experimentation has learning and creative value, but it does not silently become another committed build.

### LIFE / ADMIN / RISK
Insurance, financial/legal/admin, and other bounded obligations. High-downside risks may interrupt normal project sequencing.

## WIP limit

**Maximum: 3 major ACTIVE portfolio priorities across execution lanes.**

Do not solve overload by adding a fourth sustained execution stream. Bounded exploration and small risk/admin work can coexist, but should not become disguised major projects.

## ACTIVE

### PAID / MAX'S — AIM → Square cutover — PRIMARY WHEN IN MAX'S CONTEXT

**Why it matters:** Real operating business, Aug. 30 latest target cutover, substantial momentum, and the migration is now past much of the catalog/data-preparation work and into production validation/cutover readiness.

**Current reality:**
- Current physical bike inventory imported into Square production.
- Bike catalog structure validated around Size / Frame Style / Color.
- Manufacturer SKU/GTIN handling established.
- AIM customer source prepared/cleaned and customers imported.
- Production service items/prices and launch tax policy established.
- Production Sales and Service locations established.

**Next work when in Max's context:**
1. Transaction validation (#16/#28).
2. Checkout hardware decision (#30): Terminal + Hub vs iPad + Stand + printer; scanner/cash drawer compatibility; John/counter workflow.
3. Customer reconciliation and minimum safe Square ↔ HubSpot ↔ Smartwaiver identity flow (#28/#29).
4. Small catalog/transaction cleanup and tax/location verification.
5. Serial/receiving workflow validation; serial belongs at physical receiving/intake, not checkout.
6. Pre-cutover physical recount/reconciliation.
7. Explicit AIM cutoff/final delta/read-only transition (#17).

**Boundary:** Native Square + safe manual processes are acceptable. Do not build custom Square software or let perfect accessories/serial automation/CRM synchronization delay cutover unless testing proves a true blocker.

**Time-context rule:** On days off from Max's, this remains important but is **not the default answer to what to work on personally**. Work on it voluntarily if desired; the backlog should not convert days off into unpaid Max's development time.

**Exit ACTIVE when:** Square is the functioning transaction source of truth, first live workflows are stable, and AIM is in read-only/sunset validation.

---

### CAREER — Engineering job search / positioning — PROTECTED LANE

**Why it matters:** Direct path to the next full-time engineering leadership role; externally timed work cannot wait behind side projects.

Current focus:
- Applications and recruiter/hiring-manager follow-ups.
- Interview preparation when scheduled.
- Coherent engineering-leadership narrative connecting corporate scale with current operator/agentic work.
- `brianwpayne.com/engineering` / consulting #16 when it is the highest-leverage positioning task: the layer beneath the résumé, focused on judgment, architecture, ambiguity, systems of record, build-vs-buy, migrations/cutovers, agentic engineering, and current technical credibility.

**Override:** Scheduled interview, application deadline, or recruiter commitment wins.

**Exit ACTIVE when:** Career search is intentionally paused or a role is secured.

---

### OWNED — BCBG hosted operational pilot — PRIMARY OWNED BUILD

**Why it matters:** The local V1 workflow works end-to-end. The useful milestone is durable hosted real-world use, not more speculative features.

**Current reality:**
- Local workflow through Closed proven.
- Database/repository foundation #36 complete.

**Hosted sequence:**
1. #37 — prove hosted workflow persistence parity — NEXT.
2. #38 — private object/photo storage.
3. #39 — minimal authentication + Shop access protection.
4. #40 — recovery, backup, cost controls.
5. #43 — Next.js dependency advisory review/remediation.
6. #35 — protected Vercel/iPad deployment and validation.
7. Run real repairs through it; let usage drive backlog.

BCBG Square customer lookup/create (#47), search/filter polish (#44/#45), service-line UX (#41/#42), dashboards/Kanban, AI, and other enhancements do not outrank safe hosting unless real usage proves otherwise.

**Design exploration is explicitly allowed alongside this sequence.** Service-intake/operator UX is a good candidate for AI-assisted first-pass exploration followed by critique/collaboration with a real designer before substantial visual implementation. Design work should clarify the product rather than derail hosting into a redesign project.

**Exit ACTIVE when:** Protected hosted app is reliably used for actual BCBG repairs and immediate pilot defects are controlled.

## LIFE / ADMIN / BOUNDED RISK

### BCBG business liability insurance

BCBG #26 remains a real risk item. Get appropriate quotes/coverage for home-based bicycle/e-bike repair, including general liability, products/completed operations, customer bikes in care/custody/control, and test-riding where applicable. Investigate future Max's-branded home service coverage if that concept advances.

Handle promptly without turning it into another project.

## NEXT OWNED WORK

### Consulting client acquisition

Keep outward-facing and lightweight: real leads, conversations, cards/networking, and discovery. Do not substitute tooling/methodology/site infrastructure for talking to potential clients.

### Personal / consulting brand design

Design exploration for the personal/consulting presence is legitimate because it supports both career positioning and consulting credibility. It may include information architecture, visual language, page concepts, and how the engineering deep-dive relates to the broader site.

Use AI to develop a clearer brief/directions first; use a real designer for critique/refinement when visual quality and brand judgment become important. Do not let exploratory redesign become an open-ended website rebuild unless intentionally promoted.

### Max's customer fulfillment / serialized bike lifecycle

When Square stabilizes and during Max's context, treat #18/#19/#22/#26 as one operating problem: **we took someone's money or accepted a physical item — what do we still owe them, and where is it now?** Serial capture at receiving should anchor the physical bike lifecycle.

## CREATIVE / DESIGN EXPLORATION

Exploration here is allowed without promoting these projects to execution.

### BikeStories.bike — DESIGN EXPLORATION ALLOWED / BUILD PARKED

The implementation remains parked, but product/design exploration is allowed: mood board, visual language, owner library concepts, bike/project/story hierarchy, key screens, sharing concepts, and agent-assisted story organization.

The purpose is to learn what the product should feel like and whether the concept becomes more compelling when made concrete — **not to start coding it.** A human designer is likely especially valuable here once there is a coherent first-pass brief and set of concepts to react to.

### YourBikeSucks.com — CREATIVE TIMEBOX / WAITING

V0 is live on Vercel at `https://yourbikesucks.com`; domain/SEO/Search Console setup is complete. Serialized sticker fulfillment #4 is waiting on Prodigi and Midwest Label Supply responses. Do not build fulfillment infrastructure until a vendor validates the physical product/economics. V1 adjudication/global counter #2 remains optional.

This project can continue to serve as a bounded visual/brand playground, but it has reached a natural execution stopping point for now.

## MAINTENANCE ONLY

### Max's Test Ride application

Live/useful. Allowed: production bugs, security/reliability problems, and small changes needed for real operation. The Square checkpoint here is not a second Square program; `maxs-operations` remains authoritative. Broad Postgres/reporting/shopping-party expansion remains deferred.

## VISION / REQUIREMENTS CAPTURE ONLY

### General Manager AI / Small Retail Operations

Important long-term direction, not standalone build. Capture management questions, obligations, waiting states, exceptions, and decisions from real Max's/BCBG operations. Improve operating layers first.

## PARKED FOR EXECUTION

Preserved but not currently committed builds:
- BikeStories.bike implementation — design exploration allowed.
- DeLinkedIn.
- BustedJeep.com reboot.
- Zero-effort small-business content inbox / automated GBP product.
- Test Ride Postgres/reporting/shopping-party expansion.
- Max's service-system expansion beyond current sequencing.
- AI mechanic assistant.
- BCBG Kanban/dashboard/reporting expansion.
- General Manager AI implementation.
- Résumé single-source generator.
- Historical health/workout-data import.
- Consulting starter guide/workspace-launcher standards.
- brianwpayne.com Carrd → Git migration unless needed to deliver a high-leverage career/consulting outcome.
- Elaborate consulting methodology packaging/branding.
- Other captured ideas unless explicitly promoted.

**Parked execution does not prohibit thinking, sketching, or learning.** It prohibits accidentally turning exploration into another committed build.

## THOUGHT LEADERSHIP / CONTENT

Capture-first. Agentic engineering, delivery cadence, engineering rigor, customer journeys, human writing/AI content, ambient idea capture, etc. may be developed/published when naturally ready and effort is small. Do not create a content-production program.

## CONTEXTUAL “WHAT SHOULD I WORK ON?” RULE

First determine the current lane/context rather than blindly returning the globally highest-ranked project.

### If there is a time-sensitive career event
Do the career work.

### If currently working paid Max's time
Square cutover readiness is primary until stabilized.

### If off from Max's / discretionary personal project time
Default order:
1. Time-sensitive career work if any.
2. BCBG hosted pilot — currently #37 persistence parity.
3. Bounded BCBG insurance/risk work.
4. Consulting/client or personal-brand work with real leverage.
5. Bounded design exploration across BCBG, personal brand, BikeStories, or another captured concept when that is the kind of work desired.
6. Evaluate YourBikeSucks vendor replies when they arrive.

This is a recommendation system, not a command system. The owner can deliberately choose something else. The purpose is to expose tradeoffs and prevent everything from looking equally urgent.

## PORTFOLIO GROOMING PROCESS

1. Read this file, `PROJECT_INDEX.md`, and current repo issues/checkpoints.
2. Determine current life/work lane and availability before ranking next action.
3. Check real deadlines, interviews, customers, incidents, and risks.
4. Challenge ACTIVE against current repo reality and exit conditions.
5. Enforce WIP = 3 for sustained execution.
6. Distinguish **exploration** from **execution** explicitly.
7. Promote based on external timing, real users/revenue/career impact, risk reduction, dependency value, and momentum — not novelty alone.
8. Keep detailed implementation history in project repos; keep portfolio decisions here.

## Relationship to other portfolio files

- **`MASTER_PRIORITIES.md`** — What matters, and what deserves attention in the current context?
- **`PROJECT_INDEX.md`** — What exists, what state is it in, and what is its story?
- **Project repos/issues** — What exactly needs doing and what decisions/history belong to that project?

Together:

> **Capture broadly. Explore freely. Execute narrowly.**
