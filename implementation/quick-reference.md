# Human-AI Agency Framework

**Quick Reference for Tool Builders and Practitioners**

---

## The Agency Spectrum

| Level | Name | Human Agency | Human Role | Machine Role | Authorship Status |
|-------|------|-------------|------------|--------------|-------------------|
| **L5** | Pure Tool | ~100% | Full control | Passive instrument | Unambiguous |
| **L4** | Director | ~90-99% | All decisions | Assists on command | Clean human |
| | **--- 90% THRESHOLD (Safe Harbor) ---** | | | | |
| **L3** | Supervisor | ~70-89% | Reviews/modifies | Suggests options | Diluted/defensible |
| **L2** | Collaborator | ~40-69% | Selects/edits | Produces drafts | Diluted/disclosure required |
| **L1** | Executor | ~15-39% | Curates output | Generates content | High risk |
| **L0** | Oracle | ~0-14% | Receives output | Generates everything | No human claim |

**Above the 90% threshold** (L4-L5): Copyright is clear, guild-compliant, professional markets open.
**Below the threshold** (L0-L3): Authorship is contested, risk escalates with each level down.

---

## The Key Distinction: Suggest vs. Publish

**How does AI contribution enter your work?**

| Suggest Mode (Opt-In) | Publish Mode (Opt-Out) |
|-----------------------|------------------------|
| AI proposes; user acts to **accept** | AI auto-inserts; user acts to **reject** |
| Default = rejection | Default = acceptance |
| Preserves editorial control | Transfers authorship risk |
| User remains author | Burden shifts to user |

*If your users have to undo rather than approve, the burden has shifted.*

Research shows 20+ percentage point differences in acceptance rates between modes.

---

## 5 Design Principles for Tool Builders

### 1. Make Agency Distribution Legible
- Visualize AI vs. human contributions (color coding, highlighting, attribution markers)
- Expose default settings transparently so users know which mode is active on startup
- Include attribution data in exports, not just the UI

### 2. Preserve Editorial Control Through Defaults
- **Default to Suggest Mode** (opt-in) for all generative features
- Publish Mode is acceptable only for explicit large-scale requests (e.g., "generate entire section") with simple undo
- Opt-out systems erode agency even when users retain veto power

### 3. Enable Graduated Assistance
- **Expert Mode** (L4-L5): Minimal AI, on-demand only. Default for academic/legal/high-stakes domains
- **Intermediate Mode** (L3): Contextual co-pilot. Suggestions appear based on context
- **Novice Mode** (L1-L2): High AI initiative. Appropriate for learning contexts with clear disclosure

### 4. Build Recovery Mechanisms
- **Granular undo**: Undo a specific AI contribution without undoing human work
- **Version history**: Track human vs. AI contributions separately
- **Pre-AI revert**: Allow users to restore a document to its pre-AI state

### 5. Minimize Lock-In
- Export in standard, non-proprietary formats (Markdown, JSON, .docx, .fdx, plain text)
- Provide clear data ownership terms
- Offer contractual training opt-out guarantees
- Ensure meaningful alternatives exist

---

## 5 Tactical Questions (Evaluate Control Within a Tool)

1. Can the user interrupt generation mid-process?
2. Does the system suggest or auto-insert?
3. Can the user see which contributions are theirs vs. AI?
4. Can the user undo, reject, or rollback AI changes granularly?
5. What level does the actual workflow operate at (not what the tool advertises)?

## 5 Strategic Questions (Evaluate Before Adopting a Tool)

1. What formats can users export their work in?
2. Who owns user data and outputs? (Read the ToS.)
3. Do real alternatives exist if policies change?
4. Could users complete this work if the tool vanished?
5. Will using this tool build user skills or erode them?

---

## Authorship Risk Model

| Capability Dependency | Contribution Opacity | Accountability Attribution |
|-----------------------|----------------------|----------------------------|
| Could the user produce this without the AI? | Can the user identify what they contributed vs. AI? | Will the user be held responsible for this output? |

**Highest risk:** High dependency + High opacity + Full attribution = Responsible for something you can't produce and can't verify.

---

## Anti-Patterns to Avoid

| Anti-Pattern | Description |
|--------------|-------------|
| **Hidden Defaults** | Users unaware of AI's default mode (e.g., publish mode active on startup) |
| **Asymmetric Friction** | Accepting AI suggestions made easier than rejecting them |
| **Attribution Soup** | AI and human contributions blended and indistinguishable |
| **Forced Dependency** | Basic features require AI use, eliminating user choice |
| **Export Sabotage** | No export, proprietary format only, or degraded export |

---

## Red Flags in Deployed Tools

- Auto-insert as default (Publish mode)
- No export or proprietary format only
- Cannot distinguish AI from human work
- \>90% AI suggestion acceptance rate across users
- ToS claims platform owns outputs
- User skills declining over time with tool use

---

## Key Rules

- **The 90% Threshold:** Above 90% human agency (L4-L5), copyright is clear. Below (L3 and under), it's contested.
- **Ideas vs. Expression:** AI can provide ideas (structure, outlines). Humans must write expression.
- **The Reversibility Test:** If your users can't do it without the tool, they're dependent — not augmented.
- **Classification is behavioral:** The level is determined by what users actually do, not what the tool can do.
- **Composite Agency:** An L5 wrapper cannot "launder" an L1 generation layer. Effective agency = min(Surface Layer, Generation Layer).

---

## Agency Health Metrics

Track these over time to evaluate whether your tool preserves or erodes agency:

- **Suggestion acceptance rate** — >90% is a red flag
- **Skill trajectory** — Are users developing or atrophying skills?
- **Mode distribution** — What percentage of users stay in default mode?
- **Export frequency** — Are users able and willing to move their work?
- **Recovery usage** — How often do users undo or revert AI contributions?

---

## Domain-Specific Defaults

| Domain | Recommended Default | Rationale |
|--------|-------------------|-----------|
| Academic writing | Expert mode (L4-L5) | Intellectual honesty critical |
| Creative writing | Intermediate mode (L3-L4) | Authorship at stake |
| Data analysis | Publish mode acceptable | Accuracy > authorship; pair with attribution |
| Professional communication | Suggest mode (L3-L4) | Human makes content decisions; AI handles formatting |
| Legal/medical | Expert mode (L5) | Accountability cannot be delegated |

---

Human-AI Agency Framework | Mark Ghuneim / NARRATIVE.NEW | January 2026 | CC BY 4.0
