# BotConduct Conduct Taxonomy

**Version 1.0 — June 2026**
**Rafael Mizrahi & Alejandro Mizrahi · BotConduct Observatory · botconduct.org**
**Canonical URL:** https://botconduct.org/conduct-taxonomy

---

## Abstract

The BotConduct Conduct Taxonomy is a receiver-side vocabulary for describing the observed conduct of automated agents on web properties. It classifies each observed session along three independent dimensions: **declared identity**, **observed conduct**, and **persistence**. The taxonomy describes what an agent *did* on a property, as observed by that property — independent of what the agent claims to be, who operates it, or any inference of purpose.

It exists because the autonomous web has vocabularies for what agents *are* (user-agent strings, agent cards, registration schemes) and for what operators *promise* (terms of service, robots directives, AI-usage policies), but no shared, versioned vocabulary for what agents *do* as seen from the receiving side. Approval is not behavior. Declaration is not behavior. This taxonomy names behavior.

---

## 1. Design principles

1. **Receiver-side.** Every category is defined exclusively from evidence observable by the receiving property. Nothing in this taxonomy requires cooperation, disclosure, or instrumentation on the agent's side.
2. **Descriptive, not judicial.** Categories characterize observed conduct. They are not legal conclusions, intent attributions, or statements about future behavior (see §6).
3. **Three independent dimensions.** Identity, conduct, and persistence are assessed separately. An agent may be honest about its identity and hostile in its conduct, or anonymous and respectful. Collapsing these dimensions destroys the information that matters.
4. **Session-scoped.** The unit of classification is the session — the grouped activity of one actor on one property over a bounded interval. Actor-level views aggregate sessions; they do not replace them.
5. **Versioned and non-retroactive.** Category names and definitions change only through a new dated version of this document. Classifications issued under a given version remain interpretable under that version permanently.

---

## 2. Dimension I — Declared identity

What the agent *claims* to be, and whether that claim is consistent with the infrastructure it arrives from.

| Category | Definition |
|---|---|
| **Declared & verified** | The agent presents an identity, and that identity is consistent with the originating infrastructure. |
| **Declared** | The agent presents an identity (AI system, automation tool, or named agent) that cannot be confirmed or refuted against its infrastructure. |
| **Anonymous** | The agent presents no machine identity, or presents a generic human-browser identity while exhibiting automation. |
| **Impostor** | The agent presents an identity that is contradicted by the infrastructure it arrives from. |

Identity classification is a statement about the *claim and its consistency* — not about who operates the agent. This taxonomy never attributes sessions to named operators, companies, or persons.

## 3. Dimension II — Observed conduct

What the agent *did*, characterized against the property's published access rules and ordinary use.

| Category | Definition |
|---|---|
| **Predatory** | Active extraction behavior, with evasion or activity inconsistent with the property's published access rules. |
| **Suspicious** | Automation indicators incompatible with ordinary use; without observed open hostility. |
| **Indeterminate** | Insufficient behavioral evidence to characterize conduct. |
| **Respectful** | Conduct consistent with the property's published rules and ordinary use. |

What each category means for the receiving party:

- **Predatory** — your content or infrastructure is being actively taken or accessed at scale by parties whose observed behavior defeats identification and accountability.
- **Suspicious** — automated parties are operating on your property under identities or behaviors that would not withstand scrutiny; warrants continued observation.
- **Indeterminate** — insufficient behavioral evidence to characterize conduct; carries monitoring value, not a verdict.
- **Respectful** — automation that consults and follows your published rules; the baseline every declared agent should meet.

## 4. Dimension III — Persistence

Whether the actor *returns*.

| Category | Definition |
|---|---|
| **First visit** | The actor has been observed once. |
| **Occasional** | The actor has returned within a short window, without an established pattern. |
| **Recurrent** | The actor returns with regularity over days or weeks. |
| **Persistent** | The actor maintains a sustained, long-lived presence across the observation history. |

