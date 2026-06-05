# Hydravo 💧

Hydravo is a premium, production-ready Android water tracking and reminder application built using Flutter and Dart. Designed with a gorgeous, high-performance UI, fluid animations, and robust backend integration, Hydravo helps users maintain optimal hydration levels tailored entirely to their personal health metrics and daily routines.

Built with an emphasis on user freedom, it features an advanced continuous manual reminder interval engine, deep analytics, and an over-the-air (OTA) in-app update framework hosted completely open-source via GitHub Releases.

---

## 🚀 Features

### 🎨 Premium UI/UX & Themes
* **Fluid Motion:** Built with advanced physics-based micro-interactions and smooth layout fades using `flutter_animate`.
* **Theming Options:** Supports clean Light Mode, battery-saving Dark Mode, and a custom **Pookie Mode** (a cute personalized pink layout engine).
* **Custom Brand Assets:** Fully custom adaptive launcher icons and native splash screens running natively across varying Android API scales.

### 🔔 Advanced Custom Reminder Engine
* **Ultimate Pacing Freedom:** Ditch the rigid choices. Features a continuous manual duration slider allowing alert tracking down to the exact minute (from 10 mins to 4 hours).
* **Routine Boundaries:** Dynamically schedules smart, periodic push notification alerts strictly between user-configured Wake-up and Sleep windows.
* **Local Processing:** Powered by `flutter_local_notifications` and exact timezone matching to repeat daily without draining background device battery pools.

### 📊 Deep Historical Analytics
* **Intake Charts:** Gorgeous interactive bar charts generated via `fl_chart` detailing a rolling 7-day hydration progress analysis.
* **Dynamic Visual Cues:** Bars intelligently change color states depending on target percentage completions (Goal Hit, 75%+, Low).
* **Weekly Reports:** Automated statistical breakdowns highlighting Daily Averages, Goal Streaks, Best Tracking Days, and algorithmic text-based progress analysis.
* **Day Breakdown:** Sleek historical list layouts with accurate progress meters for quick historical logs.

### ⚙️ Personalized Health Calibration
* **Dynamic Baseline Calculator:** Automatically generates standard target hydration lines by cross-parsing user data metrics: Age, Weight (supports fluid KG/LBS calibrations), Gender, and localized Activity Levels.
* **Interactive Profile Management:** Instantly update body metrics and personal display names on the fly, with automated notification rescheduling linked directly back to your routine updates.

### 🔄 Over-The-Air (OTA) In-App Updates
* **Seamless Upgrades:** Custom update system bypassing the Play Store entirely. The app pulls changes over a cache-busted stream straight from a repository `version.json`.
* **In-App Downloading:** Downloads new releases directly inside a custom update modal using a chunked byte stream with a live-rendering percentage progress bar.
* **Native Intent Installs:** Automatically invokes native Android package installation providers (`open_filex`) as soon as the package streams hit 100%.
* **Maintenance Guard:** Built-in cloud switch to instantly lock down the application layout structure into a graceful maintenance display during breaking infrastructure upgrades.

---

## 🛠️ Tech Stack & Packages

| Layer | Technology / Package | Description |
| :--- | :--- | :--- |
| **Core Framework** | Flutter & Dart | Multi-platform compilation target layer |
| **State Management** | `flutter_riverpod` | Scalable, reactive dependency tracking and UI states |
| **Backend Integration**| Firebase Auth / Firestore | Cloud account mapping, Google Sign-In, & live logs sync |
| **Local Notifications** | `flutter_local_notifications` | High-importance exact foreground background alert streams |
| **Data Visualization** | `fl_chart` | Interactive, highly responsive analytical graphs |
| **Motion Layout** | `flutter_animate` | High-fidelity chained layout fade and scale triggers |
| **OTA Installer** | `dio` & `open_filex` | Chunked HTTP byte streams and native apk intent calls |

---

## 📂 Project Architecture

The codebase follows a modular, feature-first clean architecture pattern designed for absolute scannability and ease of scaling:

```text
lib/
├── core/
│   ├── services/       # Core background executors (Notifications, Local DB)
│   ├── theme/          # Color palettes, custom typography configurations
│   └── utils/          # Universal constants, helper string formatters
└── features/
    ├── auth/           # Login layouts, Google auth, onboarding flows
    ├── home/           # Dashboard viewports, navigation state anchors
    ├── history/        # Weekly report metrics, fl_chart bar builders
    ├── settings/       # Profile modifiers, custom manual interval selectors
    └── update/         # In-app updater dialog modules, maintenance pages
