# API & Integration Engineering

**For backend engineers: make every API you build or consume survive production.** — built in-house by [Skill&nbsp;Me](https://skillme.dev/?utm_source=github&utm_medium=readme&utm_campaign=pack-api-integration-engineering).

Reach for this when an integration has to be bulletproof - payments that can't double-charge, webhooks you don't control, third-party APIs that throttle or fall over, and contracts that change under you. It turns the hard-won production patterns into skills: idempotent writes, hardened webhook receivers, correct backoff under rate limits, circuit breakers and bulkheads for flaky upstreams, cursor pagination and delta sync, typed clients from OpenAPI, and date-pinned versioning with a real deprecation path. Install it before the integration that, if it breaks, pages you at 3am.

## Install

- **Claude, ChatGPT, Codex, Cursor (connector):** [install the whole pack from skillme.dev](https://skillme.dev/pack/api-integration-engineering?utm_source=github&utm_medium=readme&utm_campaign=pack-api-integration-engineering) — one connection, then ask for any skill by name.
- **As files for Codex, Cursor, or Claude Code:** `npx @skillme/cli add idempotency-enforcer webhook-receiver-hardener rate-limit-handler circuit-breaker-builder api-versioning-strategist pagination-and-sync-engineer api-client-generator api-design --target all`
- **With the skills CLI:** `npx skills add SkillMedev/api-integration-engineering`
- **Manually:** copy any `skills/<slug>/SKILL.md` into `.agents/skills/`, `.cursor/skills/`, or `.claude/skills/`.

⭐ **If this is useful, star the repo** — it's how we gauge what to build next.

## Skills in this pack

- **[Idempotency Enforcer](skills/idempotency-enforcer/SKILL.md)** — Designs client-supplied idempotency keys, deduplication storage, and replay semantics so at-least-once delivery and client retries return the first result instead of double-charging or double-shipping.
- **[Webhook Receiver Hardener](skills/webhook-receiver-hardener/SKILL.md)** — Hardens an inbound webhook endpoint so it verifies the sender signature on the raw body, resists replays, and acknowledges fast by persisting-then-enqueueing before any processing.
- **[Rate Limit Handler](skills/rate-limit-handler/SKILL.md)** — Adds retry-with-backoff, Retry-After handling, and client-side throttling so a caller stays under an upstream API's rate limits instead of hammering it.
- **[Circuit Breaker Builder](skills/circuit-breaker-builder/SKILL.md)** — Wraps flaky upstream dependencies in circuit breakers, aggressive timeouts, and per-dependency bulkheads so a slow or failing service degrades gracefully instead of cascading into a full outage.
- **[API Versioning Strategist](skills/api-versioning-strategist/SKILL.md)** — Produces an API version scheme (date-pinned header or URI), a breaking-vs-additive change policy, and a published deprecation/sunset timeline with translation shims.
- **[Pagination and Sync Engineer](skills/pagination-and-sync-engineer/SKILL.md)** — Designs correct cursor pagination and incremental delta sync against a mutating dataset - cursor contracts, updated_at watermarks, delete propagation, checkpointing, and idempotent reprocessing.
- **[API Client Generator](skills/api-client-generator/SKILL.md)** — Generates a typed API client from an OpenAPI/Swagger spec, with a hand-controlled transport wrapper for timeouts, auth, and typed errors.
- **[REST API Design](skills/api-design/SKILL.md)** — Designs REST API surfaces - resource naming, HTTP method and status-code semantics, error shapes, pagination, and filtering - and delivers an endpoint spec a consumer can build against without asking questions.
- **[OAuth & Auth Flow](https://skillme.dev/skill/oauth-flow)** — Implements OAuth 2.0, JWT, and session auth correctly with security best practices. _(external — see source)_

## License

MIT — see [LICENSE](LICENSE). Skills are portable `SKILL.md` files; the canonical
copies live in the [Skill&nbsp;Me catalog](https://skillme.dev/browse?utm_source=github&utm_medium=readme&utm_campaign=pack-api-integration-engineering).
