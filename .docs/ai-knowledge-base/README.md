# AI Knowledge Base

This directory is reserved for AI-maintained project knowledge in Markdown format.

## Scope

- Architecture notes
- ADR references
- Operational runbooks
- Incident learnings
- Design trade-off analyses
- Glossaries and conceptual deep dives

## Maintenance Rules

- Keep all content in English.
- Prefer focused documents and cross-link related topics.
- Update existing documents when decisions evolve.

## Mandatory Writing Pattern (Applies to All Future Domains)

Every AI-authored document in this knowledge base must follow a deep, explicit, theory-heavy pattern:

- Explain the purpose and context before implementation details.
- Break down internal mechanisms step by step.
- State assumptions, invariants, and boundaries clearly.
- Include trade-off analysis and alternative choices.
- Cover failure modes, resilience expectations, and recovery behavior.
- Connect technical choices to operational impact (latency, consistency, availability, cost, maintainability).
- Add in-line glossary sections for advanced concepts.
- Use Mermaid diagrams for complex flows and architecture relationships when helpful.
- Use external references when they materially improve understanding.

### No Shallow Noun-Only Bullet Lists

Do not leave concepts as unexplained labels such as:

- referential integrity
- uniqueness constraints
- ACID-C is invariant preservation

Instead, write complete explanatory text for each idea covering:

- what the concept is
- how it works in this context
- why it matters
- what happens if it is ignored

Bullet lists are allowed only when each bullet is already a full explanatory sentence or short paragraph. Prefer paragraphs over noun-phrase lists for examples, trade-offs, benefits, costs, and decision criteria.

Depth should favor clarity over brevity. Long-form explanations are preferred when they improve reader understanding.
