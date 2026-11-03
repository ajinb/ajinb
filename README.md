# Ajin Baby

**AI Platform & Cloud Infrastructure Architect** · 15+ years in cloud architecture · 2x founder before architect

I design and ship AI-enabled cloud platforms — **agentic infrastructure, Model Context Protocol
(MCP) servers, context/graph infrastructure, and internal developer platforms** — for
safety-critical and regulated industries. My research asks what it takes for AI agents to
operate production infrastructure *reliably*: what the tool-call plane actually delivers, when
autonomous remediation loops go unstable, and how much authority an agent should hold.

Every repository here is runnable, tested and tied to a paper, a book chapter or a long-form post.

→ [cloudandsre.com](https://cloudandsre.com) · [LinkedIn](https://www.linkedin.com/in/ajinbaby) · [YouTube](https://www.youtube.com/@cloudandsre)
→ [ORCID 0009-0007-6190-9516](https://orcid.org/0009-0007-6190-9516) · [Google Scholar](https://scholar.google.com/citations?user=fvftnCwAAAAJ) · [Semantic Scholar](https://www.semanticscholar.org/author/Baby-Ajin/100714919) · [ResearchGate](https://www.researchgate.net/profile/Ajin-Baby-6)

---

## Research artifacts

Code and data behind my papers. Each reproduces its paper's results from a clean checkout.

| Repository | Companion to | What it shows |
|---|---|---|
| [`mcp-schema-drift`](https://github.com/ajinb/mcp-schema-drift) | *Pinning the Version Is Not Pinning the Tools: Deployment-Induced Schema Loss in MCP Servers* | Of 116 working release-pairs of the official MCP servers, 18 advertise different tool schemas depending on dependency resolution — 17 with every schema emptied. Ships `mcp-surface`, a CLI and GitHub Action that catches it |
| [`remediation-stability-sim`](https://github.com/ajinb/remediation-stability-sim) | *Stable by Design: A Control-Theoretic Account of AI-Driven Self-Healing Remediation Loops* | Dead-time alone flips a correct-by-construction remediation loop into oscillation; the settle/diverge frontier follows a delay–gain product law. [DOI 10.5281/zenodo.22786822](https://doi.org/10.5281/zenodo.22786822) |
| [`autonomy-budget`](https://github.com/ajinb/autonomy-budget) | *Error Budgets for Autonomy: SLO-Driven Authority Management for Autonomous AI Operators* | Error-budget semantics for agent authority: a blast-radius-weighted budget and a fast-down/slow-up authority ladder |
| [`mcp-chaos`](https://github.com/ajinb/mcp-chaos) | *The Tool-Call Plane: An Operational Reliability Model for MCP-Based Agent Infrastructure* | Fault injection and reliability SLIs for agent tool use |

## MCP and agent infrastructure

| Repository | What it is |
|---|---|
| [`catalog-context-graph`](https://github.com/ajinb/catalog-context-graph) | Backstage software catalog → operational context graph for agents over MCP: blast radius, ownership, change risk, catalog drift. Neo4j optional. Measured against flat retrieval |
| [`mcp-task-reliability`](https://github.com/ajinb/mcp-task-reliability) | The reliability layer the MCP Tasks extension leaves unspecified: durable store, retry classes, orphan reaping, adaptive polling |
| [`agent-spend-guard`](https://github.com/ajinb/agent-spend-guard) | Runtime spend circuit breaker for agent trajectories, with OpenTelemetry GenAI cost attribution |
| [`agent-incident-corpus`](https://github.com/ajinb/agent-incident-corpus) | Public AI-agent production failures as a replayable regression corpus with a CI gate |
| [`inference-slo`](https://github.com/ajinb/inference-slo) | SLO-aware admission control for LLM inference serving — what to shed, when, against which SLO |
| [`sre-harness`](https://github.com/ajinb/sre-harness) | Minimal reference harness for SRE agents: tools, verification, memory, guardrails, observability |
| [`context-assembler`](https://github.com/ajinb/context-assembler) | Context engineering reference: typed segments, enforced token budget, reranking, compaction |
| [`cloudandsre-skills`](https://github.com/ajinb/cloudandsre-skills) | Agent Skills for SRE work with output contracts, guardrails-as-code, golden evals and an MCP server |

## AI for operations

| Repository | What it is |
|---|---|
| [`alert-explainer`](https://github.com/ajinb/alert-explainer) | Alertmanager → AI triage brief service: dedup, enrichment cache, PagerDuty/Opsgenie/Teams/Slack, Prometheus metrics, Helm chart |
| [`incident-scribe`](https://github.com/ajinb/incident-scribe) | Slack thread → blameless incident report with deterministic timelines, local secret redaction and a published JSON Schema |
| [`sre-ai-toolkit`](https://github.com/ajinb/sre-ai-toolkit) | CLI tools: alert explainer, log anomalies, Terraform plan review with a CI risk gate, Kubernetes event triage |
| [`runbook-rag-starter`](https://github.com/ajinb/runbook-rag-starter) | The smallest useful RAG, in 40 lines — a Markdown folder, sqlite-vec, and a CLI |
| [`cloudandsre-python`](https://github.com/ajinb/cloudandsre-python) | Shared utilities: async circuit breaker, retry, throttle, a token-cost meter and OpenTelemetry GenAI attributes |
| [`agent-adam`](https://github.com/ajinb/agent-adam) | Agentic personal assistant: least-privilege Google OAuth, keychain token storage, queued destructive actions |

They share one engineering baseline: CI with tests, CodeQL, OpenSSF Scorecard, SHA-pinned
actions, Dependabot, release provenance, and a citation file.

**In progress:** `mcp-gateway` — identity and scope-token exchange, Cedar authorization, schema
firewall, quarantine queue for destructive calls, provenance ledger
([design](https://cloudandsre.com/blog/the-mcp-gateway-pattern)).

## Book

**[*Self-Healing Infrastructure: Building Autonomous Cloud Systems with AI*](https://leanpub.com/self-healing-infra-with-ai)** —
free on Leanpub · [DOI 10.5281/zenodo.22245770](https://doi.org/10.5281/zenodo.22245770) · companion labs in
[`self-healing-infra-labs`](https://github.com/ajinb/self-healing-infra-labs)

---

## Production stack

**AI platform:** Azure OpenAI / Azure AI Foundry · Anthropic Claude · MCP servers · GraphRAG
**Cloud & infra:** AWS (ECS/Fargate) · Azure · Kubernetes · Terraform · Databricks
**Graph & context:** Neo4j · Cypher · knowledge-graph-backed retrieval
**Platform engineering:** Backstage · SwaggerHub · OpenTelemetry · Prometheus
**Languages:** Python (primary) · Go · Bash · SQL / Cypher

## Writing

Every post ships with working code: **[cloudandsre.com](https://cloudandsre.com)**.

## Background

- 15+ years architecting and operating cloud systems at scale
- Currently Staff Software Engineer at a global aviation-SaaS platform (a Fortune-500 aviation technology company); previously Computing Architect there for 8 years
- 2x founder before architect — Veeble SoftTech (scaled 3→20, $500→$500K ARR, 110+ countries) and ExTravelMoney Technosol (CEO)
- MS Management Information Systems, University of Arizona · MS Artificial Intelligence, Indiana Wesleyan University (in progress)
- Azure AI Engineer Associate · AWS Solutions Architect Associate · Azure Administrator Associate · Neo4j Certified Professional · CNSS 4011/4012/4013
- IEEE member for 15+ years · Senior Member application in progress
