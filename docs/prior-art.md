# Prior Art and Adjacent Ecosystem References

This document collects public prior art, adjacent ecosystems, shared vocabulary, and key concepts that inform `agent-as-code`.

These are **references, not adopted canon.** Listing a project here does not mean this repository endorses, adopts, or inherits its design, vocabulary, or governance. Each entry is included because it touches part of the agent-as-code problem space and may be useful for comparison, contrast, or inspiration.

## Public prior art

These projects represent agents, workflows, or multi-agent systems in code or configuration. They are direct prior art for the "agent-as-code" framing.

### AutoGPT

- **What it does:** An autonomous agent loop that chains LLM calls with tools, memory, and self-prompted goals to pursue open-ended objectives.
- **Relevance to this repo:** Early, widely-cited example of an autonomous agent loop expressed as a runnable program. Illustrates both the appeal and the difficulty of open-ended autonomy without explicit contracts.
- **Public docs:** https://github.com/Significant-Gravitas/AutoGPT

### BabyAGI

- **What it does:** A lightweight task-creation and prioritization loop that generates, orders, and executes tasks toward a high-level objective.
- **Relevance to this repo:** Minimal, readable example of a planning loop with task management. Useful as a contrast point for how explicit, reviewable task contracts could be represented as code.
- **Public docs:** https://github.com/yoheinakajima/babyagi

### CrewAI

- **What it does:** A framework for defining role-based agents, tasks, crews, and delegation flows in Python code.
- **Relevance to this repo:** Closest direct analog for "agents as code": roles, tools, tasks, and handoffs are declared in source. Useful for comparing how agent definitions and delegation are modeled.
- **Public docs:** https://docs.crewai.com/

### AutoGen

- **What it does:** A Microsoft Research framework for building multi-agent conversations where agents send messages, call tools, and collaborate to solve tasks.
- **Relevance to this repo:** Demonstrates conversational multi-agent orchestration and tool use. Relevant for modeling handoffs, delegation, and inter-agent messaging as explicit contracts.
- **Public docs:** https://microsoft.github.io/autogen/

### LangGraph

- **What it does:** A graph-based framework for building stateful, multi-step agent workflows as nodes and edges with explicit state transitions.
- **Relevance to this repo:** Models agent execution as an explicit, inspectable graph. Relevant for representing planning loops, state, and control flow as reviewable code.
- **Public docs:** https://langchain-ai.github.io/langgraph/

### OpenAI Swarm

- **What it does:** An experimental, lightweight framework for agent handoffs and routing where agents transfer control to other agents via tool calls.
- **Relevance to this repo:** Minimal, educational model of delegation and handoffs. Useful reference for how agent-to-agent transfer can be expressed simply.
- **Public docs:** https://github.com/openai/swarm

### Agno

- **What it does:** A framework for building stateful, multimodal agents with memory, tools, and structured reasoning, formerly known as Phidata.
- **Relevance to this repo:** Demonstrates agent definitions with sessions, memory, and tool schemas in code. Relevant for modeling stateful agent identity and tool bindings.
- **Public docs:** https://docs.agno.com/

### PydanticAI

- **What it does:** A framework for building type-safe agents using Pydantic models for tool schemas, results, and dependency injection.
- **Relevance to this repo:** Strong example of schema-driven agent definitions with typed tool contracts. Directly relevant to the schema-first, inspectable approach this repo explores.
- **Public docs:** https://ai.pydantic.dev/

## Adjacent ecosystem

These projects are not agent frameworks per se, but they address adjacent concerns — prompt engineering, tool schemas, runtime, conversational state, or orchestration — that overlap with the agent-as-code problem space.

### DSPy

- **What it does:** A framework for programming language model pipelines declaratively, compiling prompts and demonstrations rather than hand-writing them.
- **Relevance to this repo:** Treats prompts and LM behavior as composable, optimizable code rather than opaque strings. Relevant for how prompts and evals could be represented as reviewable source.
- **Public docs:** https://dspy.ai/

