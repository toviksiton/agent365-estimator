# 🚀 Azure Static Web Apps Deployment Guide

## Your GitHub Repository
**Repository URL**: https://github.com/toviksiton/agent365-estimator  
**Branch**: master (or main after renaming)

---

## 📋 Step-by-Step Deployment to Azure

### Step 1: Sign In to Azure Portal
1. Go to [portal.azure.com](https://portal.azure.com)
2. Sign in with your Azure account

### Step 2: Create Static Web App
1. Click **+ Create a resource**
2. Search for **"Static Web App"**
3. Click **Create**

### Step 3: Configure Basic Settings
Fill in the following:

| Field | Value |
|-------|-------|
| **Subscription** | Your Azure subscription |
| **Resource Group** | Create new: `rg-agent365-estimator` |
| **Name** | `agent365-estimator` |
| **Plan Type** | Free |
| **Region** | Select closest to you (e.g., East US, West Europe) |
| **Azure Functions and staging details** | Leave as default |

### Step 4: Deployment Details
1. **Source**: Select **GitHub**
2. Click **"Sign in with GitHub"** (you'll be prompted)
3. Authorize Azure to access your repos

### Step 5: Repository Selection
1. **Organization**: Select `toviksiton`
2. **Repository**: Select `agent365-estimator`
3. **Branch**: Select `master` (default)

### Step 6: Build Details
1. **Build Presets**: Select **"Custom"**
2. **App location**: `/` (root)
3. **API location**: Leave blank (no backend)
4. **Output location**: Leave blank (static files only)

Click **Review + Create**

### Step 7: Review & Deploy
- ✅ Check all settings
- Click **Create**
- Azure will create the resource (1-2 minutes)

### Step 8: GitHub Action Workflow
Azure automatically creates a GitHub Actions workflow:
- File: `.github/workflows/azure-static-web-apps-*.yml`
- Triggers on every push to `master`
- Auto-deploys to Azure within 2-3 minutes

---

## 🎉 Access Your Live Site

After deployment completes:

1. Go to your **Static Web App** resource in Azure Portal
2. Click **"Overview"**
3. Look for **"URL"** field
4. **Example**: `https://happy-plant-abc123.azurestaticapps.net`

**That's your live estimator URL!** 🎊

---

## 📊 Monitor & Manage

### View Deployment Status
1. Go to your Static Web App resource
2. Click **"Deployments"** in left sidebar
3. See real-time deployment status
4. Check GitHub Actions logs for details

### Make Updates
Any changes you push to GitHub automatically redeploy:
```bash
cd /tmp/agent365-estimator-repo
# Make changes to files
git add .
git commit -m "Update pricing or design"
git push origin master
# Deployment starts automatically!
```

### Custom Domain (Optional)
1. In Static Web App → **Custom domains**
2. Add your domain (e.g., `estimator.yourdomain.com`)
3. Verify DNS records
4. HTTPS auto-provisioned via Let's Encrypt

---

## 💰 Cost Estimate

**Free Tier includes:**
- ✅ 1 GB bandwidth/month
- ✅ 100 GB storage/month
- ✅ Auto HTTPS
- ✅ Free GitHub Actions minutes
- ✅ No charge for a static HTML calculator

**Expected Cost**: **$0/month** (stays on free tier)

If you exceed free limits:
- $0.20 per GB bandwidth (overage)
- $0.10 per GB storage (overage)

---

## 🔒 Security Features

- ✅ HTTPS enabled by default
- ✅ DDoS protection included
- ✅ CDN distribution (global edge locations)
- ✅ No data stored (static content only)

---

## 🐛 Troubleshooting

### Deployment Failed
1. Check GitHub Actions workflow log:
   - Go to repo → **Actions** → See latest run
   - Click failed workflow → See error details
2. Common fixes:
   - Check branch name (master vs main)
   - Verify file paths in build config
   - Ensure `index.html` exists in root

### Site Shows 404
- Check **Output location** in Azure config (should be empty or `/`)
- Verify `staticwebapp.config.json` exists and is valid

### Slow Performance
- Normal for first load (cold start)
- Subsequent loads cached globally
- Should be <100ms after warming up

---

## 📱 Testing the Live Site

After deployment, test:
- ✅ Open calculator tab, enter values
- ✅ Check real-time calculations
- ✅ Try export CSV
- ✅ Test on mobile (share link)
- ✅ Verify offline mode (disable network)
- ✅ Check all 4 tabs load

---

## 🚀 Next Steps

1. **Get Azure Portal URL** from deployment confirmation
2. **Test the live site** in browser
3. **Share URL with customers**: `https://happy-plant-abc123.azurestaticapps.net`
4. **Monitor deployments** in Azure Portal
5. **Update pricing** by editing files & pushing to GitHub

---

## 📞 Support

**Azure Documentation**: [Static Web Apps Docs](https://learn.microsoft.com/en-us/azure/static-web-apps/)  
**GitHub Repository**: https://github.com/toviksiton/agent365-estimator  
**Issues?** Check GitHub Actions logs or Azure deployment logs

---

**🎉 Your estimator is now live on Azure!**
