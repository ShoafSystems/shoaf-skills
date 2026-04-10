# How to Convert Your Agent Memory to Obsidian

## What This Guide Is For

You have notes. Logs. Bot outputs. Chat history. Maybe Claude memory exports, OpenClaw logs, raw markdown files, or just a messy folder of agent-generated content.

This guide shows you how to take that existing memory and convert it into a structured, visual, navigable knowledge graph using Obsidian.

The result: a multi-layer vault where raw observations, shared canonical truth, and curated syntheses all connect in a visual graph.

## The Memory Model

Before converting your files, understand the three-tier model:

| Tier | What goes here | Examples |
|------|---------------|---------|
| Tier 1: Raw bot memory | Logs, daily notes, drafts, raw outputs | agent-a/logs/2024-01-01.md, chat exports, session notes |
| Tier 2: Shared canonical pages | Durable facts about people, companies, projects, decisions | a person's role, a project's status, a decision record |
| Tier 3: Wiki sources + compiled | Curated syntheses worth keeping long-term | architecture notes, playbooks, research summaries |

Rule: raw observations go in Tier 1. Durable facts go in Tier 2. Curated knowledge goes in Tier 3.

## Step 1: Create Your Vault

Open Obsidian and create a new folder anywhere on your machine. Open it as a vault:
`File → Open folder as vault → select your folder`

Then create this structure inside it:

```text
my-memory/
├── HOME.md                         ← your main dashboard
├── vault/
│   ├── bots/
│   │   └── <agent-name>/
│   │       ├── logs/               ← Tier 1: daily logs
│   │       ├── memory/             ← Tier 1: raw notes and imports
│   │       └── working/            ← Tier 1: in-progress drafts
│   └── shared/
│       ├── people/                 ← Tier 2: canonical people pages
│       ├── companies/              ← Tier 2: canonical company pages
│       ├── projects/               ← Tier 2: canonical project pages
│       └── decisions/              ← Tier 2: decisions and architecture
├── wiki/
│   ├── sources/                    ← Tier 3: curated for compilation
│   └── compiled/                   ← Tier 3: final compiled output
└── tools/                          ← helper scripts (optional)
```

*(Optional: use the template repo for pre-built tools and graph skin — `git clone <repo-url> my-memory` — but this is not required. The folder structure above is all you need.)*

## Step 2: Sort Your Existing Memory

Go through your existing notes, logs, and exports. For each file or chunk, decide which tier it belongs to:

**Goes in vault/bots/<agent-name>/memory/** (Tier 1):
- Raw chat exports
- Session logs
- Rough notes
- Unprocessed agent outputs
- Anything uncertain or temporary

**Goes in vault/shared/** (Tier 2):
- Stable facts about a person (role, contact, background)
- A company's current status
- A project's goals and state
- A decision that was made and should stay recorded

**Goes in wiki/sources/** (Tier 3):
- A well-written explanation of a system
- A process playbook
- Research summaries
- Architecture documentation

If you're unsure, put it in Tier 1. You can always promote it later.

## Step 3: Import Your Raw Memory

Bulk import into Tier 1:
- Copy or move your existing notes/logs into vault/bots/<agent-name>/memory/
- If you have daily logs, rename them YYYY-MM-DD.md and move to vault/bots/<agent-name>/logs/
- Keep original filenames where possible

Using the helper script (if available):
```bash
python3 tools/append_bot_log.py <agent-name> "Imported memory from <source>"
```

Or just copy files directly.

## Step 4: Create Canonical Pages (Tier 2)

For each durable entity (person, company, project, decision), create a canonical page in vault/shared/:

```markdown
---
tags: [person, canonical]
---
# Person A
Short summary of who this is.

## Context
- Role: <their role>
- Status: <current status>
- Key facts: <durable facts only>

## Related
- [[vault/shared/companies/company-a]]
- [[wiki/sources/relevant-playbook]]

---
Sources: [[vault/bots/agent-a/memory/original-note]]
```

Canonical pages are the truth layer. Keep them concise and factual.

## Step 5: Wire the Graph

The graph works through wikilinks. The more links you add, the richer the graph.

In each note, link outward to the canonical pages it mentions:
- [[vault/shared/people/person-a]]
- [[vault/shared/companies/company-a]]
- [[vault/shared/projects/project-a]]

In your HOME.md, link to everything important so HOME is the hub.

Open graph view with Cmd+G in Obsidian.

## Step 6: Promote Curated Knowledge (Tier 3)

When you have a note worth keeping as durable reference material, promote it to wiki/sources/.

Manually: copy the file to wiki/sources/ and add frontmatter:
```yaml
---
tags: [architecture, durable]
source: vault/bots/agent-a/memory/original-note
promoted_at: YYYY-MM-DD
---
```

Using the helper script:
```bash
python3 tools/promote_to_wiki_source.py shared/standards/my-note.md
```

## Step 7: Compile (Optional)

If you want a clean compiled layer:
```bash
python3 tools/compile_wiki.py
```

This copies wiki/sources/ → wiki/compiled/ and generates an index.

Only run this from your designated compile authority machine (usually your primary machine).

## Operating Going Forward

Daily workflow:
- New agent output → vault/bots/<agent>/memory/ or logs/
- New durable fact → vault/shared/<type>/
- New curated synthesis → wiki/sources/
- Sync across machines via git

Key principles:
- Tier 1 is your inbox. Don't treat it as truth.
- Tier 2 is truth. Keep it maintained and concise.
- Tier 3 is knowledge. Only promote what earns it.
- The graph connects everything. Add wikilinks liberally.

## Enabling the Visual Graph Skin

The repo includes a dark/gold visual graph skin.

To enable:
1. Open Obsidian settings
2. Go to Appearance → CSS snippets
3. Toggle on the graph skin snippet
4. Open Cmd+G to see the styled graph

Color coding by default:
- People → gold
- Companies → amber
- Projects → orange
- Bot memory → bronze
- Decisions → deep orange
