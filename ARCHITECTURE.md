# Architecture Decision Record

## Decision
Start with a static, mobile-first MVP and keep AI orchestration behind a later research-engine boundary.

## Why
A 27-agent interface without evidence discipline becomes 27 ways to hallucinate. The UI and data contract should therefore be stable before attaching model calls.

## Design principles
- Specialized agents separate concerns.
- Critic / risk / fact-check roles are independent from bullish analysis.
- Machine-readable structured outputs are preferable to free-form prose.
- A facilitator synthesizes but preserves dissent.
- Paid model calls should be routed only to needed specialists.

## Proposed runtime
Browser UI
→ Research API
→ Source ingestion
→ deterministic calculations
→ agent router
→ specialists in parallel
→ Evidence Auditor + Contradiction Detector
→ Risk Gate
→ Facilitator
→ human decision

## Cost-control rule
Do not run all 27 agents on every event.
- New earnings: Earnings Reader, Financial Score, Shareholder Return, Risk, Red Team, Facilitator.
- Timely disclosure: Timely Disclosure Watcher, relevant fundamental specialist, Risk, Red Team.
- Weekly committee: portfolio rollup; reuse fresh cached specialist reports.

## Storage evolution
MVP: browser localStorage.
Next: structured backend only after schemas are stable.
