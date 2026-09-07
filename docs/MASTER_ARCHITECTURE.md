# AI Investment Office Master Architecture

Status: approved baseline consolidated by Sol; Astra architecture review pending
Last updated: 2026-09-07

## 1. Product architecture
The current static, mobile-first MVP intentionally establishes workflow, evidence rules and human decision gates before introducing live financial APIs or LLM orchestration.

Target evolution remains layered:
Browser/UI → Research API/ingestion → source normalization/provenance → deterministic calculations → selective agent router → relevant specialist roles → Evidence/Contradiction controls → Risk Gate → facilitator synthesis → human decision.

## 2. Human decision boundary
AI roles research, challenge, calculate and synthesize. They do not vote the final investment decision and do not execute brokerage orders. Human Approve / Hold / Reject is the terminal decision gate.

## 3. Evidence boundary
Every material conclusion should retain source/provenance/freshness. Missing or weak evidence can block an affirmative recommendation. LLM-generated prose never silently overwrites verified structured numbers.

## 4. Agent/orchestration boundary
The 27 roles are a capability catalog. The router selects only roles relevant to the event/question. Independent risk/red-team/fact/evidence controls remain structurally separate from bullish analysis.

## 5. Deterministic computation
Financial arithmetic, position/risk calculations and other deterministic transforms should be implemented outside free-form LLM reasoning and surfaced to agents as verified structured inputs.

## 6. Storage evolution
- Current MVP: browser/local state.
- Next durable backend: only after input/output schemas and provenance contracts are stable.
- Source ingestion must preserve document URL/identity, fetched time, document date and location/section where possible, with deduplication and freshness checks.

## 7. Cross-market scope
Japanese equities are primary, but macro/fundamental intelligence can support FX questions. Reuse shared macro evidence without merging equity and FX execution assumptions.

## 8. Knowledge sources
User-provided analytical books/materials may inform explicit rule libraries or evidence context. Derived rules must preserve source attribution/version and must not be presented as universally validated market facts.

## 9. Governance
- Astra: structured contracts, orchestration/data-ingestion architecture, deterministic risk engine, security, major automation and any execution boundary.
- Sol: research workflows, role prompts/templates, UI, bounded analytical features, documentation, Codex tasks and review.
- Codex: implementation/tests.

## 10. Escalation
Astra review is required before introducing a live financial-data source architecture, durable backend/source-of-truth, autonomous recurring actions that materially affect decisions, brokerage/execution connectivity, or root changes to evidence/risk contracts.
