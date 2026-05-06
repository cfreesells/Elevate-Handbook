# Elevate Handbook

A static, multi-page web version of the Elevate Region New Rep Handbook.
No build step. No frameworks. Just HTML + CSS — ready for Vercel.

## Pages

- `index.html` — Welcome / table of contents
- `daily-sop.html` — Daily SOP
- `code-of-conduct.html` — Code of Conduct
- `recruiting.html` — Recruiting & Onboarding
- `getting-started.html` — Getting Started Checklist
- `setting-appointments.html` — Setting Appointments
- `pitch.html` — The Pitch
- `qualifying.html` — Locking & Qualifying
- `closing.html` — Closing & Confirming
- `in-the-home.html` — In the Home
- `booklist.html` — Booklist
- `workbook.html` — Workbook (notes saved in your browser via localStorage)

## Run locally

Just open `index.html` in a browser. Or, with Python:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to Vercel

### Option 1 — Push to GitHub, import in Vercel

1. Create a new GitHub repo (e.g. `elevate-handbook`).
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/elevate-handbook.git
   git push -u origin main
   ```
3. Go to [vercel.com/new](https://vercel.com/new), import the repo.
4. Framework preset: **Other** (no build command, no output directory needed).
5. Click **Deploy**.

### Option 2 — Vercel CLI (no GitHub required)

```bash
npm i -g vercel
vercel        # follow prompts; accept defaults
vercel --prod # deploy to production
```

## Edit content

Each page is a plain `.html` file. Edit the markup directly. The shared
sidebar nav lives at the top of each page — keep it in sync if you add
or rename pages.

## Configuration

`vercel.json` enables clean URLs (so `/pitch` works as well as `/pitch.html`)
and adds a few sensible security headers.
