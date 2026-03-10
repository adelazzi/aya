# Arcus Pro — Product Review App

Two-page product review site with shared data via `localStorage`.

## Pages

| Page | File | Description |
|------|------|-------------|
| **Product & Reviews** | `index.html` | Product details, review submission form, live review feed |
| **Analytics Dashboard** | `dashboard.html` | Charts, stats, sentiment breakdown, all reviews table |

## Shared Data
Both pages read/write to the same `localStorage` key: `arcus_pro_reviews`.  
Any review submitted on `index.html` appears immediately on `dashboard.html` (auto-refreshes every 10s).

## Deploy to GitHub Pages

### Step 1 — Create the repo
1. Go to [github.com/new](https://github.com/new)
2. Name it e.g. `arcus-pro-reviews`
3. Set it to **Public**
4. Click **Create repository**

### Step 2 — Push the code
```bash
cd product-reviews
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/arcus-pro-reviews.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. The workflow runs automatically on push

### Step 4 — Access your pages
After ~1 minute your pages are live at:
- **Product page:** `https://YOUR_USERNAME.github.io/arcus-pro-reviews/`
- **Dashboard:** `https://YOUR_USERNAME.github.io/arcus-pro-reviews/dashboard.html`

> **Note:** `localStorage` is per-browser/device — data entered in one browser will only show on that same browser. For shared data across devices, a backend (Supabase, Firebase, etc.) would be needed.