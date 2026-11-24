# 🎶 Jammify Status / Downtime Page

A minimal, ultra-fast static holding page for **Jammify** when server resources or bandwidth limits are temporarily exhausted due to high streaming traffic.

---

## ⚡ Highlights
- **Zero Heavy Assets:** Ultra-lightweight (pure HTML, modern CSS & vanilla JS) — loads in under **30ms**.
- **Dynamic Equalizer Animation:** Visual cues representing music and media streams.
- **Auto-Health Checker:** Continuously counts down 30s and automatically pings `https://jammify-music.vercel.app/`. When the server is back, it auto-redirects users seamlessly!
- **100% Free Hosting:** Can be deployed to **Cloudflare Pages**, **GitHub Pages**, or a separate **Vercel** project without touching your main Vercel project limits.

---

## 🚀 How to Deploy (Choose Any 1-Minute Option)

### Option 1: Free on Vercel (Separate project)
1. Push this folder to GitHub as a new repo (e.g., `jammify-status`).
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Deploy! You'll get a URL like `https://jammify-status.vercel.app`.

### Option 2: Free on Cloudflare Pages (Recommended - 0 bandwidth limits)
1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/) > **Workers & Pages**.
2. Click **Create Application** > **Pages** > **Connect to Git** (or drag & drop this folder).
3. Deploy! It will never hit bandwidth exhaustion.

---

## 🔁 How to Switch to this Page When Jammify is Down

### Method A: In Vercel Project Settings (Redirect)
When your main project is down:
1. Open your main **Jammify** project on Vercel.
2. Go to **Settings** > **Git** or **Domains**.
3. Or in your `next.config.mjs` / `vercel.json` redirects:
   ```json
   {
     "redirects": [
       {
         "source": "/:path*",
         "destination": "https://your-status-page-url.vercel.app",
         "permanent": false
       }
     ]
   }
   ```

### Method B: DNS / Domain Switch (Instant)
If you have a custom domain on Cloudflare or your DNS provider:
- Simply change the CNAME / A record or point your domain's fallback to the status page URL.
