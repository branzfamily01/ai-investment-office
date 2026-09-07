# AI Investment Office Requirements

Status: current approved baseline, 2026-09-07

## Purpose
A human-in-the-loop investment research command center that uses specialized AI roles to improve research discipline, evidence quality, dissent, risk analysis and decision records without delegating the final investment decision.

## Core requirements
- Maintain the 7-department / 27-role research-office concept as a role catalog, not a requirement to run all roles on every case.
- Evidence-first workflow with explicit source quality/freshness/provenance.
- Independent Red Team and Risk Gate.
- One-page CEO/decision memo preserving dissent and uncertainty.
- Human Approve / Hold / Reject decision journal.
- Missing evidence must be able to block affirmative conclusions.
- Deterministic financial calculations should not be silently replaced by LLM prose.

## Safety boundaries
- Never connect to or control a brokerage account under the current product scope.
- Never store brokerage credentials.
- Never guarantee returns or imply that past performance guarantees future results.
- LLM output must not silently overwrite verified numerical/source data.
- Analysis and actual trade execution remain separate systems.

## Scope expansion
- Japanese equities are the current core use case.
- The research architecture may also support FX-relevant macro/fundamental analysis such as USD/JPY drivers, rates, inflation, central-bank policy, employment, GDP and geopolitics.
- User-provided chart-analysis books/materials may become a knowledge source; rules derived from those materials must remain traceable and distinguishable from general market theory.

## Cost discipline
Use selective routing. Call only the roles needed for the event/question and reuse fresh validated specialist outputs when appropriate.

## Governance
Astra owns data contracts, research-engine/orchestration architecture, financial data/source ingestion, deterministic risk engine, security and automation/execution boundaries. Sol owns routine research templates, prompts, UI, workflow improvements, analysis and Codex specifications. Codex implements approved changes.
