# Approval Isn't Behavior

**Alejandro Mizrahi · Research Notes · BotConduct Observatory**
*Launch note for the BotConduct Conduct Taxonomy v1.0*

---

Nearly every mechanism the autonomous web has produced so far answers one of two questions: *who is this agent?* or *what is this agent allowed to do?* Registration schemes, agent cards, signed user-agents answer the first. Robots directives, terms of service, usage policies, pay-per-crawl gates answer the second.

Neither answers the question a property owner actually has: **what did this agent do?**

That gap is not an oversight. It is structural. Identity is declared by the agent. Permission is granted by the owner. But conduct is *observed* — and observation only happens on the receiving side. No registry can see it. No policy can produce it. The only party in a position to describe an agent's behavior is the property that received it.

Today we are publishing the vocabulary we use to describe it: the **BotConduct Conduct Taxonomy v1.0** — a receiver-side, versioned classification of observed automated conduct.

## Why a taxonomy, and why public

When a property owner says "we're getting scraped," that sentence carries almost no information. Scraped by something that declared itself and followed the rules? By something anonymous that accessed the infrastructure at scale on the way through? By something that came back every day for a month? Those are different events, with different exposure, requiring different responses — and until now there has been no shared way to say which one happened.

A taxonomy is the cheapest piece of infrastructure a field can build. Before incident databases, before loss statistics, before contracts can reference behavior — there has to be a vocabulary stable enough to be cited. Naming precedes measurement; measurement precedes accountability.

So the vocabulary is public, free to use, and versioned like a specification: definitions change only through a new dated version, never retroactively. A classification issued under v1.0 stays a v1.0 classification. Anyone can adopt the vocabulary — to describe traffic, to write contracts, to compare notes across properties.

## The three dimensions

The taxonomy classifies each observed session along three independent axes:

- **Declared identity** — what the agent claims to be, and whether the claim is consistent with the infrastructure it arrives from.
- **Observed conduct** — what it did: *Predatory, Suspicious, Indeterminate,* or *Respectful*, characterized against the property's published rules and ordinary use.
- **Persistence** — whether it returns: *First visit, Occasional, Recurrent, Persistent.*

The independence of the axes is the point. An agent can be honest and hostile, anonymous and respectful, declared and relentless. Collapse the dimensions — as block/allow tooling does — and the information that matters disappears. What receiver-side observation surfaces most clearly is the *combinations*: identity that wouldn't withstand scrutiny, sustained over weeks, with conduct that defeats accountability.

And persistence deserves its own sentence: a hostile request is noise; the same actor returning daily for a month is a relationship. Traditional tooling measures requests. In the Observatory's experience, exposure tracks persistence.

## What the taxonomy refuses to do

By design, the taxonomy does not attribute intent, does not predict future behavior, does not identify operators, and does not issue legal conclusions. It maps to existing governance frameworks — NIST AI RMF, OWASP Agentic AI, MITRE ATLAS/ATT&CK, EU AI Act — as *descriptive references*, never as findings of contravention. It describes conduct. Everything else is someone else's job, and pretending otherwise is how vocabularies lose their neutrality and their usefulness in the same week.

The methodology that assigns sessions to categories — signals, thresholds, precedence — is not part of the public document. The vocabulary is open; the oracle is closed. Its outputs are cryptographically verifiable and reproducible; the method itself is never disclosed. Independent third-party audit of consistency and integrity is available under NDA, without disclosure of the method. That separation is deliberate: a public vocabulary anyone can cite, grounded in an observation method that cannot be gamed by reading it.

## Where this goes

Every report the Observatory issues now classifies conduct per this taxonomy, citing the version in force, with assignments materialized and cryptographically signed at generation time. When two properties, or an insurer and an insured, or a platform and a regulator need to talk about what an automated agent did — they can now do it in the same words.

Version 1.0 is the floor, not the ceiling. The vocabulary will evolve the way useful vocabularies do: in public, in versions, and never retroactively.

**BotConduct Conduct Taxonomy v1.0:** https://botconduct.org/conduct-taxonomy

---

*BotConduct Observatory — botconduct.org. We observe, characterize, reference, and sign.*
