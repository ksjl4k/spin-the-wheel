# 🚀 Setup & Deployment Guide

## Step 1: Initialize Git Repository

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Spin The Wheel"

# Add remote repository (replace with your GitHub repo URL)
git remote add origin https://github.com/YOUR_USERNAME/spin-the-wheel.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 2: Deploy to Vercel

### Option A: Using Vercel CLI (Recommended)

```bash
# Install Vercel CLI globally
npm install -g vercel

# Deploy from project directory
vercel

# Follow the prompts:
# - Confirm project setup
# - Select GitHub as source
# - Authorize Vercel to access GitHub
# - Select your repository
# - Accept default settings
```

### Option B: Using Vercel Web Dashboard

1. Go to [vercel.com](https://vercel.com)
2. Click "New Project"
3. Select "Import Git Repository"
4. Find and select your `spin-the-wheel` repository
5. Project settings should auto-detect (no build needed)
6. Click "Deploy"
7. Your site will be live at `https://spin-the-wheel.vercel.app`

### Option C: GitHub Push-to-Deploy (Automatic)

1. After deploying once with Vercel, every `git push` to `main` will auto-deploy
2. Check deployment status in Vercel dashboard
3. View deployment logs for troubleshooting

## Step 3: Configure GitHub

### Enable GitHub Pages (Optional - for backup hosting)

1. Go to your repository settings
2. Scroll to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Choose `main` branch
5. Save
6. Your site will also be available at `https://YOUR_USERNAME.github.io/spin-the-wheel`

### Add Repository Secrets (For CI/CD)

If using GitHub Actions workflow:

1. Go to **Settings** → **Secrets and variables** → **Actions**
2. Click "New repository secret"
3. Add the following secrets:

```
VERCEL_TOKEN: [Get from vercel.com/account/tokens]
VERCEL_ORG_ID: [Get from Vercel project settings]
VERCEL_PROJECT_ID: [Get from Vercel project settings]
```

## Step 4: Verify Deployment

### Check Vercel Status
```bash
vercel status
```

### Test Your Live Site
- Open your Vercel deployment URL
- Test wheel spinning
- Add/remove segments
- Test on mobile device
- Verify responsive design

## Step 5: Continuous Deployment

Your setup is now complete with:

✅ **Local Development**: Run `npm run dev` or `python -m http.server 3000`
✅ **GitHub Repository**: Code backed up and version controlled
✅ **Vercel Deployment**: Live site auto-updates on push to main
✅ **GitHub Pages**: Optional backup deployment
✅ **CI/CD**: Optional GitHub Actions workflow

## Making Updates

To deploy new changes:

```bash
# Make changes to your files
# ...

# Commit and push
git add .
git commit -m "Your commit message"
git push origin main

# Vercel automatically deploys!
# Check https://vercel.com/dashboard for status
```

## Troubleshooting

### Site shows 404
- Ensure `index.html` is in the root directory
- Check Vercel deployment logs: `vercel logs`

### Changes not reflecting live
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Wait 30 seconds for Vercel to rebuild
- Check deployment status in Vercel dashboard

### Local server not starting
```bash
# Try Python instead of Node
python -m http.server 3000

# Or install http-server
npm install -g http-server
http-server -p 3000
```

## Environment-Specific URLs

After deployment:
- **Local**: `http://localhost:3000`
- **Vercel**: `https://spin-the-wheel.vercel.app`
- **GitHub Pages**: `https://YOUR_USERNAME.github.io/spin-the-wheel`

## Best Practices

1. **Test locally first**: Always test changes with `npm run dev`
2. **Commit frequently**: Small, meaningful commits are easier to track
3. **Use meaningful commit messages**: Helps with version history
4. **Create branches for features**: `git checkout -b feature/name`
5. **Monitor Vercel dashboard**: Check for build issues
6. **Mobile testing**: Always test on mobile devices before deployment

## Next Steps

- ✅ Set custom domain (in Vercel settings)
- ✅ Add analytics (Vercel Web Analytics)
- ✅ Set up email notifications (GitHub/Vercel)
- ✅ Create GitHub Issues for feature requests
- ✅ Set up Pull Request reviews

---

**Questions?** Check the main README.md or GitHub Issues.
