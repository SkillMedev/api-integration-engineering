# API & Integration Engineering

**Ship integrations that survive retries, rate limits, and breaking changes.** — built in-house by [Skill&nbsp;Me](https://skillme.dev).

The resilience layer for backend engineers building and consuming APIs: enforce idempotency, harden webhook receivers, back off correctly under rate limits, add circuit breakers and bulkheads, design date-pinned versioning and deprecation, build cursor pagination and delta sync, and generate typed resilient clients from OpenAPI.

⭐ **If this is useful, star the repo** — it's how we gauge what to build next.

## Install

- **From the catalog:** [skillme.dev/pack/api-integration-engineering](https://skillme.dev/pack/api-integration-engineering) — install the whole pack into Claude in one step.
- **With the skills CLI:** `npx skills add aouellets/api-integration-engineering`
- **Manually:** copy any `skills/<slug>/SKILL.md` into your Claude skills directory.

## Skills in this pack

- **[Idempotency Enforcer](skills/idempotency-enforcer/SKILL.md)** — Adds idempotency keys and request deduplication so at-least-once delivery and client retries never double-charge or double-ship.
- **[Webhook Receiver Hardener](skills/webhook-receiver-hardener/SKILL.md)** — Builds a signature-verified, replay-resistant, fast-acking async webhook endpoint that verifies-then-enqueues and survives retries and out-of-order delivery.
- **[Rate Limit Handler](skills/rate-limit-handler/SKILL.md)** — Implements exponential backoff with full jitter, honors Retry-After, and adds client-side throttling so you stay under an upstream API's rate limits instead of hammering them.
- **[Circuit Breaker Builder](skills/circuit-breaker-builder/SKILL.md)** — Adds circuit breakers, timeouts, and bulkheads around flaky upstream dependencies so a slow or failing service degrades gracefully instead of cascading.
- **[API Versioning Strategist](skills/api-versioning-strategist/SKILL.md)** — Designs date-pinned or header-based API versioning plus a humane deprecation path, defining what counts as breaking and how long old versions live.
- **[Pagination and Sync Engineer](skills/pagination-and-sync-engineer/SKILL.md)** — Builds correct cursor pagination and incremental delta sync against a paginated API, handling inserts, deletes, watermarks, and resumability.
- **[API Client Generator](skills/api-client-generator/SKILL.md)** — Generates a typed, resilient client from an OpenAPI spec with retries, timeouts, and typed errors baked into the transport layer.
- **[REST API Design](skills/api-design/SKILL.md)** — Designs RESTful APIs with consistent naming, versioning, error codes, and OpenAPI documentation.
- **[OAuth & Auth Flow](aouellets)** — Implements OAuth 2.0, JWT, and session auth correctly with security best practices. _(external — see source)_

## License

MIT — see [LICENSE](LICENSE). Skills are portable `SKILL.md` files; the canonical
copies live in the [Skill&nbsp;Me catalog](https://skillme.dev).
