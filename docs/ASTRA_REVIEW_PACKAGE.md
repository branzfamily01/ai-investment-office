# ASTRA REVIEW PACKAGE — AI Investment Office

## Mode
ASTRA ARCHITECTURE REVIEW

## Current design
- Human-in-the-loop research office; no brokerage execution.
- Static workflow-first MVP; live LLM/data integration intentionally deferred until schemas/contracts are stable.
- 27 roles are selectively routed, not universally invoked.
- Evidence provenance/freshness, independent Red Team/Risk, deterministic calculations and dissent preservation are core invariants.
- Japanese equities are primary; macro intelligence may support FX analysis.

## Inspect
- `README.md`
- `ARCHITECTURE.md`
- `AGENTS.md`
- `docs/REQUIREMENTS.md`
- `docs/MASTER_ARCHITECTURE.md`
- `docs/DECISIONS.md`
- `docs/PROJECT_STATE.md`
- current app data structures/workflows

## Questions for Astra
1. What stable machine-readable research case/evidence/specialist-output schemas should precede model integration?
2. What source-ingestion architecture best supports EDINET/TDnet/issuer IR and later macro/market sources with provenance, freshness and deduplication?
3. How should deterministic calculations, model analysis and human verification be separated in the data contract?
4. What selective-routing policy minimizes model cost while preserving independent risk/red-team scrutiny?
5. What durable backend/source-of-truth should be introduced only after schemas stabilize?
6. How should user-provided chart-analysis books/materials be versioned and cited as rule/evidence sources?
7. Which recurring monitoring actions are safe to automate while preserving the human decision gate?

## Required output
Classify every proposed architecture delta as Maintain / Modify / Retire / Hold. Do not auto-adopt major changes. Return architecture findings, target contracts/topology, cost and safety risks, migration phases, docs to update and a bounded SOL HANDOFF.
