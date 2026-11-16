# API Specification

**Status:** No implementation or frozen contract exists.

Intended capabilities: authenticated batch ingestion; idempotent acceptance by `event_id`; per-event acknowledgement/errors; device registration/configuration; history queries; health/sync status; dashboard live updates.

Contract requirements: version payloads; UTC timestamps; explicit units; define batch limits, timeouts, rate limits, retry semantics; distinguish permanent validation errors from transient failures; acknowledge only after durable central commit; never log secrets.

Authentication, token lifecycle, request signing, endpoints, schemas, and error codes remain Phase 0 decisions.
