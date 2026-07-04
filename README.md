# Agent as Code

`agent-as-code` explores how to represent agents, tools, permissions, prompts, evals, handoffs, and execution contracts as version-controlled, reviewable, testable, auditable, and agent-operable source material.

## Working Definition

`Agent-as-Code` means treating agents, tools, permissions, prompts, evals, handoffs, and execution contracts as canonical operational state expressed through files, schemas, examples, tests, and reviewable change history.

## Goals

- Define the domain clearly.
- Collect prior art and examples.
- Provide reusable schemas and templates.
- Support human review and agent execution.
- Preserve auditability, provenance, and governance boundaries.

## Non-Goals

- This repo is not a universal standard.
- This repo is not legal, security, compliance, or operational advice.
- This repo does not canonize HUMMBL/BaseN/Ownward concepts unless explicitly marked and audited.

## Status

- packet-status: `seed` -> `v0.1-draft`

Public repo. Early public seed repository.

## v0.1 packet locations

- Boundary: [`docs/v0.1-boundary.md`](docs/v0.1-boundary.md)
- Schema: [`schemas/agent-as-code-v0.1.json`](schemas/agent-as-code-v0.1.json)
- Example: [`examples/agent-v0.1.example.json`](examples/agent-v0.1.example.json)
- Fixtures: [`fixtures/valid/agent-v0.1.valid.json`](fixtures/valid/agent-v0.1.valid.json), [`fixtures/invalid/agent-v0.1.invalid.json`](fixtures/invalid/agent-v0.1.invalid.json)
