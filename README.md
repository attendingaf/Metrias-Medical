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
2. You will see the "Initial commit" in the history.
3. Click **"Publish repository"** in the top right toolbar.
4. Name the repository (e.g., `metrias-medical-site`) and uncheck "Keep this code private" if you want it to be a public site (private is fine too for Cloudflare).
5. Click **Publish Repository**.

### 2. Deploy to Cloudflare Pages (Recommended)

1. Log in to the [Cloudflare Dashboard](https://dash.cloudflare.com/) > **Workers & Pages**.
2. Click **Create Application** > **Pages** > **Connect to Git**.
3. Select your new `metrias-medical-site` repository.
4. **Build Settings**:
   - **Framework Preset**: None / Static HTML
   - **Build Command**: (Leave blank)
   - **Build Output Directory**: (Leave blank / root)
5. Click **Save and Deploy**.

### 3. Configure Custom Domain (Godaddy, Namecheap, etc.)

Once deployed on Cloudflare Pages, you will get a `.pages.dev` URL. To map `metriasmedical.com`:

1. In Cloudflare Pages project settings, go to **Custom Domains**.
2. Click **Set up a custom domain**.
3. Enter `metriasmedical.com` and click **Continue**.

#### If you use Cloudflare DNS (Best)

- Cloudflare will automatically add the CNAME record for you. Just confirm the assignment.

#### If you use External DNS (Godaddy/Namecheap)

Cloudflare will give you a CNAME target (e.g., `metrias-medical-site.pages.dev`).

1. Log in to your registrar (e.g., Godaddy).
2. Go to **DNS Management**.
3. **Delete** any existing A records for `@` or `www`.
4. Add the following records:

| Type | Name | Content / Value | TTL |
|------|------|-----------------|-----|
| CNAME | @   | `metrias-medical-site.pages.dev` | Auto / 1 Hour |
| CNAME | www | `metrias-medical-site.pages.dev` | Auto / 1 Hour |

*Note: Some registrars (like Godaddy/Namecheap) don't support CNAME at the root (@). If so, Cloudflare Pages will ask you to verify via a TXT record, or you might prefer to move your Nameservers to Cloudflare (Free) for easier management.*

## Local Development

Since this is a static site, you can view it by simply opening `index.html` in your web browser. No server or build process is required.
