# Ataberk Ayhan
Ataberk Ayhan

**Backend & Full-Stack Engineer** · Ankara, Turkey
Backend & Full-Stack Engineer · Ankara, Turkey

I build event-driven systems, privacy infrastructure, and full-stack products — mostly in TypeScript. I care about correctness under failure, clean boundaries between components, and systems that stay simple as they scale.
I build event-driven systems, trading platforms, and privacy infrastructure — mostly in TypeScript and Java. I care about correctness under failure, clean system boundaries, and scalable architecture that stays simple under load.

---
Focus Areas
Distributed Systems — Event-driven architecture, CQRS, Saga orchestration, transactional outbox, idempotent consumers
Backend Engineering — NestJS, Spring Boot, Fastify, REST & WebSocket APIs, PostgreSQL, Redis, Kafka
Frontend & Full-Stack — React, Next.js, TypeScript, real-time UIs, Three.js
System Design — concurrency, low-latency pipelines, streaming systems, event processing
Privacy & Infrastructure — PII detection, masking pipelines, secure API gateways
Tooling — Docker, Turborepo, pnpm, GitHub Actions, CI/CD pipelines
Selected Projects
Crypto Spot Trading Terminal

## Focus Areas
Real-time Binance-based crypto trading + paper trading platform

- **Distributed Systems** — Event-driven architecture, CQRS, Saga orchestration, Transactional Outbox, idempotent consumers
- **Backend Engineering** — NestJS, Fastify, tRPC, REST & WebSocket APIs, PostgreSQL, Redis, Apache Kafka
- **Frontend & Full-Stack** — React, Next.js 15, Three.js, real-time collaboration (Yjs CRDT)
- **Privacy & Compliance** — PII detection & masking pipelines, KVKK / GDPR / HIPAA patterns
- **Tooling** — Turborepo monorepos, Docker, pnpm, GitHub Actions, Vitest
Full-stack trading terminal streaming live market data from Binance (WebSocket + REST) with a complete paper trading system (virtual portfolio, positions, PnL, market/limit orders). Built around a high-throughput concurrent price-alarm engine that processes ticks in-memory and guarantees exactly-once alarm triggering using atomic CAS guards. Trigger events are pushed to the UI via SSE, while market data is consumed directly from Binance for minimal backend overhead.

---
Java 21 · Spring Boot 3 · Spring Security (JWT) · PostgreSQL · React · TypeScript · Vite · WebSocket · SSE

## Selected Projects
Min-TradeOff

### [llm-gateway](https://github.com/ataberk388-ux/llm-gateway)
> Privacy-preserving reverse proxy for Claude and OpenAI
AI-powered trading analysis platform

Sits between your application and cloud LLMs. Detects Turkish TC Kimlik No (checksum-validated), IBANs (MOD-97), credit cards (Luhn), medical codes, emails, and custom keyword blocklists — replaces each with deterministic session tokens before the prompt leaves your network, then restores them in the response. Handles streaming (SSE, chunk-level restoration), assigns a 0–100 privacy risk score per request, fires Slack / PagerDuty webhooks on critical events, and ships a TypeScript client SDK that's a drop-in replacement for the Anthropic SDK.
Full-stack investment analysis platform that helps users evaluate trading opportunities using AI-assisted insights. Provides portfolio tracking, risk scoring, and market interpretation through LLM-based analysis. Focused on combining financial data visualization with intelligent decision support.

`Node.js 22` · `TypeScript` · `Fastify 5` · `Redis` · `Docker` · `Vitest`
React · TypeScript · Node.js · Express.js · PostgreSQL · OpenAI API · JWT

---
llm-gateway

### [Event-Driven Order Service](https://github.com/ataberk388-ux/Event-driven)
> NestJS + Kafka + PostgreSQL · CQRS · Saga · Event Sourcing
Privacy-preserving reverse proxy for LLM providers

