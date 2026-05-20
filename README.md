# GWA World Cup 2026 — Step by Step Setup

Follow these steps IN ORDER. Takes about 15 minutes total.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
STEP 1 — CREATE A GITHUB ACCOUNT (if you don't have one)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Go to https://github.com
2. Click "Sign up"
3. Enter your email, create a password, choose a username
4. Verify your email
→ Done. You have GitHub.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
STEP 2 — CREATE A GITHUB REPOSITORY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Click the "+" icon top right → "New repository"
2. Repository name: gwa-worldcup
3. Set to Public
4. Click "Create repository"
5. On the next screen, click "uploading an existing file"
6. Drag ALL 5 files from this zip into the upload area:
   - index.html
   - style.css
   - firebase-config.js  ← you'll edit this in Step 4
   - gwa-logo.png
   - .gitignore
7. Click "Commit changes"
→ Your files are now on GitHub.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
STEP 3 — SET UP FIREBASE (free)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Go to https://console.firebase.google.com
2. Click "Add project" → name it: gwa-worldcup → Continue → Create project
3. AUTHENTICATION:
   - Left menu → Build → Authentication → Get started
   - Click "Sign-in method" tab
   - Click "Google" → toggle Enable → enter your email → Save
4. FIRESTORE DATABASE:
   - Left menu → Build → Firestore Database → Create database
   - Choose "Start in test mode" → Next → Enable
5. GET YOUR CONFIG:
   - Click ⚙️ gear icon (top left) → Project settings
   - Scroll down to "Your apps" section
   - Click the </> Web icon
   - App nickname: gwa-worldcup → click "Register app"
   - You'll see a block of code with apiKey, authDomain, etc.
   - COPY ALL OF IT — you need it in the next step

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
STEP 4 — PASTE YOUR FIREBASE CONFIG
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Open firebase-config.js and replace each placeholder:

  "PASTE_YOUR_apiKey_HERE"            → your apiKey value
  "PASTE_YOUR_authDomain_HERE"        → your authDomain value
  "PASTE_YOUR_projectId_HERE"         → your projectId value
  "PASTE_YOUR_storageBucket_HERE"     → your storageBucket value
  "PASTE_YOUR_messagingSenderId_HERE" → your messagingSenderId value
  "PASTE_YOUR_appId_HERE"             → your appId value

Then upload the updated firebase-config.js to GitHub:
- Go to your GitHub repo → click firebase-config.js → click the ✏️ pencil icon
- Paste your updated content → click "Commit changes"

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
STEP 5 — DEPLOY ON CLOUDFLARE PAGES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Go to https://pages.cloudflare.com
2. Click "Sign up" → create a free account
3. Click "Create a project" → "Connect to Git"
4. Click "Connect GitHub" → authorize Cloudflare
5. Select your "gwa-worldcup" repository → click "Begin setup"
6. Build settings:
   - Framework preset: None
   - Build command: (leave completely empty)
   - Build output directory: /
7. Click "Save and Deploy"
8. Wait 30 seconds → your site is LIVE!
9. Copy your site URL — looks like: gwa-worldcup.pages.dev

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
STEP 6 — FINAL: ADD YOUR URL TO FIREBASE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
(Without this step, Google login won't work)
1. Go back to https://console.firebase.google.com
2. Left menu → Authentication → Settings tab
3. Scroll to "Authorized domains"
4. Click "Add domain"
5. Paste your Cloudflare URL (e.g. gwa-worldcup.pages.dev)
6. Click "Add"
→ DONE! Your site is fully live.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ACCEPTED EMAIL DOMAINS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  @gemsedu.com  ✓
  @gemsed.com   ✓
  @gemswa.com   ✓

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
POINTS SYSTEM
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  Exact score    → +3 points
  Correct result → +1 point
  Wrong          → 0 points

Live scores auto-refresh every 60 seconds from World Cup 2026 data.
