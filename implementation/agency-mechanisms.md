# Agency Mechanisms: Engineering Spec for Tool Builders

**Tactical control, strategic freedom, legal anchors, and implementation checklists**

---

## The Core Principle

Agency preservation operates on two levels: what users can do *within* a tool (tactical) and whether users can *leave* a tool (strategic). Both must be present. High tactical control in a locked platform is illusory freedom.

---

## Tactical Agency: Control Within the Tool

**Core Question:** How does the user impose their intent on the AI during use?

| Mechanism | Legal Anchor | What It Enables |
|---|---|---|
| **Interruption** | "Meaningful human oversight" (EU AI Act) | Stop generation mid-stream. Prevent runaway output. |
| **Direction** | "Human-led creative process" (WGA) | Steer what the AI produces. Set constraints before generation. |
| **Editing** | "Significant human control" (USCO) | Modify AI output before finalization. Transform machine suggestion into human expression. |
| **Configuration** | "Adjustable automation levels" (ISO/IEC) | Control AI involvement level. Scale from L5 to L2 as needed. |

**The USCO Test:** The U.S. Copyright Office requires demonstrable human control over the "specific expression." Editing is the mechanism that transforms AI-generated text into copyrightable human expression. Without editing capability, users are selecting, not authoring.

**The WGA Standard:** Guild contracts require the creative process to be "human-led." Direction and interruption establish that the human initiates and can halt the process — not merely react to machine output.

---

## The Suggest/Publish Implementation

The single design choice that most determines authorship preservation.

| Mode | Default | User Action | Agency Impact |
|---|---|---|---|
| **Suggest** (Opt-In) | Rejection | Must click to accept | Preserves editorial control |
| **Publish** (Opt-Out) | Acceptance | Must delete to reject | Transfers authorship risk |

### DO: Suggest Mode (Opt-In)

```
User writes: "The project timeline is"
AI shows overlay: "tight" | "aggressive" | "challenging"
User clicks to accept → Content inserted
```

### DON'T: Publish Mode (Opt-Out)

```
User writes: "The project timeline is"
AI auto-inserts: "tight and requires immediate attention"
User must actively delete if unwanted
```

### Suggestion Patterns by Friction Level

| Friction | Pattern | Accept | Dismiss |
|---|---|---|---|
| **Low** | Gray inline overlay | Tab to accept | Esc to dismiss |
| **Medium** | Sidebar panel | Click to insert | Ignore or close |
| **High** | On-demand via shortcut | Explicit selection | Never automatic |

**Legal implication:** Publish mode makes "significant human control" harder to demonstrate. If the default is acceptance, the human's role shifts from *author* to *curator*, and curation alone does not satisfy USCO requirements.

---

## Strategic Agency: The Ability to Leave

**Core Question:** Can the user exit this platform with their work and capabilities intact?

| Mechanism | Legal Anchor | What It Enables |
|---|---|---|
| **Export** | Data portability (GDPR Art. 20) | Take work in standard formats |
| **Ownership Clarity** | Copyright assignment (ToS) | Know who owns what is created |
| **Data Control** | Training opt-out (contractual) | Prevent work from training future models |
| **Alternatives** | Competition law principles | Meaningful choice between different architectures |

**The Lock-In Problem:** Three foundation models dominate the market with similar ToS. "Choice" between identical constraints isn't strategic agency — it's the illusion of choice.

**The Training Trap:** Free-tier platforms extract user work into training data. The user's style becomes part of the model. The model competes with the user using their own patterns. Paid relationships with training opt-out partially mitigate this, but only partially.

---

## The Two-Level Test

| Level | Question | Failure Mode |
|---|---|---|
| **Tactical** | Can I control this tool? | High control, but locked in = illusory agency |
| **Strategic** | Can I leave this tool? | Can leave, but alternatives identical = false choice |

**Both required.** A tool that gives control but won't let you leave is a trap. A market with exit but no differentiation is a cartel.

---

## Compliance Alignment

Maps each legal/professional standard to the mechanisms your tool must implement:

| Standard | Tactical Mechanism Required | Strategic Mechanism Required |
|---|---|---|
| USCO "significant human control" | Editing + Direction | Ownership clarity |
| WGA "human-led creative process" | Direction + Interruption | Platform alternatives |
| EU AI Act "meaningful oversight" | Interruption + Configuration | Data portability |
| SAG-AFTRA consent requirements | N/A | Contract negotiation leverage |
| GDPR data subject rights | N/A | Export + Data control |

---

## Stakeholder Implementation Matrix

### For Creators: Tool Audit Checklist

