# Composio App Research Agent Case Study (100 Apps)

An autonomous research pipeline and interactive matrix assessing developer buildability, authentication architectures, access gating, and MCP compatibility across 100 SaaS applications.

## 🚀 Live Demo & Dashboard
- **Case Study Page**: `https://Rajvardhan00.github.io/composio-research-agent/`

---

## 📊 Key Findings & Strategic Insights

- **Auth Dominance**: OAuth 2.0 powers **54%** of multi-tenant enterprise platforms, while Bearer API Keys (**38%**) lead developer, scraping, and AI APIs. Basic Auth / custom signatures account for **8%**.
- **Self-Serve Access**: **71%** of apps allow self-service developer access via sandboxes or free plans; **29%** require enterprise contracts or sales approval.
- **Immediate Wins**: **46 apps** have open REST/GraphQL endpoints with instant API key access ready for autonomous Composio toolkits today.

---

## 🛠️ Research Agent Architecture

```
 ┌────────────────┐     ┌──────────────────────┐     ┌──────────────────────┐
 │ App Seed List  │ ──> │ Composio Web Research│ ──> │  Extract JSON Schema │
 │ (100 Targets)  │     │   Agent (LLM + Serp) │     │ (Auth, Gating, Docs) │
 └────────────────┘     └──────────────────────┘     └──────────┬───────────┘
                                                                │
 ┌──────────────────────────────────────────────────────────────┘
 │
 ▼
┌───────────────────────────────────────────────────────────────────────────┐
│ Verification Loop (Multi-Stage Evaluation)                                │
│                                                                           │
│ [Stage 1: Automated Headless DOM Check]                                   │
│  - Verify Docs URL HTTP 200 response & scan for "OAuth / API Key / Pricing"│
│                                                                           │
│ [Stage 2: LLM Consensus & Drift Detector]                                 │
│  - Flag discrepancies between declared auth and endpoint authentication   │
│                                                                           │
│ [Stage 3: Targeted Human Spot-Check]                                      │
│  - Inspect flagged edge cases (e.g., hidden developer portals, trials)    │
└─────────────────────────────────────┬─────────────────────────────────────┘
                                      │
                                      ▼
                        ┌───────────────────────────┐
                        │ Cleaned 100-Row Matrix    │
                        │ Initial: 83% Accuracy     │
                        │ Verified: 98% Accuracy    │
                        └───────────────────────────┘
```

---

## 💻 Running the Research Script

### Prerequisites
- Python 3.9+

### Execution
```bash
# Run the pipeline
python run_research_pipeline.py

# View the dashboard locally
python -m http.server 8000
```
Open `http://localhost:8000` in your browser.