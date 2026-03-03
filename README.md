# On the Calculation of The Human-AI Agency Spectrum

**A framework for measuring authorship distribution in AI-participated creative work.**

By Mark Ghuneim | [Narrative.new](https://narrative.new) | Version 1.0 | January 2026 | License: CC BY 4.0

---

## What This Is

A six-layer model (L0-L5) that maps qualitative standards like "human-led" and "significant human control" to operational configurations. It synthesizes:

- **Legal requirements** — USCO, EU AI Act Article 50
- **Professional standards** — WGA, SAG-AFTRA, DGA
- **Cognitive research** — on human-AI interaction and creative intent
- **Market analysis** — compliance constraints that create market tiers

The result is a shared vocabulary for discussing agency that connects to the rules already governing professional work.

## Why It Matters

The existing language ("AI-generated," "AI-assisted," "human-written") fails to capture the spectrum of configurations actually in use. Guild contracts reference "human-led" processes without defining the threshold. Copyright law requires "significant human control" without specifying what qualifies. Everyone operates from intuition where precision is needed.

This framework provides the precision.

## The Document

- **[executive-summary.md](executive-summary.md)** — Start here (5-minute read)
- **[On_the_Calculation_of_The_Human-AI_Agency_Spectrum.md](On_the_Calculation_of_The_Human-AI_Agency_Spectrum.md)** — The full paper

## Structure

| Part | Contents |
|---|---|
| **Part I: The Framework** | The six layers (L0-L5), the 90% threshold, work-level vs. interaction-level agency |
| **Part II: Market Structure** | Compliance landscape, four dimensions, three-tier market |
| **Part III: Mechanisms & Constraints** | Tactical/strategic agency, behavioral constraints, design countermeasures |
| **Appendices** | Iterative workflow case studies, design principles & patterns for tool builders |

## Key Concepts

- **The Six Layers** — From L0 (Oracle, ~0-14% human) to L5 (Pure Tool, ~100% human)
- **The 90% Threshold** — The L4/L3 boundary where legal, professional, cognitive, and economic standards converge
- **Work Agency vs. Interaction Agency** — Measuring the full creative process, not just the generation moment
- **The Three-Tier Market** — Premium (L4-L5), Standard (L3), Budget (L2) — shaped by compliance constraints

## Implementation

Building tools with human agency in mind? The `implementation/` directory provides practical resources for developers and product teams:

- **[quick-reference.md](implementation/quick-reference.md)** — The agency spectrum, design principles, anti-patterns, and red flags at a glance
- **[best-practices.md](implementation/best-practices.md)** — State management patterns, phased roadmap, composite agency calculation, and behavioral constraints to design against

These guides translate the framework into actionable decisions: default to Suggest Mode, track contributions by source, enable granular undo, and minimize lock-in.

## Contributing

See **[contributing.md](contributing.md)** for how to participate in the RFC process.

**Quick guide:**
- **Typos and formatting** — Submit a PR
- **Factual corrections** (e.g., contract language, regulatory text) — Submit a PR with sources
- **Conceptual discussion** (e.g., threshold placement, layer definitions) — Open an Issue

## Citation

```
Ghuneim, M. (2026). On the Calculation of The Human-AI Agency Spectrum. Narrative.new.
```