Production-style order processing service demonstrating the full event-driven stack: commands hit the write side, events flow through Kafka (KRaft — no Zookeeper), sagas coordinate cross-module workflows via `@nestjs/cqrs`, and every domain event is appended to a PostgreSQL-backed event store for full audit and replay. The architecture deliberately surfaces the hard problems — outbox, idempotency, saga state persistence — as first-class design decisions rather than afterthoughts.
Middleware system between applications and LLM APIs (OpenAI / Claude). Detects sensitive data (IDs, IBANs, credit cards, emails, medical codes, etc.), replaces them with deterministic tokens before requests leave the system, and restores responses afterward. Supports streaming, per-request privacy scoring, and webhook-based alerting.

`NestJS` · `Apache Kafka (KRaft)` · `PostgreSQL` · `Drizzle ORM` · `pnpm`
Node.js · TypeScript · Fastify · Redis · Docker · Vitest

---
Event-Driven Order Service

### [Synapse](https://github.com/ataberk388-ux/Event-driven)
> Collaborative work OS — Kanban · Docs · Whiteboard
NestJS + Kafka + PostgreSQL · CQRS · Saga · Event Sourcing

Full-stack monorepo (Turborepo) with real-time collaboration across boards, documents (Yjs CRDT with live cursors), and a shared whiteboard (tldraw). tRPC runs **in-process** inside Next.js — no separate API server, no spoofable identity header, end-to-end type safety from DB to UI. Event fanout (activity feed, audit log, notifications, analytics) is driven by a single background worker reading a transactional Outbox via Postgres `LISTEN/NOTIFY` — no Kafka, no message broker, exactly-once semantics. 3 processes, 2 containers.
Production-grade distributed order system built around event-driven architecture. Commands are processed via CQRS, events flow through Kafka (KRaft), and sagas coordinate cross-service workflows. Includes outbox pattern, idempotent consumers, and PostgreSQL-backed event store for full audit and replay capability.

`Next.js 15` · `React 19` · `tRPC` · `Prisma` · `PostgreSQL` · `Redis` · `WebSocket` · `Yjs` · `Auth.js`
NestJS · Kafka · PostgreSQL · Drizzle ORM · pnpm

---
Synapse

### [PC Builder AI](https://github.com/ataberk388-ux/chat-app)
> AI-powered configurator with an interactive 3D build viewer
Collaborative work OS — Kanban · Docs · Whiteboard

Describe your workload, get part recommendations from an AI consultant (OpenAI, Groq, Gemini, Claude, or local Ollama), and watch the build assemble in a Three.js scene — real-time compatibility engine (socket, RAM gen, form factor, PSU headroom), FPS estimates per game/resolution, exploded-view spring animations, and a shareable build URL. API key stays server-side behind an Express proxy.
Real-time collaborative workspace using Yjs CRDT. Includes Kanban boards, documents, and whiteboard system. Built with Next.js + tRPC in-process architecture and Postgres-based outbox system for event fanout (notifications, analytics, audit logs) without external brokers.

`React 18` · `TypeScript` · `Three.js / @react-three/fiber` · `TailwindCSS` · `Vite` · `GSAP` · `Framer Motion`
Next.js 15 · React 19 · tRPC · Prisma · PostgreSQL · Redis · WebSocket · Yjs

---
PC Builder AI

## Stack at a Glance
AI-powered PC configurator with 3D visualization

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
AI-driven PC building platform where users describe workloads and receive optimized hardware recommendations. Includes real-time compatibility engine (socket, RAM, PSU headroom), FPS estimation, and interactive Three.js assembly visualization. Supports multiple LLM providers (OpenAI, Claude, Gemini, Ollama).

---
React · TypeScript · Three.js · Tailwind · Vite · GSAP

## Contact
Stack at a Glance

[ataberk388@hotmail.com](mailto:ataberk388@hotmail.com) · [GitHub](https://github.com/ataberk388-ux)
Java · Spring Boot · TypeScript · Node.js · NestJS · React · Next.js · PostgreSQL · Redis · Kafka · Docker · Python

Contact

Email: ataberk388@hotmail.com
GitHub: https://github.com/ataberk388-ux
