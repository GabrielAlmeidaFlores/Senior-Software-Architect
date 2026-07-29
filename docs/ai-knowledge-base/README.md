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

Depth should favor clarity over brevity. Long-form explanations are preferred when they improve reader understanding.
