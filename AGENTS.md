# AGENTS.md — AI Investment Office

## Astra–Sol governance
- GPT-6 Astra: **Chief Architect** for root research/data contracts, source-ingestion architecture, deterministic risk engine, security, durable backend/source-of-truth, and any major automation/execution boundary.
- GPT-5.6 Sol: **Main Operator** for the majority of workflow design, prompts/templates, UI/UX, bounded analytical features, investigation, documentation, Codex specifications, and review.
- Codex: **Repository Implementer** for scoped code changes and verification against approved design.

Do not escalate to Astra merely because it is a higher-tier model.

## Repository sources of truth
Before non-trivial work read:
- `docs/REQUIREMENTS.md`
- `docs/MASTER_ARCHITECTURE.md`
- `docs/DECISIONS.md`
- `docs/PROJECT_STATE.md`
- `ARCHITECTURE.md`

The detailed product/role/safety rules below remain binding unless explicitly changed through the approved decision process.

## Product objective
Build a human-in-the-loop Japanese equity research office. The product should make disciplined research faster without delegating the final investment decision.

## Core / Delight / Signature
### Core
- Create research cases for Japanese equities
- Evidence-first workflow
- 7 departments / 27 specialist roles
- Red Team and Risk Gate
- One-page decision memo
- Human approval / hold / rejection
- Decision journal

### Delight
- Mobile-first CEO dashboard
- Clear department status
- Fast one-page weekly briefing
- Reusable decision templates

### Signature
- "AI employees do not vote; they disagree."
- "No evidence, no affirmative decision."
- Every important conclusion exposes its evidence and dissent.

## Safety boundaries
- Never implement brokerage execution or credential storage under the current approved scope.
- Never imply guaranteed returns.
- Keep a visible informational/research disclaimer.
- Do not let LLM output silently overwrite verified numerical data.
- Missing evidence must trigger ANALYSIS BLOCKED.
- Analysis and actual trading/execution remain separate systems.

## Agent roster
### Management Office (2)
1. Policy Guardian
2. Committee Facilitator

### Fundamental Analysis (7)
3. Earnings Reader
4. Financial Score Analyst
5. Industry Structure Analyst
6. Management & Mid-term Plan Analyst
7. Competitor Analyst
8. Shareholder Return Analyst
9. Macro Sensitivity Analyst

### Technical Analysis (3)
10. Long-term Trend Analyst
11. Volume / Supply-Demand Analyst
12. Staged Entry Analyst

### Risk Management (5)
13. Position Sizing Analyst
14. Sector Concentration Analyst
15. Drawdown Analyst
16. Bad-News Stress Analyst
17. Macro Shock Analyst

### Red Team (3)
18. Short Thesis Analyst
19. Assumption Breaker
20. Failure Pattern Matcher

### Intelligence (4)
21. Earnings Calendar Analyst
22. Timely Disclosure Watcher
23. Relevant News Analyst
24. Overheating / Sentiment Analyst

### Back Office (3)
25. Trade Journal Analyst
26. Quarterly Review Analyst
27. Compliance Analyst

## Cross-cutting controls
- Evidence Auditor
- Contradiction Detector
- Data Quality Gate
These are controls, not additional employees, so the public roster remains 27.

## Implementation phases
### Phase 1 — static MVP
- local research cases
- evidence gate
- department workflow
- decision memo
- local decision journal

### Phase 2 — structured local research engine
- JSON schemas for inputs/outputs
- deterministic financial calculations outside LLM
- per-agent prompt/instruction files
- orchestration with only required departments

### Phase 3 — source ingestion
- EDINET and TDnet/issuer IR ingestion
- source metadata: URL, fetchedAt, document date, page/section
- duplicate detection and freshness checking

### Phase 4 — portfolio/risk
- holdings import
- position/sector concentration
- scenario tests
- portfolio-level risk memo

### Phase 5 — recurring committee
- weekly Monday briefing
- quarterly thesis review
- event-triggered disclosure review

## Cost/routing rule
The 27 roles are a capability catalog, not a mandate to run all roles on every event. Use only the specialists needed for the event/question, retain independent risk/red-team scrutiny when material, and reuse fresh validated outputs where appropriate.

## Architecture escalation
Report to Sol and require Astra review before adopting changes that materially alter:
- research/evidence schemas or source-of-truth
- live financial-data ingestion topology
- deterministic calculation/risk-engine architecture
- security/credential boundaries
- major autonomous recurring actions that affect investment decisions
- brokerage/execution connectivity

For escalation, start from `docs/ASTRA_REVIEW_PACKAGE.md` and narrow to the specific decision.

## Change control
For important architecture/policy proposals classify the delta as:
- Maintain
- Modify
- Retire
- Hold

A major change is not adopted until the user explicitly accepts it.

## UI requirements
- iPhone portrait first
- large tap areas
- no horizontal overflow
- manual.html always reachable in one tap
- no fake live-data labels
- distinguish not run / blocked / complete / human verified

## Testing gate
- app opens on iPhone portrait width
- no horizontal overflow
- manual opens and returns
- case can be created
- blocked case cannot be approved
- hold and reject are allowed when blocked
- decisions persist after reload
- reset deletes local data only after confirmation
- no brokerage or secret fields exist

## Completion report
After changes report:
- files changed
- checks/tests run
- actual results
- unresolved risks/questions
- whether Sol/Astra architecture review is recommended

Never claim a command or test succeeded unless it actually ran successfully.
