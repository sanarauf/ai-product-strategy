# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status | 
| ----- | ----- | ----- | ----- | ----- | 
| **Recursive Learning** | User corrections on generated risk briefs & regulatory summaries | Retrained retrieval weights & verified Golden Dataset candidate rows | Y | active | 
| **Cross-Domain Transfer** | Real-time CoinDesk Indices (CDI) volatility streams & macro market news | Cross-asset sentiment shift models (e.g., L1 gas fees → DeFi token liquidations) | Y | active | 
| **Network Intelligence** | Anonymized search volumes & institutional query clusters | Systemic risk anomaly alerts (e.g., spike in SEC regulatory inquiry searches) | Y | active | 

**Broken loop identified by partner:**
The Network Intelligence loop is currently siloed at the individual fund level due to strict institutional confidentiality boundaries, preventing cross-firm intelligence sharing.

**Fix plan:**
Implement an aggregated, zero-knowledge telemetry pipeline that anonymizes firm-specific queries to surface macro search volume surges and regulatory anomaly trends across the entire subscriber base without exposing proprietary fund positions or strategies.

## Context Connectivity

Knowledge flows dynamically between the real-time CoinDesk editorial newsroom pre-feeds, proprietary CoinDesk Indices (CDI) benchmark data streams, and institutional RAG vector databases. Knowledge silos occur between competing hedge fund accounts due to strict financial privacy firewalls; however, structured cross-domain synthesis safely bridges real-time macro news with underlying token index metrics without cross-contaminating client portfolio data.

## Governance Policy

**Scope:** AI features in the CoinDesk Terminal AI product line, automated research brief synthesis, real-time news summarization, CoinDesk Index (CDI) data correlation, and regulatory risk analysis. Excludes: Internal-only editorial planning tools and corporate business dashboards (covered by separate internal data policies).

**Autonomy boundaries:** Synthesizing breaking market risk briefs, auto. Generating citation-backed index analysis and regulatory summaries, auto. Executing institutional trades, modifying ledger balances, or transmitting unreviewed automated communications directly to external regulators or end-clients, never auto (strictly read-only oracle).

**Escalation triggers:** (1) Model confidence < 50% on quantitative index metrics or regulatory interpretation. (2) Customer input flagged for adversarial prompt injection, jailbreak attempts, or data poisoning. (3) Contradictory primary source citations (e.g., conflicting SEC filing language vs. breaking news claims). (4) System hallucination rate exceeding the >2% alert threshold during evaluation runs. (5) Institutional client requests live human analyst verification or custom desk validation.

**Audit cadence:** Weekly, Automated evaluation against the 150+ row ground-truth Golden Dataset. Monthly, Human-in-the-Loop (HITL) review of all flagged low-confidence queries and client-reported edge-case corrections. Quarterly, Full policy review with security, legal, and CTO sign-off.

**Regulatory exposure (EU AI Act / other):** EU AI Act, SEC/FINRA record-keeping (Rule 17a-4), SOC 2. Risk tier: High-risk AI system (financial services / institutional risk assessment). Controls: Strict technical logging of output lineage · No training on institutional PII or proprietary fund portfolio data · Immutable audit trails for citation chains · DPIA and compliance documentation on file.

## Agent Topology

*Not shipping agents this version.*

## Shadow AI Audit (User-Side)

### Discover: User-Side Workarounds

| Workaround | Source | Signal | Freq | Spend | Decision |
|---|---|---|---|---|---|
| Analysts export raw market risk briefs → paste into Claude to reformat into investment committee memo format | User interview | Workflow gap | H | $200/mo | Build |
| Piping output into Perplexity Pro to verify SEC filing citations against external sources | Support ticket | Trust gap | H | $200/mo | Build |
| Zapier automation: CoinDesk Terminal AI webhook → ChatGPT → Telegram bot for real-time trader alerts | Zapier/Make | Capability gap | M | $100/mo | Partner |
| Running Terminal AI risk briefs through custom Python scripts in Claude Code to calculate portfolio VaR impact | Sales call | Capability gap | M | $200/mo | Build |
| Exporting CDI index data to ChatGPT Plus to generate executive chart graphics for LP pitch decks | User interview | Workflow gap | L | $100/mo | Partner |
| Desk analysts running risk briefs through DeepL to translate market notes for APAC branch offices | Sales call | Capability gap | L | $100/mo | Ignore |

### Pattern Assessment

* **Workarounds found:** 6
* **Build candidates:** 3
* **Partner candidates:** 2
* **Ignore decisions:** 1
* **Adjacent spend:** $900/mo (across surveyed institutional user seats)
* **Dominant signal:** Workflow gap

### Action Plan

#### Build
* **Investment Committee Memo Generator:** Native 1-click export to customizable IC memo and PDF board formats (high frequency, clear workflow gap).
* **Inline Citation Verifier Panel:** One-click source verification and primary document comparison panel inside the UI to solve the citation trust gap.
* **Portfolio VaR & Delta Risk Calculator:** Native scenario simulation widget to convert qualitative briefs into quantitative portfolio risk metrics.

#### Partner
* **Telegram/Slack Trading Alert Bot Integration:** Partner with enterprise webhooks and messaging infrastructure for compliant real-time alert delivery.
* **Advanced Charting & LP Presentation Export:** Partner with institutional charting tools (e.g., TradingView / Canva for Enterprise) for high-res graphics generation.

#### Ignore + Monitor
* **APAC Multi-language Translation:** Out of scope for v1 core institutional product; monitor APAC desk requests before investing in dedicated localization pipelines.

### Roadmap Brief

Based on your audit: 6 user-side workarounds discovered.
Decisions: 3 build · 2 partner · 1 ignore · 0 TBD.
Estimated adjacent spend: $900/mo across surveyed institutional user seats.
Dominant signal: Workflow gap.

**Recommended next step:** Workflow gaps dominate on institutional trading desks where analysts spend time reformatting, recalculating, and verifying outputs. The strongest near-term move is natively building the IC memo formatter and inline citation verifier to lock users inside CoinDesk Terminal AI.