# 🖥️ Personal Portfolio — Setup & Deployment Guide

## Folder Structure

```
portfolio/
├── index.html          ← The entire site (one clean file)
├── assets/             ← Create this folder yourself
│   ├── photo.jpg       ← Your profile photo
│   └── favicon.ico     ← Optional: browser tab icon
└── README.md           ← This file
```

> **Why single-file?** For a portfolio this size, one HTML file is easiest
> to edit, version-control, and deploy. All CSS and JS are embedded inside.

---

## ✏️ How to Personalize (Quick Checklist)

Open `index.html` in any text editor and search for `✏️` — every line
that needs your real info is marked with that emoji.

| What to change | Where (search for) |
|---|---|
| Your name | `Your Name` (3 places) |
| Hero tagline | `hero-role` paragraph |
| Hero description | `hero-desc` paragraph |
| About paragraphs | The 3 `<p>` blocks in `#about` |
| Stat numbers | `.fact-number` values |
| Photo | Replace `.about-image-placeholder` with `<img src="assets/photo.jpg">` |
| Project titles & descriptions | Each `.project-title` / `.project-desc` |
| Project links | Replace `href="#"` with real URLs |
| Email | `href="mailto:you@email.com"` |
| LinkedIn | `href="https://linkedin.com/in/yourprofile"` |
| GitHub | `href="https://github.com/yourusername"` |
| Footer year | `© 2025 Your Name` |

---

## 🚀 Run Locally

### Option A — Just open the file (simplest)
Double-click `index.html` — it opens directly in your browser.  
No server needed because there's no backend or module imports.

### Option B — Local dev server (recommended for live reload)
Requires Node.js installed ([nodejs.org](https://nodejs.org)).

```bash
# Install a simple static server globally (one-time)
npm install -g serve

# Navigate to your portfolio folder
cd path/to/portfolio

# Start the server
serve .
```

Then visit **http://localhost:3000** in your browser.

**Alternative with VS Code:**  
Install the **Live Server** extension → right-click `index.html` → *Open with Live Server*.  
The page auto-refreshes every time you save.

---

## 🌐 Deploy for Free (Get a Live Link)

### Option 1 — GitHub Pages (Recommended ⭐)
Free, reliable, and your URL will be `yourusername.github.io/portfolio`.

```bash
# 1. Create a new repo on github.com named "portfolio"

# 2. In your portfolio folder:
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/yourusername/portfolio.git
git push -u origin main

# 3. On GitHub: Settings → Pages → Source: Deploy from branch → main / root
```

Your live site will be ready in ~1 minute at:  
`https://yourusername.github.io/portfolio`

---

### Option 2 — Vercel (Easiest drag-and-drop)
1. Go to [vercel.com](https://vercel.com) and sign up (free)
2. Click **Add New → Project**
3. Drag your `portfolio` folder onto the upload area  
   **OR** connect your GitHub repo for auto-deploys on every push
4. Click **Deploy** — done in ~30 seconds

Your URL: `your-name.vercel.app`

---

### Option 3 — Netlify (Also great)
1. Go to [netlify.com](https://netlify.com) and sign up (free)
2. Drag the `portfolio` folder onto the **"Deploy manually"** drop zone
3. Get your live URL instantly

You can also set a custom subdomain like `yourname.netlify.app`.

---

## 🔧 Adding a Custom Domain (Optional)
If you own a domain (e.g., `yourname.dev`):
- All three platforms above (GitHub Pages, Vercel, Netlify) support custom
  domains for free in their settings panel.
- Point your domain's DNS CNAME record to the platform's URL.

---

## 🗂️ Adding More Projects
In `index.html`, find the `<!-- PROJECT CARD N -->` comment and copy
any existing `.project-card` block. Paste it inside `.projects-grid`
and update the title, description, tags, and links.

---

## 📱 Testing Responsiveness
- Open Chrome DevTools (`F12`) → click the device icon (top-left)
- Test at iPhone SE (375px), iPad (768px), and desktop (1440px)
- The layout switches to single-column on mobile automatically

---

*Built with plain HTML, CSS, and vanilla JS — no build tools, no dependencies.*