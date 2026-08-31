# Ostromgep: Detailed User Guide

Welcome to **Ostromgep**! This application was created to help you precisely log your workouts, track your progress, and consciously apply Progressive Overload.

---

## 1. Dashboard

The **Dashboard** is the main screen where you get a quick overview of your current status and your next tasks. Every card here is a widget you can rearrange.

- **Next Mission**: The app suggests your next workout based on your saved routines. Tap **"Start Mission"** to begin immediately.
- **Weekly Battle Log**: Monday to Sunday. A filled circle marks each day you have already worked out this week.
- **Ready to Siege (Muscle Recovery)**: A heatmap of how fatigued each muscle group is.
  - **Green**: Recovered, ready for load.
  - **Yellow**: Mild fatigue, noticeable exertion.
  - **Red**: Strong fatigue — rest that muscle group.
- **Wall of Fame**: Scroll through your latest **Personal Records**.
- **Quick Metrics**: Tap the input field to record your daily body weight, then save it with the check button. The chart below shows the trend of your last 7 measurements.
- **Edit Layout**: The button at the bottom of the dashboard opens a dialog where you can **reorder** the widgets or **hide** ones you don't use.

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
- **Explore Routines**: A two-tab screen. One tab has pre-assembled plans (Push-Pull-Legs, Full Body, …) you can save with **"Add to my routines"** — these are placeholders, not perfect programs. The other tab is the **AI Workout Generator** (see section 7).
- **Training Block**: Opens the periodization planner (see section 8).

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
- **Monthly Summary**: per-month workout and volume totals.

---

## 6. Profile, History and Settings

On the **Profile** tab:

- **Recent Workouts Volume Chart**: a bar chart of recent total volume, so you can see whether your load is trending up.
- **Workouts**: opens your full **Workout Log**. Tap a past workout for details, then use **AI Evaluation** to get a detailed retroactive analysis of that session (in the app's language).
- **Calendar**: browse the past in a calendar; a dot marks a workout day, and today is outlined.
- **Recent Workouts list**: cards for your last workouts — tap for details, or use **Copy workout** / **Save as routine** to reuse them.
- **Settings** (gear icon): a screen grouped into cards:
  - **Appearance**: name, profile picture, app language, and accent color (**Red, Yellow, Green, Blue, Purple**).
  - **Timer**: rest-timer vibration, volume, and sound.
  - **Focus Mode (App Blocker)**: an overlay that reminds you to return to your workout if you open another app mid-session.
  - **Data & Cloud Sync**: sign in with Google (Firebase) to back up and restore history, templates and library. **Export / Import full data as JSON**, or **Import CSV** to bring in a **Hevy** workout export.
  - **AI (Gemini API Key)**: paste your key (stored encrypted on-device).
  - **Cable Presets**: save common weight configurations for cable machines to speed up logging.

---

## 7. AI Workout Generator (Gemini 3 Flash)

The **Explore Routines** screen has an **AI Workout Generator** tab for building unique, personalized plans.

- **API Key**: you need your own **Gemini API key**.
  1. **Get a key**: open [Google AI Studio](https://aistudio.google.com/api-keys), sign in, and create a key.
  2. **Add it in the app**: Profile → **Settings** (gear) → **AI (Gemini API Key)** — paste and save. It is stored securely and encrypted (**EncryptedSharedPreferences**) on your device.
- **Training days per week**: a slider (1–7). The AI picks an appropriate split (PPL, Upper/Lower, Full Body, Arnold Split, …) for that count.
- **Additional preferences** (optional): free text, e.g. *"I have a shoulder injury, focus more on legs and back"* or *"more isolation work for arms"*.
- **Generate Workout Plan**: the AI builds the plan from the factory exercise library (**default_exercises.json**) and saves one routine per day into **My Routines**. Notes are written in the app's set language.

---

## 8. Training Block (Periodization)

The **Training Block** screen turns a routine into a structured multi-week mesocycle.

**Planning a block:**
- **Source**: *Use existing routines* (pick a routine rotation — its routines become the training days) or *Generate with AI* (describe what you want and the AI produces the split).
- **Block length**: 4–8 weeks.
- **Deload every N weeks**: how often a lighter recovery week is inserted (the final week is always a deload).
- **Extra sets per week**: how aggressively working-set volume ramps up across each non-deload cycle.

**How it runs:** the app generates a week-by-week plan. Working (non-warm-up) sets scale up each week within a cycle and reset after each deload; deload weeks cut working-set volume roughly in half and are marked with a **DELOAD** badge. From the block screen you see **Week X / Y**, and you start the current week's workout straight from there. Warm-up sets are never scaled.

Delete the block at any time to return to normal routine training.

---

## 9. Auto Updater & Maintenance

The app checks its official GitHub page (**ateszk0/Ostromgep-workout-app**) on startup:

- A popup notifies you of a new version.
- **Update** opens your browser at the release page to download the new `.apk`. Export your data first.
- It never interrupts a workout: with no internet it stays silent in the background.

---

*Have a great workout and successful progress with Ostromgép!*
