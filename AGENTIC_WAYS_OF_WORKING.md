# Agentic Ways of Working — Working Thesis

This is a working operating-model document, not a claim that the model is settled. It consolidates ideas already being explored across the personal backlog and consulting playbook about how AI/agents may change product and engineering teams.

## Core thesis

Agentic development does not simply make the existing software-development process faster. It changes the economics of implementation enough that the operating system around software teams may need to change with it.

> **When implementation and translation become dramatically cheaper, the scarce resources move toward understanding the problem, making good decisions, validating them in reality, and coordinating the organization around those decisions.**

The implication is broader than coding productivity:

**implementation speed → changes cadence → cadence changes coordination → coordination changes team boundaries → team boundaries change roles, decision authority, and measures of effectiveness**

## The bottleneck may move from development to the business

Traditional software organizations created significant machinery around expensive engineering capacity:

- grooming and refinement
- estimation
- sprint commitments
- story points
- detailed acceptance criteria
- roadmap and planning gates
- functional handoffs

As implementation gets cheaper and faster, those mechanisms may stop protecting the primary constraint.

Engineering may be able to move through multiple build/test/revise loops while the business is still trying to schedule a meeting, obtain stakeholder input, resolve a policy question, or decide what it actually wants.

The scarce capabilities increasingly become:

- understanding the real human/customer problem
- deciding what should exist
- prioritizing despite the ability to build many things
- product and design judgment
- supplying domain/business context
- making consequential decisions quickly enough
- validating changes in reality
- maintaining architectural and product coherence
- measuring outcomes
- knowing when to discard or change something

The governing question moves from:

> Can we afford to build this?

Toward:

> Should this exist, and have we learned enough to build or change it?

A useful warning:

> **If 10× engineering throughput creates 10× more meetings, approvals and synchronous questions, the organization did not become 10× faster. It moved the bottleneck.**

## The sprint may survive, but its job changes

The traditional two-week sprint did more than estimate and schedule engineering output. It also created a useful social contract with the rest of the organization:

> We have agreed on what this team is doing. Give it protected time to execute.

That protection from interruption and context switching still matters.

Simply shortening sprints because implementation is faster may therefore be exactly wrong. One-week sprints or continuous replanning can consume the productivity gain in coordination overhead.

A two-week period may remain useful, but increasingly as a **protected outcome / learning / decision horizon** rather than a container for a predicted quantity of coding work.

Old framing:

> Here is the engineering work we estimate we can complete during the next two weeks.

Possible new framing:

> Here is the problem/outcome this multidisciplinary team owns for this period. The team has protected execution time, decision authority inside agreed boundaries, and a small mechanism for obtaining consequential business decisions when necessary.

Inside that period the team may run many rapid loops:

**understand → make → use → observe → decide → change → repeat**

At the boundary, review:

- What did we learn?
- What changed for users or the business?
- What assumptions were disproven?
- What did we build and discard?
- What decisions did the team make?
- What remains uncertain?
- What technical/product debt accumulated?
- What outcome deserves the next protected period?

## Different clocks are emerging

Implementation speed and business-learning speed are not the same thing.

Engineering can potentially complete several build/test/revise loops in a day. Reality still takes time. Teams need to observe users, talk to customers, discover edge cases, measure outcomes, and make consequential decisions.

A possible model is therefore:

- **Business/product cadence:** deliberate learning, outcome selection, priority and consequential decisions.
- **Execution cadence:** continuous rapid implementation, testing, experimentation and revision inside the decision envelope.

The goal is not to make the whole company operate at the clock speed of a coding agent. It is to remove unnecessary waiting while preserving the time required for actual learning and judgment.

## Protect the team, not just Engineering

Fast implementation puts pressure on the traditional functional handoff model:

**Product → Design → Engineering → QA → Business → repeat**

Even organizations that call these people one cross-functional team often still operate this way in practice.

When an engineer or agent can reach the next product/design decision hours after starting, sequential handoffs cannot reliably keep pace.

The emerging unit may need to be a genuinely embedded multidisciplinary team:

**Business/Product + Design + Engineering + relevant specialists**

Specialist expertise does not become less important. The interaction model changes.

- Engineers need stronger product/design judgment.
- Designers can work against live software and rapid prototypes rather than primarily producing handoff artifacts.
- Product people spend less time manufacturing implementation specifications and more time inside the problem, decision and learning loop.
- Data/database/domain specialists inject expertise continuously instead of primarily handing artifacts to Engineering.
- Team members need enough shared context and authority to make tactical decisions without constant synchronous approval.

Potential principle:

> **Protect the multidisciplinary team, not the engineering function.**

## Agents as a translation and context layer

One of the most interesting possibilities is not replacing specialists, but reducing the translation cost between them.

A traditional interaction might look like:

**Designer → design artifact → ticket/specification → engineer interprets → implementation → designer review**

An agentic interaction could look more like:

**Designer works in their natural medium → agent helps translate the artifact and context into the shared project system → implementation agent consumes it → working software returns quickly → designer critiques live behavior → iteration continues**

