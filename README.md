# Metrias Medical Marketing Site

This is the single-page marketing website for Metrias Medical.

## Tech Stack

- **HTML5**: Single file structure.
- **CSS3**: Embedded in `index.html` (no external stylesheets).
- **Assets**: SVG logos and favicons.
- **Scripts**: None (Pure HTML/CSS).

## Project Structure

```
.
├── index.html      # Main website file
├── favicon.svg     # Browser tab icon (vector)
├── logo_mark.svg   # Header logo
└── README.md       # This file
```

## Deployment & Domain Configuration

### 1. Push to GitHub

Since you have GitHub Desktop:

1. Open GitHub Desktop.
2. You will see the commits in the history.
3. Click **"Publish repository"** in the top right.
4. Name the repository (e.g., `metrias-medical-site`).
5. Click **Publish Repository**.

### 2. Deployment Options

#### Option A: Netlify (Easiest DNS)

1. Log in to [Netlify](https://www.netlify.com/).
2. Click **"Add new site"** > **"Import an existing project"**.
3. Select **GitHub** and choose your `metrias-medical-site` repo.
4. **Build Settings**: Leave blank. Click **Deploy**.
5. Once deployed, go to **Domain management** > **Add custom domain**.
6. Enter `metriasmedical.com`.
7. Netlify will give you a CNAME (e.g., `metrias-medical.netlify.app`). Update your registrar's DNS to point `@` and `www` to this address.

#### Option B: GitHub Pages (Free, Built-in)

1. In your repository on GitHub.com, go to **Settings** > **Pages**.
2. Under "Build and deployment", select **Source** as `Deploy from a branch`.
3. Select branch: `main` / folder: `/(root)`. Click **Save**.
4. In "Custom domain", enter `metriasmedical.com` and click **Save**.
5. GitHub will provide DNS instructions (usually creating A records to GitHub's IPs and a CNAME for www).

#### Option C: Cloudflare Pages (Fastest Global CDN)

*See previous instructions if you prefer Cloudflare's performance features.*

## Local Development

Since this is a static site, you can view it by simply opening `index.html` in your web browser. No server or build process is required.
