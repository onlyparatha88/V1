# Deployment Guide

## GitHub — Version 1 Setup

```bash
# 1. Initialize repo
git init
git add .
git commit -m "feat: launch OnlyParatha v1.0.0 — bulk paratha sourcing site"

# 2. Create GitHub repo (via GitHub.com or CLI)
gh repo create only-paratha --public --source=. --push

# 3. Tag as Version 1
git tag -a v1.0.0 -m "Version 1.0.0 — Initial launch"
git push origin v1.0.0
```

## Vercel — One-Click Deploy

```bash
# Install Vercel CLI (once)
npm i -g vercel

# Deploy (from project folder)
vercel --prod

# Or connect to GitHub for auto-deploy on push:
# vercel.com > New Project > Import Git Repository > only-paratha
```

## After Connecting GitHub to Vercel
Every `git push` to `main` auto-deploys. 
Every new `git tag` can be a versioned preview URL.
