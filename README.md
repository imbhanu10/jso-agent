# JSO Candidate Experience Agent

AI-powered candidate satisfaction measurement tool for the JSO platform.
Built with Gemini 2.0 Flash + Vercel Edge Functions.

---

## Deploy to Vercel (Step-by-Step)

### Option A — Vercel CLI (recommended)

1. Install Vercel CLI (if you don't have it):
   ```
   npm install -g vercel
   ```

2. Inside the project folder, run:
   ```
   vercel
   ```
   Follow the prompts — choose your account, give the project a name, default settings are fine.

3. Add your Gemini API key as an environment variable:
   ```
   vercel env add GEMINI_API_KEY
   ```
   Paste your key when prompted. Select: Production, Preview, Development.

4. Redeploy with the env variable active:
   ```
   vercel --prod
   ```

Your live URL will be printed — e.g. `https://jso-agent.vercel.app`

---

### Option B — GitHub + Vercel Dashboard

1. Push this folder to a new GitHub repo.

2. Go to https://vercel.com → New Project → Import your repo.

3. In Project Settings → Environment Variables, add:
   - Key: `GEMINI_API_KEY`
   - Value: your Gemini API key (get one free at https://aistudio.google.com/apikey)

4. Click Deploy.

---

## Project Structure

```
jso-agent/
├── api/
│   └── chat.js          ← Vercel Edge Function (calls Gemini API)
├── public/
│   └── index.html       ← Full frontend (3 dashboards)
├── vercel.json          ← Routing config
└── package.json
```

## Get a Gemini API Key (free)

1. Go to: https://aistudio.google.com/apikey
2. Sign in with Google
3. Click "Create API Key"
4. Copy and use as GEMINI_API_KEY
