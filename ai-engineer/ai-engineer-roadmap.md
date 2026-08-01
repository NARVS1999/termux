# AI Engineer Developer Roadmap: Fundamentals → Intermediate

> General knowledge for software developers, with AI engineering-specific context.

## AI Fundamentals (Prerequisites)

- [x] **Phase 1** — What is an AI Engineer: role overview, AI Engineer vs ML Engineer, responsibilities
- [x] **Phase 2** — AI basics: AI vs ML vs DL, LLMs, training vs inference
- [x] **Phase 3** — Core terminology: tokens, context window, pre-trained models, AI vs AGI
- [x] **Phase 4** — Programming prerequisites: Python, APIs, data handling
- [x] **Phase 5** — Impact on product development: frontend, backend, full-stack, use cases

## How LLMs Work

- [x] **Phase 6** — LLM architecture: transformer basics, attention, next-token prediction
- [x] **Phase 7** — Model lifecycle: pre-training, fine-tuning, alignment
- [x] **Phase 8** — Proprietary models: OpenAI (GPT, o-series), Anthropic Claude, Google Gemini
- [x] **Phase 9** — Open source models: Meta Llama, Mistral, Cohere, Gemma, Qwen

## Prompt Engineering

- [x] **Phase 10** — Prompt anatomy: instructions, input format, system prompting, context
- [x] **Phase 11** — Prompting techniques: zero-shot, few-shot, chain-of-thought (CoT)
- [x] **Phase 12** — Advanced prompting: ReAct, role & behavior, constraints
- [x] **Phase 13** — Sampling parameters: temperature, top-k, top-p, repetition penalties
- [x] **Phase 14** — Structured output: JSON mode, function calling, output schemas
- [x] **Phase 15** — Production prompting: prompt caching, streaming responses, context engineering

## AI Safety & Ethics

- [x] **Phase 16** — AI safety issues: bias and fairness, hallucination, privacy concerns
- [x] **Phase 17** — Prompt injection attacks: attack types, mitigation, robust prompting
- [x] **Phase 18** — Security & privacy: end-user IDs in prompts, constraining inputs and outputs
- [x] **Phase 19** — Safety best practices: adversarial testing, content moderation APIs, know your use cases

## Working with LLMs

- [x] **Phase 20** — Model selection: closed vs open source, self-hosted models, trade-offs
- [x] **Phase 21** — Local tooling: Ollama, LM Studio, Hugging Face Hub, Transformers.js
- [x] **Phase 22** — OpenAI APIs: Responses API, embeddings, SDKs
- [x] **Phase 23** — Other providers: Google Gemini API, Anthropic Messages API, OpenAI-compatible APIs
- [x] **Phase 24** — Platforms & ecosystem: Hugging Face Inference SDK, OpenRouter, Vertex AI Agent Builder

## Embeddings & Vector Databases

- [x] **Phase 25** — Embeddings: what they are, semantic search, use cases
- [x] **Phase 26** — Embedding models: OpenAI Embeddings API, Cohere, Gemini Embedding, Jina, Sentence Transformers
- [x] **Phase 27** — Vector databases: purpose and functionality, Chroma, FAISS
- [x] **Phase 28** — More vector DBs: Pinecone, Weaviate, Qdrant, LanceDB, Supabase, MongoDB Atlas
- [x] **Phase 29** — Vector search: indexing embeddings, similarity search, implementing vector search

## RAG (Retrieval-Augmented Generation)

- [x] **Phase 30** — RAG fundamentals: what is RAG, use cases, RAG vs fine-tuning
- [x] **Phase 31** — RAG pipeline: chunking, embedding, vector database, retrieval, generation
- [x] **Phase 32** — Implementing RAG: using SDKs directly, LangChain, LlamaIndex
- [x] **Phase 33** — RAG frameworks: Haystack, RAGFlow
- [x] **Phase 34** — Advanced RAG: external memory, dynamic filters, context compaction, context isolation
- [x] **Phase 35** — RAG evaluation: retrieval quality, groundedness, RAGAS, DeepEval

## AI Agents & MCP

- [x] **Phase 36** — AI agents: what they are, use cases, agent workflows
- [x] **Phase 37** — Tools & function calling: tool definitions, execution loop
- [x] **Phase 38** — Agent frameworks: OpenAI AgentKit & Agent SDK, Claude Agent SDK, Google ADK
- [x] **Phase 39** — ReAct prompting: reasoning + acting loop, manual implementation
- [x] **Phase 40** — Model Context Protocol (MCP): core components, host, server, client, data layer, transport layer
- [x] **Phase 41** — Multi-agent systems: multi-agents, orchestration patterns

## Multimodal AI

- [x] **Phase 42** — Multimodal tasks: image understanding, image generation, video understanding, audio processing
- [x] **Phase 43** — Multimodal APIs: OpenAI Vision API, DALL-E, Whisper, TTS, speech-to-text
- [x] **Phase 44** — Multimodal apps: LangChain and LlamaIndex for multimodal, Hugging Face models

## Evaluation & Observability

- [x] **Phase 45** — LLM evaluations: deterministic, model-based, human evals, metrics, regression testing
- [x] **Phase 46** — Observability: tracing & logging, cost/latency monitoring, production monitoring
- [x] **Phase 47** — Eval tools: LangSmith, Langfuse, Helicone, Arize AI, evaluation types

## Recommended Learning Path (priority order)

1. **Phase 1–5** — AI fundamentals & terminology
2. **Phase 6–9** — How LLMs work
3. **Phase 10–12** — Prompt engineering basics
4. **Phase 16–19** — AI safety & ethics
5. **Phase 20–22** — Working with LLM APIs
6. **Phase 25–29** — Embeddings & vector databases
7. **Phase 30–35** — RAG

> Focus on building real projects — employers hire mid-level AI engineers for clean, performant, well-tested AI features plus ownership of features end-to-end.