| Mechanism | What to Audit | Red Flag | Green Flag |
|---|---|---|---|
| Interruption | Can I stop generation mid-stream? | No pause/cancel option | One-click halt |
| Direction | Can I constrain before generation? | Prompt-only interface | Style/tone/scope controls |
| Editing | Can I modify AI output? | Accept/reject binary | Full text editing with AI attribution |
| Configuration | Can I adjust AI involvement? | Fixed automation level | Slider from L5 to L2 |
| Export | Can I take my work? | Proprietary format only | Markdown, .docx, .fdx standard |
| Ownership | Who owns what I create? | "Platform retains rights" | "User owns all output" |
| Training | Does my work train the model? | Silent training, no opt-out | Explicit opt-out, contractual guarantee |

### For Studios: Compliance Requirements

| Compliance Dimension | Tactical Requirement | Strategic Requirement |
|---|---|---|
| USCO Registration | Must demonstrate editing, not just selection | Must own clear chain of title |
| Guild Compliance | Human-led process (direction + interruption) | Cannot be locked to non-compliant platform |
| E&O Insurance | Auditable AI contribution trail | Alternative tools available if platform fails |
| Chain of Title | L4-L5 for clean copyright | Training opt-out for paid tiers |

### For Unions: Protection Safeguards

| Protection Goal | Tactical Safeguard | Strategic Safeguard |
|---|---|---|
| Member Work Definition | Suggest mode default (opt-in) | Guild can certify compliant tools |
| Credit Integrity | Direction + editing documented | Members not locked to single platform |
| Compensation Basis | Layer determines rate structure | Alternatives exist for each layer |
| Skill Preservation | Interruption prevents over-reliance | Training programs for tool-agnostic skills |

---

## Design Countermeasures for Behavioral Constraints

| Constraint | Countermeasure | Implementation |
|---|---|---|
| **Anchoring Bias** | Generate before seeing AI | Require user draft before suggestions appear |
| **Selection Bias** | Transparency about filtering | Show what was *not* suggested and why |
| **Cognitive Friction** | Effortless rejection | One-click dismiss, no confirmation required |
| **Overton Window** | Vary suggestions | Randomize across users, show diverse options |
| **Homogenization** | Diversity metrics | Track and report convergence at platform level |

---

## Stakeholder Risk Tables

### Creators

| Risk | Indicator | Mitigation |
|---|---|---|
| Unconscious convergence | Work sounds like everyone else's | Deliberate AI-free practice sessions |
| Skill atrophy | Can't generate without suggestions | Regular "blank page" exercises |
| Style erosion | Voice becomes the model's voice | Track pre-AI work as baseline |

### Studios

| Risk | Indicator | Mitigation |
|---|---|---|
| Portfolio homogenization | Projects blur together | Mandate diverse tool/model usage across productions |
| Audience fatigue | "Everything feels the same" | Audit for AI-pattern convergence |
| Competitive erosion | No differentiation from competitors using same models | Invest in proprietary processes |

### Unions

| Risk | Indicator | Mitigation |
|---|---|---|
| Masked skill loss | Members "can't work without it" | Require baseline human-only competency tests |
| Invisible displacement | Same headcount, less human creativity | Track actual human contribution per project |
| Negotiating weakness | "Anyone can do it with AI" | Emphasize the constraints AI introduces |

---

## The Reversibility Test

A diagnostic for evaluating dependency:

**Could your users complete this task if the AI vanished tomorrow?**

| Answer | Diagnosis | Action |
|---|---|---|
| Yes, same quality | Tool assistance — skills intact | Healthy usage |
| Yes, lower quality | Partial dependency — skills atrophying | Implement AI-free modes, track trajectory |
| No | Full dependency — skills absent or lost | Critical intervention needed |

Track this over time. If the answer shifts from "yes" to "no," the behavioral constraints have done their work.

---

## Implementation Checklist

### Phase 1: Foundation

- [ ] Suggest mode implemented as default
- [ ] AI contribution attribution visible in UI
- [ ] Basic undo working for AI contributions
- [ ] Data export available in at least one standard format

### Phase 2: Refinement

- [ ] Graduated assistance levels (Expert/Intermediate/Novice)
- [ ] Version control with human vs. AI source tracking
- [ ] Settings dashboard with mode indicator
- [ ] Keyboard shortcuts for accept and reject (equal friction)

### Phase 3: Sophistication

- [ ] Adaptive assistance based on observed user behavior
- [ ] Analytics dashboard on agency distribution
- [ ] Domain-specific presets (Academic, Creative, Professional)
- [ ] API for third-party integrations and export

---

## Measurement KPIs

| Category | Metrics | Red Flag |
|---|---|---|
| **Adoption** | % users customizing settings, distribution across assistance levels | <5% customization |
| **Engagement** | Acceptance rate, rejection rate, edit-after-accept rate | >90% acceptance |
| **Agency Health** | Human vs. AI attribution %, user-reported sense of control | Skill decline over time |
| **Operations** | Undo success rate, export completion rate | High support tickets about control |

---

Human-AI Agency Framework | Mark Ghuneim / NARRATIVE.NEW | January 2026 | CC BY 4.0
