# Agent 365 Cost Estimator - Deployment Guide

## Quick Links
- **Live Demo**: [View in browser](/estimator/index.html)
- **File**: `index.html` (self-contained, no dependencies)

## Option 1: GitHub Pages (Recommended)
1. Create a new public GitHub repository (e.g., `agent365-estimator`)
2. Clone locally
3. Copy `index.html` to repository root
4. Push to `main` branch
5. Go to **Settings > Pages** → Select **Deploy from branch** → **main** → Save
6. Access at: `https://{username}.github.io/agent365-estimator/`

## Option 2: Deploy to Vercel/Netlify
1. Drag & drop `index.html` to Vercel or Netlify
2. Instant live URL in < 1 minute

## Option 3: Azure Static Web Apps
1. Create new Static Web App in Azure Portal
2. Connect to GitHub repo containing `index.html`
3. Auto-deployed with CI/CD

## Option 4: Simple HTTP Server (Local Testing)
```bash
# Python 3
python -m http.server 8000

# Node.js (http-server)
npx http-server

# Then visit: http://localhost:8000
```

## File Contents
- **Standalone HTML** - No dependencies, works offline
- **Responsive** - Mobile, tablet, desktop friendly
- **Modern Design** - microsoft.ai aesthetic
- **Interactive Calculator** - Real-time cost estimates
- **4 Tabs**: Calculator, How It Works, Pricing, FAQ

## Features
✅ Agent 365 governance licensing
✅ Activity-based consumption pricing
✅ Work IQ API costs included
✅ Foundry compute costs (optional)
✅ Export to CSV
✅ Scenario examples
✅ FAQ & pricing reference

## Customer Sharing
- **Public Link**: Share GitHub Pages URL or Vercel link
- **Email**: Attach `index.html` directly
- **CRM**: Embed in customer portal/knowledge base
- **White-label**: Customize colors in CSS `<style>` section

## Customization
Edit the `<style>` section to:
- Change brand colors
- Adjust pricing defaults
- Modify company name/logo
- Translate to Hebrew (add lang="he" attribute)

---
**Version**: 1.0 | **Pricing Verified**: October 25, 2026
