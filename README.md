# OpenFang Cloud Deployment

## 💏 what's Already Done

1. **GitHub Repository Created**: https://github.com/leviathan-devops/glm-openfang-cloud
2. **Dockerfile Pushed**: Contains the OpenFang Docker configuration
3. **GitHub Actions Workflow Added**: Automatic deployment to Railway on push

## 😠 Next Steps to Complete Deployment

### Step 1: Create Railway Project

1. Go to https://railway.app
2. Login with your GitHub account
3. Click "New Project" → "Deploy from GitHub repo"
4. Select `glm-openfang-cloud` repository
5. Railway will automatically detect the Dockerfile and start building

### Step 2: Get Railway Token for GitHub Actions

1. In Railway dashboard, go to Settings → Tokens
2. Click "Generate Token"
3. Name it "GitHub Actions"
4. Copy the token

### Step 3: Add Secrets to GitHub Repository

1. Go to your GitHub repository: https://github.com/leviathan-devops/glm-openfang-cloud
2. Click "Settings" ‒ "Secrets and variables" ‒ "Actions"
3. Add these secrets:
   - `RAILWAY_TOKEN`: Your Railway token from Step 2
   - `DEEPSEEK_API_KEY`: `sk-d525583378094d5cb7ff8d0c019ec805`
   - `DISCORD_TOKEN`: `MTQ7OTAUMTE101153794A.GlN6-8.ctVy42DReSqQeKh9pRsTDOnBuT8wIhJZQFTe_E`

### Step 4: Trigger Deployment

1. The GitHub Actions workflow will automatically run when you push to main
2. You can also manually trigger it in GitHub Actions tab
3. Wait 2-3 minutes for deployment

### Step 5: Access Your Application

1. Go to Railway dashboard
2. Find your project
3. Click on the generated URL (e.g., `https://openfang-cloud.up.railway.app`)
4. Your OpenFang application should be running!

## 💇 Alternative

if you prefer to deploy manually:

```bash
# Install Railway CLI
npm install -g @railway/cli

# Login
railway login

# Create project
railway init --name openfang-cloud

# Link to repo
railway link