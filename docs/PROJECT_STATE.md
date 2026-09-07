# AI Investment Office Project State

Snapshot: 2026-09-07

## Current baseline
- Static/mobile-first MVP.
- 7 departments / 27 specialist roles visualized.
- Research case creation, evidence quality gate, Red Team/Risk workflow, one-page CEO paper and human Approve/Hold/Reject journal exist.
- Current MVP deliberately has no LLM API and no live financial-data API.
- No brokerage connectivity exists.
- Existing `ARCHITECTURE.md` defines selective routing, structured outputs, deterministic calculations and later source ingestion/backend phases.

## Governance work
This snapshot adds canonical requirements, architecture, decisions, project state and an Astra review package, and upgrades the existing `AGENTS.md` without changing runtime application behavior.

## Immediate next work
1. Run Astra review using `docs/ASTRA_REVIEW_PACKAGE.md` before choosing the durable research-engine/data-ingestion architecture.
2. Stabilize machine-readable input/output schemas before connecting live model/data providers.
3. Keep deterministic calculations and evidence provenance outside free-form model output.
4. Add external sources incrementally with freshness/deduplication metadata.
5. Keep brokerage execution out of scope unless explicitly re-architected and approved later.
