# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | **2/5** |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | **3/5** |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | **5/5** |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | **2/5** |

### Correction Loop - 2/5
**What you capture today:** Basic thumbs-up / thumbs-down ratings on generated risk briefs and inline user text edits on synthesized regulatory notes before export.
**How it compounds:** Currently captured primarily as static feedback logs. To compound, corrections need to automatically adjust retrieval weights and citation confidence parameters for future queries across that enterprise account.

### Preference Loop - 3/5
**What you capture today:** Individual analyst watchlists, custom compliance risk tolerances, saved prompt templates, and institutional memo styling formats.
**How it compounds:** As analysts query more events, the model tunes its focus—filtering out irrelevant noise and prioritizing specific token sectors (e.g., DeFi vs. Real World Assets) or regulatory jurisdictions (e.g., SEC vs. FCA) per team.

### Domain Context Loop - 5/5
**What you capture today:** Proprietary real-time CoinDesk Indices (CDI) data streams, pre-publication editorial breaking scoops, metadata-tagged historical crypto news archives, and institutional research notes.
**How it compounds:** Every breaking news event analyzed by the AI maps directly against real-time Index price movements and historical market precedents. As the CoinDesk newsroom publishes and Index feeds update continuously, the AI's contextual precision deepens automatically, creating a proprietary corpus general models cannot access.

### Network Loop - 2/5
**What you capture today:** Isolated, firm-level query history and private research exports due to strict financial privacy and compliance boundaries between competing funds.
**How it compounds:** Limited direct network compounding across institutions due to confidentiality. Compounding occurs indirectly as aggregate, anonymized search volume highlights emerging market anomalies or regulatory ambiguity trends across the whole user base.

**Total Flywheel Score: 12/20**
**Weakest Loop:** Correction Loop (Score: 2/5) & Network Loop (Score: 2/5)
**Fix for weakest loop:** Build an automated RLHF/RAG correction pipeline: whenever institutional compliance officers edit or correct a synthesized regulatory rule interpretation, automatically convert that edit into a verified high-confidence ground-truth anchor for all future retrieval queries across the platform.

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** OpenAI (GPT-4o / Deep Research Agents)
**Vector:** Native web search and deep research capabilities integrated directly into ChatGPT Enterprise, partnered with public block explorers.
**Time-to-threat:** 3 to 6 months
**% of value at risk:** 60% (Commoditizes generic news summary and basic market sentiment queries).

### 2. Vertical Competitor
**Attacker:** Messari Enterprise (MessariAI / Copilot)
**Vector:** Deep, analyst-verified tokenomics databases, governance tracking, and native AI research copilots tailored strictly for crypto funds.
**Time-to-threat:** Already active
**% of value at risk:** 40% (Competes directly for specialized crypto analyst workflow and due diligence budgets).

### 3. Adjacent Expansion
**Attacker:** Bloomberg Terminal (Bloomberg Intelligence & Crypto Workflows)
**Vector:** Adding automated AI crypto risk synthesis directly into the existing Terminal workspace used daily by traditional TradFi asset managers.
**Time-to-threat:** 6 to 12 months
**% of value at risk:** 50% (Risk of losing cross-over TradFi institutional capital entering digital assets).

---

## 90-Day Encroachment Plan
*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:** OpenAI (GPT-4o / Deep Research)
**Attack vector (target the weakest loop):** Exploiting our weak Network and Correction loops by launching a free, native "Financial Web Search & Regulatory Digest" agent that aggregates public crypto news with zero setup cost.
**Weeks 1-4 - what they ship:** A native "Crypto Deep Research" mode inside ChatGPT that searches public crypto sites and auto-summarizes breaking news and SEC filings.
**Weeks 5-8 - how they poach users:** Free tier distribution targeting junior analysts; offering instant multi-document summarization without requiring an institutional enterprise subscription.
**Weeks 9-12 - why users don't come back:** Users build custom ChatGPT GPTs/Workspaces with saved prompts, locking their daily research workflow into OpenAI's ecosystem.
**Your defense:** Lock down exclusive API integration rights with **CoinDesk Indices (CDI)** benchmark data. Shift from a simple "news summarizer" to an **Audit-Ready Regulatory Oracle** featuring verified citation logs, zero-hallucination compliance guarantees, and direct newsroom pre-feed speed that public web crawlers cannot access.
