# Ostromgep

**Ostromgep** is an Android workout application built for efficiency and results. It pairs advanced set-by-set tracking with AI-driven planning and full mesocycle periodization, wrapped in a deliberate, high-contrast dark interface designed for the gym.

## Key Features

- **AI Workout Generator & Evaluation**: Powered by **Google Gemini** (via a Cloudflare Worker proxy, or your own API key), the app generates personalized multi-day routines, suggests starting weights from your history, produces dynamic warm-up / static cooldown protocols with illustrated stretches, and writes a bilingual post-workout analysis into your log.
- **Training Blocks (Periodization)**: Plan a 4–8 week mesocycle with automatic deload weeks. Choose block length, deload frequency, and a weekly set-volume ramp; the app builds a week-by-week plan from an existing routine rotation or an AI-generated split, scales working sets each week, and halves them on deload weeks.
- **Advanced Set Tracking**: Log sets, reps, weight and RPE with a fast table UI. Supersets, warm-up sets, a swipe-to-delete gesture, and a distraction-free **Simple view** for one-set-at-a-time logging.
- **Progressive Overload**: AI weight suggestions based on prior performance, machine-specific weight-increment settings, **Cable Machine Presets**, and an in-workout **Plate Calculator**.
- **Statistics**: Summary tiles (volume, time, longest streak, monthly totals), a 7-day heatmap, muscle-group distribution (chart + body map), top exercises, personal records, **Stalled Lifts** detection with coaching hints (deload / technique / variation / more volume), and **1RM Progression** — an estimated one-rep-max trend per exercise (Epley / Brzycki).
- **The Campaign (Hadjárat)**: A full siege-themed gamification layer computed entirely from your workout history. Earn **XP and levels** from every workout, wage a **weekly siege** against a castle sized to your own target volume (5 visual tiers, from an Outpost to a full Citadel, that crumbles as you log volume and keeps escalating past 100% up to a 150% overrun), clear 3 rotating **weekly quests**, climb a **Copper-to-Diamond league** each monthly season, and unlock **34 badges** across Bronze/Silver/Gold/Platinum difficulty. A dedicated Campaign screen has a full in-app guide, a tap-for-detail badge grid, and a league ladder showing exactly how far you are from the next tier.
- **Customizable Dashboard**: Reorder or hide the home widgets — Ready to Siege recovery heatmap, Next Mission, Weekly Battle Log, Quick Metrics, Today's Workout, Campaign status, Training Block status, Stalled Lifts, Fresh Conquests (recent PRs) and a Siege Watch castle preview.
- **Cloud Sync & Data Portability**: Back up and restore history, custom exercises, routines and body-weight data via Firebase. Import/export full data as JSON, and **import a Hevy CSV export** to migrate your history in.
- **Focus Mode (App Blocker)**: An anti-procrastination overlay that nudges you back to your workout if you open another app mid-session.
- **QR Code Routine Sharing**: Data-agnostic serialization — share routines including fully custom exercises, no dependency on factory defaults.
- **Smart Rest Timer**: Foreground-service rest timer with live notifications between sets.
- **Exercise Library**: Built-in video form demonstrations and fuzzy-matching search by name or muscle group.
- **Auto Updater**: Checks GitHub for new releases on startup and notifies you without interrupting a workout.

## Design

- **Tactical, dark or light**: Choose **System, Light or Dark** in Settings. Dark is a warm near-black (not pure black); Light is a warm paper tone (not screen-white) — neither is a plain Material default. A single deliberate accent per your choice runs through both. Surfaces read through tone and a 1px top edge highlight rather than heavy shadows.
- **Bundled typography**: **Oswald** (condensed display) for headers against **IBM Plex Sans** for body — shipped as variable fonts, not system defaults.
- **Phosphor icon set**: A single coherent icon family, bundled as local vector drawables.
- **Accent colors**: Red (default), Yellow, Green, Blue, Purple — retuned to earthy, muted tones with per-accent contrast handling.
- **Animated splash screen**: Android 12+ compliant splash on startup.

## Tech Stack

- **Jetpack Compose** + **Material 3** — the entire UI, with a custom design-system layer (`OstromgepTheme`, semantic color/type/shape/spacing tokens, reusable primitives).
- **Google Gemini** (`gemini-3.6-flash`) via the Google AI client SDK (`com.google.ai.client.generativeai`) and a Cloudflare Worker proxy - AI generation and evaluation.
- **Firebase** (Auth + Firestore) — Google sign-in and cloud sync.
- **Room** — local persistence for the collections that grow with use (history, templates, exercise library, routine rotations, body-weight log, cable presets, training blocks).
- **Media3 ExoPlayer** — exercise-demo video playback.
- **Coil** (+ SVG & GIF decoders) — image and stretch-illustration loading.
- **ZXing** (`zxing-android-embedded`) — QR scan/generate for routine sharing.
- **EncryptedSharedPreferences** — on-device storage of the user's Gemini API key.
- **Kotlin Coroutines + Flow** — reactive state; **StateFlow**-backed `ViewModel` (no DI framework).
- **Foreground Service** — the rest timer and workout-keep-alive.
- Navigation is a lightweight in-app screen state + `HorizontalPager`; charts are drawn directly on `Canvas`.

## Get started

- Download the latest release from the [Releases](https://github.com/ateszk0/Ostromgep-workout-app/releases) page.
- Read the guide: [English Tutorial](tutorial_en.md) · [Magyar Útmutató](tutorial_hu.md)
