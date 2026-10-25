# 🤖 Agent 365 Cost Estimator

## What Is This?
An **interactive calculator** to estimate monthly operating costs for your standalone Autopilot powered by Agent 365 and Work IQ API integration.

## How It Works
1. **Enter your expected monthly activities** (Q&As, summaries, drafts, etc.)
2. **See real-time cost breakdown**:
   - Agent 365 governance license ($15/month)
   - AI consumption (Work IQ + Copilot Studio)
   - Optional Foundry compute costs
3. **Export as CSV** for your budget planning
4. **Reference tables** for activity pricing & sources

## Key Insights
✨ **Governance is fixed** — $15/month for your agent owner, regardless of usage  
✨ **Activities are cheap** — Simple Q&A = $0.011, even at scale it's cents  
✨ **Usage-agnostic** — 1 user × 100 calls = same cost as 100 users × 1 call  
✨ **Work IQ dominates** — 85-90% of variable costs from M365 data access  

## Design
- **Modern microsoft.ai aesthetic** — clean, professional, friendly
- **Fully responsive** — works on phone, tablet, desktop
- **No dependencies** — pure HTML/CSS/JavaScript, works offline
- **Fast** — instant calculations as you type

## Pricing Source
All rates verified against **official Microsoft documentation** (June-October 2026):
- Agent 365: $15/user/month (July 2026)
- Copilot Credits: $0.01/credit (October 2026)
- Work IQ API: 0.1 credits/call (June 2026)
- Foundry vCPU-hours: $0.10–$0.25 (October 2026)

---
**Ready to use? Just open `index.html` in your browser.** 🚀
