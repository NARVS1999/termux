# AI Agents Concept Hierarchy

## Foundational Concepts

1. LLM Basics — basic — ang pag-generate ng text gamit ang large language models
2. Tokens & Context — basic — ang pag-split ng text into tokens at context window limit
3. Model Selection — basic — ang pag-choose ng tamang LLM model para sa reasoning at multimodal tasks
4. Instruction Following — basic — ang pag-follow ng instructions at output formatting ng LLM
5. Prompt Engineering — basic — ang pag-structure ng prompts para sa better outputs

## Core Concepts

1. Prompting for Agents — intermediate — ang pag-design ng instructions, constraints, output formats para sa agents
2. Tool Calling — intermediate — ang pag-call ng external functions gamit ang function calling schemas
3. Agent Loop — intermediate — ang cyclical na perceive-reason-act-observe process
4. Reasoning & Planning — advanced — ang step-by-step reasoning, subgoal decomposition, replanning

## Implementation Concepts

1. Tool Schemas — basic — ang pag-define ng JSON parameters, descriptions, validation para sa tools
2. Structured Output — intermediate — ang JSON mode, schema enforcement, output parsing
3. Tool Execution — intermediate — ang pag-run ng tools, result handling, error responses
4. Tool Design — intermediate — ang pag-design ng capabilities, naming, permissions ng tools
5. Tool Selection & Routing — advanced — ang pag-choose ng tamang tool, conflict resolution, delegation

## Integration Concepts

1. Error Handling — intermediate — ang retries, fallbacks, feedback loops sa tool failures
2. Short-term Memory — intermediate — ang conversation history, scratchpads, session state
3. Long-term Memory — advanced — ang persistent storage, knowledge retention across sessions
4. Retrieval Memory — advanced — ang embeddings, vector search, semantic recall
5. Context Management — advanced — ang trimming, compression, relevance filtering ng context

## Architectural Concepts

1. Single vs Multi-Agent — intermediate — ang trade-offs ng complexity at coordination
2. LangChain Basics — intermediate — ang chains, tools, memory integration ng LangChain
3. LangGraph — advanced — ang state machines, checkpoint-based workflows, graph execution
4. OpenAI Agents SDK — intermediate — ang built-in agents, handoffs, guardrails ng SDK
5. RAG Integration — advanced — ang retrieval-augmented generation, grounding, citations
6. Vector Stores — intermediate — ang indexes, embedding pipelines para sa vector data

## Design Concepts

1. Orchestration Patterns — advanced — ang supervisor, pipeline, swarm architectures
2. Agent Registries — intermediate — ang discovery, reuse, catalog management ng agents
3. Roles & Delegation — intermediate — ang specialist roles, task assignment sa multi-agent
4. Communication Patterns — intermediate — ang messages, channels, handoffs between agents
5. Coordination — advanced — ang leader-follower, consensus, debate mechanisms
6. Shared State — advanced — ang repositories, locks, consistency management sa agents

## Advanced Concepts

1. Failure Modes — advanced — ang loops, conflicts, cascades sa multi-agent systems
2. Summarization — intermediate — ang history compression, state checkpoints, summarization
3. Evals — advanced — ang task success, trajectory analysis, quality scoring metrics
4. Tracing & Observability — intermediate — ang monitoring ng steps, tool calls, token usage
5. Guardrails — intermediate — ang input/output filters, constraints, safety boundaries
6. Testing — advanced — ang unit, integration, scenario suite testing ng agents

## Production Concepts

1. Error Recovery — advanced — ang retries, escalation, graceful exits sa failures
2. Deployment — intermediate — ang serving, scaling, autoscaling ng agents
3. Monitoring — intermediate — ang latency, cost, quality drift tracking sa production
4. Versioning — intermediate — ang prompts, models, agent releases management
5. Prompt Injection — advanced — ang defenses, detection, sandboxing ng attacks
6. Permissions — intermediate — ang tool scopes, approval flows, least privilege access

## Optimization Concepts

1. Data Safety — intermediate — ang PII handling, retention policies, encryption
2. Abuse Prevention — advanced — ang rate limits, monitoring, red teaming strategies
3. Cost & Latency — advanced — ang caching, routing, batching optimization techniques
4. Model Versioning — intermediate — ang pag-select ng model version at provider routing
5. Agent Releases — intermediate — ang versioning ng prompts, configs, agent deployments

## Expert/Strategic Concepts

1. Real-world Patterns — advanced — ang customer support, research, coding agents deployment
2. Orchestration Mastery — advanced — ang pag-choose ng tamang pattern para sa use case
3. Multi-Agent Scaling — advanced — ang pag-scale ng multi-agent systems sa production
4. Safety-First Design — advanced — ang pag-design ng agents na may built-in safety controls