Persistence is the dimension most existing tooling ignores. A single hostile request is noise; the same actor returning daily for a month is a relationship — and it is the persistence of conduct, not its single occurrence, that defines exposure.

---

## 5. The conduct × identity matrix

Combining observed conduct with declared identity produces the matrix below. Declared & verified shares the Declared column (see reading notes); the remaining combinations yield twelve distinct risk levels. Descriptive risk to the receiving party:

| | **Anonymous** | **Impostor** | **Declared** |
|---|---|---|---|
| **Predatory** | HIGH | HIGH | MEDIUM-HIGH |
| **Suspicious** | MEDIUM-HIGH | HIGH | MEDIUM |
| **Indeterminate** | MEDIUM-LOW | MEDIUM | LOW |
| **Respectful** | LOW | MEDIUM | NONE |

Reading notes:

- Risk levels describe *exposure of the receiving party*, not severity of any individual request.
- An impostor identity raises the risk of otherwise identical conduct: behavior under a falsified identity defeats accountability by construction.
- Declared & respectful is the reference cell — the conduct every declared agent's operator implicitly promises. Divergence from it is measurable per property and per period.
- Persistence acts as a multiplier across all cells: the same cell sustained over weeks represents different exposure than the same cell observed once.
- Declared & verified shares the Declared column in this matrix; verification strengthens accountability but does not change the conduct observed.

---

## 6. What this taxonomy is — and is not

**It is:**

- A vocabulary for describing observed automated conduct from the receiving side.
- Session-scoped, evidence-bound, and reproducible: every classification issued in a BotConduct report is materialized and cryptographically signed at generation time.
- Mappable to existing governance frameworks as descriptive references (§7).

**It is not:**

- **Not an attribution of intent or authorship.** Categories describe conduct, never purpose, motivation, or operator identity.
- **Not a forecast.** A classification states what was observed in a period; it makes no claim about future behavior.
- **Not a legal judgment.** No category constitutes a legal finding of any kind, under any law or contract. Framework references (§7) are descriptive pointers, not conclusions.
- **Not a reputation score.** Cells are observations per property and period, not global verdicts about an agent.

---

## 7. Framework references

The taxonomy's categories can be read alongside existing governance frameworks. These references *characterize and cite* — they do not assert contravention.

| Conduct | Descriptive references |
|---|---|
| **Predatory** | OWASP Agentic AI — control evasion, offensive capability; MITRE ATLAS — defense evasion; MITRE ATT&CK T1595 — active reconnaissance; EU AI Act Art. 50 — duty to disclose AI interaction. |
| **Suspicious** | OWASP Agentic AI — unauthorized resource use, agent identity; EU AI Act Art. 50 — transparency; EU AI Act Art. 53(1)(c) — TDM rights reservation (Dir. 2019/790 Art. 4); NIST AI RMF GOVERN 6.1 — data provenance; MAP 5.1 — third-party impacts. |
| **Indeterminate** | NIST AI RMF MEASURE — continuous monitoring. |
| **Respectful** | Positive reference across frameworks — compliant by behavior, independent of declaration. |

---

## 8. Versioning policy

- This document is versioned. The current version is **v1.0 (June 2026)**.
- Definitions change **only** through a new, dated version published at the canonical URL. Changes are never retroactive: a classification issued under v1.0 remains a v1.0 classification.
- Each version carries a changelog. Reports issued by the BotConduct Observatory cite the taxonomy version in force at generation time.

**Changelog**

| Version | Date | Changes |
|---|---|---|
| 1.0 | June 2026 | Initial public release. |

---

## 9. License and citation

This taxonomy is free to use, reference, and redistribute with attribution.

**Suggested citation:**

> BotConduct Observatory. *BotConduct Conduct Taxonomy*, v1.0, June 2026. https://botconduct.org/conduct-taxonomy

---

*Closed oracle. Classification is produced by the Observatory's behavioral engine. Its outputs are cryptographically verifiable and reproducible. The method itself — signals, thresholds, precedence — is never disclosed. Independent third-party audit of consistency and integrity is available under NDA, without disclosure of the method.*
