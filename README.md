# Nurzhan Kalmurat

Python backend developer. I build LLM-powered services that talk to real customers — tool-calling agents, a voice ordering agent, data pipelines — and I put the work into the parts that keep them safe: deterministic pricing, idempotent writes, output guards, tests.

Full Stack Developer at [Qorsa](https://qorsa.ru) (web studio) for 1+ year · Software Engineering student at KBTU (3rd year, graduating 2028) · Almaty, Kazakhstan

## Selected work

**[llm-sales-agent](https://github.com/nurzhan2/llm-sales-agent)** — LLM agent that answers Avito buyers for a leisure complex: exact prices from a pricing engine, live availability from YCLIENTS, hand-off to a manager. In production since Aug 2026: 467 customer chats, median first reply 21 s versus 31 min for the human managers, output guards stopped 53 of 769 model replies before they were sent; 1,658 tests.
`FastAPI` `PostgreSQL` `Redis` `DeepSeek`

**[voice-ordering-agent](https://github.com/nurzhan2/voice-ordering-agent)** — Phone agent that takes food delivery orders in Russian and puts them on a kitchen board. Piloted in Aug 2026; I traced one-way audio to asymmetric RTP through NAT with a packet capture and fixed it.
`LiveKit Agents` `FastAPI` `PostgreSQL` `Redis`

**[who-wants-an-offer](https://github.com/nurzhan2/who-wants-an-offer)** — CV-driven job search: crawls hh.kz within `robots.txt`, ranks vacancies with local embeddings, writes a letter per vacancy, applies only after a person confirms. ~3,000 tests, `mypy --strict`, 94% coverage.
`FastAPI` `PostgreSQL + pgvector` `React` `Playwright`

**[b2b-lead-pipeline](https://github.com/nurzhan2/b2b-lead-pipeline)** — Python workers collect companies from public sources; a Java core deduplicates and scores them, and hot leads go to amoCRM so that reruns don't create duplicate deals. 820 tests, including PostgreSQL integration tests via Testcontainers.
`Java 21 / Spring Boot` `Python asyncio` `PostgreSQL`

**[TacticalMedicine](https://github.com/nurzhan2/TacticalMedicine)** — VR trainer for combat first aid on Meta Quest 3S: 8 scenarios where you stop bleeding, seal a chest wound and drag a casualty with your own hands, then get a scored debrief. Presented at the Satbayev University open day.
`Unity 6` `C#` `OpenXR` `Meta XR SDK`

Client work that is not on GitHub: automated reporting for a district heating operator (metering API + 1C, boiler efficiency for 56 sites, 94 tests), and a Telegram AI assistant whose model cost per reply I cut 2.07x in an 8-day pilot by moving it to a self-hosted gateway.

## How I build

- **The model never decides money or facts.** Prices, menu items and free slots come from code and the database; the LLM has to call a tool, and a guard checks the answer before it goes out.
- **One door for every outbound message.** Kill switch, daily limits and human takeover live in one place, not in the prompt.
- **Numbers come with a date and a method.** If I haven't measured it, it's not in the README.

## Stack

Python · FastAPI · SQLAlchemy (async) · PostgreSQL / pgvector · Redis · Docker · pytest · GitHub Actions · LLM tool calling (DeepSeek, OpenAI) · LiveKit · Java 21 / Spring Boot · React

## Beyond code

- ICPC 2026, first participation: 63rd of 173 teams at the quarterfinal stage.
- Freestyle wrestling for 2.5 years without a missed session; swimming from age 12 to 17.

## Contact

Open to Python backend, LLM and ML roles and internships, in Almaty or remote. English B2, Russian, Kazakh.
[LinkedIn](https://www.linkedin.com/in/kalmuratnurzhan/) · kalmuratnurzhan@gmail.com
