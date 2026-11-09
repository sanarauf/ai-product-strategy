# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| | | | Y/N | active / broken / missing |
| | | | Y/N | active / broken / missing |
| | | | Y/N | active / broken / missing |

**Broken loop identified by partner:**
**Fix plan:**

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

## Governance Policy

<!-- Governance Policy, SupportCopilot v1.2 -->

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