The same pattern can apply to data specialists, researchers, product managers, operations experts and other domain experts.

This raises a more interesting organizational question than “how many engineers can AI replace?”

> **What team structures become possible when the translation cost between skilled people collapses?**

## Decision envelopes instead of continuous interruption

Faster execution should not require Product, Design or the business to answer a new question every hour.

Before a protected execution period, establish a decision envelope:

- problem/outcome being pursued
- priorities
- constraints and non-negotiables
- experience and technical principles
- known business/domain rules
- who has authority to make which decisions

When new decisions appear during execution:

1. **The team has sufficient context and authority** → decide and continue.
2. **The decision is cheap and reversible** → make an assumption, record it and continue.
3. **The decision is consequential and requires missing business/domain knowledge** → put it in a small decision/input queue.

Batch category 3 into predictable decision windows where practical rather than creating constant interruption.

> **AI should reduce the cost of implementation without increasing the organizational cost of coordination.**

## Measures of team effectiveness need to change

Traditional velocity becomes even less useful as an effectiveness measure when agentic tools make software output highly variable and cheap.

Story points may remain locally useful for planning or team self-reflection, but they should not become a cross-team productivity KPI.

Candidate measures are closer to flow, outcomes, learning and quality:

### Flow / responsiveness
- cycle time from observed problem to deployed improvement
- time from a consequential business question to a usable decision
- time from deployment to meaningful feedback
- carryover / blocked time
- PR or change turnaround where relevant

### Outcomes
- customer/business outcome changed
- adoption or behavior change
- operational improvement
- whether the original problem was actually reduced

### Learning
- number and quality of validated learning loops
- assumptions tested/disproven
- speed from evidence to changed direction
- ability to discard work when evidence says it is wrong

### Quality / sustainability
- defects and incidents
- rework caused by avoidable quality failures
- change failure / rollback rate
- architectural/product coherence
- debt created by rapid iteration and whether it is being managed proportionally to maturity/risk

### Team / developer experience
- unnecessary coordination burden
- waiting on decisions or other functions
- cognitive load
- ability to work with sustained focus
- whether specialists can contribute through their natural expertise/tools

A strong agentic team may look bad under traditional sprint accounting: discover something Monday, ship Monday afternoon, learn Tuesday that half the hypothesis was wrong, throw away part of the implementation, and ship a better solution Wednesday.

That may be exceptional performance rather than churn.

The more useful question becomes:

> **How quickly and reliably can this team turn a real customer/business observation into a validated improvement?**

## Human judgment becomes more important, not less

Cheap implementation makes it cheap to build the wrong thing.

Humans increasingly own:

- intent
- problem selection
- constraints
- product/design judgment
- consequential architecture and business decisions
- validation
- accountability for outcomes

Agents can absorb increasing amounts of:

- investigation
- translation between artifacts
- implementation
- test generation/execution
- migration work
- documentation
- repository/context maintenance
- production of intermediate artifacts

The boundary is not “humans think, agents code.” It should be determined by risk, reversibility, available context, authority and the need for human judgment.

## Relationship to current experiments

This thinking is being tested rather than merely theorized.

Current examples include:

- using agents across requirements, repository history, implementation, testing, migrations, product thinking and documentation;
- collaborating with an experienced designer while exploring how he can work through his natural design tools without needing to become a Git/terminal user;
- considering the same model for a database/data specialist;
- operating Max's and BCBG close enough to real users that rapid implementation can immediately encounter actual business rules and workflow friction;
- maintaining Git as durable project context so humans and agents can resume work without relying on conversational memory.

## Questions still open

This is not a finished methodology. Important questions include:

- What is the right protected planning/learning interval for different kinds of teams?
- Which traditional sprint ceremonies disappear, and which remain useful for reasons unrelated to coding speed?
- How should decision latency be measured without creating another management KPI that teams game?
- How much autonomy can a multidisciplinary team safely receive in regulated, high-risk or dependency-heavy environments?
- How do we prevent rapid implementation from creating design incoherence or technical debt faster than humans can perceive it?
- What artifacts remain necessary when agents can translate among artifacts cheaply?
- How should managers distinguish productive learning/rework from careless churn?
- How does this model change when the business itself cannot supply decisions or validation at the required pace?
- What team size/topology best exploits reduced translation cost while retaining deep specialist expertise?

## Source threads

This working thesis consolidates and extends ideas already captured in:

- `personal-backlog` Issue #13 — **Develop an operating model for agentic product & engineering teams**
- `consulting` Issue #11 — **Playbook: Rethink product delivery cadence for agentic development**
- `consulting` Issue #12 — **LinkedIn idea: How agentic development changes the two-week sprint**
- `consulting` Issue #16 — **Engineering leadership deep-dive page for brianwpayne.com**
- `WHAT_IM_BUILDING_AUG_2026.md` — current-thinking snapshot

Future changes to the core operating-model thesis should be consolidated here. Smaller posts, talks, portfolio pages and consulting material can derive from this document rather than becoming competing sources of truth.
