# Company Brain / GBrain Guide

Use this guide to build a practical company brain from multiple connected repos. The first version is an Obsidian-compatible Markdown vault indexed by GBrain. Graphify comes later if you need richer entity and relationship enrichment.

## What you get

- A portable Markdown/Obsidian vault
- Source-linked summaries of four related repos or folders
- Indexes for systems, decisions, runbooks, entities, and open questions
- GBrain search/graph import readiness
- A maintenance loop that keeps the brain from going stale

## Prerequisites

- Access to the repos or local folders you want to include
- Git, if any sources are remote repos
- Obsidian or any Markdown editor
- GBrain installed or available in your environment
- Optional later: Graphify for richer graph enrichment

## 1. Collect four sources

Start with four repos or folders that define the company or product. For each source, capture:

```text
Name: <short-name>
Source: <git URL or local path>
Purpose: <one sentence>
Default branch/snapshot: <branch, tag, commit, or date>
Focus areas: <architecture | product | ops | sales | support | research | all>
```

Example using public-safe placeholder paths:

```text
Name: web-app
Source: https://github.com/example/company-web-app.git
Purpose: Customer-facing application.
Default branch/snapshot: main
Focus areas: architecture, product, ops

Name: agent-workflows
Source: /local/example/repos/agent-workflows
Purpose: Internal agent runbooks and automations.
Default branch/snapshot: 2026-05-01 snapshot
Focus areas: ops, runbooks, decisions
```

Do not paste secrets into the brain. Summarize credentials, customers, tokens, and production data as redacted patterns.

## 2. Create the vault structure

Create a folder named `company-brain` or another clear name:

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

Folder purpose:

- `00-inbox/` — temporary notes and unprocessed imports
- `10-sources/` — one folder per repo/folder snapshot
- `20-systems/` — cross-repo systems, architecture, workflows, data flows
- `30-decisions/` — decisions, tradeoffs, why something works this way
- `40-runbooks/` — repeatable procedures
- `50-entities/` — people, products, services, integrations, vendors, concepts
- `90-indexes/` — maps of content, status, and common query paths

## 3. Extract each repo into source pages

For each repo or folder, create these pages:

```text
10-sources/<source-name>/overview.md
10-sources/<source-name>/architecture.md
10-sources/<source-name>/operations.md
10-sources/<source-name>/open-questions.md
```

Recommended page template:

```markdown
# <Source Name> Overview

## Purpose
<what this source owns>

## Important paths
- `<path>` — <why it matters>

## Key workflows
- <workflow> — <where it starts, where it ends>

## Source references
- Repo/path: <URL or local path label>
- Snapshot: <branch, commit, tag, or date>
- Files reviewed: <key files>

## Open questions
- <unknown or stale area>
```

Promote durable cross-repo knowledge out of `10-sources/` and into shared folders. For example:

- A system that spans two repos → `20-systems/<system-name>.md`
- A deployment procedure → `40-runbooks/deploy-<service>.md`
- A product or integration → `50-entities/products/<product-name>.md` or `50-entities/integrations/<integration-name>.md`
- A why/why-not tradeoff → `30-decisions/<date-or-topic>.md`

## 4. Build useful indexes

Create these minimum index files:

```text
90-indexes/source-map.md
90-indexes/system-map.md
90-indexes/decision-log.md
90-indexes/runbook-index.md
90-indexes/open-questions.md
```

Each index should link to the pages that answer common questions. Keep them short and navigable.

## 5. Import into GBrain

Use GBrain as the MVP search and graph layer.

General import flow:

1. Open GBrain.
2. Create or select a workspace for the company brain.
3. Add the vault root folder as a Markdown source.
4. Index Markdown files first.
5. If needed, add selected source-code folders later with ignores for dependencies, build output, cache folders, and generated files.
6. Re-index after edits.

Recommended ignore patterns if GBrain supports them:

```text
.git/
node_modules/
dist/
build/
.next/
coverage/
.cache/
.env*
*.log
```

## 6. Validate with queries

Run queries that mimic real work, not demo questions:

```text
What are the main systems and how do they connect?
Which repos own customer-facing behavior?
What runbooks exist for deployment or recurring operations?
What decisions explain the current architecture?
What open questions or stale areas need human review?
Which source files support this answer?
```

If GBrain answers vaguely, fix the Markdown. Usually the issue is missing source references, weak indexes, or too much unstructured text in `00-inbox/`.

## 7. Maintenance loop

Run this weekly, monthly, or after meaningful repo changes:

1. Pull or snapshot each source.
2. Review diffs for docs, architecture, configuration, workflows, and scripts.
3. Update `10-sources/<source-name>/` pages first.
4. Promote durable changes into systems, decisions, runbooks, and entity pages.
5. Update index files.
6. Re-index GBrain.
7. Re-run 3–5 validation queries.
8. Record stale areas and open decisions in `90-indexes/open-questions.md`.

## 8. Escalate to Graphify later

Bring in Graphify when the Markdown + GBrain layer is useful but not enough.

Good triggers:

- Many duplicated entities across repos
- Conflicting names for the same service, product, vendor, or workflow
- Need typed relationships like `owns`, `depends_on`, `calls`, `deploys_to`, `replaced_by`
- Need richer visual graph exploration for stakeholders
- Manual linking is becoming too slow

Graphify should enrich the already-useful vault. Do not use it as a substitute for clean source-linked Markdown.

## Done checklist

- [ ] Four sources collected or the missing sources are documented
- [ ] Vault folders created
- [ ] Source pages created for each repo/folder
- [ ] Cross-repo systems, decisions, runbooks, and entities promoted
- [ ] Index files created
- [ ] GBrain import/index completed
- [ ] Validation queries run
- [ ] Maintenance cadence chosen
- [ ] Graphify escalation criteria noted
