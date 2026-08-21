# lukezumwalt.github.io
Personal Website Source

## File Structure

```
personal-site/
├── index.html          # Main page — edit this with your info
├── CNAME               # Your custom domain — edit this
├── css/
│   └── styles.css      # All styling — edit colors via CSS variables at top
├── js/
│   └── main.js         # Minimal JS — scroll behavior + active nav
└── assets/
    └── images/
        └── favicon.ico # Drop your favicon here
```

## Setup: GitHub Pages

1. Create a GitHub repo. Name it anything (e.g. `personal-site` or `yourname.github.io`).
   - If you name it `yourusername.github.io` it auto-enables Pages on the `main` branch.
   - Otherwise go to **Settings → Pages** and set Source to `main` branch, `/ (root)`.

2. Push all these files to the repo.

3. GitHub Pages will serve your site at `https://yourusername.github.io`.

## Connecting Your Custom Domain

### Step 1: Edit the CNAME file
Replace the contents of `CNAME` with your domain (no `https://`, no trailing slash):
```
yourdomain.com
```

### Step 2: Configure DNS at your registrar

Go to your domain registrar (Namecheap, Cloudflare, Google Domains, etc.)
and add the following DNS records:

#### A Records (point apex domain → GitHub)
Add all four of these A records for your root domain (@):

| Type | Host | Value          |
|------|------|----------------|
| A    | @    | 185.199.108.153 |
| A    | @    | 185.199.109.153 |
| A    | @    | 185.199.110.153 |
| A    | @    | 185.199.111.153 |

#### CNAME Record (point www → GitHub)
| Type  | Host | Value                        |
|-------|------|------------------------------|
| CNAME | www  | yourusername.github.io       |

### Step 3: Set custom domain in GitHub
- Go to your repo → **Settings → Pages**
- Under "Custom domain" enter `yourdomain.com` and click Save
- Check "Enforce HTTPS" once it appears (may take a few minutes)

### Step 4: Wait for DNS propagation
DNS changes can take anywhere from a few minutes to 48 hours.
You can check propagation at https://dnschecker.org

## Customization Checklist

- [X] Replace "Your Name" everywhere in `index.html`
- [X] Update monogram initials in the header
- [X] Fill in your LinkedIn / GitHub / GitLab handles in the link cards
- [X] Update `CNAME` with your actual domain
- [X] Write your About section
- [X] Add real project entries
- [ ] Drop a `favicon.ico` in `assets/images/`
- [X] Tweak `--accent` color in `css/styles.css` to your preference
