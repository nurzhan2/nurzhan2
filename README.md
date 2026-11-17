# Nurzhan Kalmurat

Python backend developer. I build LLM-powered services that talk to real customers — tool-calling agents, a voice ordering agent, data pipelines — and I put the work into the parts that keep them safe: deterministic pricing, idempotent writes, output guards, tests.

1 year as a Full Stack Developer at [Qorsa](https://qorsa.ru) (web studio) · Student at KBTU · Almaty, Kazakhstan

## Selected work

**[llm-sales-agent](https://github.com/nurzhan2/llm-sales-agent)** — LLM agent that answers Avito buyers for a leisure complex: exact prices from a pricing engine, live availability from YCLIENTS, hand-off to a manager. In production; in 20–30 Oct 2026 its output guards corrected or withheld 11 of 113 replies before they were sent.
`FastAPI` `PostgreSQL` `Redis` `DeepSeek`

**[voice-ordering-agent](https://github.com/nurzhan2/voice-ordering-agent)** — Phone agent that takes food delivery orders in Russian and puts them on a kitchen board. Piloted in Aug 2026; I traced one-way audio to asymmetric RTP through NAT with a packet capture and fixed it.
`LiveKit Agents` `FastAPI` `PostgreSQL` `Redis`

**[who-wants-an-offer](https://github.com/nurzhan2/who-wants-an-offer)** — CV-driven job search: crawls hh.kz within `robots.txt`, ranks vacancies with local embeddings, writes a letter per vacancy, applies only after a person confirms. ~3,000 tests, `mypy --strict`, 94% coverage.
`FastAPI` `PostgreSQL + pgvector` `React` `Playwright`

**[b2b-lead-pipeline](https://github.com/nurzhan2/b2b-lead-pipeline)** — Python workers collect companies from public sources; a Java core deduplicates and scores them, and hot leads go to amoCRM so that reruns don't create duplicate deals. Integration tests on PostgreSQL via Testcontainers.
`Java 21 / Spring Boot` `Python asyncio` `PostgreSQL`

## How I build

- **The model never decides money or facts.** Prices, menu items and free slots come from code and the database; the LLM has to call a tool, and a guard checks the answer before it goes out.
- **One door for every outbound message.** Kill switch, daily limits and human takeover live in one place, not in the prompt.
- **Numbers come with a date and a method.** If I haven't measured it, it's not in the README.

## Stack

Python · FastAPI · SQLAlchemy (async) · PostgreSQL / pgvector · Redis · Docker · pytest · GitHub Actions · LLM tool calling (DeepSeek, OpenAI) · LiveKit · Java 21 / Spring Boot · React

## Contact

Open to Python backend roles (LLM integrations) in Almaty or remote — [LinkedIn](https://www.linkedin.com/in/kalmuratnurzhan/)
