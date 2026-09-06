# Ostromgép: Detailed User Guide

Welcome to **Ostromgep**! This application was created to help you precisely log your workouts, track your progress, and consciously apply Progressive Overload.

---

## 1. Dashboard

The **Dashboard** is the main screen where you get a quick overview of your current status and your next tasks. Every card here is a widget you can rearrange.

- **Next Mission**: The app suggests your next workout based on your saved routines. Tap **"Start Mission"** to begin immediately.
- **Weekly Battle Log**: Monday to Sunday. A filled circle marks each day you have already worked out this week.
- **Ready to Siege (Muscle Recovery)**: A heatmap of how fatigued each muscle group is, painted on a front and back body figure.
  - **Green**: Recovered, ready for load.
  - **Yellow**: Mild fatigue, noticeable exertion.
  - **Red**: Strong fatigue — rest that muscle group.
  - Tap the **gear icon** in the top-right of the card to switch the figure between the **male** and **female** body. The choice is remembered and synced with your account.
- **Quick Metrics**: Tap the input field to record your daily body weight, then save it with the check button. The chart below shows the trend of your last 7 measurements.
- **Today's Workout**: Let the AI build a full session from your recent training with one tap.
- **Campaign**: Your level, XP bar, weekly streak, quest progress and league tier at a glance — tap it (or the trophy icon top-right) to open the full **Campaign** screen (see section 6).
- **Training Block**: If you have an active periodization block, shows the current week and a **DELOAD** badge on recovery weeks. Empty if you have not started one.
- **Stalled Lifts**: Exercises whose estimated max has not moved in a while, each with a coaching hint (deload / check technique / try a variation / add volume). Empty if nothing is currently stalled.
- **Fresh Conquests**: Your personal records from the last 30 days, labelled with what kind of record it is (max weight or session volume) and how long ago you set it.
- **Siege Watch**: A live miniature of your castle from this week's siege — tap it to jump into the Campaign screen.
- **Edit Layout**: The button at the bottom of the dashboard opens a dialog where you can **reorder** the widgets or **hide** ones you don't use. The list scrolls if it does not fit the screen.

---

## 2. Starting a Workout and Managing Routines

On the **Workout** tab (bottom navigation), choose how you want to train:

- **Start Empty Workout**: No fixed plan — assemble exercises on the spot.
- **My Routines**: Your saved templates. Tap **"Start Routine"** on a card to begin.
- **QR Code Import/Export**: Use the **QR icon** above the routine list to import plans shared by others. Share your own via **Share via QR** in the three-dot (⋯) menu on a routine card. The serialization is data-agnostic, so fully custom exercises transfer seamlessly without being tied to factory defaults.
- **Manage Rotations**: The **rotation icon** (circular arrows, top right) lets you group routines you cycle through.
  - **Create Rotation**: Name it and choose which routines belong to it.
  - **Active Rotation**: Select a rotation and only its routines cycle through the **Next Mission** widget on the dashboard.
- **New Routine**: Create a new savable plan in the **Routine Editor** (add exercises, set default reps, build supersets).
- **Explore Routines**: A two-tab screen. One tab has pre-assembled plans (Push-Pull-Legs, Full Body, …) you can save with **"Add to my routines"** — these are placeholders, not perfect programs. The other tab is the **AI Workout Generator** (see section 8).
- **Training Block**: Opens the periodization planner (see section 9).

---

## 3. Active Workout

When you start a workout, these tools are available:

### Top bar
- **Simple view toggle** (list / fullscreen icon): switches between the full sets table and a distraction-free **Simple view** that shows one set at a time and lets you swipe between them.
- **Plate Calculator** (calculator icon): enter a target weight and bar weight; it tells you which plates to load per side.
- **AI Assistant** (robot icon): opens a menu to request **weight suggestions** for the current exercises, or to generate a **dynamic warm-up** or **static cooldown** protocol — a short list of illustrated stretches produced for this session.

### Workout Stats Header
At the top you always see **Duration**, **Volume**, **Sets**, plus the rest-timer countdown.

### Exercise Block interactions
- **Thumbnail image**: tap the small image next to the exercise — a demo video plays if one exists, otherwise the image enlarges.
- **Notes**: write notes directly under the exercise name.
- **Rest Timer**: tap the time in the rest bar to adjust it (±15s) or skip it.
- **⋯ menu**: **Move Up/Down**, **Edit**, **Create / Remove Superset**, **Replace exercise**, and **Delete**.

