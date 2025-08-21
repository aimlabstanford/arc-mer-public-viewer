# GitHub Pages Deployment Instructions

## ✅ Completed Steps
1. Created deployment directory at `/home/larrychu/arc-mer-public-viewer`
2. Copied all necessary files (HTML, JSON data, logo)
3. Created `index.html` for easy access
4. Initialized git repository with all files committed

## 📌 Next Steps (You Need to Do)

### Step 1: Create GitHub Repository
1. Go to https://github.com/new
2. Repository name: `arc-mer-public-viewer` (or any name you prefer)
3. Description: "Public viewer for ARC Working Group IV Medical Education Research grants and publications data"
4. Set to **Public** (required for GitHub Pages)
5. DO NOT initialize with README, .gitignore, or license
6. Click "Create repository"

### Step 2: Push to GitHub
After creating the repository, GitHub will show you commands. Run these in your terminal:

```bash
cd /home/larrychu/arc-mer-public-viewer

# Add the remote repository (replace YOUR-USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR-USERNAME/arc-mer-public-viewer.git

# Push to GitHub
git branch -M main
git push -u origin main
```

If you're using GitHub CLI or SSH, use:
```bash
# For GitHub CLI
git remote add origin gh:YOUR-USERNAME/arc-mer-public-viewer

# For SSH
git remote add origin git@github.com:YOUR-USERNAME/arc-mer-public-viewer.git
```

### Step 3: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click "Settings" tab (in the repository, not your profile)
3. Scroll down to "Pages" section (left sidebar)
4. Under "Source", select:
   - Source: "Deploy from a branch"
   - Branch: "main" (or "master")
   - Folder: "/ (root)"
5. Click "Save"

### Step 4: Access Your Site
After 2-10 minutes, your site will be available at:
- **With index.html**: `https://YOUR-USERNAME.github.io/arc-mer-public-viewer/`
- **Direct file**: `https://YOUR-USERNAME.github.io/arc-mer-public-viewer/arc_working_group_public.html`

## 🔍 Verify Everything Works
1. Check the "Actions" tab in your repository - should show green checkmark
2. Visit the GitHub Pages URL
3. Verify the table loads with data
4. Test clicking on grant/publication numbers

## 📝 Optional: Custom Domain
If you have a custom domain:
1. In Settings > Pages, add your custom domain
2. Create a CNAME file in the repository with your domain

## 🔄 Future Updates
To update the data:
```bash
cd /home/larrychu/arc-mer-public-viewer

# Copy new data file
cp /path/to/new/data.json data/arc_mer_public_data.json

# Commit and push
git add .
git commit -m "Update MER data - [DATE]"
git push
```

## 🎉 Success Indicators
- ✅ Green checkmark in GitHub Actions
- ✅ "Your site is published at..." message in Settings > Pages
- ✅ Page loads with all statistics visible
- ✅ Table shows all specialties and mechanisms

## ⚠️ Troubleshooting
- **404 Error**: Wait 10 minutes, GitHub Pages takes time to deploy
- **Data not loading**: Check browser console, might be cache issue
- **Permission denied**: Make sure repository is PUBLIC, not private

## 📊 What You're Deploying
- 2,471 MER Grants across 6 specialties
- 14,791 Publications linked to grants
- Data from 2014-2024
- Interactive table with grant mechanisms
- Completely public, no authentication required