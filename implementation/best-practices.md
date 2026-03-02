# Best Practices for Agency-Preserving Tools

**Implementation Guide for Developers and Product Teams**

---

## State Management

Track contributions in your application state with source attribution:

```
contributions: [
  { id: 1, content: "...", source: "human", timestamp: "..." },
  { id: 2, content: "...", source: "ai", timestamp: "...", accepted_by: "human" },
  ...
]
```

Tag every content modification with its source. This enables granular undo, attribution views, and agency metrics.

---

## Implementation Patterns

### Confirmation Escalation

Require increasing user confirmation for higher-risk actions:

| Action | Confirmation Level |
|--------|--------------------|
| Accept single suggestion | One click |
| Accept multiple suggestions | Summary review |
| Accept all suggestions | Explicit confirmation dialog |
| Auto-generate entire section | Warning + confirmation + easy revert |

### Graduated Disclosure

Present agency information in layers:

1. **Always visible:** Simple indicator of current mode (Suggest/Publish) and AI activity level
2. **On hover/click:** Contribution breakdown (% human vs. AI)
3. **In settings:** Full agency configuration, export options, data policies
4. **In documentation:** Complete methodology, calculation details

### Contextual Mode Switching

Suggest (don't force) changes in agency mode based on task context:

- Brainstorming phase: Higher AI involvement acceptable
- Drafting phase: Intermediate mode
- Revision/finalization: Suggest mode, minimal AI
- Publication-ready: Human review required, AI contributions flagged

---

## Product Roadmap (Phased)

### Phase 1: Foundation
- Implement Suggest Mode as default for all generative features
- Build contribution tracking (human vs. AI tagging)
- Add basic undo for AI contributions
- Export in at least one standard format

### Phase 2: Transparency
- Visual indicators for AI vs. human contributions
- Agency level display in UI
- Graduated assistance levels (Expert/Intermediate/Novice)
- Version history with source attribution

### Phase 3: Maturity
- Agency health dashboard (acceptance rates, skill metrics)
- Contextual mode recommendations
- Full export in multiple standard formats
- User-facing agency audit tools

---

## Composite Agency in Layered Architectures

When building on top of AI APIs or chaining tools:

```
Effective Agency = min(Surface Layer, Generation Layer) + Data Policy Modifier
```

- An L5 UI wrapper around an L1 generation engine = **L1 effective agency**
- A paid API with training opt-out eliminates temporal agency erosion but does not change the base tactical level
- Transactional agency (paid API with contractual opt-out) partially mitigates low tactical agency

**Disclose the full stack.** Users deserve to know what's generating their content, not just what's presenting it.

---

## Strategic Questions for Product Managers

Before implementing an AI feature, ask:

1. **What values are at stake in this domain?** (authorship, accuracy, creativity, accountability)
2. **What agency level does this feature operate at?**
3. **Is the default mode Suggest or Publish? Why?**
4. **What happens if a user can't distinguish their work from the AI's?**
5. **What is the exit path?** (export, alternatives, skill preservation)

---

## Business Model Alignment

| Model | Agency Risk | Why |
|-------|-------------|-----|
| **Subscription** | Lowest | Incentive is long-term user satisfaction |
| **Per-use/credit** | Moderate | Incentive to increase usage, but user controls spend |
| **Ad-supported** | High | More engagement = more ads; agency secondary |
| **Data model** | Highest | More AI use = more training data; incentive for dependency |

Choose business models that align commercial incentives with user agency.

---

## Troubleshooting Common Issues

| Symptom | Likely Cause | Solution |
|---------|-------------|----------|
| >90% suggestion acceptance rate | Asymmetric friction or publish mode default | Audit friction balance; switch to suggest mode |
| Users ignoring AI features | Poor suggestion quality or excessive intrusiveness | Improve relevance; reduce interruption frequency |
| Users can't tell AI from human work | No visual attribution | Implement color coding, filter views, export metadata |
| Cognitive overload from settings | Too many options exposed at once | Better defaults, progressive disclosure, task-based presets |
| User skills declining | Over-reliance on AI suggestions | Implement "AI-free" modes; track skill trajectory |
| Attribution confusion in exports | No metadata carried through | Include source tags in all export formats |

---

## The Cockpit Analogy

Think of your AI tool like an aircraft cockpit:

- **Legibility** = Clear instruments showing what the autopilot is doing
- **Control** = Easy-to-reach override button, always accessible
- **Recovery** = Granular undo, not just "disengage everything"
- **Strategic agency** = The pilot's certainty they can land the plane themselves

If your user can't "land the plane" without your tool, you've built dependency, not augmentation.

---

## Five Behavioral Constraints to Design Against

1. **Anchoring Bias** — First AI suggestion becomes the gravitational center. Mitigation: show multiple alternatives, allow blank-slate starts.
2. **Selection Bias** — AI output is pre-filtered through training data, platform incentives, and interface design. Mitigation: disclose training methodology and filtering.
3. **Cognitive Friction** — Rejection costs effort; acceptance costs nothing. Mitigation: make accept and reject equally easy.
4. **Overton Window** — Suggestions define "reasonable options"; others become invisible. Mitigation: preserve user ability to generate from scratch.
5. **Homogenization at Scale** — Individual choices aggregate into cultural convergence. Mitigation: vary suggestions, track diversity metrics.

---

Human-AI Agency Framework | Mark Ghuneim / NARRATIVE.NEW | January 2026 | CC BY 4.0
