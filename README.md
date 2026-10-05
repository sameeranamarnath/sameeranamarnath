<h1 align="center">Amar S</h1>
<h3 align="center">Full-stack / cloud / AI engineer &amp; architect - 16 years building systems that have to stay up</h3>

I design and build distributed systems - mostly event-driven, mostly on AWS or
Azure, and increasingly with LLMs in the loop. Sixteen years in, that has meant AR
and IoT, embedded firmware and Android, microservices at scale, and the CI/CD and
infrastructure-as-code that keeps it honest. I also train teams, which is where a
number of the repos below came from.

Most of what is below is GenAI work that behaves like production software: evals
that gate pull requests, guardrails that fail closed, tracing, per-request cost
accounting, and decision records explaining the trade-offs.

### What I do

| Area | Depth |
| --- | --- |
| **GenAI / LLM engineering** | LangGraph agent orchestration, RAG over Qdrant, self-hosted inference with vLLM, evals (golden datasets, deterministic scorers, LLM-as-judge, calibration), guardrails and PII redaction, token and cost metering, OpenTelemetry GenAI tracing |
| **Full-stack** | TypeScript / React / Next.js, Python (FastAPI, Django, Flask), Node.js, Go, PostgreSQL, MongoDB, Redis, REST and GraphQL, Socket.io and WebSockets |
| **Cloud and platform** | AWS (Lambda, API Gateway, DynamoDB, SQS, ECS), Azure (OpenAI, Container Apps), Terraform, Docker, Kubernetes, Skaffold, CI/CD |
| **Earlier depth** | Embedded C++ firmware, Android, TensorFlow, AR and IoT |

### How I build

Do more with less. Boring, debuggable infrastructure over clever abstractions, and
the failure path treated as a first-class design concern. Every claim in the repos
below is something you can clone and run.

---

## Featured projects

### Real-time and distributed systems

| Repo | What it is |
| --- | --- |
| [fleet-telemetry-web](https://github.com/sameeranamarnath/fleet-telemetry-web) / [fleet-telemetry-api](https://github.com/sameeranamarnath/fleet-telemetry-api) / [fleet-telemetry-infra](https://github.com/sameeranamarnath/fleet-telemetry-infra) | Real-time fleet tracking - Next.js map and dashboard, API Gateway WebSockets, Lambda handlers, DynamoDB, Terraform VPC |
| [realtime-ecommerce-stack](https://github.com/sameeranamarnath/realtime-ecommerce-stack) | Microservices e-commerce on Kubernetes with Skaffold - Node/TypeScript services, Mongo, event-bus communication |
| [real-estate-microservices](https://github.com/sameeranamarnath/real-estate-microservices) | Event-driven property marketplace - Django and Flask services over RabbitMQ, React front end |
| [social-chat-api](https://github.com/sameeranamarnath/social-chat-api) | Creator chat backend - live rooms, screenshare signalling, DMs, friend invites; Express + Socket.io, Postgres, Redis, GraphQL, AWS |

### AI / LLM

| Repo | What it is |
| --- | --- |
| [youtube-transcript-summarizer](https://github.com/sameeranamarnath/youtube-transcript-summarizer) | Ask questions about a YouTube video, answered only from its transcript - LangChain + HNSWLib retrieval on Next.js |
| [natural-text-to-sql](https://github.com/sameeranamarnath/natural-text-to-sql) | Plain English to SQL against any database, with a Streamlit UI - LangChain + GPT-3.5/4 |
| [cryptowhiz](https://github.com/sameeranamarnath/cryptowhiz) | Crypto momentum screener - market data in, charts and an LLM read on each candidate out |
| [multimodal-pdf-rag](https://github.com/sameeranamarnath/multimodal-pdf-rag) | Multimodal PDF RAG - text, tables and images into pgvector via Azure OpenAI, served as FastAPI, Streamlit and an MCP server |

### Freight and logistics

| Repo | What it is |
| --- | --- |
| [eld-trip-planner](https://github.com/sameeranamarnath/eld-trip-planner) / [eld-trip-planner-v2](https://github.com/sameeranamarnath/eld-trip-planner-v2) | FMCSA hours-of-service trip planner - an HOS simulator, a filled log sheet for every calendar day, a turn-by-turn route and PDF export (Django + React + Leaflet) |
| [fuel-stop-planner](https://github.com/sameeranamarnath/fuel-stop-planner) | Cost-optimal fuel-stop planning for a 500-mile / 10 MPG truck on any US route, with station matching against the driving corridor (Django REST + React) |

### Earlier work

| Repo | What it is |
| --- | --- |
| [real-estate-price-model](https://github.com/sameeranamarnath/real-estate-price-model) | TensorFlow service predicting property appreciation/depreciation - fetch, train and serve pipeline (~80% accuracy) |
| [ring-scanner-android](https://github.com/sameeranamarnath/ring-scanner-android) | Android app driving a custom C++-firmware ring scanner over Bluetooth (2019) |
| [production-architecture-samples](https://github.com/sameeranamarnath/production-architecture-samples) | Reference architecture diagrams from production assignments |

---

---

## Engineering practice

The repos below are not demos. What that means concretely:

| Practice | Evidence |
| --- | --- |
| Tests that need no model, database or network | 87 unit tests in [natural-text-to-sql](https://github.com/sameeranamarnath/natural-text-to-sql), 69 in each of the other agent services - they run in under a second |
| Evals as a release gate | golden datasets and deterministic scorers in `ai/evals/`, run on every pull request |
| Decisions written down, not implied | [ADRs](https://github.com/sameeranamarnath/natural-text-to-sql/tree/master/docs/adr) for choices that are not self-evident |
| CI that is fast and green | lint, format, type check and tests on every PR; the safety modules are standard-library only, so the gate finishes in seconds |
| Security posture stated | a threat model in each `SECURITY.md`, guardrails in `ai/guardrails.py` |
| Cost as a first-class signal | per-request token and spend reporting with an optional budget ceiling |

<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://aws.amazon.com/amplify/" target="_blank" rel="noreferrer"> <img src="https://docs.amplify.aws/assets/logo-dark.svg" alt="amplify" width="40" height="40"/> </a> <a href="https://aws.amazon.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" alt="aws" width="40" height="40"/> </a> <a href="https://azure.microsoft.com/en-in/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/microsoft_azure/microsoft_azure-icon.svg" alt="azure" width="40" height="40"/> </a> <a href="https://getbootstrap.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" alt="bootstrap" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.cypress.io" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/simple-icons/simple-icons/6e46ec1fc23b60c8fd0d2f2ff46db82e16dbd75f/icons/cypress.svg" alt="cypress" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> </a> <a href="https://cloud.google.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" alt="gcp" width="40" height="40"/> </a> <a href="https://golang.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" alt="go" width="40" height="40"/> </a> <a href="https://heroku.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/heroku/heroku-icon.svg" alt="heroku" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://jestjs.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/jestjsio/jestjsio-icon.svg" alt="jest" width="40" height="40"/> </a> <a href="https://kubernetes.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://mochajs.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/mochajs/mochajs-icon.svg" alt="mocha" width="40" height="40"/> </a> <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="mongodb" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://nextjs.org/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/nextjs-2.svg" alt="nextjs" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="40" height="40"/> </a> <a href="https://github.com/puppeteer/puppeteer" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/pptrdev/pptrdev-official.svg" alt="puppeteer" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://redis.io" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-original-wordmark.svg" alt="redis" width="40" height="40"/> </a> <a href="https://www.tensorflow.org" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" alt="tensorflow" width="40" height="40"/> </a> <a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40"/> </a> </p>
