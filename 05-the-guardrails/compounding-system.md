# Compounding System Design
## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | User corrections on generated risk briefs & regulatory summaries | Retrained retrieval weights & verified Golden Dataset candidate rows | Y | active |
| Cross-Domain Transfer | Real-time CoinDesk Indices (CDI) volatility streams & macro market news | Cross-asset sentiment shift models (e.g., L1 gas fees → DeFi token liquidations) | Y | active |
| Network Intelligence | Anonymized search volumes & institutional query clusters | Systemic risk anomaly alerts (e.g., spike in SEC regulatory inquiry searches) | Y | active |

**Broken loop identified by partner:** The Network Intelligence loop is currently siloed at the individual fund level due to strict institutional confidentiality boundaries, preventing cross-firm intelligence sharing.

**Fix plan:** Implement an aggregated, zero-knowledge telemetry pipeline that anonymizes firm-specific queries to surface macro search volume surges and regulatory anomaly trends across the entire subscriber base without exposing proprietary fund positions or strategies.

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** Knowledge flows dynamically between the real-time CoinDesk editorial newsroom pre-feeds, proprietary CoinDesk Indices (CDI) benchmark data streams, and institutional RAG vector databases.

**Where it silos:** Knowledge silos occur between competing hedge fund accounts due to strict financial privacy firewalls; however, structured cross-domain synthesis safely bridges real-time macro news with underlying token index metrics without cross-contaminating client portfolio data.

## Governance Policy

**Scope:** AI features in the CoinDesk Terminal AI product line:
- automated research brief synthesis
- real-time news summarization
- CoinDesk Index (CDI) data correlation
- and regulatory risk analysis. Excludes: Internal-only editorial planning tools and corporate business dashboards (covered by separate internal data policies).

**Autonomy boundaries:** Executing institutional trades, modifying ledger balances, or transmitting unreviewed automated communications directly to external regulators or end-clients, never auto.

**Escalation triggers:** (1) Model confidence < 50% on quantitative index metrics or regulatory interpretation. (2) Customer input flagged for adversarial prompt injection, jailbreak attempts, or data poisoning. (3) Contradictory primary source citations (e.g., conflicting SEC filing language vs. breaking news claims). (4) System hallucination rate exceeding the >2% alert threshold during evaluation runs. (5) Institutional client requests live human analyst verification or custom desk validation.

**Audit cadence:** Weekly, Automated evaluation against the 150+ row ground-truth Golden Dataset (PM: Sam). Monthly, Human-in-the-Loop (HITL) review of all flagged low-confidence queries and client-reported edge-case corrections (Legal: Priya). Quarterly, Full policy review with security, legal, and CTO sign-off (CTO sign-off).

**Regulatory exposure (EU AI Act / other):** EU AI Act, SEC/FINRA, SOC 2

AI system (financial services / institutional risk assessment). Controls: - Strict technical logging of output lineage
- No training on institutional PII or proprietary fund portfolio data
- Immutable audit trails for citation chains
- DPIA and compliance documentation on file.

## Agent Topology

Not shipping agents this version.


## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
