---
name: company-brain
description: Build and maintain an Obsidian/Markdown company brain from multiple connected repositories, using GBrain as the MVP search and graph layer and escalating to Graphify later for enriched entity/relation mapping. Use when asked to turn repo docs, code, decisions, runbooks, or project context into a queryable company knowledge base.
---

# Company Brain

Create a public-safe Markdown company brain from 2–6 related repos or folders. Keep the first version boring and useful: Obsidian-compatible files, stable indexes, source links, and GBrain import/query readiness.

## Default Approach

1. Collect repo sources.
2. Build a vault skeleton.
3. Extract durable knowledge from each source.
4. Link related systems, decisions, owners, runbooks, and risks.
5. Import/index with GBrain for search + graph queries.
6. Maintain with a lightweight recurring update loop.
7. Escalate to Graphify only after the Markdown/GBrain layer proves useful.

## Source Collection

Ask for or discover four source inputs when possible:
- repo URL or local path
- one-line purpose
- default branch or snapshot date
- what knowledge matters most: architecture, product, ops, sales, support, research, or all

If sources contain secrets or private customer data, do not copy raw values. Summarize patterns and redact sensitive details.

## Vault Shape

Use this structure unless the project already has a stronger convention:

```text
company-brain/
├── README.md
├── 00-inbox/
├── 10-sources/
│   └── <source-name>/
├── 20-systems/
├── 30-decisions/
├── 40-runbooks/
├── 50-entities/
│   ├── people/
│   ├── products/
│   ├── services/
│   └── integrations/
└── 90-indexes/
```

## Extraction Rules

For each repo or folder, create:
- `10-sources/<source-name>/overview.md` — purpose, scope, key directories, entry points
- `10-sources/<source-name>/architecture.md` — components, data flow, dependencies
- `10-sources/<source-name>/operations.md` — setup, deploy, monitoring, recurring tasks
- `10-sources/<source-name>/open-questions.md` — unknowns, risks, follow-ups

Promote cross-source material into shared pages:
- systems and workflows → `20-systems/`
- decisions and tradeoffs → `30-decisions/`
- repeatable procedures → `40-runbooks/`
- products, services, integrations, important people → `50-entities/`

Every extracted claim should include a source reference: repo/path, URL, commit, file path, or snapshot date.

## GBrain MVP Indexing

After the vault has useful Markdown:

1. Point GBrain at the vault root.
2. Index Markdown first; include source code only if GBrain supports scoped ignores and the user wants code-level answers.
3. Query the brain for common work questions.
4. Fix missing links or weak pages based on bad query results.

Good validation prompts:
- `What are the main systems and how do they connect?`
- `Which repos own customer-facing behavior?`
- `What deployment or operational runbooks exist?`
- `What decisions have been made and what risks remain?`
- `Which files or docs support this answer?`

## Maintenance Loop

Run this after meaningful repo changes or on a weekly/monthly cadence:

1. Pull latest source snapshots.
2. Diff docs, architecture, config, scripts, and runbooks.
3. Update source pages first.
4. Promote durable changes into systems, decisions, runbooks, and entity pages.
5. Re-index GBrain.
6. Run 3–5 validation queries.
7. Log what changed, what is stale, and what needs a human decision.

## Graphify Escalation

Use Graphify later when the brain needs richer relationship extraction, entity normalization, or visual graph workflows beyond GBrain's MVP search/graph layer.

Escalate when:
- multiple repos have many duplicated or conflicting entities
- teams need canonical owners, services, dependencies, and lineage
- graph queries need typed edges such as `owns`, `depends_on`, `calls`, `deploys_to`, or `replaced_by`
- manual Markdown linking is becoming the bottleneck

Do not start with Graphify if a clean Markdown vault plus GBrain can answer the current questions.

## Output Standard

Return:
- vault path or repo branch
- sources processed
- key indexes created
- GBrain import/index status
- validation queries and results
- stale areas, risks, and next maintenance action
