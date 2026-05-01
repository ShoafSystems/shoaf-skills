# Shoaf Systems Skills

Public Shoaf Systems skills repo for practical agent skills and guides built around OpenClaw-style workflows.

Use this repo for public skills, guides, and patterns you can read directly, install into a compatible agent environment, or adapt for your own agent operations.

## Current packages

### Obsidian Memory

Helps convert loose agent memory, logs, and notes into a structured Obsidian vault with raw observations, shared canonical pages, and curated long-term sources.

Included:
- `obsidian-memory/GUIDE.md` — human guide for converting existing notes, logs, exports, and agent memory into the Obsidian format
- `obsidian-memory/shared-memory-system.skill` — installable OpenClaw skill for organizing, promoting, and maintaining that memory model

Useful for:
- OpenClaw users
- Claude-based agent workflows
- teams that want an Obsidian-first knowledge layer for agent operations

### Delegation First

A practical orchestration pattern for agents that need to delegate work clearly instead of turning the main agent into the bottleneck.

Included:
- `delegation-first/GUIDE.md` — public guide for running delegation-first orchestration
- `delegation-first/delegation-first-orchestrator/` — source skill folder
- `delegation-first/delegation-first-orchestrator.skill` — packaged installable OpenClaw skill

Useful for:
- multi-agent coding, research, or ops workflows
- tasks where workers need clear ownership and evidence of progress
- agents that need better blocker reporting and final synthesis

## Whop

The broader Shoaf Systems skills library lives on Whop: [https://whop.com/shoaf-dev/](https://whop.com/shoaf-dev/)

Whop has deeper implementation material, templates, build walkthroughs, additional resources, and the larger library beyond the public GitHub skills and guides.

## Using the skills

Download the `.skill` files from this repo and install them in OpenClaw or a compatible skill environment. The `GUIDE.md` files can also be read directly without installing anything.
