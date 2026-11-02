# Cost Curve & Pricing Strategy

## Packaging Decision
| Leader | Filler | Killer | Killer Usage % | Bundle or Add-on |
| --- | --- | --- | --- | --- |
| Instant Audit-Ready Market Risk Briefs | Headline & SEC Filing Summarizer | Deep Multi-Jurisdiction Regulatory Impact Simulator (Heavy RAG/Reasoning) | 35% | Add-on (Enterprise Tier) |

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) | $45.00 | Frontier models (GPT-4o/o3) for deep multi-asset risk synthesis (~15 queries/user/day) |
| Inference (cascading/triage) | $12.00 | Mid/small models (Llama 3 / Claude 3.5 Haiku) for headline triage & basic extraction (~25 queries/user/day) |
| Infrastructure | $28.00 | Vector database indexing (Pinecone/Supabase) & high-availability API gateway hosting |
| Data/storage | $65.00 | Real-time CoinDesk Indices (CDI) stream licensing & dedicated enterprise document storage |
| Human-in-the-loop | $15.00 | Optional expert compliance analyst verification on flagged high-ambiguity regulatory outputs |
| **Total AI COGS** | **$165.00** | Blended monthly variable cost per active user seat |

## Cascading Strategy

**Triage model:** Claude 3.5 Haiku / Llama 3 70B (Fast, low-cost extraction)  
**Frontier model:** GPT-4o / Claude 3.5 Sonnet (Complex reasoning & compliance synthesis)  
**Routing rule:** Route simple headline alerts, sentiment tagging, and index lookup queries to Triage model. Escalate to Frontier model only when query requires cross-referencing multi-document SEC regulatory text against CoinDesk Index price volatility anomalies.  
**Expected cascade ratio:** 65% Triage / 35% Frontier  

## Pricing Model

**Strategy:** Maximize (Institutional Enterprise Capture)  
**Unit of work:** Per Audit-Ready Risk Brief generated  
**Structure:** Base fee + Usage metered allocation  

**Current pricing:** $2,500/month flat enterprise user seat (Legacy CoinDesk Data/Terminal SaaS)  
**Proposed AI pricing:** $4,500/month base platform fee (includes 5 seats & 250 briefs) + $15/additional risk brief  
**Model:** hybrid (seat base + outcome/usage tier)  

## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x | Gross margin drops from 81.6% to 67.5% | Shift default triage ratio from 65/35 to 80/20 using prompt compression and semantic caching. |
| Heaviest segment doubles | COGS increases by $57/user; margin drops ~6% | Enforce monthly Brief cap tiers on base plan and trigger automatic conversion to per-output usage pricing. |
| Model provider raises prices 50% | COGS increases by $28.50/user; margin drops ~3% | Activate Kill Switch: route 100% of triage/mid-tier traffic to open-source models via AWS Bedrock. |

## Board One-Pager

### BEFORE, TRADITIONAL SAAS
* **Revenue:** $2,500 / seat × 10 seats = $25,000 / month
* **COGS:** $1,200 (fixed data/hosting)
* **Gross margin:** 95.2%

### AFTER, AI-POWERED
* **Revenue:** $4,500 base + $3,750 usage (250 additional briefs) = $8,250 / seat/account equivalent ($825/user)
* **COGS:** $165 (variable AI + data) per user
* **Gross margin:** 80.0%

### NET MARGIN SHIFT
* **Δ margin %:** -15.2%
* **Δ gross $:** +$5,100 / month per account (+34% net dollar growth)
* **Narrative:** While the AI inference layer slightly compresses our gross margin percentage from 95% down to 80%, absolute gross dollars per account increase significantly. Our hybrid usage pricing captures a larger share of the enterprise workflow value, while automated model cascading hedges against token cost spikes.