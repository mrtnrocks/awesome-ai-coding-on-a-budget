<p align="center">
  <img src="./banner.png" alt="Awesome AI Coding on a Budget Banner" width="100%">
</p>

# Awesome AI Coding on a Budget 🚀

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/mrtnrocks/awesome-ai-coding-on-a-budget)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/mrtnrocks/awesome-ai-coding-on-a-budget)
[![Wayfinder Map](https://img.shields.io/badge/Wayfinder-Map%20%231-blueviolet)](https://github.com/mrtnrocks/awesome-ai-coding-on-a-budget/issues/1)

> A curated guide to cost-efficient AI software engineering. Reduce token consumption by up to 90%, run local inference models, and increase output quality for each dollar in multi-agent workflows.

---

## Table of Contents

- [1. Model Selection & Benchmarking](#1-model-selection--benchmarking)
  - [Core Benchmarking & Intelligence Indexes](#core-benchmarking--intelligence-indexes)
  - [The 3-Tier Budget Model Strategy](#the-3-tier-budget-model-strategy)
  - [Empirical Selection Guidelines](#empirical-selection-guidelines)
- [2. LLM Gateways, Routing, API Proxies & Multi-Account Rotation](#2-llm-gateways-routing-api-proxies--multi-account-rotation)
  - [Open-Source AI Gateway & Proxy Matrix](#open-source-ai-gateway--proxy-matrix)
  - [Core Gateway & Proxy Deep Dives](#core-gateway--proxy-deep-dives)
  - [Multi-Account Account Rotation Strategies](#multi-account-account-rotation-strategies)
  - [Managed Cloud Routers & Intelligent Dispatchers](#managed-cloud-routers--intelligent-dispatchers)
  - [Telemetry, Spend Tracking & Usage Analytics](#telemetry-spend-tracking--usage-analytics)
- [3. Token Optimization & Prompt Compression](#3-token-optimization--prompt-compression)
  - [Token Compression & Optimization Tool Matrix](#token-compression--optimization-tool-matrix)
  - [Input Prompt Compression & Context Reduction](#input-prompt-compression--context-reduction)
  - [Output Token Minimization & Anti-Bloat Techniques](#output-token-minimization--anti-bloat-techniques)
  - [Recommended Production Recipe](#recommended-production-recipe)
- [4. Codebase Intelligence, RAG & MCP Context Preservation](#4-codebase-intelligence-rag--mcp-context-preservation)
  - [Codebase Intelligence & RAG Tool Matrix](#codebase-intelligence--rag-tool-matrix)
  - [Deep Dive: Core Codebase Intelligence Engines](#deep-dive-core-codebase-intelligence-engines)
  - [Model Context Protocol (MCP) Architecture](#model-context-protocol-mcp-architecture)
  - [Practical MCP Setup Configuration](#practical-mcp-setup-configuration)
- [5. Agent Harnesses, Skills & Quality Guardrails ("Fixing Vibe Coding")](#5-agent-harnesses-skills--quality-guardrails-fixing-vibe-coding)
  - [Quality Guardrail & Harness Tool Matrix](#quality-guardrail--harness-tool-matrix)
  - [Agent Harnesses & Composable Skills](#agent-harnesses--composable-skills)
  - [Static Linters, AST Guardrails & Runtime Telemetry](#static-linters-ast-guardrails--runtime-telemetry)
  - [Headless Browser Execution & Visual Verification](#headless-browser-execution--visual-verification)
  - [The 8 Tech Choices Before "Agentmaxxing"](#the-8-tech-choices-before-agentmaxxing)
- [6. Local Runtimes & Self-Hosted Inference](#6-local-runtimes--self-hosted-inference)
  - [Local Runtime & Self-Hosted Inference Matrix](#local-runtime--self-hosted-inference-matrix)
  - [Deep Dive: Core Local & Self-Hosted Engine Suite](#deep-dive-core-local--self-hosted-engine-suite)
  - [Quantization & Hardware Sizing Reference](#quantization--hardware-sizing-reference)
  - [Best Practices for Local & Self-Hosted AI Coding](#best-practices-for-local--self-hosted-ai-coding)
- [7. Pricing Intelligence, Deals & Grey Market Awareness](#7-pricing-intelligence-deals--grey-market-awareness)
  - [Pricing Intelligence & Grant Matrix](#pricing-intelligence--grant-matrix)
  - [Deep Dive: Pricing Intelligence, Grants & Risk Safeguards](#deep-dive-pricing-intelligence-grants--risk-safeguards)
  - [Economic Decision Architecture](#economic-decision-architecture)
  - [Official Deal & Grant Qualification Matrix](#official-deal--grant-qualification-matrix)
- [Contributing & Community](#contributing--community)
- [License](#license)

---

## 1. Model Selection & Benchmarking

You must balance model capability, execution speed, and token cost when you select a Large Language Model (LLM). Compare preference leaderboards, software benchmarks, and pricing indexes to build a model matrix. This matrix decreases API costs and keeps code quality high.

### Core Benchmarking & Intelligence Indexes

* **[LMSYS Chatbot Arena Leaderboard](https://arena.ai/leaderboard)**: Human Elo ratings for LLMs. Filter by **Coding** and **Hard Prompts** to measure human preference for code generation and debugging.
* **[DeepSWE Leaderboard](https://deepswe.datacurve.ai)**: Measures repository-level software engineering performance. Evaluates multi-file fixes, bug resolution, and unit test execution.
* **[Artificial Analysis](https://artificialanalysis.ai/#price-and-cost)**: Tracks model performance against cost. Shows real-time metrics for:
  * Quality Index against Price (per 1M input or output tokens)
  * Output Speed (Tokens per second)
  * Latency (Time-to-First-Token or TTFT)
* **[Models.dev](https://models.dev)** ([GitHub](https://github.com/opencode-ai/models)): Open-source database and JSON API. Gives model specifications, context limits, provider endpoints, and token prices.

---

### The 3-Tier Budget Model Strategy

Do not send every request to expensive flagship models. Divide agent operations into three cost tiers:

| Tier | Primary Use Case | Recommended Pareto-Optimal Models | Benchmark & Cost Focus |
| :--- | :--- | :--- | :--- |
| **Tier 1: High-Reasoning & Architecture** | Spec creation, system architecture, root-cause diagnosis across large codebases, complex refactoring | Top-tier reasoning & frontier architecture models | DeepSWE / LMSYS Coding top scores; used sparingly for planning and complex fixes. |
| **Tier 2: Routine Execution & Component Dev** | Feature implementation, test-driven development (TDD), API integration, code review | High-efficiency mid-tier execution & coding models | High Artificial Analysis speed/cost efficiency ($0.05–$0.30 / 1M tokens). |
| **Tier 3: Autocomplete & Background Tasks** | Inline code completion, docstring generation, linter warning fixes, git commit messages | Lightweight open-weights (7B–14B local) & zero-cost free-tier endpoints | Near-zero or zero API cost; ultra-low latency (<500ms TTFT). |

---

### Empirical Selection Guidelines

1. **Compare Quality with Pricing**: Do not select a model by Elo rank alone. Compare LMSYS and DeepSWE ranks against Artificial Analysis cost charts to find cost-efficient models. Efficient mid-tier models can give 90% of flagship performance at less than 10% of the cost.
2. **Use Programmatic Route Weighting**: Read the `models.dev` JSON API inside custom gateways (for example, OmniRoute or LiteLLM). Send fallback requests to the lowest-cost provider for that model tier.
3. **Match Model to Task Context**: Use fast and low-cost models (Tier 2 or Tier 3) for routine tasks, such as unit test fixes. If tests fail repeatedly or you need architectural decisions, use Tier 1 reasoning models.

---

## 2. LLM Gateways, Routing, API Proxies & Multi-Account Rotation

You must use local gateways and proxy daemons to run AI coding tools at scale. Gateways pool free API tiers, balance load across multiple accounts, compress prompts, and retry failed requests when primary endpoints reach rate limits.

---

### Open-Source AI Gateway & Proxy Matrix

| Feature / Metric | OmniRoute | 9router | CLIProxyAPI | LiteLLM | Manifest |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Primary Language** | TypeScript / Node.js | TypeScript / Node.js | **Go** (Golang) | **Python** | TypeScript / Node.js |
| **Primary Focus** | Free-tier pooling & CLI setup | Context token optimization | Multi-account OAuth load balancing | Enterprise backend proxy & governance | Agent routing & request auto-fix |
| **Provider Support** | **290+ providers** (90+ free) | 40+ providers | OAuth + major LLM APIs | 100+ LLM providers | 300+ models (32 providers) |
| **Token Saver Tech** | RTK + Caveman compression | RTK, Caveman, Ponytail, Headroom | Pure pass-through | Caching only | Full-body logging & cost tracking |
| **Multi-Account OAuth** | Supported (visual dashboard) | Supported (Round-robin) | **Best-in-class** (Instant 429 retry) | Virtual Keys & Team Budgets | Tiered API key fallback |
| **GUI / Dashboard** | Built-in Next.js App (`:20128`) | Built-in Next.js App (`:20128`) | Separate Docker UI | Streamlit / Web UI | Web Portal (`manifest.build`) |
| **CLI Setup Helpers** | `omniroute setup-claude`, `launch-codex` | Manual configuration / CLI launch scripts | Terminal flags (`--claude-login`) | Configuration via `config.yaml` | Configuration via YAML / CLI |
| **Resource Footprint** | Medium (Node.js + Web UI) | Medium (Node.js + Web UI) | **Ultra-low** (Single binary) | Medium (Python + Postgres/Redis) | Lightweight |

---

### Core Gateway & Proxy Deep Dives

* **[OmniRoute](https://github.com/diegosouzapw/OmniRoute)** ([omniroute.online](https://omniroute.online)): Open-source AI gateway under the MIT license. It combines more than 290 providers and 90 free tiers to give up to 1.5 billion free tokens each month. It includes a Next.js web interface, launcher tools (`omniroute setup-claude`), prompt compression, and MCP server support.
* **[9router](https://github.com/decolua/9router)**: Terminal proxy for developers who pay per token. It uses specialized engines (**RTK** to remove git diff noise, **Caveman Mode** for short output, **Ponytail Mode** for simple code, and **Headroom** for context management).
* **[CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI)**: Fast background daemon written in Go. It helps developers with multiple paid subscriptions. It receives API requests at `localhost:8317` and retries requests with alternate credentials when HTTP 429 rate limit errors occur.
* **[LiteLLM](https://github.com/BerriAI/litellm)**: Python proxy server for backend development. It converts 100 or more LLM APIs into the OpenAI format. It gives virtual API keys, team spend limits, load balancing, and access controls.
* **[Manifest](https://github.com/mnfst/manifest)** ([manifest.build](https://manifest.build/)): Open-source LLM router for AI agents. It supports 300 or more models across 32 providers. It includes custom routing rules, payload logging, cost tracking, and automatic request corrections.

---

### Multi-Account Account Rotation Strategies

You can manage multiple accounts with three methods:

| Approach | Tool | Mechanism | Network Proxy? | Key Advantage |
| :--- | :--- | :--- | :--- | :--- |
| **Native Profile Swapper** | **[claude-swap](https://github.com/Alishahryar1/free-claude-code)** (`cswap`) | Swaps `~/.claude.json` profile credentials proactively based on quota threshold (`cswap auto`). | No (Direct connection) | Native CLI function; zero proxy latency; supports per-terminal isolation (`cswap run 2`). |
| **Request Load Balancer** | **[CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI)** | Local HTTP proxy (`localhost:8317`) intercepting API calls; retries 429 rate limits instantly with alternate OAuth token. | Yes (Go HTTP Proxy) | Retries requests without user action; terminal session keeps state. |
| **Gateway & Safety Net** | **[OmniRoute](https://github.com/diegosouzapw/OmniRoute)** | Full local proxy (`localhost:20128`) with custom multi-model fallback chains (Primary Provider -> Secondary Account -> Alternative Model Fallback). | Yes (Next.js Proxy Server) | Web interface dashboard, context compression (RTK/Caveman), and cross-provider emergency fallback. |

---

### Managed Cloud Routers & Intelligent Dispatchers

Managed routers evaluate prompt complexity and select models automatically:

* **[OpenRouter Auto Router](https://openrouter.ai/openrouter/auto)** (`openrouter/auto`): Evaluates input prompt complexity and sends requests to the lowest-cost model that can complete the query.
* **[OpenRouter Fusion Router](https://openrouter.ai/openrouter/fusion)** (`openrouter/fusion`): Combines responses or routes across top models to increase output reliability.
* **[OpenRouter Pareto Code Router](https://openrouter.ai/openrouter/pareto-code)** (`openrouter/pareto-code`): Selects coding models on the Pareto frontier for speed, cost, and benchmark score.

---

### Telemetry, Spend Tracking & Usage Analytics

* **[tokscale](https://github.com/junhoyeo/tokscale)** ([tokscale.ai](https://tokscale.ai)): Terminal tool and leaderboard that tracks token consumption, throughput, and costs across 30 or more agent environments.
* **[ccusage](https://github.com/ccusage/ccusage)**: Terminal analytics tool that summarizes token usage and cost for terminal agent platforms.
* **[SandBase CLI](https://github.com/sandbaseai/cli)**: Apache-2.0 CLI and local MCP bridge whose inspection tool shows current model pricing before a call and whose run history reports per-call costs across a catalog of 2,000+ AI models.

---

### Selection Decision Matrix

* **For free tier pooling**: Use **OmniRoute** to combine 90 or more free API tiers.
* **To reduce token spend on paid APIs**: Use **9router** to remove diff logs and compress prompt payloads before you call paid endpoints.
* **For multi-account profile rotation**: Use **claude-swap** for profile swapping without proxies, or use **CLIProxyAPI** for HTTP request retries.
* **For production infrastructure**: Use **LiteLLM** or **Manifest** for team virtual keys, OpenAI formatting, and audit logs.

---

## 3. Token Optimization & Prompt Compression

Token consumption increases latency and API costs. Large context windows send large repositories and verbose logs. Uncompressed context reduces model focus, increases latency, and exhausts rate limits.

You must optimize tokens in two ways: **Input Compression** (remove git noise, prune ASTs, and reduce prompts) and **Output Compression** (remove conversational filler, generate short responses, and avoid extra code).

---

### Token Compression & Optimization Tool Matrix

| Feature / Metric | RTK (Rust Token Killer) | Headroom | WOZCODE | Caveman Mode | Ponytail | SimpleEnglish | The Token Company (TTC) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Optimization Target** | **Input** (CLI / Diff logs) | **Input** (Tool outputs / AST) | **Input / Tooling** (Claude Code AST) | **Output** (Terse responses) | **Output** (Minimalist code) | **Output** (Simplified prose) | **Input** (Prompt payload) |
| **Primary Mechanism** | Terminal output interceptor | AST pruning & local cache | AST-aware tool substitution | System prompt injection | YAGNI decision ruleset | ASD-STE100 vocabulary | Neural model compression |
| **Token Reduction** | **60% – 90%** (CLI outputs) | **60% – 95%** (Data/AST) | **25% – 55%** (Claude Code tokens) | **60% – 75%** (Output tokens) | **~54%** (Generated code) | **15% – 30%** (Text output) | **40% – 66%** (Input prompt) |
| **Reversibility** | Lossy (Strips noise) | **Reversible** (CCR cache) | Lossless / Structural AST | N/A (Style constraint) | N/A (Code design) | N/A (Prose constraint) | Lossy / Semantic |
| **Delivery Format** | Rust binary CLI proxy | Local proxy / MCP / SDK | Claude Code Plugin (`WithWoz`) | Agent Skill / Ruleset | Agent Skill / `.cursorrules` | System prompt constraint | Cloud API Middleware / SDK |
| **Best For** | `git diff`, test suite output | Codebase context & RAG | Claude Code CLI sessions | Daily terminal chat | Feature implementation | Docstrings & explanations | Heavy prompt middleware |

---

### Input Prompt Compression & Context Reduction

* **[RTK (Rust Token Killer)](https://github.com/rtk-org/rtk)**: Rust CLI proxy that reads shell output (`git diff`, `git status`, `cargo test`, `pytest`, `npm test`) before the model receives it. It removes non-essential headers, git advice text, and passing test logs to reduce input tokens by up to 90%.
* **[Headroom](https://github.com/headroomlabs-ai/headroom)** ([headroom.ai](https://headroom.ai)): Open-source context optimization tool. It uses AST code compression (`CodeCompressor`), JSON object reduction (`SmartCrusher`), and neural log compression (`Kompress-base`). It includes **Content-Centric Retrieval (CCR)** so that the model can fetch full uncompressed data with the `headroom_retrieve` tool call.
* **[WOZCODE](https://www.wozcode.com/)** ([GitHub](https://github.com/WithWoz/wozcode-plugin)): Plugin for Claude Code CLI (`WithWoz/wozcode-plugin`). It runs locally and replaces default terminal file inspection tools with AST-aware tools (`woz:code`). It reduces token usage by 25% to 55%.
* **[The Token Company (TTC)](https://thetokencompany.com)** ([GitHub Python](https://github.com/the-token-company/the-token-company-python) | [GitHub Node](https://github.com/the-token-company/the-token-company-node)): Cloud middleware service. It uses neural networks (`bear-1` and `bear-1.2`) to compress up to 100,000 input tokens in under 100ms with 40% to 66% size reduction.

---

### Output Token Minimization & Anti-Bloat Techniques

* **[Caveman Mode](https://github.com/JuliusBrussee/caveman)**: Agent skill that reduces output tokens by 60% to 75%. It forces the LLM to remove conversational preambles and polite filler text. It supports intensity levels (`lite`, `full`, `ultra`).
* **[Ponytail](https://github.com/DietrichGebert/ponytail)**: Minimalist code generation ruleset. It prevents LLMs from over-engineering solutions. It forces the model to use standard libraries, native platform features, and existing codebase tools first.
* **[SimpleEnglish](https://github.com/AminBlg/SimpleEnglish)**: System prompting framework that enforces Simplified Technical English (**ASD-STE100**). It removes passive voice and complex verbosity to create short technical text and decrease output token costs.

---

### Input vs. Output Savings Breakdown

```
                            ┌──────────────────────────────────────────────┐
                            │    LLM Token Optimization Strategy           │
                            └──────────────────────┬───────────────────────┘
                                                   │
                 ┌─────────────────────────────────┴─────────────────────────────────┐
                 ▼                                                                   ▼
    INPUT CONTEXT COMPRESSION                                          OUTPUT TOKEN MINIMIZATION
  (Saves 60-90% of Input Tokens)                                     (Saves 50-75% of Output Tokens)
 ┌───────────────────────────────┐                                 ┌───────────────────────────────┐
 │ • RTK: CLI & Diff Filtering   │                                 │ • Caveman: No Conversational  │
 │ • Headroom: AST & CCR Caching │                                 │   Filler / Terse Responses    │
 │ • WOZCODE: Claude Code Plugin │                                 │ • Ponytail: YAGNI-First Code  │
 │ • TTC: Neural Prompt Pruning  │                                 │ • SimpleEnglish: ASD-STE100   │
 └───────────────────────────────┘                                 └───────────────────────────────┘
```

---

### Recommended Production Recipe

To get maximum cost efficiency during terminal agent coding, combine these layers:

1. **CLI Proxy Layer**: Intercept commands with **RTK** to remove `git diff` noise.
2. **Context Layer**: Send repository inspection requests through **Headroom** for AST compression with CCR fallback.
3. **Claude Code Plugin**: If you use Claude Code CLI sessions, install **WOZCODE** (`/plugin marketplace add WithWoz/wozcode-plugin`) to replace default file inspection with AST tools.
4. **Agent Persona**: Install **Caveman Mode** (`full` intensity) to remove conversational filler text.
5. **Code Generation Rules**: Enforce **Ponytail** in `.cursorrules` or `.clinerules` to prevent extra boilerplate code.

---

## 4. Codebase Intelligence, RAG & MCP Context Preservation

Large codebases exceed LLM context limits. AI agents need tools to find files, trace function signatures, and fetch correct documentation. Sending whole codebases wastes tokens and increases costs.

Cost-efficient projects use **Model Context Protocol (MCP)** servers, AST indexers, and local vector storage to send context to models on demand.

---

### Codebase Intelligence & RAG Tool Matrix

| Feature / Metric | Codebase Memory MCP | Context7 | Repomix | Aider Repo Map | LanceDB (Local) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Category** | Persistent Knowledge Graph | Up-to-date Docs RAG | Static Repository Packager | AST Symbol Call-Graph | Embedded Vector DB |
| **Delivery Format** | C Binary / MCP Server | MCP Server & CLI Skill | Node.js CLI (`npx repomix`) | Built-in CLI (Aider) | Native Library (Py/TS) |
| **Cost / License** | 100% Free (MIT) | Free Tier / Open-Source | 100% Free (MIT) | 100% Free (Apache 2.0) | 100% Free (Apache 2.0) |
| **Context Mechanism** | Tree-sitter + Hybrid LSP | Versioned Doc Fetching | Secretlint + AST Pruning | Tree-sitter + PageRank | Disk-vector (lance format) |
| **Token Reduction** | **Up to 99%** | High (Targeted snippets) | 40% – 60% with `--compress` | **85%+** vs full files | Precision retrieval |
| **Primary Focus** | Whole-repo call-graphs | External library docs | Prompt packing for chats | Inline symbol mapping | Custom local RAG |

---

### Deep Dive: Core Codebase Intelligence Engines

* **[Codebase Memory MCP](https://github.com/DeusData/codebase-memory-mcp)** ([codebase-memory-mcp.com](https://codebase-memory-mcp.com)): Knowledge graph indexer written as a C binary with zero external dependencies. It supports 158 languages with Tree-sitter parsing. It builds persistent AST call graphs and LSP type definitions to resolve symbol definitions and reduce token usage by up to 99%.
* **[Context7](https://github.com/upstash/context7)** ([context7.com](https://context7.com)): Model Context Protocol (MCP) server made by Upstash. It gives AI agents current documentation and code examples directly from source repositories. It prevents model errors when you use updated libraries.
* **[Repomix](https://github.com/yamadashy/repomix)** ([repomix.com](https://repomix.com)): Command-line tool (formerly Repopack) that combines repositories into a single file (XML, Markdown, or JSON). It includes `Secretlint` security checks to prevent API key leaks and uses Tree-sitter compression (`--compress`) to remove implementation details.
* **[Aider Repo Map](https://aider.chat/docs/repomap.html)** ([GitHub](https://github.com/Aider-AI/aider)): Graph-based repository mapping system. It uses Tree-sitter to parse source files and calculates PageRank over the call graph. It gives LLMs a 1,000-token map of class signatures and functions.
* **[LanceDB](https://github.com/lancedb/lancedb)** ([lancedb.com](https://lancedb.com)): Open-source embedded vector database written in Rust. It runs locally without external database daemons for local code embeddings and semantic search.

---

### Model Context Protocol (MCP) Architecture

The Model Context Protocol (MCP) connects AI agent hosts (such as Claude Code, Cursor, Windsurf, or OpenCode) to external context servers:

```
                          ┌──────────────────────────────────┐
                          │   AI Agent Host (Claude Code /   │
                          │     Cursor / Windsurf / etc.)    │
                          └─────────────────┬────────────────┘
                                            │
                                  MCP Protocol (JSON-RPC)
                                            │
           ┌────────────────────────────────┼────────────────────────────────┐
           ▼                                ▼                                ▼
┌─────────────────────┐          ┌─────────────────────┐          ┌─────────────────────┐
│ Codebase Memory MCP │          │    Context7 MCP     │          │ Local Filesystem    │
│  (C Binary Graph)   │          │ (Upstash Live Docs) │          │  (Read/Write Tools) │
└─────────────────────┘          └─────────────────────┘          └─────────────────────┘
```

---

### Practical MCP Setup Configuration

To enable persistent codebase intelligence and documentation retrieval in your agent setup, add the servers to your `mcpServers` configuration file (for example, `~/.mcp/config.json` or `.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "codebase-memory": {
      "command": "codebase-memory-mcp",
      "args": ["--workspace", "."]
    },
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

---

### Best Practices for Budget Context Preservation

1. **Do Not Send Whole Codebases**: Never paste raw codebases into system prompts. Use **Repomix** with `--compress` or use **Codebase Memory MCP** to send only necessary function signatures.
2. **Prevent Errors with Versioned Documentation**: When you add new dependencies, add `use context7` to your prompt. This fetches current library signatures instead of model memory.
3. **Store Local Embeddings at Zero Cost**: For offline projects, combine **LanceDB** with a local embedding model (for example, `nomic-embed-text` in Ollama) for local search.

---

## 5. Agent Harnesses, Skills & Quality Guardrails ("Fixing Vibe Coding")

Unchecked AI agents can produce unverified or fragile code. You must wrap agent execution loops in engineering guardrails: agent skills, static linters, duplicate code detectors, headless browser verification, and local telemetry.

---

### Quality Guardrail & Harness Tool Matrix

| Tool / Skill | Category | Primary Focus | Mechanism / Tech | Token & Quality Impact |
| :--- | :--- | :--- | :--- | :--- |
| **[Matt Pocock Skills](https://github.com/mattpocock/skills)** | Agent Skill Suite | Structured engineering workflows | `/grill-me`, `/wayfinder`, `/tdd`, `/triage` | Prevents premature execution; structures decisions before coding. |
| **[Fallow](https://github.com/fallow-rs/fallow)** | Static Analysis / MCP | TS/JS codebase intelligence & circular dependencies | Rust static analyzer + MCP server | Catches circular dependencies & structural decay before commits. |
| **[JSCPD](https://github.com/kucherenko/jscpd)** | Code Duplication | Copy/paste duplicate code detection | 223 language formats + AI token-efficient reporter | Prevents agent-generated code duplication across modules. |
| **[Knip](https://github.com/webpro-nl/knip)** | Dead Code Purge | Unused files, exports, and dependency cleanup | AST export graph analysis | Eliminates unreferenced code bloat & unused npm packages. |
| **[Sentry / Spotlight](https://spotlightjs.com)** | Local Telemetry | Real-time local dev error & trace debugging | Overlay UI + local SDK collector (`localhost:8969`) | Gives agents instant, structured stack traces without manual logging. |
| **[Chrome DevTools MCP](https://github.com/ChromeDevTools/devtools-mcp)** | Browser Verification | DOM inspection & visual UI debugging | Model Context Protocol over Chrome Puppeteer | Enables LLMs to inspect rendered UI, console errors, and network calls. |
| **[LightPanda](https://lightpanda.io)** | Headless Browser | Ultra-fast JS browser execution for AI | WebAssembly / Rust headless engine | 10x faster execution & 90% less memory than full Chromium. |
| **[Agent Browser](https://github.com/browserbase/agent-browser)** | Automation Harness | Headless web agent navigation & interaction | Playwright / Puppeteer abstraction | Automates visual testing and end-to-end user path validation. |

---

### Agent Harnesses & Composable Skills

* **[Matt Pocock Agent Skills](https://github.com/mattpocock/skills)**: Open-source engineering skills to direct AI agents:
  * `/grill-me`: Interactive interview skill to test architecture choices before you write code.
  * `/wayfinder`: Decision process that divides work into unblocked decision tickets.
  * `/tdd`: Test-Driven Development harness that enforces red-green-refactor cycles.
  * `/to-spec` & `/to-tickets`: Converts requirements into technical specifications and tickets.
* **[Fallow](https://github.com/fallow-rs/fallow)**: TypeScript and JavaScript static analysis engine written in Rust. It runs as a CLI tool and an MCP server. It finds circular dependencies and module boundary errors.
* **[JSCPD](https://github.com/kucherenko/jscpd)**: Code duplication detector for 223 file formats. It includes a token-efficient reporter that alerts agents to duplicate code blocks.
* **[Knip](https://github.com/webpro-nl/knip)** ([knip.dev](https://knip.dev)): Unused code finder for JavaScript and TypeScript projects. It scans ASTs to locate unreferenced files, unused exports, and dead dependencies.

---

### Static Linters, AST Guardrails & Runtime Telemetry

* **ESLint & Stylelint AI Guardrails**: Strict linter configurations that filter agent output. Enforce strict types, zero `any` usage, unused variable checks, and automatic code formatting before commits.
* **[Sentry Spotlight](https://spotlightjs.com)** ([GitHub](https://github.com/getsentry/spotlight)): Desktop toolbar for Sentry. It captures exceptions, console errors, database queries, and traces at `localhost:8969`. It lets agents inspect structured error tracebacks locally.
* **[Vite+](https://vitejs.dev)**: Application builder and hot-module replacement environment. It provides instant validation for web app components created by AI agents.

---

### Headless Browser Execution & Visual Verification

To verify UI layout success, combine agent harnesses with headless browser control:

* **[Chrome DevTools MCP](https://github.com/ChromeDevTools/devtools-mcp)**: MCP server that connects models to Chrome DevTools. Agents can inspect the DOM tree, trigger click events, check CSS styles, read console errors, and capture screenshots.
* **[LightPanda](https://lightpanda.io)**: Headless browser written in WebAssembly and Rust for AI agents. It uses 90% less memory and runs 10 times faster than full Chromium instances.
* **[Agent Browser](https://github.com/browserbase/agent-browser)**: Browser automation framework that gives agents API primitives for page navigation, visual tests, and form validation.

---

### The 8 Tech Choices Before "Agentmaxxing"

Before you run agents on a codebase, set up these 8 guardrails:

1. **Strict Type System**: Enforce TypeScript `strict: true`, Rust strict typing, or Python type hints. Do not allow implicit `any`.
2. **Automated Static Analysis**: Run linters (ESLint, Biome, or Ruff) as git hooks or pre-commit steps.
3. **Delete Dead Code and Duplication**: Add **Knip** and **JSCPD** to CI pipelines to block duplicate code and unreferenced exports.
4. **Test-Driven Development (TDD)**: Force agents to write failing unit tests before they generate feature code.
5. **Modular Seam Architecture**: Keep modules small and single-purpose to avoid complex code and large context sizes.
6. **Headless Visual Verification**: Use **Chrome DevTools MCP** or **LightPanda** to make sure that rendered web UI components display correctly before you complete the task.
7. **Local Telemetry & Structured Logging**: Connect **Sentry Spotlight** locally so agents read JSON stack traces instead of guessing runtime errors.
8. **Structured Skill Harnesses**: Standardize agent workflows with **Matt Pocock Skills** (`/wayfinder`, `/tdd`, `/grill-me`) to plan decisions before execution.

---

## 6. Local Runtimes & Self-Hosted Inference

You can run AI coding workflows on local hardware or self-hosted servers. Local runtimes give total data privacy, zero API costs, and offline operation.

---

### Local Runtime & Self-Hosted Inference Matrix

| Feature / Tool | Ollama | Hermes (Nous Research) | OpenCode Go | open-design.ai | vLLM / llama.cpp |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Category** | Local LLM Server | Open Agent Model Family | Lightweight Agent CLI | AI Design & UI Engine | Inference Backend Engine |
| **Language / Core** | Go & C++ (llama.cpp) | PyTorch / GGUF Weights | Go | TypeScript & Web UI | Python / C++ CUDA |
| **Cost / License** | 100% Free (MIT) | Free Open Weights | 100% Free (MIT) | Free Open-Source | 100% Free (Apache 2.0) |
| **VRAM / Hardware** | 4GB – 48GB VRAM | VRAM Dependent (8B-70B) | Minimal CPU (<20MB RAM) | Light Local Server | GPU VRAM Heavy |
| **Primary Focus** | Standardized local LLM API | Structured tool & function calling | Sub-second CLI agent runner | Local UI design to code | High-throughput batch server |

---

### Deep Dive: Core Local & Self-Hosted Engine Suite

* **[Ollama](https://github.com/ollama/ollama)** ([ollama.com](https://ollama.com)): Local runtime to run open-weights LLMs on macOS, Linux, and Windows. It gives an OpenAI-compatible API endpoint (`http://localhost:11434/v1`), automatic GPU offloading (Metal, CUDA, ROCm), GGUF quantization, and custom `Modelfile` configurations for system prompts and context limits (`num_ctx 32768`).

```
┌──────────────────────────────────────────────────────────────────┐
│                       Ollama Runtime                             │
│  ┌────────────────────────────────────────────────────────────┐  │
│  │  Open-Weights / GGUF Quantized Models                      │  │
│  │  - Native Function Calling & XML Tool Invocations          │  │
│  │  - Metal / CUDA GPU VRAM Offloading                        │  │
│  └────────────────────────────────────────────────────────────┘  │
└──────────────────────────────────────────────────────────────────┘
```

---

### Quantization & Hardware Sizing Reference

| Model Class & Parameter Count | Recommended Quantization | VRAM Required | Target Hardware | Primary Engineering Use Case |
| :--- | :--- | :--- | :--- | :--- |
| **7B–8B Parameters** | Q4_K_M / Q8_0 | 6GB – 10GB | Apple M1/M2/M3 (8GB+) / RTX 3060/4060 | Real-time inline autocomplete, fast TDD loops |
| **14B–32B Parameters** | Q4_K_M | 16GB – 24GB | Apple Mac Studio / RTX 3090/4090 | Full file generation, function calling, routine refactoring |
| **70B Parameters** | Q4_K_M / IQ3_XS | 40GB – 48GB | Dual RTX 3090/4090 / Mac Studio 64GB+ | Complex multi-file reasoning, deep architectural design |

---

### Best Practices for Local & Self-Hosted AI Coding

1. **Optimize Context Windows (`num_ctx`)**: Ollama sets a 2,048-token context window by default. In your `Modelfile` or API requests, set `num_ctx 32768` (or the limit of your model) to process long code context.
2. **Combine Function-Calling Models with Local Agents**: Set open-source function-calling models as the default backend for tools such as `OpenCode Go`. This gives reliable tool calls without cloud API costs.
3. **Generate UI with open-design.ai**: Do not send prompts to expensive cloud vision models. Run **open-design.ai** locally to convert wireframes into React or Tailwind code.
4. **Use OpenAI Compatibility Layer**: Run local servers with the `--api` flag or the Ollama `/v1` endpoint. This lets existing agent hosts connect to local servers without code changes.

---

## 7. Pricing Intelligence, Deals & Grey Market Awareness

To decrease spend, use provider discounts, startup grants, and regional purchasing power parity (PPP) adjustments. Avoid high-risk grey market options.

---

### Pricing Intelligence & Grant Matrix

| Category | Primary Platforms & Tools | Cost Efficiency / Discount Rate | Key Value & Utility | Risk Profile |
| :--- | :--- | :--- | :--- | :--- |
| **PPP & Geo Intelligence** | OpenTheRank, Country-Specific API Pricing | Up to 50–70% PPP Discounts | Regional pricing parity tracking and legitimate local purchasing power adjustments | Zero Risk (Vendor Sanctioned) |
| **Batch API Processing** | OpenAI Batch API, Anthropic Message Batches, Gemini Batch API | 50% Flat Discount (vs Real-time API) | Asynchronous bulk code refactoring, test suite generation, and doc building within 24h SLA | Zero Risk (Official API Specs) |
| **OSS & Startup Grants** | Microsoft Founders Hub, AWS Activate, Google for Startups, OpenAI OSS Grants | $1,000 – $150,000 Free Credits | Direct cloud and LLM API credits for open-source maintainers and early-stage startups | Zero Risk (Official Developer Grants) |
| **Price Aggregators** | Artificial Analysis, Models.dev, OpenRouter | Real-Time Live Comparison | Live latency vs cost benchmarking per million tokens across 50+ providers | Zero Risk (Analytical Engine) |
| **Grey Market / Key Resellers** | Shared Key Proxies, Carded Accounts, Unauthorized Aggregators | 80–90% Suspiciously Cheap | **DO NOT USE**: High risk of token theft, code leakage, MITM logging, and permanent account bans | **EXTREME RISK** (TOS Violation & Data Breach) |

---

### Deep Dive: Pricing Intelligence, Grants & Risk Safeguards

* **[OpenTheRank](https://opentherank.com)**: Purchasing Power Parity (PPP) tracking for SaaS and API platforms. It helps developers evaluate regional pricing and discount structures across global API providers.
* **[Artificial Analysis](https://artificialanalysis.ai)** ([artificialanalysis.ai/models](https://artificialanalysis.ai/models)): Price intelligence platform that tracks API pricing (cost per 1 million input or output tokens), latency (TTFT), and throughput across major LLM hosts.
* **Batch APIs (OpenAI, Anthropic, Google Gemini)**:
  * **[OpenAI Batch API](https://platform.openai.com/docs/guides/batch)**: 50% discount on tokens for asynchronous jobs completed within 24 hours. Use this for codebase indexing, refactoring, and test generation.
  * **[Anthropic Message Batches](https://docs.anthropic.com/en/docs/build-with-claude/batch-processing)**: 50% discount on Claude models for asynchronous jobs with 24-hour completion windows.
  * **[Google Gemini Batch API](https://ai.google.dev/gemini-api/docs/batch)**: 50% token cost reduction for batch processing with large context windows.
* **OSS Maintainer & Startup Grant Programs**:
  * **[Microsoft for Startups Founders Hub](https://founders.startups.microsoft.com)**: Gives up to $150,000 in Azure credits for Azure OpenAI Service and cloud model deployments.
  * **[AWS Activate & Google Cloud for Startups](https://aws.amazon.com/activate/)**: Gives $1,000 to $100,000 in cloud credits for Bedrock and Vertex AI endpoints.
  * **GitHub & Open Source AI Grants**: Grants for open-source maintainers through GitHub Sponsors, Hugging Face Community Grants, and AI research grants.
* **Grey Market Safety & Security Warning (Reseller Proxies & Transfer Stations)**:
  * **Threat Intelligence & Security Research**:
    * **[Sysdig Research: LLMjacking & Stolen Credentials](https://sysdig.com/blog/llmjacking-stolen-cloud-credentials-tokencaching/)**: Security analysis of unauthorized proxy stations, stolen API keys, and carded accounts.
    * **[OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)** (**LLM07: System Information Disclosure** & **LLM10: Unchecked Resource Consumption**): Vulnerability standards that map the risks of unvetted middleman proxies.
    * **[OpenAI Terms of Use](https://openai.com/policies/terms-of-use)** & **[Anthropic Commercial Terms of Service](https://www.anthropic.com/legal/commercial-terms)**: Terms of Service policies that prohibit API credential resale and unauthorized account sharing.
  * **Common Marketplaces for Digital Goods (Grey-Market Risk Exposure)**:
    These are third-party marketplaces where digital goods (including grey-market accounts and credentials) are traded:
    * [g2g.com](https://www.g2g.com/)  
    * [Eldorado.gg](https://www.eldorado.gg/)  
    * [Z2U](https://www.z2u.com/)  
    * [PlayerAuctions](https://www.playerauctions.com/)  
    * [EpicNPC](https://www.epicnpc.com/)  
    * [iGV](https://www.igv.com/)  
    * [Gameflip](https://gameflip.com/)  
    * [G2A](https://www.g2a.com/)  
    * [Kinguin](https://www.kinguin.net/)
  * **MITM Telemetry & Code Exposure**: CAUTION: Do not send code through third-party key resellers or transfer stations. Untrusted middleman servers route your prompts and can log your private code, API keys, and sensitive tokens.
  * **Account Termination & IP Blacklisting**: Do not use carded accounts, shared subscription tokens, or reseller proxies. These violate provider Terms of Service (ToS) and cause account bans and loss of API access.
  * **Stolen Financials & Carding Rings**: Grey market sellers use stolen credit cards to create API keys. If chargebacks occur, provider accounts stop working immediately.

---

### Economic Decision Architecture

```
                               ┌────────────────────────────────────────┐
                               │   AI Developer Budget Strategy         │
                               └──────────────────┬─────────────────────┘
                                                  │
                       ┌──────────────────────────┴──────────────────────────┐
                       ▼                                                     ▼
        ┌─────────────────────────────┐                       ┌─────────────────────────────┐
        │   LEGITIMATE OPTIMIZATION   │                       │    GREY MARKET RESELLERS    │
        │    (Zero Security Risk)     │                       │    (EXTREME RISK / HAZARD)  │
        └──────────────┬──────────────┘                       └──────────────┬──────────────┘
                       │                                                     │
       ┌───────────────┼───────────────┐                     ┌───────────────┼───────────────┐
       ▼               ▼               ▼                     ▼               ▼               ▼
┌──────────────┐┌──────────────┐┌──────────────┐     ┌──────────────┐┌──────────────┐┌──────────────┐
│  Batch APIs  ││  OSS Grants  ││ OpenTheRank  │     │ MITM Logging ││ Account Bans ││ Stolen Cards │
│  (50% Off)   ││ ($1k–$150k)  ││ PPP Analysis │     │ Data Breach  ││ TOS Violate  ││ Infrastructure│
└──────────────┘└──────────────┘└──────────────┘     └──────────────┘└──────────────┘└──────────────┘
```

---

### Official Deal & Grant Qualification Matrix

| Resource / Tier | Qualification Criteria | Average Value | Best Applied To |
| :--- | :--- | :--- | :--- |
| **Batch API Tier** | Any developer running async jobs (<24h SLA) | 50% Token Discount | Large codebases, batch docs, test generation |
| **OSS Maintainer Grants** | Open source maintainer with active public repo | $1,000 – $10,000 credits | CI/CD testing, automated PR review bots |
| **Startup Accelerator Credits** | Early-stage startup (Incorporated, <5 yrs) | $25,000 – $150,000 credits | Scaling multi-tenant AI coding features |
| **PPP Regional Pricing** | Developer residing in eligible PPP regions | 30% – 60% software discount | Solopreneurs and regional engineering teams |

---

## Contributing & Community

Contributions are welcome! If you know of high-quality tools, proxies, local runtimes, or token-compression libraries that belong in this guide:

1. Fork the repository.
2. Ensure any proposed tools have zero-fluff empirical value and clean security records.
3. Submit a Pull Request following standard GitHub Flavored Markdown guidelines.

---

## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.
