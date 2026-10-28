# 🌿 Clear Thicket Website (`clearthicket.co.uk`)

The official portfolio, app showcase, and privacy hub for **Clear Thicket** — an independent native Android development studio.

Home to:
- **LeafRescue** (`com.clearthicket.leafrescue`): AI Plant Care, Leaf Disease Diagnosis & Smart Watering Tracker.
- **BreatheRun** (`com.darren.breatherun`): Audio-Guided Breathing Coach & GPS Running Tracker.

---

## 📁 Site Architecture & Directory Structure

```text
clearthicket-website/
├── index.html                  # Clear Thicket Studio Homepage
├── about.html                  # About Darren Bromwich & Studio Philosophy
├── privacy.html                # Clear Thicket Umbrella Privacy Policy
├── contact.html                # Studio & App Contact Directory
├── style.css                   # Core responsive styling & studio card components
├── themes.css                  # Multi-palette theme system (Forest, Ocean, Azure, etc.)
├── script.js                   # IntersectionObserver scroll animations & mobile nav
├── CNAME                       # clearthicket.co.uk
├── robots.txt                  # Search engine crawl rules
├── sitemap.xml                 # XML sitemap covering all pages and app routes
├── site.webmanifest            # Progressive web app manifest
├── favicon/                    # Clear Thicket brand SVG favicon
├── images/
│   ├── brand/
│   │   ├── logo-horizontal.svg # Full Clear Thicket Studio wordmark & emblem
│   │   └── logo-icon.svg       # Standalone emblem
│   └── apps/
│       ├── leafrescue-icon-512.png
│       └── breatherun-icon-512.png
│
├── leafrescue/                 # 🌿 LeafRescue App Section
│   ├── index.html              # Full app showcase (AI diagnosis, Gemini, watering, £4.99 unlock)
│   ├── privacy.html            # Google Play Store Privacy Policy for LeafRescue
│   ├── support.html            # LeafRescue Support & Help Center
│   ├── style.css
│   ├── themes.css
│   ├── script.js
│   └── images/                 # App icon, feature graphic & real app screenshots
│
└── breatherun/                 # 🫁 BreatheRun App Section
    ├── index.html              # BreatheRun app landing page
    ├── privacy.html            # BreatheRun Privacy Policy
    ├── support.html            # BreatheRun Support Page
    ├── style.css
    ├── themes.css
    ├── script.js
    ├── favicon/                # BreatheRun brand favicons
    └── images/                 # BreatheRun screenshots & brand marks
```

---

## 🚀 Local Development & Preview

Because this site is built purely with standards-compliant HTML5, CSS3, and modern vanilla JavaScript without heavy Node build steps, you can run and test it locally using any static HTTP server:

```bash
# Using Python
cd D:\Code\AndroidApps\clearthicket-website
python -m http.server 8080

# Or using Node / npx
npx serve .
```

Then visit:
- **Studio Homepage:** [http://localhost:8080/](http://localhost:8080/)
- **LeafRescue Showcase:** [http://localhost:8080/leafrescue/](http://localhost:8080/leafrescue/)
- **LeafRescue Google Play Privacy Policy:** [http://localhost:8080/leafrescue/privacy.html](http://localhost:8080/leafrescue/privacy.html)
- **BreatheRun Showcase:** [http://localhost:8080/breatherun/](http://localhost:8080/breatherun/)
- **About Developer:** [http://localhost:8080/about.html](http://localhost:8080/about.html)
- **Contact:** [http://localhost:8080/contact.html](http://localhost:8080/contact.html)

---

## 🌐 Deploying to `clearthicket.co.uk`

The website is ready to deploy directly to **GitHub Pages**, **Cloudflare Pages**, **Netlify**, or **Vercel**:

### Option 1: GitHub Pages
1. Create a repository on GitHub (e.g. `darren221980/clearthicket-website`).
2. Push the files in `D:\Code\AndroidApps\clearthicket-website`.
3. In GitHub repo settings > **Pages**, set source to `main` branch root (`/`).
4. Under **Custom domain**, enter `clearthicket.co.uk` (the `CNAME` file in the repo will automatically link it).
5. In your DNS provider for `clearthicket.co.uk`, point the `@` record to GitHub's IPs or CNAME to `<username>.github.io`.

### Option 2: Cloudflare Pages
1. Connect repository in Cloudflare Dashboard.
2. Build settings: Framework: None (Static HTML), Build command: (leave empty), Output directory: `.`.
3. Add custom domain `clearthicket.co.uk`.

---

## 📄 Google Play Store Compliance

When publishing **LeafRescue** (`com.clearthicket.leafrescue`) to the Google Play Console:
- **Privacy Policy URL:** `https://clearthicket.co.uk/leafrescue/privacy.html`
- **Developer Support Email:** `leafrescue@clearthicket.co.uk`
- **Developer Website:** `https://clearthicket.co.uk/leafrescue/`
