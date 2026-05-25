# Automated GitHub Pages Deployment Setup

## Step 1: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `meeting-ai`
3. Description: `MeetingAI v4 - Automated Meeting Notes for Trident 1995`
4. Public ✅
5. Initialize with README (skip - we have one)
6. Click "Create repository"

## Step 2: Clone & Push

```bash
# On your PC
git clone https://github.com/YOUR-USERNAME/meeting-ai.git
cd meeting-ai

# Copy all files from this directory into that folder
# Then commit and push

git add .
git commit -m "Initial commit: MeetingAI v4"
git push origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repo Settings
2. Left sidebar → "Pages"
3. Source: "Deploy from a branch"
4. Branch: "main" / "/ (root)"
5. Click "Save"
6. Wait 30 seconds
7. You'll get URL: `https://YOUR-USERNAME.github.io/meeting-ai/`

## Step 4: Auto-Deploy on Every Push

The `.github/workflows/deploy.yml` file automatically:
- Watches for pushes to `main` branch
- Builds and deploys to GitHub Pages
- Takes ~30 seconds per deployment

## Step 5: Use It

1. Copy your GitHub Pages URL
2. Open in Android Chrome
3. Insert Anthropic API Key
4. Start using MeetingAI!

## To Update

Just edit `index.html`, commit, and push:
```bash
git add index.html
git commit -m "Update: fix x, add y"
git push origin main
# Auto-deploys in 30 seconds!
```

---

**Automatic updates every time you push!** 🚀
