---
permalink: /privacy/en/
title: Ostromgep - Privacy Policy
---

# Ostromgep - Privacy Policy

_Last updated: 2026-09-18 • Draft - review with a lawyer before publishing._

**Controller:** Attila Nagy, ostromgep@atisn.com.
This is a personal fitness-tracking app for adults. It is not intended for children under 16.

## Short version

- Everything you log lives **on your device** by default.
- There are **no analytics, no ads, and no third-party trackers**.
- Two things are optional and off until you turn them on: **cloud backup** (Firebase) and the **AI features** (Google Gemini).
- You can **export** all your data as JSON, and **delete** your account and all data from inside the app.

## What the app stores on your device

Held locally in an on-device database and app settings:

- Workout history (exercises, sets, reps, weights, RPE/RIR, notes, timestamps)
- Routines, training blocks, custom exercises, folders
- Body-weight log (if you use it)
- Your display name
- App settings (theme, language, reminders, timer, app-blocker list, and
  whether the recovery heatmap draws a male or female body figure)
- Your personal Gemini API key, if you enter one (stored encrypted via the Android Keystore)

This data is not sent anywhere unless you enable cloud sync or the AI features.

## Optional: Cloud backup (Firebase)

If you create an account (email + password, or Google Sign-In, which shares
your email address and name) and choose to sync, the app stores a copy of the
local data listed above in **Google Firebase** (Firestore + Authentication),
under a document keyed to your account.

- Signing in on a device with no local data yet restores your data from the
  cloud automatically. If the device already has data, the app asks you to
  choose: upload (overwrite the cloud), download (overwrite the device), or
  merge (combine both, nothing deleted). You can also trigger any of these
  manually later from **Settings → Data & Sync**.
- Purpose: so you can restore your data on another device.
- Retention: kept until you delete it. **Settings → Data & Sync → "Delete account & data"**
  removes the cloud document and your sign-in account.
- Processor: Google (Firebase). See Google's privacy policy.

## Optional: AI features (Google Gemini)

The routine generator, weight suggestions, warm-up/cool-down protocols and
post-workout analysis send text to **Google's Gemini API**.

- **By default** this goes through a proxy server operated by the developer
  (Cloudflare Workers), which forwards it to Gemini. The proxy holds the API
  key; it also briefly stores your IP address (about 24 hours) to limit abuse.
- **What is sent:** the exercise/workout data relevant to the request, any text
  you type in the optional "additional preferences" box, and - only if you tick
  the box - your latest body weight. Age and height are not collected by the app.
- **Free-tier note:** the default path uses Gemini's free tier. Google may use
  content submitted on the free tier to improve their models, and it may be
  reviewed by humans. If you do not want this, enter your own Gemini API key in
  **Settings → AI** - the app then calls Gemini directly and Google's paid-tier
  terms (no training use) apply to your key.
- AI output is generated text and can be wrong. It is not medical or nutrition advice.
- Processors: Google (Gemini), Cloudflare (proxy).

## Optional: Friends

If you sign in and choose to add friends (by scanning or sharing a QR
code), the app shares a small, separate subset of your gamification stats
with people you've connected with:

- **What's shared:** your display name, league tier and score, weekly
  streak, this week's workout volume, workout count, which badges you've
  unlocked, your chosen avatar, frame and title, your finished-season
  results (month, tier, score), a "most improved" percentage, and your
  last few achievements (a record, a badge, a promotion, a streak
  milestone or a duel win) shown in your friends' activity feed.
  **Never shared:** your workout log, routines, body
  weight, or anything else in your private backup.
- **Who sees it:** only accounts you've connected with - scanning a QR
  code only sends a request, and the other person must approve it. There
  is no public directory, search, or global
  leaderboard. This data is stored in a separate Firestore location
  (`publicProfiles`) that any signed-in user of the app could technically
  read if they already knew your account ID, though nothing in the app
  exposes account IDs other than your own QR code.
- **Nudge delivery:** the app checks for nudges roughly every 30 minutes in the background (only while signed in and with nudge notifications on) and when you open Friends; there is no push server. The check reads only your own inbox.
- **Nudges and duels:** a friend can nudge you (a short predefined
  message, at most once every 4 hours per friend) and challenge you to a
  weekly volume duel. This stores your name, your friend's name and the
  duel's weekly volume totals in Firestore; nudges are deleted once
  delivered and duels a few weeks after they end. You can turn nudge
  notifications off in Settings -> Reminders.
- **Blocking:** you can block someone from **Friends**; they can then no
  longer send you requests, nudges or duels.
- **Stopping it:** remove the friend from **Friends** in the app - they
  stop seeing new updates immediately, though this doesn't retroactively
  un-show anything they already saw while you were connected.
- **Note on accuracy:** league tier, streak, and badges are calculated on
  your own device using its own clock, the same as everywhere else in the
  app (see the in-app Campaign guide) - there is no server-side check that
  this data is accurate, only that it was written by your own account.
- Processor: Google (Firebase), same as cloud backup above.

## Other network activity

- **Update check:** on launch the app asks GitHub whether a newer release
  exists. GitHub sees your IP address. No personal data is sent. If you choose
  to update, the app can download the new APK from GitHub and pass it to
  Android's package installer, which you confirm yourself; you can also just
  open the release page in a browser instead.
- **Android system backup:** the app disables Android's automatic Google cloud
  backup (`allowBackup=false`), so your local data is not copied to your Google
  account backup. Move it to a new device with the JSON export or cloud sync.
  (Direct device-to-device transfer during phone setup can still carry it.)

## Your rights

Depending on where you live (e.g. GDPR/EEA, UK, California) you may have the
right to access, correct, delete, or port your data, and to object to
processing. In this app:

- **Access / portability:** Settings → Data & Sync → "Export full data (JSON)".
- **Deletion:** Settings → Data & Sync → "Delete account & data" (removes cloud +
  account). Uninstalling removes the on-device data.
- For anything else, contact ostromgep@atisn.com.

## Changes

Material changes to this policy will be noted here with a new "last updated" date.

- 2026-09-21: Friends now use approval-based requests, blocking, nudges,
  weekly duels, an activity feed, avatars/frames/titles and season medals
  (see "Optional: Friends" above). Deleting your account also deletes
  these.
- 2026-09-18: added the optional Friends feature - a small subset of your
  gamification stats (name, league tier/score, streak, weekly volume,
  workout count, badges) is shared with people you connect with via QR
  code, and never anything from your private workout data.
- 2026-09-12: noted that signing in can now restore your data from the cloud
  automatically (if the device has none yet) or ask you to choose between
  upload/download/merge (if it does), instead of always requiring a manual
  "Upload to cloud" tap.
- 2026-09-06: noted that the recovery heatmap's male/female body-figure choice
  is part of app settings (and therefore included in a cloud backup if you use
  one), and that the update check can now download and install the new APK
  in-app.
