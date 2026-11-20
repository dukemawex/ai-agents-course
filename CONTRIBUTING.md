# Contributing to the AI Agents Course

Thank you for helping. Every fix, clearer sentence and new exercise makes the course better for the next learner.

## Where to contribute

| You want to... | Go to |
| --- | --- |
| Fix or improve a lesson | The level repo: [beginner](https://github.com/dukemawex/ai-agents-beginner), [intermediate](https://github.com/dukemawex/ai-agents-intermediate) or [advanced](https://github.com/dukemawex/ai-agents-advanced) |
| Change the learning path, syllabus or these guides | This hub repo |
| Ask a question or report a bug | An issue in the repo where it happened, using a template |

## Ground rules for lessons

1. **Plain, warm English.** Short sentences. Explain every new term the first time it appears. Avoid jargon where a simple word works. Do not use em-dashes.
2. **Every module has the same shape:** `README.md` (objectives, concepts in plain English, step by step, exercises, checkpoint quiz with answers, further reading), `starter/`, `solution/` and `tests/`.
3. **Provider-agnostic code.** Use the OpenAI-compatible client with `LLM_BASE_URL`, `LLM_API_KEY` and `LLM_MODEL` from the environment. Examples must work with a free option such as Ollama or a free tier.
4. **Offline tests only.** Tests use `FakeLLM` from `course_testing.py` (or `httpx.MockTransport` for SDKs that make their own HTTP calls). CI must never need an API key.
5. **Verify APIs against official docs.** Library APIs change quickly. When you use a library feature, check it against the current official documentation, and link that documentation in "Further reading".
6. **Real links only.** Link to official docs, standards and well-known primary sources. Check that every link opens.
7. **No secrets, ever.** Never commit keys, tokens or `.env` files. Use obvious placeholders in examples.
8. **Be honest about limits.** Especially for safety topics, say what a technique does not protect against.

## Workflow

1. Fork the repo and create a branch: `git checkout -b fix/module-05-typo`.
2. Make your change. Keep starter and solution in sync with the README.
3. Run the checks:
   ```bash
   pip install -r requirements.txt -r requirements-dev.txt
   ruff check .
   ruff format --check .
   pytest
   ```
4. Open a pull request, fill in the template, and link any related issue.

A maintainer will review it. We may ask for changes; that is normal and not a judgement of you.

## Adding a new module

Open an issue first with the module's objectives and where it fits in the path, so we can agree on scope before you write it. Then copy an existing module folder as a template.
