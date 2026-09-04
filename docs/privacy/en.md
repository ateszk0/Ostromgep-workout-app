---
permalink: /privacy/en/
title: Ostromgep - Privacy Policy
---

# Ostromgep - Privacy Policy

_Last updated: 2026-09-01 • Draft - review with a lawyer before publishing._

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
- Your display name and (optional) profile picture
- App settings (theme, language, reminders, timer, app-blocker list)
- Your personal Gemini API key, if you enter one (stored encrypted via the Android Keystore)

This data is not sent anywhere unless you enable cloud sync or the AI features.

## Optional: Cloud backup (Firebase)

If you create an account and use "Upload to cloud", the app stores a copy of the
local data listed above in **Google Firebase** (Firestore + Authentication),
under a document keyed to your account.

- Sign-in: email + password, or Google Sign-In (which shares your email address and name).
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

## Other network activity

- **Update check:** on launch the app asks GitHub whether a newer release
  exists. GitHub sees your IP address. No personal data is sent.
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
