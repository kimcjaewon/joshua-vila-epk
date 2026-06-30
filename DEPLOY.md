# Joshua Vila EPK — Deploy Guide

## One-time setup (GitHub + Vercel)

### 1. Rename the folder (removes a trailing space that breaks the terminal) and open it
```
cd ~/Desktop && mv "Joshua Villa EPK " "joshua-vila-epk" && cd joshua-vila-epk
```

### 2. Turn the folder into a git repo and make the first commit
```
git init && git add -A && git commit -m "Joshua Vila EPK — initial site"
git branch -M main
```

### 3. Create the GitHub repo
Go to https://github.com/new
- Repository name: `joshua-vila-epk`
- Owner: kimcjaewon
- Public, and DO NOT check "Add a README"
- Click "Create repository"

### 4. Connect and push
```
git remote add origin https://github.com/kimcjaewon/joshua-vila-epk.git
git push -u origin main
```

### 5. Put it live on Vercel
Go to https://vercel.com/new
- Import the `joshua-vila-epk` repo
- Framework Preset: "Other" (it's a plain static site)
- Click "Deploy"
Vercel gives you a live URL in ~30 seconds. Add a custom domain later under
Project → Settings → Domains.

---

## Updating the site later (the normal workflow)
After I make changes in this folder, paste this to push them live:
```
cd ~/Desktop/joshua-vila-epk && git add -A && git commit -m "update" && git push
```
Vercel auto-redeploys on every push to `main`.
