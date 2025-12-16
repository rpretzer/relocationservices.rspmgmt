# Relocation Services Site — relocationservices.rspmgmt.com

This repository contains the website for relocationservices.rspmgmt.com, hosted on GitHub Pages.

## Setup Instructions

### 1. Create GitHub Repository

1. Go to GitHub and create a new repository (e.g., `relocationservices.rspmgmt.com`)
2. **Do not** initialize it with a README, .gitignore, or license (we already have these)

### 2. Push to GitHub

```bash
cd /home/rpretzer/relocationservices-site
git add .
git commit -m "Initial commit: relocationservices.rspmgmt.com site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

### 3. Configure GitHub Pages

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Select **main** branch and **/ (root)** folder
5. Click **Save**

### 4. Configure Custom Domain

1. In the same **Settings** → **Pages** section
2. Under **Custom domain**, enter: `relocationservices.rspmgmt.com`
3. Check **Enforce HTTPS** (after DNS propagation completes)
4. Click **Save**

### 5. Configure DNS

Add a CNAME record at your DNS provider (Squarespace):

- **Type**: CNAME
- **Name**: `relocationservices` (or `relocationservices.rspmgmt.com` depending on your DNS provider)
- **Value**: `rpretzer.github.io`

**Note**: The CNAME file in the repository (`relocationservices.rspmgmt.com`) will automatically be used by GitHub Pages once the DNS is configured.

### 6. Verify

- DNS propagation can take 24-48 hours
- Once DNS propagates, GitHub Pages will automatically provision SSL
- Visit `https://relocationservices.rspmgmt.com` to verify the site is live

## Local Development

The site is static HTML/CSS/JS. Simply open `index.html` in a browser or use a local server:

```bash
# Python 3
python3 -m http.server 8000

# Node.js (http-server)
npx http-server

# Or any static file server
```

Then visit `http://localhost:8000`

