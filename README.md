# Ostromgep

**Ostromgep** is an Android workout application built for efficiency and results. It pairs advanced set-by-set tracking with AI-driven planning and full mesocycle periodization, wrapped in a deliberate, high-contrast dark interface designed for the gym.

## Key Features

- **AI Workout Generator & Evaluation**: Powered by **Google Gemini** (via a Cloudflare Worker proxy, or your own API key), the app generates personalized multi-day routines, suggests starting weights from your history, produces dynamic warm-up / static cooldown protocols with illustrated stretches, and writes a bilingual post-workout analysis into your log.
- **Training Blocks (Periodization)**: Plan a 4–8 week mesocycle with automatic deload weeks from an existing routine rotation or an AI-generated split. Each week adds a fixed number of working sets per exercise; deload weeks halve them. Progression is **completion-driven** — the app checks off each workout you finish and you advance to the next week yourself, it never rolls over on a timer.
- **Advanced Set Tracking**: Log sets, reps, weight and RPE with a fast table UI. Supersets, warm-up sets, a swipe-to-delete gesture, and a distraction-free **Simple view** for one-set-at-a-time logging.
- **Progressive Overload**: AI weight suggestions based on prior performance, machine-specific weight-increment settings, **Cable Machine Presets**, and an in-workout **Plate Calculator**.
- **Statistics**: Summary tiles (volume, time, longest streak, monthly totals), a 7-day heatmap, muscle-group distribution (chart + body map), top exercises, personal records, **Stalled Lifts** detection with coaching hints (deload / technique / variation / more volume), and **1RM Progression** — an estimated one-rep-max trend per exercise (Epley / Brzycki).
- **The Campaign (Hadjárat)**: A full siege-themed gamification layer computed entirely from your workout history. Earn **XP and levels** from every workout, wage a **weekly siege** against a castle sized to your own target volume (5 visual tiers, from an Outpost to a full Citadel, that crumbles as you log volume and keeps escalating past 100% up to a 150% overrun), clear 3 rotating **weekly quests**, climb a **Copper-to-Diamond league** each monthly season, and unlock **57 badges** across Bronze/Silver/Gold/Platinum/Diamond difficulty - from milestones to creative feats (a workout on a full moon, on Christmas Eve, 15,000 kg in one session...). Most badges also unlock a **profile avatar**. A dedicated Campaign screen has a full in-app guide, a tap-for-detail badge grid, and a league ladder showing exactly how far you are from the next tier.
- **Friends & Social**: Add friends by scanning a QR code (requests need approval; you can block people), then compare on a friends-only **leaderboard** with six rankings (Season, Total volume, This week, Streak, Badges, Most improved) and a gold/silver/bronze podium. A friend's screen shows their rank, stats, a comparison with yours, badges and season medals. Send a **nudge** (with a cooldown), challenge a friend to a **weekly 1v1 volume duel**, and follow an **activity feed** of records, badges and promotions. Pick a badge-unlocked **avatar**, a league-unlocked **frame** and a **title** - they are your profile picture everywhere. Only a small, separate subset of your stats is shared, never your workout log.
- **Customizable Dashboard**: Reorder or hide the home widgets — Ready to Siege recovery heatmap (front + back body figure, switchable between a male and female body from a gear on the card), Next Mission, Weekly Battle Log, Quick Metrics, Today's Workout, Campaign status, Training Block status, Stalled Lifts, Fresh Conquests (recent PRs) and a Siege Watch castle preview.
- **Cloud Sync & Data Portability**: Back up and restore history, custom exercises, routines and body-weight data via Firebase. On sign-in the app pulls your data down automatically if the device is empty, otherwise it asks whether to upload, download or **merge**. The merge (union both sides, drop nothing) or overwrite, in either direction. Every destructive sync/import first writes a local auto-backup you can restore. Import/export full data as JSON, and **import a Hevy, Strong or FitNotes CSV export** to migrate your history in.
- **Focus Mode (App Blocker)**: An anti-procrastination overlay that nudges you back to your workout if you open another app mid-session.
- **QR Code Routine Sharing**: Data-agnostic serialization — share routines including fully custom exercises, no dependency on factory defaults.
- **Smart Rest Timer**: Foreground-service rest timer with live notifications between sets.
- **Exercise Library**: Built-in video form demonstrations and fuzzy-matching search by name or muscle group.
- **Auto Updater**: Checks GitHub for new releases on startup and notifies you without interrupting a workout. Download and install the matching APK (debug or release) right from the popup, or open the GitHub release page manually - your choice.

## Design

- **Tactical, dark or light**: Choose **System, Light or Dark** in Settings. Dark is a warm near-black (not pure black); Light is a warm paper tone (not screen-white) — neither is a plain Material default. A single deliberate accent per your choice runs through both. Surfaces read through tone and a 1px top edge highlight rather than heavy shadows.
- **Bundled typography**: **Oswald** (condensed display) for headers against **IBM Plex Sans** for body — shipped as variable fonts, not system defaults.
- **Phosphor icon set**: A single coherent icon family for the UI chrome, bundled as local vector drawables. Muscle-group icons are a separate set — a zoomed crop of an anatomy render (gray body, target muscle in red) per group.
- **Accent colors**: Red (default), Yellow, Green, Blue, Purple — retuned to earthy, muted tones with per-accent contrast handling.
- **Avatars**: custom vector avatars (crossed swords, trophy, shield, anvil, crown, owl, phoenix, dragon, ...) coloured by the tier of the badge that unlocks them.
- **Animated splash screen**: Android 12+ compliant splash on startup.

## Tech Stack

- **Jetpack Compose** + **Material 3** — the entire UI, with a custom design-system layer (`OstromgepTheme`, semantic color/type/shape/spacing tokens, reusable primitives).
- **Google Gemini** (`gemini-3.6-flash`) via the Google AI client SDK (`com.google.ai.client.generativeai`) and a Cloudflare Worker proxy - AI generation and evaluation.
- **Firebase** (Auth + Firestore) — Google sign-in, cloud sync and the Friends feature (rules in `firestore.rules`).
- **Room** — local persistence for the collections that grow with use (history, templates, exercise library, routine rotations, body-weight log, cable presets, training blocks).
- **Media3 ExoPlayer** — exercise-demo video playback.
- **Coil** (+ SVG & GIF decoders) — image and stretch-illustration loading.
- **ZXing** (`zxing-android-embedded`) — QR scan/generate for routine sharing and friend requests.
- **WorkManager** — daily reminders and the ~30-minute friend-nudge check (no push server).
- **EncryptedSharedPreferences** — on-device storage of the user's Gemini API key.
- **Kotlin Coroutines + Flow** — reactive state; **StateFlow**-backed `ViewModel` (no DI framework).
- **Foreground Service** — the rest timer and workout-keep-alive.
- Navigation is a lightweight in-app screen state + `HorizontalPager`; charts are drawn directly on `Canvas`.

## Get started

- Download the latest release from the [Releases](https://github.com/ateszk0/Ostromgep-workout-app/releases) page.
- Read the guide: [English Tutorial](tutorial_en.md) · [Magyar Útmutató](tutorial_hu.md)
