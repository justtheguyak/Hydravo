# Hydravo

**A production-ready Android hydration tracking application built with Flutter.**

Hydravo helps users maintain optimal hydration through personalized goal-setting, intelligent reminders, and detailed progress analytics — all powered by a clean, performant UI with full Firebase backend integration.

---

## Features

### UI & Theming

- **Smooth animations** via physics-based micro-interactions using `flutter_animate`
- **Three theme modes:** Light, Dark, and Pookie (a custom pink palette)
- **Native asset support** including adaptive launcher icons and splash screens across Android API levels

### Smart Reminder Engine

- **Granular scheduling** with a continuous interval slider from 10 minutes to 4 hours
- **Routine-aware delivery** — notifications are restricted to user-defined wake and sleep windows
- **Battery-efficient** local processing via `flutter_local_notifications` with exact timezone handling

### Analytics & History

- **7-day bar charts** built with `fl_chart`, with color-coded bars reflecting goal completion levels
- **Weekly summaries** including daily averages, streaks, peak performance days, and trend analysis
- **Detailed day view** with scrollable intake logs and per-entry progress indicators

### Health Personalization

- **Automatic goal calculation** based on age, weight (kg/lbs), gender, and activity level
- **Live profile editing** with instant notification rescheduling on any update

### Over-the-Air Updates

- **GitHub Releases delivery** — updates bypass the Play Store via a versioned `version.json` manifest
- **In-app download UI** with a chunked byte stream and live progress display
- **Native installation** triggered automatically via `open_filex` on download completion
- **Maintenance mode** — a cloud flag locks the UI into a graceful hold screen during breaking deployments

---

## Tech Stack

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| Framework | Flutter & Dart | Cross-platform compilation |
| State Management | `flutter_riverpod` | Reactive dependency injection and UI state |
| Backend | Firebase Auth & Firestore | Authentication, Google Sign-In, cloud sync |
| Notifications | `flutter_local_notifications` | Scheduled foreground and background alerts |
| Charts | `fl_chart` | Interactive data visualizations |
| Animations | `flutter_animate` | Chained layout transitions and motion |
| OTA Updates | `dio` & `open_filex` | HTTP streaming and native APK installation |

---

## Architecture

The project follows a feature-first clean architecture for clarity and scalability.

```
lib/
├── core/
│   ├── services/       # Background services (notifications, local storage)
│   ├── theme/          # Color tokens and typography configuration
│   └── utils/          # Constants and shared formatting helpers
└── features/
    ├── auth/           # Login screens, Google auth flow, onboarding
    ├── home/           # Dashboard, navigation state
    ├── history/        # Weekly analytics, chart builders
    ├── settings/       # Profile editor, reminder interval controls
    └── update/         # OTA update dialog, maintenance screen
```
