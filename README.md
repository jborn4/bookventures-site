# BookVentures Website

Simple static website for BookVentures iOS app, including:
- Landing page
- Privacy Policy (required for App Store)

## Quick Setup (GitHub Pages)

### 1. Create a new GitHub repository
- Go to github.com → New repository
- Name it `bookverse-site` (or whatever you prefer)
- Make it **Public** (required for free GitHub Pages)
- Don't initialize with README (we have files already)

### 2. Push this folder to GitHub
```bash
cd bookverse-site
git init
git add .
git commit -m "Initial commit - BookVentures website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/bookverse-site.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to your repository on GitHub
- Settings → Pages (in left sidebar)
- Source: "Deploy from a branch"
- Branch: `main` / `/ (root)`
- Click Save

### 4. Access your site
After a few minutes, your site will be live at:
```
https://YOUR_USERNAME.github.io/bookverse-site/
```

Privacy policy URL:
```
https://YOUR_USERNAME.github.io/bookverse-site/privacy/
```

## Using a Custom Domain (Optional)

If you own a domain like `bookverse.app`:

### 1. Add CNAME file
Create a file called `CNAME` (no extension) with your domain:
```
bookverse.app
```

### 2. Configure DNS
Add these records at your domain registrar:

**For apex domain (bookverse.app):**
```
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
```

**For www subdomain:**
```
CNAME   www   YOUR_USERNAME.github.io
```

### 3. Enable HTTPS
- GitHub Pages → Custom domain → Check "Enforce HTTPS"

## File Structure

```
bookverse-site/
├── index.html          # Landing page
├── style.css           # Shared styles
├── privacy/
│   └── index.html      # Privacy policy
├── icon.png            # (optional) favicon
├── CNAME               # (optional) custom domain
└── README.md           # This file
```

## Updating the Privacy Policy

1. Edit `privacy/index.html`
2. Update the "Last Updated" date
3. Commit and push:
```bash
git add .
git commit -m "Update privacy policy"
git push
```

Changes go live automatically within a few minutes.

## App Store Connect

When submitting to the App Store, use this URL for your Privacy Policy:
```
https://YOUR_USERNAME.github.io/bookverse-site/privacy/
```

Or with custom domain:
```
https://bookverse.app/privacy/
```
