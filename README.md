# Hydravo 💧

**Hydravo** is a modern, production-grade hydration tracking and reminder application built with Flutter and Dart. Designed around performance, personalization, and user experience, Hydravo helps users maintain healthy hydration habits through intelligent reminders, personalized water intake goals, insightful analytics, and seamless over-the-air updates.

The application combines a polished user interface, robust notification scheduling, cloud-backed user management, and advanced progress tracking to deliver a reliable daily hydration companion.

---

## ✨ Key Features

### 🎨 Modern User Experience

* Beautiful, responsive interface optimized for Android devices.
* Smooth animations and micro-interactions powered by `flutter_animate`.
* Multiple theme options including:

  * Light Mode
  * Dark Mode
  * Pookie Mode (custom pink-themed experience)
* Adaptive launcher icons and native splash screens for a consistent branded experience across Android versions.

---

### 🔔 Intelligent Reminder System

Hydravo provides complete control over hydration reminders without limiting users to predefined intervals.

#### Features

* Fully customizable reminder intervals from **10 minutes to 4 hours**
* Minute-level precision through an interactive interval selector
* User-defined wake-up and sleep schedules
* Automatic notification scheduling within active hours
* Timezone-aware reminder generation
* Battery-efficient local notification processing

Built using `flutter_local_notifications`, reminders operate entirely on-device for reliability and privacy.

---

### 📊 Advanced Hydration Analytics

Track progress and identify hydration patterns through detailed historical insights.

#### Analytics Dashboard

* Interactive 7-day hydration charts
* Daily intake tracking and goal comparison
* Color-coded achievement indicators
* Historical intake logs with progress visualization

#### Weekly Insights

* Daily average consumption
* Goal completion streaks
* Highest-performing hydration days
* Automated progress summaries and trend analysis

Visualizations are powered by `fl_chart` for a smooth and responsive experience.

---

### ⚙️ Personalized Hydration Goals

Hydravo automatically calculates recommended daily water intake based on individual user metrics.

#### Supported Parameters

* Age
* Weight (KG / LBS)
* Gender
* Activity Level

Users can update their profile at any time, with hydration targets and reminder schedules recalculated instantly to reflect new preferences.

---

### ☁️ Cloud Integration

Secure authentication and cloud synchronization ensure a seamless experience across sessions.

#### Capabilities

* Google Sign-In
* Firebase Authentication
* Firestore-based user data storage
* Secure profile management
* Real-time hydration data synchronization

---

### 🔄 Over-The-Air (OTA) Updates

Hydravo includes a custom update delivery system that enables users to receive application updates directly without requiring Play Store releases.

#### Update Framework Features

* GitHub Releases-powered distribution
* Automatic version checking via remote `version.json`
* In-app APK downloads with live progress tracking
* Native Android installation flow integration
* Cache-busted update delivery for reliability

#### Maintenance Mode

A remotely controlled maintenance switch allows critical updates or infrastructure maintenance to be performed without requiring a new application release.

---

## 🏗️ Technology Stack

| Layer                   | Technology                  | Purpose                                      |
| ----------------------- | --------------------------- | -------------------------------------------- |
| Framework               | Flutter & Dart              | Cross-platform application development       |
| State Management        | Riverpod                    | Reactive and scalable state management       |
| Authentication          | Firebase Auth               | User authentication and account management   |
| Database                | Cloud Firestore             | Cloud-based data storage and synchronization |
| Notifications           | flutter_local_notifications | Local hydration reminders                    |
| Analytics Visualization | fl_chart                    | Interactive charts and progress tracking     |
| Animations              | flutter_animate             | UI transitions and micro-interactions        |
| OTA Updates             | dio, open_filex             | Update downloading and APK installation      |

---

## 📁 Project Structure

Hydravo follows a feature-first modular architecture designed for maintainability, scalability, and clean separation of concerns.

```text
lib/
├── core/
│   ├── services/
│   │   ├── notifications/
│   │   ├── storage/
│   │   └── updates/
│   ├── theme/
│   └── utils/
│
├── features/
│   ├── auth/
│   ├── home/
│   ├── history/
│   ├── settings/
│   └── update/
│
└── main.dart
```

This architecture enables independent feature development while keeping business logic, UI, and services organized and easy to scale.

---

## 🎯 Mission

Hydravo was built with a simple goal:

> Help people build consistent hydration habits through intelligent reminders, personalized goals, and meaningful insights—without compromising performance, privacy, or user experience.

By combining thoughtful design with reliable technology, Hydravo transforms water tracking from a daily task into a seamless habit.
