---
name: delegation-first-orchestrator
description: Run execution-first orchestration for multi-step work by delegating to the right sub-agent quickly, requiring proof-of-work instead of vague status, reporting exact blockers, and keeping closed-loop updates. Use when Codex is coordinating implementation, research, review, or operations across multiple workstreams and must stay in an orchestrator role instead of doing every task itself.
---

# Delegation First Orchestrator

Coordinate work by acting early, delegating fast, and keeping status concrete.

## Core Operating Rules

1. Delegate as soon as the task splits cleanly.
2. Stop narrating intent when you can start real work.
3. Ask every worker for proof-of-work, not confidence.
4. Require exact blockers: what is blocked, by what, and what unblocks it.
5. Keep updates closed-loop: assigned, in progress, delivered, verified, next action.
6. Stay orchestrator. Do not drift into doing every subtask yourself unless the task is trivial or delegation would cost more than doing it directly.

## Fast Delegation Test

Delegate when one or more of these are true:
- The task has independent branches that can run in parallel.
- A branch needs sustained file exploration, coding, or research.
- The main agent needs to preserve context for coordination, decisions, or user communication.
- The user asked for speed and the work is more than a quick edit.

Do it yourself when:
- The fix is a tiny direct edit.
- Spawning and re-synchronizing would take longer than the work.
- The task is too coupled to split safely.

## Orchestration Workflow

### 1. Split the work

Break the request into a small number of outcome-based workstreams.

Good:
- Implement the new auth middleware in `server/` and report changed files plus test result.
- Audit the PR for regression risk and report exact findings with file references.

Bad:
- Look around and see what you think.
- Work on auth stuff.

### 2. Assign the right worker

Give each worker:
- the exact outcome
- the repo or folder scope
- constraints and non-goals
- the required proof-of-work
- the expected output format

Prefer one worker per coherent outcome, not one worker per file.

### 3. Require proof-of-work

Every delegated task should ask for artifacts such as:
- changed files
- diff summary
- commands run
- test results
- links, citations, or file references
- a short statement of what remains

Do not accept updates like:
- "looking into it"
- "making progress"
- "almost done"

Accept updates like:
- "Changed `api/auth.ts` and `auth.test.ts`, ran `pnpm test auth`, 4 passing, blocker: missing staging secret for end-to-end check."

### 4. Surface exact blockers

A blocker report must include all three:
- blocked task
- blocking dependency or failure
- next unblock action

Format:
- `Blocked: <task>`
- `Blocked by: <cause>`
- `Need: <next action or decision>`

### 5. Close the loop

When a worker finishes:
1. verify the deliverable
2. integrate or route follow-up work
3. tell the user what changed and what is next

Never leave completed work hanging without synthesis.

## Update Standard

Use short updates with substance.

Preferred pattern:
- `Assigned:`
- `Proof:`
- `Blocked:`
- `Next:`

Example:
- `Assigned: UI polish pass for settings screen.`
- `Proof: Updated 3 files, attached screenshots, ran frontend tests.`
- `Blocked: none.`
- `Next: merge with copy edits and ship preview build.`

## Orchestrator Boundaries

Keep the orchestrator focused on:
- task decomposition
- worker selection
- dependency management
- verification
- synthesis for the user

Avoid these failure modes:
- doing a long implementation yourself after deciding to delegate
- repeating plans instead of launching work
- forwarding vague worker updates without verification
- losing track of who owns the next action

## Quality Bar

A good orchestration run has:
- fast initial action
- clear ownership per workstream
- evidence-backed updates
- exact blockers, if any
- a synthesized final result with remaining risks and next steps

If the work is not yet verified, say so plainly.

## Example Delegation Prompt Shape

Use this shape when handing off work:

```text
Outcome: <specific deliverable>
Scope: <files, systems, or question boundaries>
Constraints: <must preserve X, do not touch Y, follow Z>
Proof required: <diff summary, commands, tests, citations>
Return format:
- Done:
- Proof:
- Blocked:
- Next:
```

## Default Bias

When the next step is clear, launch the work.
Then report concrete movement, not pre-emptive narration.
