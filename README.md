# AI Agents Course by Dukers Ltd

[![Docs check](https://github.com/dukemawex/ai-agents-course/actions/workflows/docs.yml/badge.svg)](https://github.com/dukemawex/ai-agents-course/actions/workflows/docs.yml)

A free, hands-on course that teaches you to set up, build, test, secure and deploy AI agents, from your very first model call to production systems. It is made by **Dukers Ltd** and is open to everyone.

**Start here.** This repository is the hub: it explains the learning path and links to the three level repositories, where all the lessons and code live.

## What you will learn

An **AI agent** is a program where a language model decides what to do next, uses tools to act, and repeats until a job is done. This course teaches you to build them well:

- how agents work, with no magic: the model, the tools and the loop;
- how to call models from any provider, including free ones;
- tools, memory, retrieval over your own documents, and MCP servers;
- structured outputs, evals, retries and APIs;
- multi-agent systems, durable workflows, tracing, cost control and deployment;
- safety and security throughout: API key hygiene, prompt-injection defence, tool sandboxing and red-teaming.

## Learning path

```
  Beginner (8 modules)  -->  Intermediate (8 modules)  -->  Advanced (9 modules, incl. capstone)
  about 8 hours              about 10 hours                 about 16 hours + capstone
```

| Level | Repository | You will be able to | Before you start |
| --- | --- | --- | --- |
| Beginner | [ai-agents-beginner](https://github.com/dukemawex/ai-agents-beginner) | Build a tool-calling agent with memory, good prompts and safety basics | A little Python and a terminal |
| Intermediate | [ai-agents-intermediate](https://github.com/dukemawex/ai-agents-intermediate) | Build multi-tool, retrieval and MCP agents, evaluate them and serve them as an API | Beginner level or equivalent |
| Advanced | [ai-agents-advanced](https://github.com/dukemawex/ai-agents-advanced) | Ship observable, secure, cost-aware agent systems and prove their quality | Intermediate level or equivalent |

Already experienced? Skim the module list below and jump in where it gets new for you. Each module says what it builds on.

## Syllabus

| Level | # | Module | Key ideas |
| --- | --- | --- | --- |
| Beginner | 01 | What is an AI agent? | Model, tools, loop, step limits |
| Beginner | 02 | Set up Python and pick a provider | venv, OpenAI-compatible APIs, Ollama and Groq |
| Beginner | 03 | Keep API keys safe | .env, .gitignore, masking, leak scanning |
| Beginner | 04 | Your first chat call | Messages, roles, statelessness, tokens |
| Beginner | 05 | Your first tool-calling agent | Tool schemas, tool calls, safe maths, the agent loop |
| Beginner | 06 | Simple memory | Sliding windows, long-term notes |
| Beginner | 07 | Prompt basics for agents | Role, task, rules, format; few-shot; defensive parsing |
| Beginner | 08 | Safety basics | Least privilege, confirmations, redaction, injection awareness |
| Intermediate | 01 | Multi-tool agents | Tool registries, schemas from type hints, parallel calls |
| Intermediate | 02 | Structured outputs | JSON mode, strict schemas, Pydantic, repair loops |
| Intermediate | 03 | RAG with a local vector store | Chunking, embeddings, cosine similarity, citations |
| Intermediate | 04 | MCP servers | Build an MCP server, connect agents and hosts to it |
| Intermediate | 05 | Agent frameworks | OpenAI Agents SDK, handoffs, choosing a framework |
| Intermediate | 06 | Evaluation basics | Cases, graders, pass rates |
| Intermediate | 07 | Error handling and retries | Retryable errors, backoff, jitter, fallback |
| Intermediate | 08 | Deploy an agent as an API | FastAPI, validation, auth, sessions |
| Advanced | 01 | Multi-agent orchestration | Manager and specialists, plan validation, review loops |
| Advanced | 02 | Durable, long-running workflows | Checkpoints, resume, idempotency, human approval |
| Advanced | 03 | Observability and tracing | OpenTelemetry, GenAI semantic conventions |
| Advanced | 04 | Advanced evals and red-teaming | LLM judges, canary tokens, attack success rate, CI gates |
| Advanced | 05 | Guardrails and prompt-injection defence | Spotlighting, taint tracking, tool gating, output checks |
| Advanced | 06 | Cost and latency optimisation | Caching, routing, cascades, budgets |
| Advanced | 07 | Production deploy | Health checks, JSON logs, rate limits, Docker, CI |
| Advanced | 08 | Security of tool use | Path traversal, command injection, SSRF, audit logs |
| Advanced | 09 | Capstone project | Build, evaluate and ship a real agent |

## Prerequisites and setup

- **Python 3.11 or newer** and a terminal. Each level repo has a one-page quick start.
- **A model provider.** You do not need to pay. Every lesson uses the OpenAI-compatible API, so the same code works with:
  - [Ollama](https://ollama.com), free and local (recommended to start);
  - [Groq](https://console.groq.com), a free tier in the cloud;
  - [OpenRouter](https://openrouter.ai) or [OpenAI](https://platform.openai.com), if you prefer.
- **Git and a GitHub account** to clone the repos and, later, to share your capstone.
- **Docker** (optional) for the advanced deployment module.

## How to use the level repositories

1. Clone the level you are on, for example:
   ```bash
   git clone https://github.com/dukemawex/ai-agents-beginner.git
   ```
2. Follow its quick start: create a virtual environment, install requirements, copy `.env.example` to `.env`.
3. Work through `modules/` in order. Each module has a README (concepts, steps, exercises, a short quiz and further reading), a `starter/` folder for you, a `solution/` folder, and offline tests.
4. Check your work with `TARGET=starter pytest modules/<module>`. The tests use a scripted fake model, so they are free and need no key.
5. Stuck? Read the solution, then close it and try again. Still stuck? Open a "Question or stuck" issue in that repo.

**Learning in a group or teaching a class?** Each module fits one session: concepts and demo (20 minutes), starter exercise (30 to 60 minutes), quiz and discussion (10 minutes). The capstone works well as a team project with a demo day.

## Principles of this course

- **Understand first, then use frameworks.** You build the loop by hand before using a framework, so nothing feels like magic.
- **Free to learn.** Everything runs on free providers, and all tests run offline.
- **Safety is not an extra.** Every level includes security and safety, because agents take actions in the real world.
- **Honest about limits.** No defence here makes an agent perfectly safe. We say what each technique does and does not do.
- **Current and verified.** Library usage is checked against official docs. APIs change fast, so if something breaks, please open an issue.

## Contributing

Contributions are very welcome: fixes, clearer explanations, new exercises, translations and new modules. Read the [contribution guide](CONTRIBUTING.md) and our [code of conduct](CODE_OF_CONDUCT.md).

## License

[MIT](LICENSE), copyright Dukers Ltd. You may use, adapt and share the material, including for teaching, as long as you keep the copyright and license notice. Third-party tools, libraries and services mentioned in the course have their own licenses and terms.
