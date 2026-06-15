Ataberk Ayhan

Backend & Full-Stack Engineer · Ankara, Turkey

I build event-driven systems, trading platforms, and privacy infrastructure — mostly in TypeScript and Java. I care about correctness under failure, clean system boundaries, and scalable architecture that stays simple under load.

Focus Areas
Distributed Systems — Event-driven architecture, CQRS, Saga orchestration, transactional outbox, idempotent consumers
Backend Engineering — NestJS, Spring Boot, Fastify, REST & WebSocket APIs, PostgreSQL, Redis, Kafka
Frontend & Full-Stack — React, Next.js, TypeScript, real-time UIs, Three.js
System Design — concurrency, low-latency pipelines, streaming systems, event processing
Privacy & Infrastructure — PII detection, masking pipelines, secure API gateways
Tooling — Docker, Turborepo, pnpm, GitHub Actions, CI/CD pipelines
Selected Projects
Crypto Spot Trading Terminal

Real-time Binance-based crypto trading + paper trading platform

Full-stack trading terminal streaming live market data from Binance (WebSocket + REST) with a complete paper trading system (virtual portfolio, positions, PnL, market/limit orders). Built around a high-throughput concurrent price-alarm engine that processes ticks in-memory and guarantees exactly-once alarm triggering using atomic CAS guards. Trigger events are pushed to the UI via SSE, while market data is consumed directly from Binance for minimal backend overhead.

Java 21 · Spring Boot 3 · Spring Security (JWT) · PostgreSQL · React · TypeScript · Vite · WebSocket · SSE

Min-TradeOff

AI-powered trading analysis platform

Full-stack investment analysis platform that helps users evaluate trading opportunities using AI-assisted insights. Provides portfolio tracking, risk scoring, and market interpretation through LLM-based analysis. Focused on combining financial data visualization with intelligent decision support.

React · TypeScript · Node.js · Express.js · PostgreSQL · OpenAI API · JWT

llm-gateway

Privacy-preserving reverse proxy for LLM providers

Middleware system between applications and LLM APIs (OpenAI / Claude). Detects sensitive data (IDs, IBANs, credit cards, emails, medical codes, etc.), replaces them with deterministic tokens before requests leave the system, and restores responses afterward. Supports streaming, per-request privacy scoring, and webhook-based alerting.

Node.js · TypeScript · Fastify · Redis · Docker · Vitest

Event-Driven Order Service

NestJS + Kafka + PostgreSQL · CQRS · Saga · Event Sourcing

Production-grade distributed order system built around event-driven architecture. Commands are processed via CQRS, events flow through Kafka (KRaft), and sagas coordinate cross-service workflows. Includes outbox pattern, idempotent consumers, and PostgreSQL-backed event store for full audit and replay capability.

NestJS · Kafka · PostgreSQL · Drizzle ORM · pnpm

Synapse

Collaborative work OS — Kanban · Docs · Whiteboard

Real-time collaborative workspace using Yjs CRDT. Includes Kanban boards, documents, and whiteboard system. Built with Next.js + tRPC in-process architecture and Postgres-based outbox system for event fanout (notifications, analytics, audit logs) without external brokers.

Next.js 15 · React 19 · tRPC · Prisma · PostgreSQL · Redis · WebSocket · Yjs

PC Builder AI

AI-powered PC configurator with 3D visualization

AI-driven PC building platform where users describe workloads and receive optimized hardware recommendations. Includes real-time compatibility engine (socket, RAM, PSU headroom), FPS estimation, and interactive Three.js assembly visualization. Supports multiple LLM providers (OpenAI, Claude, Gemini, Ollama).

React · TypeScript · Three.js · Tailwind · Vite · GSAP

Stack at a Glance

Java · Spring Boot · TypeScript · Node.js · NestJS · React · Next.js · PostgreSQL · Redis · Kafka · Docker · Python

Contact

Email: ataberk388@hotmail.com
GitHub: https://github.com/ataberk388-ux
