# HealthLoop — Android APK Build Guide
## Complete step-by-step from GitHub to phone

---

## FILES TO UPLOAD TO GITHUB FIRST

Before anything else, push ALL these files to your repository
(kumrunnaharkeya/keya-s-lens) in the root folder:

```
keya-s-lens/
├── index.html          ← main app
├── admin.html          ← admin portal
├── manifest.json       ← PWA config (NEW - replace old one)
├── sw.js               ← service worker (NEW - replace old one)
├── icon-192.png        ← app icon 192x192 (NEW)
├── icon-512.png        ← app icon 512x512 (NEW)
└── privacy-policy.html ← required by stores
```

---

## METHOD 1 — PWABUILDER (Easiest, 10 minutes, free)

### Step 1 — Wait for GitHub Pages to deploy
After pushing files, wait 2–3 minutes for GitHub Pages to update.
Visit: https://kumrunnaharkeya.github.io/keya-s-lens/
Check that the app loads correctly.

### Step 2 — Open PWABuilder
Go to: https://www.pwabuilder.com

### Step 3 — Enter your URL
Type in the search box:
```
https://kumrunnaharkeya.github.io/keya-s-lens/
```
Click Start

### Step 4 — Wait for analysis
PWABuilder will scan your app (~30 seconds).
You should see a green score for Manifest and Service Worker.
If there are warnings, ignore them — the app will still build.

### Step 5 — Package for Android
1. Click "Package for stores"
2. Click the Android tile
3. Fill in these details:
   - Package ID:    com.healthloop.app
   - App name:      HealthLoop
   - Version:       1.0.0
   - Version code:  1
4. Leave all other options as default
5. Click "Download"

### Step 6 — You receive a ZIP file
Inside the ZIP you will find:
- app-release-unsigned.apk  ← use this to install directly
- (other signing files for Play Store)

### Step 7 — Install on your Android phone

Option A — Transfer via USB:
1. Connect phone to laptop with USB cable
2. On phone: Allow File Transfer
3. Copy the APK to your phone Downloads folder
4. On phone: open the APK file

Option B — Transfer via WhatsApp/Telegram to yourself:
1. Send the APK file to yourself on WhatsApp
2. Open on phone and tap Download
3. Open the downloaded APK

Option C — Transfer via Google Drive:
1. Upload APK to Google Drive
2. Open Drive on phone
3. Download and open the APK

### Step 8 — Enable Unknown Apps (one time only)
When you tap the APK, Android will ask:
Settings → Install unknown apps → Allow from this source
Tap Allow, then Install

### Step 9 — Done!
HealthLoop will appear on your home screen like a native app.

---

## METHOD 2 — DIRECT PHONE INSTALL (No PC needed)

If you just want to install on YOUR phone right now:

1. Open Chrome on your Android phone
2. Go to: https://kumrunnaharkeya.github.io/keya-s-lens/
3. Log in to the app
4. Tap the 3-dot menu (⋮) in Chrome
5. Tap "Add to Home screen"
6. Tap "Add"

HealthLoop will appear on your home screen with the teal icon.
This is a PWA install — works like an app, no APK needed.

---

## METHOD 3 — GOOGLE PLAY STORE (Proper listing, $25)

For a real Play Store listing visible to everyone:

### Requirements
- Google account
- $25 one-time developer registration fee
- A computer (Windows/Mac/Linux)

### Step 1 — Register as developer
1. Go to: https://play.google.com/console
2. Sign in with your Google account
3. Pay the $25 registration fee
4. Fill in your developer profile

### Step 2 — Get the signed APK from PWABuilder
Follow Method 1 above, but in Step 5:
- Choose "Android App Bundle (.aab)" instead of APK
- Follow the signing instructions PWABuilder provides

### Step 3 — Create app in Play Console
1. Click "Create app"
2. App name: HealthLoop
3. Default language: English
4. Category: Health & Fitness
5. Tick: Free app
6. Tick: This app is not primarily directed at children

### Step 4 — Fill store listing
Content rating → complete the questionnaire
(Select "Health" category, no violence, no user-generated content)

Store listing details:
- Short description (max 80 chars):
  "PCOS & sugar health tracker with fasting, GI table & food logging"

- Full description (max 4000 chars):
  HealthLoop is your personal health companion built especially for
  women managing PCOS, insulin resistance, and weight goals.

  FEATURES:
  🍽️ Food Log — 500+ foods including Bangladeshi & South Asian dishes
  ⏱️ Fasting Tracker — 16:8, 18:6, OMAD with fat-burning stage alerts
  📊 Insights — 7-day calorie charts and macro tracking
  ⚖️ Weight & BMI — Body fat calculator (3 methods, metric + imperial)
  🩺 Sugar Health — T2D diabetes risk indicator + IR calculator
  🌸 PCOD Tracker — Cycle, symptoms, mood and medication log
  👥 Health Circle — Share progress with trusted friends
  📋 GI Table — Glycemic index reference for 90+ foods
  🌿 Personal Coaching — Connect with a health coach directly

  DISCLAIMER: HealthLoop is a wellness tracking tool, not a medical
  device. Always consult your doctor for medical decisions.

### Step 5 — Upload your AAB
Internal testing → Production → Upload the .aab file

### Step 6 — Submit for review
Review takes 1–7 days for new apps.
You will receive an email when approved.

---

## PRIVACY POLICY (Required by Google Play)

Your privacy policy is already built. Host it at:
https://kumrunnaharkeya.github.io/keya-s-lens/privacy-policy.html

Use this URL in the Play Console "Privacy policy" field.

---

## TROUBLESHOOTING

### "App not installed" error
→ Your phone already has an older version. Uninstall it first.

### PWABuilder score is low
→ Make sure manifest.json and sw.js are uploaded to GitHub.
→ Wait 5 minutes after pushing for GitHub Pages to update.
→ Clear browser cache and retry.

### "Parse error" when opening APK
→ The download may be corrupted. Re-download and retry.

### App crashes on open
→ Make sure index.html is working at your GitHub Pages URL first.
→ The APK is just a wrapper — if the web app works, the APK works.

### Firebase not connecting inside APK
→ This is expected — Firebase connects over internet.
→ Make sure your phone has mobile data or WiFi.

---

## COST SUMMARY

| What                    | Cost        |
|-------------------------|-------------|
| PWABuilder APK          | FREE        |
| GitHub Pages hosting    | FREE        |
| Firebase (Spark plan)   | FREE        |
| Google Play listing     | $25 one-time|
| Apple App Store         | $99/year    |

---

## YOUR APP DETAILS

- URL:        https://kumrunnaharkeya.github.io/keya-s-lens/
- Package ID: com.healthloop.app
- App name:   HealthLoop
- Theme:      #0EA5A0 (teal)
- Privacy:    https://kumrunnaharkeya.github.io/keya-s-lens/privacy-policy.html

