# Delegation-First Orchestration

## What this package is for

This package is for agents and teams that want faster execution without turning the main orchestrator into a bottleneck.

The operating idea is simple:
- delegate to the right sub-agent fast
- stop narrating instead of acting
- require proof-of-work over vague status
- surface exact blockers
- keep updates closed-loop
- let the orchestrator stay the orchestrator

## The pattern in one sentence

The main agent should spend less time explaining what it plans to do, and more time assigning clear outcomes, verifying results, and synthesizing progress.

## The six rules

1. **Delegate early when the work splits cleanly**  
   If a task has parallel branches, hand them off instead of carrying them all in one context.

2. **Act before narrating**  
   If the next step is obvious, start it. Status should follow movement, not replace it.

3. **Ask for proof-of-work**  
   Every update should contain evidence: changed files, commands run, test output, citations, screenshots, or concrete findings.

4. **Make blockers exact**  
   "Blocked" is incomplete unless it says what is blocked, what caused it, and what unblocks it.

5. **Close the loop**  
   Work is not done when a worker stops. It is done when the orchestrator verifies, integrates, and tells the user what changed and what comes next.

6. **Keep the orchestrator in role**  
   The orchestrator should coordinate, verify, and synthesize. It should not drift into doing every long branch itself.

## What good delegation looks like

Bad:
- "Can you check the backend?"
- "Let me think through the plan first"
- "Still working on it"

Good:
- "Implement the rate-limit fix in `api/`, preserve public response shape, run relevant tests, and report changed files plus any remaining risk."
- "Audit the PR for regression risk and return exact findings with file references."
- "Research the API behavior and return 3 sourced conclusions plus the open question, if any."

## The required update format

Use a small, hard-to-fake status format:

- `Assigned:` what this worker owns
- `Proof:` artifacts or evidence
- `Blocked:` exact blocker, or `none`
- `Next:` next action

Example:

- `Assigned: Fix flaky auth test in CI.`
- `Proof: Updated 2 test files, ran pnpm test auth, 6 passing.`
- `Blocked: none.`
- `Next: open PR note about the race-condition root cause.`

## When to use this skill

Use the included skill when the main agent is coordinating:
- coding work that splits into implementation, review, and validation
- research with multiple answer branches
- ops work where one agent should coordinate and others should execute
- any multi-step job where vague status updates are slowing things down

## Package contents

- `delegation-first/GUIDE.md` — this human-readable guide
- `delegation-first/delegation-first-orchestrator/` — source skill folder
- `delegation-first/delegation-first-orchestrator.skill` — packaged installable skill

## Installation

Install the `.skill` file in your OpenClaw or compatible skill environment.

Then invoke or rely on the skill when you want execution-first orchestration behavior for multi-step tasks.

## Practical expectation

If this package is working, you should notice:
- shorter time to first real action
- fewer hand-wavy progress updates
- clearer ownership
- better visibility into blockers
- cleaner final synthesis