### Inference (useGpu/Inference)

- **What it does:** An open-source runtime for serving and orchestrating LLM inference, including model loading, routing, and API compatibility.
- **Relevance to this repo:** Addresses the model-routing and execution runtime layer that agent-as-code contracts would run on top of. Relevant for separating agent contracts from inference infrastructure.
- **Public docs:** https://github.com/useInference/inference

### BAML (Boundary Markup Language)

- **What it does:** A schema-first language for defining LLM functions, tool schemas, prompts, and test cases in version-controlled files.
- **Relevance to this repo:** Directly models prompts, schemas, and tests as reviewable code. Strong reference for the "as-code" treatment of LLM interfaces and structured outputs.
- **Public docs:** https://docs.boundaryml.com/

### Semantic Kernel

- **What it does:** A Microsoft SDK that orchestrates "skills" (functions), planners, and memory for LLM-based applications across multiple languages.
- **Relevance to this repo:** Models tools as registered functions and uses planners to compose them. Relevant for tool schemas, planning, and memory as explicit, composable units.
- **Public docs:** https://learn.microsoft.com/en-us/semantic-kernel/

### Eliza

- **What it does:** An open-source, multi-platform autonomous agent framework with character definitions, memory, and plugin-based tools.
- **Relevance to this repo:** Demonstrates agent identity, character files, and plugin tooling as configurable source. Relevant for modeling agent definitions and extensible tool bindings.
- **Public docs:** https://elizaos.github.io/eliza/

### Rasa

- **What it does:** An open-source framework for building conversational AI assistants with intent classification, dialogue management, and rules.
- **Relevance to this repo:** Mature example of representing conversational flows, rules, and training data as version-controlled files. Relevant for stateful dialogue, guardrails, and testable conversation contracts.
- **Public docs:** https://rasa.com/docs/

## Vocabulary references

These are common terms used across the agent ecosystem. They are collected here for shared language, not as adopted definitions. This repo may refine or reject any of them.

- **agent-as-code** — Treating agents, tools, permissions, prompts, evals, handoffs, and execution contracts as version-controlled source material. (This repo's working definition.)
- **agent orchestration** — Coordinating the execution of one or more agents, including sequencing, routing, state, and handoffs.
- **multi-agent** — Systems in which multiple agents interact, collaborate, delegate, or negotiate to accomplish tasks.
- **tool use** — Agents invoking external functions, APIs, or capabilities according to defined schemas and permissions.
- **planning** — Agents decomposing goals into steps, tasks, or sub-goals, often with prioritization and re-planning loops.

## Key concepts

These concepts recur across the prior art and adjacent ecosystem. They are listed here as the shared shape of the problem space, not as a mandated feature set for this repo.

- **Agent definitions** — Declaring an agent's role, identity, scope, permissions, and bindings as explicit, inspectable source.
- **Tool schemas** — Describing the functions an agent may call, including inputs, outputs, types, and constraints, in a machine-readable form.
- **Memory** — Persisting context, history, or learned state across agent runs or turns, with explicit retention and retrieval boundaries.
- **Planning loops** — Generating, ordering, executing, and revising tasks toward a goal, with observable state transitions.
- **Guardrails** — Explicit constraints on agent behavior, including scope limits, permission boundaries, safety checks, and escalation rules.
- **Delegation** — One agent transferring control, context, or sub-tasks to another agent, with defined handoff contracts.

## Non-canon note

This document is a reference collection, not an adopted standard.

- Nothing listed here is canon for `agent-as-code` unless separately and explicitly adopted through this repository's review process.
- Links point to public documentation for comparison and attribution only.
- Vocabulary and concepts are recorded for shared language; this repo may redefine, narrow, or reject them.
- This repository remains `seed`/`v0.1-draft` until an explicit non-canon override is recorded.
