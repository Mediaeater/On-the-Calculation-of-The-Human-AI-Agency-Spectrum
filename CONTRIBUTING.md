# Contributing

Thank you for your interest in providing feedback or contributions to this framework. To maintain a structured review process, please follow these guidelines.

## 1. The RFC Process

This document follows a formal Request for Comments (RFC) lifecycle:

| Stage | Description |
|---|---|
| **Draft** | Initial proposal under active internal development. |
| **Review** | Open for public comment and peer review. Structural changes accepted. |
| **Final** | Stable version. Only errata, factual corrections, and regulatory updates accepted. |

**Current Status: Review**

## 2. How to Provide Feedback

### High-Level Discussion (Issues)

Use **GitHub Issues** for conceptual feedback, architectural concerns, or questions that require discussion before drafting changes.

- Search existing issues to avoid duplicates
- Use a descriptive title (e.g., "Clarification needed on Section: The 90% Threshold")
- State your position clearly with evidence or reasoning
- Reference specific sections of the document by heading

Examples of good issues:
- Threshold placement (e.g., "Should the L4/L3 boundary be at 85% rather than 90%?")
- Layer definitions and boundaries
- Missing stakeholder perspectives
- New compliance dimensions or regulatory developments
- Framework application questions ("How would this apply to X?")
- Challenges to the framework's assumptions

### Specific Edits (Pull Requests)

Use **Pull Requests (PRs)** for direct improvements to the text:

- **Typos and formatting fixes** — Submit directly.
- **Factual corrections** — Contract language, regulatory text, case law updates. Include the source (link to official document, statute, or ruling).
- **Table/data corrections** — If a compliance mapping is wrong, show what it should be and why.
- **Adding references** — New research, rulings, or standards that strengthen or challenge existing analysis.

**PR requirements:**
1. Target the `main` branch
2. Provide a brief summary of why the change is necessary
3. Reference specific sections by heading
4. Cite authoritative sources for any factual claims
5. One logical change per PR
6. Ensure your changes do not break Markdown formatting

### What We're Looking For

| Priority | Area | Example |
|---|---|---|
| High | Regulatory updates | New USCO guidance, EU AI Act implementation details, guild contract amendments |
| High | Factual corrections | Misrepresented contract language, incorrect legal interpretations |
| Medium | New case studies | Real-world applications of work-level agency assessment |
| Medium | International coverage | Jurisdictions beyond US/EU (UK, Japan, South Korea, etc.) |
| Low | Additional design patterns | Tool builder implementations of the framework's principles |

### What We Won't Merge

- Changes that remove the spectrum model in favor of binary classification
- Advocacy for specific tools or platforms
- Content that isn't relevant to authorship, agency, or the creative industries
- Unsourced claims about legal or regulatory standards

## 3. Style Guidelines

- **Tone:** Professional, technical, and objective. The framework describes configurations, not prescriptions.
- **Formatting:** Standard Markdown. Use `##` / `###` headers, pipe tables, and `---` horizontal rules consistent with the existing document.
- **Citations:** Use inline references with full source name, year, and specific provision where applicable (e.g., "WGA 2023 MBA, Article 72.C"). List full references at the end of each major section.
- **Terminology:** Use the framework's defined terms consistently — "agency level" not "autonomy score," "layer" not "tier" (tiers refer to markets), "interaction agency" vs. "work agency" where the distinction matters.

## 4. Process

1. **Check existing Issues** before opening a new one — your topic may already be under discussion
2. **For PRs:** Fork, make your change, submit with a clear description targeting `main`
3. **For conceptual changes:** Open an Issue first, discuss, then PR if consensus emerges
4. **Review:** Maintainers will review within the context of the framework's goals and accuracy standards

## 5. Scope

This framework specifically covers:
- Text-based generative processes
- Pre-rendering/pre-visualization phase
- Authorship and agency in professional creative contexts

Multimodal concerns (voice, likeness, visual generation) are addressed only where they intersect with writing. Full treatment of these areas is reserved for future work.

## 6. Licensing

This project is licensed under **CC BY 4.0**. By contributing to this repository, you agree that your contributions will be licensed under the same terms.
