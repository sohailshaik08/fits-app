# Fits App — Deploy Guide

## What you have
- index.html       → the app your testers open
- api/claude.js    → the backend that holds your API key
- vercel.json      → Vercel config

---

## Step 1 — Create a free Vercel account
Go to vercel.com → Sign up with GitHub (free)

---

## Step 2 — Install Vercel CLI
Open Terminal and run:
  npm install -g vercel

---

## Step 3 — Deploy the app
In Terminal, navigate to this folder and run:
  vercel

Follow the prompts:
- "Set up and deploy?" → Y
- "Which scope?" → your account
- "Link to existing project?" → N
- "Project name?" → fits-app (or anything you like)
- "Directory?" → ./ (just press Enter)
- "Override settings?" → N

Vercel will give you a live URL like: https://fits-app.vercel.app

---

## Step 4 — Get your Anthropic API key
1. Go to console.anthropic.com
2. Sign up / log in
3. Go to "API Keys" → Create new key
4. Copy the key (starts with sk-ant-...)
5. Go to "Billing" → Add $10 credit (covers ~1,000 scans)

---

## Step 5 — Add your API key to Vercel
In Terminal run:
  vercel env add ANTHROPIC_API_KEY

Paste your key when prompted.
Select: Production, Preview, Development (all three)

Then redeploy:
  vercel --prod

---

## Step 6 — Test it yourself first
Open your Vercel URL on your phone.
Add a few items, generate outfits, make sure everything works.

---

## Step 7 — Share with testers
Send them your Vercel URL. That's it.
They open it in their phone browser — no app install, no account needed.

Each tester gets 20 AI scans tracked in their own browser.
Outfit generation is unlimited.

---

## Cost reminder
- Vercel hosting: $0
- 20 testers × 20 scans = ~$4-6 total on your Anthropic account
- Add $10 credit and you're covered with room to spare

---

## If you want to reset a tester's scan count
They can clear their browser's local storage for your site, or
you can remove the scan limit for v2 once you're done testing costs.