### Sets table
- **Set number (1, 2, 3…)**: **tap the number** to mark it a **Warm-up set** — the row turns yellow.
- **Previous**: your data from the last time you did this exercise.
- **KG / Reps**: tap into the fields to enter data.
- **RPE**: tap the dash in the RPE column and pick from the popup.
- **Complete toggle**: tap the square at the end of the row to finish the set — this also starts the automatic rest timer. Beating your historic best flashes a record indicator.
- **Remove set**: **swipe the row left** to reveal the delete action.

Superset exercises are grouped with a coloured left rail and a "SUPERSET" label.

---

## 4. Managing Exercises

On the **Profile** tab, open the **Exercises** library:

- **Create Exercise**: the **"Create"** button (top right). Name it, set the default **Rep Range**, upload an image, and pick the affected **Muscle Groups** and required **Equipment**.
- **Edit Exercise**: tap any exercise in the list or the in-workout menu.
  - Custom exercises: edit everything (name, image, muscles, equipment).
  - Default exercises: for safety only the rep range is editable; the image is fixed.

---

## 5. Statistics

The **Statistics** screen (Profile tab) is a full analytics view:

- **Summary**: Workouts, Volume, Time, Avg. Workout, Longest Streak, This Month.
- **Last 7 Days**: a heatmap of which days you trained.
- **Muscle Group Distribution**: a donut chart and a front/back body map of what you worked recently.
- **Set Distribution**: set count per muscle group.
- **Top Exercises**: your most-performed movements.
- **Personal Records**: heaviest set and highest volume per exercise.
- **1RM Progression**: pick an exercise to see the trend of its estimated one-rep max over time (Epley / Brzycki estimation). Needs a few logged sessions of that exercise.
- **Stalled Lifts**: exercises whose estimated one-rep max has not improved in a few weeks, each with a hint on what to try (deload, check technique, swap in a variation, or add volume). Tap one to jump to its exercise detail.
- **Monthly Summary**: per-month workout and volume totals.

---

## 6. The Campaign (Hadjárat)

Tap the trophy icon top-right on the Dashboard (or the Campaign widget) to open the **Campaign** screen — a siege-themed gamification layer computed entirely from your workout history. Tap the **(i)** info icon at the top for the full in-app guide with exact formulas; here is the short version.

- **XP and Levels**: every finished workout earns XP (a base amount, a volume bonus, a bonus for every personal record you beat, all scaled up by your weekly streak). Level up as XP adds up.
- **This Week's Siege**: each week is a raid on a castle. The castle's HP is your own recent weekly volume target, so the castle's **size** scales with it too — from a small Outpost or Fort up to a full towered Citadel for a large target. Log volume during the week to damage it: 50% breaches the gate, 100% takes the keep, and 150% is a full overrun (the castle raises a white flag). The walls and towers visibly crumble as you progress, never quite the same way twice.
- **Weekly Quests**: 3 rotating challenges each week (train N times, beat a PR, hit a volume or set goal, train several muscle groups, a long session, training early in the week). Clearing all 3 earns bonus XP.
- **League and Season**: a season is one calendar month. Your league score comes from consistency — workouts, active weeks, and your streak, not raw strength — so it stays fair for beginners. Climb from Copper through Bronze, Silver, Gold, Platinum, up to Diamond. Tap the League card for a full ladder showing your distance to every tier.
- **Badges**: 34 achievements sorted Bronze → Platinum by difficulty, medal-colored, in a 3-column grid. Tap any badge to see exactly what unlocks it.
- **Notifications**: a push notification on a league promotion, clearing all weekly quests, and a new badge. Turn it off in **Settings → Reminders → Campaign notifications**.

---

## 7. Profile, History and Settings

On the **Profile** tab:

