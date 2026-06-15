# Ataberk Ayhan

**Backend & Full-Stack Engineer** · Ankara, Turkey

I build event-driven systems, privacy infrastructure, and full-stack products — mostly in TypeScript. I care about correctness under failure, clean boundaries between components, and systems that stay simple as they scale.

---

## Focus Areas

- **Distributed Systems** — Event-driven architecture, CQRS, Saga orchestration, Transactional Outbox, idempotent consumers
- **Backend Engineering** — NestJS, Fastify, tRPC, REST & WebSocket APIs, PostgreSQL, Redis, Apache Kafka
- **Frontend & Full-Stack** — React, Next.js 15, Three.js, real-time collaboration (Yjs CRDT)
- **Privacy & Compliance** — PII detection & masking pipelines, KVKK / GDPR / HIPAA patterns
- **Tooling** — Turborepo monorepos, Docker, pnpm, GitHub Actions, Vitest

---

## Selected Projects

### [llm-gateway](https://github.com/ataberk388-ux/llm-gateway)
> Privacy-preserving reverse proxy for Claude and OpenAI

Sits between your application and cloud LLMs. Detects Turkish TC Kimlik No (checksum-validated), IBANs (MOD-97), credit cards (Luhn), medical codes, emails, and custom keyword blocklists — replaces each with deterministic session tokens before the prompt leaves your network, then restores them in the response. Handles streaming (SSE, chunk-level restoration), assigns a 0–100 privacy risk score per request, fires Slack / PagerDuty webhooks on critical events, and ships a TypeScript client SDK that's a drop-in replacement for the Anthropic SDK.

`Node.js 22` · `TypeScript` · `Fastify 5` · `Redis` · `Docker` · `Vitest`

---

### [Event-Driven Order Service](https://github.com/ataberk388-ux/Event-driven)
> NestJS + Kafka + PostgreSQL · CQRS · Saga · Event Sourcing

Production-style order processing service demonstrating the full event-driven stack: commands hit the write side, events flow through Kafka (KRaft — no Zookeeper), sagas coordinate cross-module workflows via `@nestjs/cqrs`, and every domain event is appended to a PostgreSQL-backed event store for full audit and replay. The architecture deliberately surfaces the hard problems — outbox, idempotency, saga state persistence — as first-class design decisions rather than afterthoughts.

`NestJS` · `Apache Kafka (KRaft)` · `PostgreSQL` · `Drizzle ORM` · `pnpm`

---

### [Synapse](https://github.com/ataberk388-ux/Event-driven)
> Collaborative work OS — Kanban · Docs · Whiteboard

Full-stack monorepo (Turborepo) with real-time collaboration across boards, documents (Yjs CRDT with live cursors), and a shared whiteboard (tldraw). tRPC runs **in-process** inside Next.js — no separate API server, no spoofable identity header, end-to-end type safety from DB to UI. Event fanout (activity feed, audit log, notifications, analytics) is driven by a single background worker reading a transactional Outbox via Postgres LISTEN/NOTIFY — no Kafka, no message broker, exactly-once semantics.

`Next.js 15` · `React 19` · `tRPC` · `Prisma` · `PostgreSQL` · `Redis` · `WebSocket` · `Yjs` · `Auth.js`

---

### [PC Builder AI](https://github.com/ataberk388-ux/chat-app)
> AI-powered configurator with an interactive 3D build viewer

Describe your workload, get part recommendations from an AI consultant (OpenAI, Groq, Gemini, Claude, or local Ollama), and watch the build assemble in a Three.js scene — real-time compatibility engine (socket, RAM gen, form factor, PSU headroom), FPS estimates per game/resolution, exploded-view spring animations, and a shareable build URL. API key stays server-side behind an Express proxy.

`React 18` · `TypeScript` · `Three.js / @react-three/fiber` · `TailwindCSS` · `Vite` · `GSAP` · `Framer Motion`

---

### [Crypto Spot Trading Terminal](https://github.com/ataberk388-ux/crypto-trading-terminal)
> Real-time Binance-style crypto spot trading terminal with paper trading and concurrent alarm engine

A full-stack trading terminal that streams live market data directly from Binance (candles, order book, trades, markets) and enables paper trading with a virtual portfolio. Built around a high-throughput, thread-safe price alarm engine that evaluates ticks in real time and pushes triggers to the UI via Server-Sent Events (SSE).

`Java 21` · `Spring Boot 3.5` · `Spring Security (JWT OAuth2)` · `PostgreSQL` · `WebSocket (Binance ingestion)` · `Server-Sent Events (SSE)` · `React 19` · `TypeScript` · `Vite` · `TanStack Query` · `TailwindCSS` · `lightweight-charts`

---

## Stack at a Glance

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

---

## Contact

[ataberk388@hotmail.com](mailto:ataberk388@hotmail.com) · [GitHub](https://github.com/ataberk388-ux)
