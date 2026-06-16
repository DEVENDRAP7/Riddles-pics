# Riddles - Pics

Part of the **Riddles** brand (5-app family). See brand strategy in `../PLAN.md`.

## This App
- **Category:** picture / visual riddles. Heaviest content lift (needs image per riddle) → build LAST.
- **Repo:** https://github.com/DEVENDRAP7/Riddles-pics.git
- **Package id (FINAL, permanent):** `com.devendrap7.riddles.pics`
- **Accent color:** pink. Glyph: image.
- **Privacy policy URL:** TBD (separate per app).

## Brand Constraints (all 5 apps)
- Android only — no iOS.
- No login / signup. Progress local only.
- Splash → 3 animated game-styled onboarding screens (visual only, first run) → home.
- No premium plans / subscriptions. Ads only.
- Firebase Analytics + Crashlytics (own separate Firebase project + google-services.json). No Firestore.
- User data LOCAL only (Hive) — no cloud sync.
- AdMob: own App ID + own ad unit IDs (not shared with other apps).

## Game Format — "4 Pics 1 Word" style (pics app specific)
- Each level shows **4 images** that share **one common word**.
- Below the images: **empty letter boxes = number of letters** in the answer.
- A **scrambled letter bank** (answer letters + a few decoy letters) — player taps letters to fill the boxes.
- Player works out the word linking all 4 pictures and fills the boxes.
- 100 levels, sequential unlock, ascending difficulty (no easy/med/hard labels).

## Hint / Reveal — REWARDED ADS ONLY (no coins, no IAP, no hint currency)
- **NO coins and NO hint currency of any kind.** All help is gated purely by watching rewarded ads.
- **Reveal a letter:** player watches **3 rewarded ads → unlocks/reveals one correct letter** placed in its box (brand-standard 3-ads-per-hint).
- Player can repeat (watch 3 more rewarded ads → reveal another letter) as needed.
- Full solution: 1 more rewarded ad reveals the whole word (player still types/fills it). No purchasable hints ever.

## Monetization — Ads only (no IAP)
- Rewarded (reveal-a-letter), app-open, banner, interstitial (placement TBD). AdMob + consent.

## Content
- 100 entries, each = **answer word + 4 image concepts** (brief for the 4 pictures) + letter-bank (answer letters + decoys).
- 4 images per level × 100 = ~400 images to generate/source (AI-generated, e.g. Nano Banana / Figma). Bundle in assets. Heaviest content lift → build LAST.

## Stack
- Flutter, Riverpod, Hive, go_router, google_mobile_ads.

## Status
- [ ] Not started. Awaiting build command. Do NOT code until user says go.
