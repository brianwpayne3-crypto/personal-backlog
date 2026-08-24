# What I'm Building / Thinking About — August 2026

This is not a pitch deck or a roadmap. It is a lightweight snapshot of the things I have been building, operating, and thinking about — mostly so I can share them with smart people I know, compare notes, and get reactions.

Some of this is real operational work. Some may become consulting or product work. Some is deliberately exploratory or ridiculous.

## The idea tying the operational work together: Manager AI

The most interesting idea emerging from the work is an AI-powered **Manager / General Manager layer for a small business**.

This did not start as "I should build an AI product." It emerged from actually working inside small businesses, especially Max's Electric Bikes and Bucks County Bike Garage, and seeing how many separate systems, workflows, obligations, and bits of context an owner/operator has to hold together.

A small retailer might have Square for transactions, HubSpot for customer data, Smartwaiver for waivers, service workflows, inventory/order data, customer messages, test rides, special orders, repairs, deliveries, and a bunch of human knowledge that exists nowhere except someone's head.

The longer-term question is:

> **What if the owner did not have to constantly operate all of those systems directly? What if a Manager AI could sit above them, understand the state of the business, and help run the operation the way a good general manager would?**

Examples:
- What needs my attention today?
- Which customers are waiting on us?
- What did we promise someone that has not happened yet?
- Which service jobs are blocked or overdue?
- Which bikes or parts still need to be ordered?
- What arrived but has not been assembled or assigned?
- Which test-ride customers look worth following up with?
- What sold this week?
- Is anything likely to have fallen through the cracks?
- What decisions do I actually need to make today?

The important part is that the AI layer only becomes useful if the operational layers underneath it are trustworthy. A lot of what I am doing now is effectively creating or cleaning up those layers.

This idea has also been shaped through conversations with people I trust. Mike Doolittle, in particular, helped me see/crystallize the Manager AI idea while we were talking through the operational work.

## The real-world laboratory: Max's Electric Bikes

I work inside the business, not outside it as a consultant making recommendations. That has turned Max's into a useful laboratory for understanding what small-business transformation actually looks like.

The approach has generally been:

> **Work inside the operation → notice friction and dropped context → understand how the people actually work → improve an existing system when possible → build something small only when necessary.**

### AIM → Square migration

We are replacing the legacy AIM point-of-sale/operating system with Square.

This has involved much more than selecting software: extracting and cleaning customer/inventory data, defining the production catalog, modeling bike variations, thinking through serialized physical inventory, service transactions, tax behavior, payment hardware, special orders, cutover strategy, and what information belongs at receiving versus checkout.

A major principle has been **do not build custom software just because I can**. Use native Square capabilities and safe manual processes first; customize only where real operational friction proves it is necessary.

### Test Ride app

A small Next.js application built around the actual in-store test-ride workflow.

It connects customer/test-ride activity with HubSpot and the waiver process, gives staff a lightweight operating interface, and creates better customer context than the previous ad-hoc process.

This is already a functioning real-world application rather than a portfolio demo.

### Smartwaiver → HubSpot

Work to connect waiver/customer identity with the CRM and Test Ride experience. The interesting part is less the API plumbing than the identity and workflow questions: shared emails, matching the correct human, repeat waivers, and deciding which system should own which fact.

### Customer fulfillment / serialized bike lifecycle

An emerging problem after the Square work: once someone pays us, or once a physical bike arrives, what exactly do we still owe that customer and where is that physical unit in its lifecycle?

The developing model is something like:

**ordered → arrived/received → serial captured → assembly/build requirements → accessories/parts owed → ready → customer notified → fulfilled**

This is exactly the kind of cross-system operating state that eventually makes the Manager AI idea interesting.

## Bucks County Bike Garage / Service Intake

BCBG is my own small bicycle service operation and another place to test workflows directly.

I have built an iPad-first service workflow covering:

**Intake → Inspection → Findings/approval → Authorized work → Final QC → Ready → Pickup/payment → Closed**

The local workflow works end-to-end. I am now moving it toward a durable hosted pilot with Postgres, photo storage, minimal authentication, recovery/backup controls, and Vercel deployment.

