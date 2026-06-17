# Riddles - Pics

Part of the **Riddles** brand (5-app family). See brand strategy in `../PLAN.md`.

## Brand Brief (the big picture)
**Riddles** is a brand umbrella over 5 separate Android puzzle apps — Brain, Maths, Fun, Words, Pics — published under one developer account so they read as one family (tree model: brand = trunk, each app = branch, same DNA, different content). The format is modeled on proven, top-grossing puzzle apps (100 levels, ad-gated hints, 100% free).

**What we are building:** a single clean **template app**, then cloning it into the other repos by swapping content JSON + theme color + icon + name. Same code, 5 independent GitHub repos, 5 Play listings, cross-promoted via a "More Riddles →" section in each.

**Core loop (brand standard):** 100 sequential levels, ascending difficulty (no easy/med/hard labels). **Pics is the exception to the type-answer format** → it uses a **"4 Pics 1 Word"** mechanic: 4 images sharing one word, empty boxes = letter count, scrambled letter bank to tap. Stuck → watch **3 rewarded ads** to **reveal one correct letter** (repeatable); **1 more rewarded ad** reveals the full word (user still fills it).

**Monetization:** ads only — rewarded (reveal-a-letter), app-open, banner, interstitial (placement TBD). AdMob + GDPR consent. **No coins, no hint currency, no IAP, no premium, no subscriptions.**

**Data/Backend:** Firebase Analytics + Crashlytics only (5 separate projects), **no Firestore**. All user data (progress, settings, onboarding flag) **local-only via Hive** — no login, no cloud sync.

**Tech:** Flutter, **Android only**. Riverpod (state), Hive (local DB), go_router (nav), google_mobile_ads, firebase_core/analytics/crashlytics. Per-app: own applicationId, icon, name, accent color, content JSON, privacy-policy URL.

**Flow:** Splash → app-open ad → 3 animated game-styled onboarding screens (first run only) → home (level grid: locked/unlocked/solved + "More Riddles") → play screen. Plus settings (theme/sound/rate/share/privacy) and a rate-app popup every 3rd home visit.

**Pics content note:** each level = 1 answer word + **4 images** + letter bank → ~400 images to generate/source. Heaviest content lift → **build this app LAST**.

**Goal/outcome:** ship 5 lightweight, offline, ad-funded puzzle apps fast by reusing one battle-tested template, building a recognizable brand family on the Play Store.

## This App
- **Category:** picture / visual riddles. Heaviest content lift (needs image per riddle) → build LAST.
- **Repo:** https://github.com/DEVENDRAP7/Riddles-pics.git
- **Package id (FINAL, permanent):** `com.devendrap7.riddles.pics`
- **Accent color:** pink. Glyph: image.
- **Privacy policy URL:** https://devendrap7.github.io/Riddles-pics/privacy-policy.html (live, GitHub Pages).

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
