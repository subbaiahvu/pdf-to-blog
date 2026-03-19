# PDF → Blogger Post Generator
### postalrulings.blogspot.com · AI-Powered Deployment

---

## 🚀 Deploy to Vercel in 10 Minutes

### Step 1 — Get Your Anthropic API Key

1. Go to **https://console.anthropic.com**
2. Sign up / log in
3. Click **API Keys → Create Key**
4. Copy the key — it starts with `sk-ant-…`
5. Add credits: **Billing → Add Credits** (start with $5 — enough for ~300–500 posts)

---

### Step 2 — Upload to GitHub

1. Go to **https://github.com** and sign up (free)
2. Click **"New repository"**
3. Name it: `pdf-to-blogger`
4. Set to **Public** (required for free Vercel)
5. Click **"Create repository"**
6. Click **"uploading an existing file"**
7. Upload ALL THREE files:
   - `index.html`
   - `api/generate.js`  ← make sure this is inside an `api/` folder
   - `vercel.json`
8. Click **"Commit changes"**

---

### Step 3 — Deploy on Vercel

1. Go to **https://vercel.com** → Sign up with GitHub (free)
2. Click **"Add New Project"**
3. Click **"Import"** next to your `pdf-to-blogger` repository
4. Leave all settings as default
5. Click **"Deploy"**
6. Wait ~30 seconds → you'll see **"Congratulations!"**

---

### Step 4 — Add Your API Key (CRITICAL)

Without this step the app will not work.

1. In Vercel, go to your project dashboard
2. Click **Settings → Environment Variables**
3. Click **"Add New"**
4. Fill in:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** `sk-ant-YOUR_KEY_HERE`
   - **Environments:** ✅ Production ✅ Preview ✅ Development
5. Click **Save**
6. Go to **Deployments → ⋯ → Redeploy** (required for env vars to take effect)

---

### Step 5 — Your App is Live! 🎉

Your URL will be: `https://pdf-to-blogger.vercel.app` (or similar)

Share it with anyone — they can use it directly in their browser.

---

## 📁 File Structure

```
pdf-to-blogger/
├── index.html          ← The complete web app UI
├── api/
│   └── generate.js     ← Serverless proxy (keeps API key secret)
└── vercel.json         ← Vercel routing config
```

---

## 💰 Cost Estimate

| Usage | Approx. Cost |
|-------|-------------|
| 1 PDF post (short OM, 2–3 pages) | ~$0.01–0.02 |
| 1 PDF post (long ruling, 6+ pages) | ~$0.03–0.05 |
| 100 posts | ~$1–5 |
| $5 credit | ~150–500 posts |

---

## ❓ Troubleshooting

**"ANTHROPIC_API_KEY is not set"**
→ You forgot Step 4. Add the env var and redeploy.

**"Error: generation failed"**
→ Check your API key is correct and you have credits at console.anthropic.com

**Blank preview / no output**
→ Open browser DevTools (F12) → Console tab → look for red error messages

**PDF not uploading**
→ File must be a real PDF. Max recommended size: 10MB

---

## 🔄 Updating the App

1. Edit `index.html` locally
2. Go to GitHub → your repo → `index.html` → click the pencil ✏️ icon → paste new content → Commit
3. Vercel auto-deploys within 30 seconds

---

*Built for postalrulings.blogspot.com · Government Document Formatting Tool*