- **Recent Workouts Volume Chart**: a bar chart of recent total volume, so you can see whether your load is trending up.
- **Workouts**: opens your full **Workout Log**. Tap a past workout for details, then use **AI Evaluation** to get a detailed retroactive analysis of that session (in the app's language).
- **Calendar**: browse the past in a calendar; a dot marks a workout day, and today is outlined.
- **Recent Workouts list**: cards for your last workouts — tap for details, or use **Copy workout** / **Save as routine** to reuse them.
- **Settings** (gear icon): a screen grouped into cards:
  - **Appearance**: name, profile picture, app language, **theme (System, Light or Dark)**, and accent color (**Red, Yellow, Green, Blue, Purple**).
  - **Timer**: rest-timer vibration, volume, and sound.
  - **Focus Mode (App Blocker)**: an overlay that reminds you to return to your workout if you open another app mid-session.
  - **Data & Cloud Sync**: sign in with Google (Firebase) to back up and restore history, templates and library. **Export / Import full data as JSON**, or **Import CSV** to bring in a **Hevy** workout export.
  - **AI (Gemini API Key)**: paste your key (stored encrypted on-device).
  - **Cable Presets**: save common weight configurations for cable machines to speed up logging.

---

## 8. AI Workout Generator (Gemini 3 Flash)

The **Explore Routines** screen has an **AI Workout Generator** tab for building unique, personalized plans.

- **API Key**: you need your own **Gemini API key**.
  1. **Get a key**: open [Google AI Studio](https://aistudio.google.com/api-keys), sign in, and create a key.
  2. **Add it in the app**: Profile → **Settings** (gear) → **AI (Gemini API Key)** — paste and save. It is stored securely and encrypted (**EncryptedSharedPreferences**) on your device.
- **Training days per week**: a slider (1–7). The AI picks an appropriate split (PPL, Upper/Lower, Full Body, Arnold Split, …) for that count.
- **Additional preferences** (optional): free text, e.g. *"I have a shoulder injury, focus more on legs and back"* or *"more isolation work for arms"*.
- **Generate Workout Plan**: the AI builds the plan from the factory exercise library (**default_exercises.json**) and saves one routine per day into **My Routines**. Notes are written in the app's set language.

---

## 9. Training Block (Periodization)

The **Training Block** screen turns a routine into a structured multi-week mesocycle.

**Planning a block:**
- **Source**: *Use existing routines* (pick a routine rotation — its routines become the training days) or *Generate with AI* (describe what you want and the AI produces the split).
- **Block length**: 4–8 weeks.
- **Deload every N weeks**: how often a lighter recovery week is inserted (the final week is always a deload).
- **Extra sets per week**: how aggressively working-set volume ramps up across each non-deload cycle.

**How it runs:** the app generates a week-by-week plan. Working (non-warm-up) sets scale up each week within a cycle and reset after each deload; deload weeks cut working-set volume roughly in half and are marked with a **DELOAD** badge. From the block screen you see **Week X / Y**, and you start the current week's workout straight from there. Warm-up sets are never scaled.

Delete the block at any time to return to normal routine training.
- **API Key**: To use the generator, you will need your own **Gemini API key**.
    1. **Obtaining a Key**: Visit [Google AI Studio]([https://aistudio.google.com/](https://aistudio.google.com/api-keys)), sign in with your Google account, and click the **'Get API key'** button to create a new key.
    2. **Setup in the app**: Go to the **Profile** tab, click the **Settings** (gear) icon in the top right, and scroll down to the **AI (Gemini API Key)** section. Paste the key and save it. The app stores this securely and encrypted (**EncryptedSharedPreferences**) on your device.
- **Training days per week**: Use the slider to set how many days you plan to work out in a week (1-7 days). The AI will automatically suggest an optimal split (e.g., PPL, Upper/Lower, Full Body, Arnold Split) based on the number of days.
- **Additional preferences**: This is an optional field where you can provide specific requests to the AI. For example: *"I have a shoulder injury, let's focus more on legs and back"*, or *"I want more isolation exercises for arms"*.
- **Generate Workout Plan**: After pressing the button, the AI will assemble your plan from the elements of the factory exercise library (**default_exercises.json**) and automatically save the routines for each day separately in your **My Routines** list. The AI generation is now bilingual, so it writes notes according to the app's set language.

---

## 10. Auto Updater & Maintenance

The app checks its official GitHub page (**ateszk0/Ostromgep-workout-app**) on startup:

- A popup notifies you of a new version. Export your data first, just in case.
- **Download** downloads the matching APK for your build (debug or release) right in the popup, with a progress bar, then **Install** hands it to the system installer - no browser needed. The first time, Android asks you to allow "install unknown apps" for Ostromgép; grant it once and tap Install again.
- **View on GitHub** is always available too, if you'd rather download it yourself from the release page.
- It never interrupts a workout: with no internet it stays silent in the background.

---

*Have a great workout and successful progress with Ostromgép!*
