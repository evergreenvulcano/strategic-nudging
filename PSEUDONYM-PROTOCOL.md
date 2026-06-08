# Pseudonym Protocol

This document defines the rules for anonymizing cases within this repository.

---

## Principle

No real names enter the repository. No company names, product names, personal names, domain names, or other identifying markers may appear in any committed file.

Every subject of a case is translated into a codename before the work begins. The work then proceeds entirely within that translated layer.

This is not censorship. It is **semantic translation** — the kind that forces conceptual clarity by removing the distraction of specifics.

---

## Codename Tiers

Each case uses four tiers of codenames:

| Tier | What It Covers | Example Format |
|------|---------------|----------------|
| **EMPIRE** | The overall subject entity (company, studio, project cluster) | `THE EMPIRE` |
| **SECTOR** | Individual products or verticals within the empire | `SECTOR PRIME`, `SECTOR TWO` |
| **ROLE** | Key human actors | `THE ARCHITECT`, `THE TRANSLATOR` |
| **DOMAIN** | External categories (markets, technologies) | Keep generic: "ad market", "cloud ops" |

---

## Naming Rules

1. **Codenames are permanent** within a case version. Do not rename mid-document.
2. **Codenames are evocative, not descriptive.** They should not accidentally encode the real identity.
3. **SECTOR PRIME** always designates the flagship product — the one with the most developed surface, most vertical breadth, or most strategic weight.
4. **THE ARCHITECT** always designates the primary builder/founder.
5. **THE TRANSLATOR** always designates the consultant/advisor producing the framework material.

---

## Local Mapping File

The real-to-pseudonym mapping must be stored in a local, gitignored file:

```
registry/mapping.local.md
```

This file is listed in `registry/.gitignore` and must never be committed. It is the operator's responsibility to maintain this file locally.

Format:
```
THE EMPIRE        → [real entity name]
SECTOR PRIME      → [real product name]
THE ARCHITECT     → [real person name]
THE TRANSLATOR    → [real person name]
```

---

## When to Create a New Empire

Each distinct subject entity gets its own empire-level codename and its own subfolder under the repository root. Multiple cases can coexist without cross-contamination.

A new empire is created when:
- A genuinely new subject entity enters the workflow.
- A prior subject entity has changed enough that continuity of codename would be misleading.

---

## Language Note

Codenames are tools, not labels. They are chosen to fit the **conceptual language of the framework** — specifically the empire/control-room metaphor. This alignment keeps the work internally consistent and prevents code-name drift into neutral or bureaucratic language.

The codename should feel like something the receiver could wear. Not a ticket number. Not an anonymized ID. A **position**.
