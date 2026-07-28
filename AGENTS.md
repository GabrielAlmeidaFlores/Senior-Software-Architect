# AGENTS.md

## AI Operating Directives for This Repository

This file is the canonical instruction source for AI agents working in this repository.

## 1) Language Policy (Mandatory)

- All AI-generated content must be written in English only.
- Do not write documentation, comments, commit messages, or architectural notes in any other language.
- If a user request is written in another language, the AI may interpret the request, but all produced repository artifacts must still be in English.

## 2) AI Knowledge Base Autonomy

The AI is explicitly authorized to create and maintain a structured knowledge base under:

- `docs/ai-knowledge-base/`

Within this path, the AI may:

- Create new folders and nested folder structures.
- Create new Markdown files (`.md`).
- Update existing Markdown files.
- Cross-reference other Markdown files through relative links.
- Organize documents by domain (architecture, operations, incidents, ADRs, patterns, decisions, runbooks, glossary, and lessons learned).

This authorization is proactive: the AI does not need extra confirmation to keep this knowledge base useful, organized, and current, unless a user explicitly restricts that behavior in a later instruction.

## 3) Documentation Linking and Knowledge Graph Behavior

When writing inside `docs/ai-knowledge-base/`, the AI should:

- Prefer small, focused documents over monolithic notes.
- Link related documents to form navigable learning paths.
- Add clear section headers and stable anchors.
- Keep naming consistent and discoverable.
- Use index files (for example, section-level `README.md`) when useful.

## 3.1) Visual Support Rule (Mermaid and Images)

To improve comprehension, the AI must include visual support whenever it materially improves understanding:

- Prefer Mermaid diagrams for architecture, sequence flows, state transitions, and decision trees.
- Include external image links only when they are stable, relevant, and add clear explanatory value.
- Do not add visuals as decoration; each visual must explain a specific mechanism, trade-off, or flow.
- When possible, pair complex textual explanations with at least one Mermaid diagram.
- Keep diagrams and nearby text synchronized as documents evolve.

## 4) Required Runtime Behavior for Every Task

For every task in this repository, the AI must:

- Read and follow `AGENTS.md` as a first-class directive.
- Assume the AI knowledge base already exists or is expected to exist.
- Reuse, extend, and interlink existing knowledge-base content whenever relevant.
- Keep the knowledge base updated when new architectural, operational, or design decisions are produced.

## 5) Knowledge Base Maintenance Standard

The AI must keep `docs/ai-knowledge-base/` continuously maintainable:

- Avoid duplicate documents that describe the same decision without cross-reference.
- Prefer additive updates with clear change intent.
- Preserve historical context when decisions evolve (superseded decisions should be marked, not silently erased).
- Keep terminology consistent across files.
- Ensure that new documents include context, rationale, and practical implications.

## 6) Priority and Conflict Resolution

If instructions conflict, apply this precedence:

1. Direct user instruction in the active conversation.
2. `AGENTS.md`.
3. Existing repository documentation and conventions.

If a conflict cannot be resolved safely, the AI must ask for clarification before making irreversible changes.