What interests me here is not merely making a repair-shop app. It is figuring out how to represent the actual relationship between the mechanic, the physical bike, findings, customer authorization, work performed, communication, and handoff without making the operator fight the software.

### Design question

The workflow is far enough along that I want stronger design judgment applied to it. I can use AI to explore information hierarchy, screens, and directions quickly, but I think this is an area where critique from an experienced product/UI designer could materially improve the product before I over-invest in visual implementation.

## Consulting / transformation work

There is a consulting thesis emerging from the same work:

**systems around people, rather than forcing people around systems.**

The interesting consulting work for me is not "I can build an app." It is entering an ambiguous operation, understanding how work actually happens, finding where information/context/obligations break down, deciding what should be process versus software versus integration, and then getting something useful into operation quickly.

I am also working on how to represent this on my personal/consulting site without turning it into another generic technology-consulting website.

## Agentic development as a way of working

Another experiment underneath all of this is the development process itself.

Agentic tools have dramatically changed the cost of turning an idea into working software. I am using agents not just to generate code but to help with requirements, repository history, implementation, tests, migrations, product thinking, operational documentation, and portfolio grooming.

The interesting organizational question is what happens when this expands beyond one person. I am especially interested in how an experienced designer or data/database person could contribute using the tools they naturally use while agents help bridge artifacts, code, Git, implementation, and context rather than requiring everyone to become a traditional software engineer.

## BikeStories.bike — product/design exploration

A product idea for people who own bikes they actually care about.

Instead of a generic bike inventory, each bike becomes a living project/story: photos, specifications, documents, modifications, components, history, ride stories, and eventually material that can be shared publicly or used when selling the bike.

A major part of the concept is reducing the amount of organization required from the owner. An agent could ingest photos/documents/details and help construct the bike's story rather than forcing someone to manually maintain a database.

It could also generate selected outputs from that history: a shareable bike page, social posts, a blog/story, or a detailed sale listing.

I own `bikestories.bike`, but implementation is intentionally parked. This is currently a good candidate for product/design exploration: what does the owner library feel like, what is a "bike story," what information deserves prominence, and what would make someone actually want to maintain/share one?

## YourBikeSucks.com — deliberately tiny creative experiment

This is the opposite end of the spectrum.

I bought `yourbikesucks.com` and built a deliberately absurd Bureau of Bicycle Assessment identity around an official-looking bicycle inspection sticker that declares:

**THIS BIKE SUCKS**

The V0 site is live. The next possible interaction is an official adjudication with a globally incremental case number. I am also investigating whether the physical stickers can be manufactured/dropshipped with real unique case numbers; two potential vendors are currently evaluating the requirement.

This project is intentionally allowed to be funny and small. It is useful partly because it lets me experiment with brand, product restraint, and visual language without needing to justify a large business case.

## Personal / engineering / consulting brand

I am also trying to figure out how to represent what I actually do now.

My résumé covers the traditional engineering-leadership history. The more interesting missing layer is the judgment underneath it: architecture and product decisions, operating through ambiguity, systems of record, build-vs-buy, migration/cutover thinking, transformation, and this newer agentic way of working.

There is probably both an engineering-leadership version and a consulting/business-transformation version of that story. I want design help making it coherent rather than simply adding more text to a website.

## Things I'd love reactions to

Not assignments — just things I am genuinely curious to compare notes on:

- Does the **Manager AI** concept feel like a coherent product/thesis when seen above the actual operating systems?
- What is visually/product-wise weak or confusing in the BCBG service-intake workflow?
- Where should a designer enter an agentic workflow like mine without having to become a Git/terminal person?
- Which of these things feel like real products or consulting opportunities versus interesting experiments?
- Does BikeStories become compelling when treated as a designed experience rather than a feature list?
- How should my personal/consulting presence communicate this body of work without looking like a giant résumé or a generic consultancy?
- What are you working on, and where are you seeing AI/agents change your own process?

## Why I'm sharing this

I am not trying to recruit anyone into a project or hand out assignments. I have been building and thinking about enough interconnected things that I want to get them out of my own head, show them to people whose judgment I respect, hear what they are working on, and see what conversations or collaborations naturally emerge.
