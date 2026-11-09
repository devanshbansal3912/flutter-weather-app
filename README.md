# Flutter Weather App ⛅

A modern, responsive weather application built with **Flutter** and the **OpenWeatherMap API**. The app provides real-time current weather conditions, hourly forecasts, and detailed atmospheric metrics wrapped in a clean, dark-themed UI with glassmorphic backdrop filter styling.

---

## 📱 Features

- **Current Weather Overview**: Displays current temperature, weather conditions (Clouds, Rain, Clear, etc.), and dynamic weather icons inside a glassmorphism-styled card.
- **Hourly Weather Forecast**: Displays an interactive horizontal timeline of upcoming forecasts with formatted timestamps (`HH:mm`), weather icons, and temperatures.
- **Additional Weather Metrics**:
  - 💧 **Humidity**: Real-time atmospheric moisture percentage.
  - 💨 **Wind Speed**: Current wind velocity metrics.
  - ⏱️ **Atmospheric Pressure**: Barometric air pressure.
- **Pull/Tap to Refresh**: Instant weather data refresh via the AppBar refresh action.
- **Asynchronous State Management**: Handled via `FutureBuilder` with adaptive loading spinners and error handling.
- **Material 3 Dark Theme**: Immersive dark design language configured natively.

---

## 🛠️ Tech Stack & Dependencies

- **Framework**: [Flutter](https://flutter.dev) (Dart SDK `^3.10.4`)
- **API**: [OpenWeatherMap 5 Day / 3 Hour Forecast API](https://openweathermap.org/forecast5)
- **Key Packages**:
  - [`http: ^1.6.0`](https://pub.dev/packages/http) — Asynchronous HTTP networking for REST API requests.
  - [`intl: ^0.20.2`](https://pub.dev/packages/intl) — Internationalization and time/date parsing & formatting.
  - [`cupertino_icons: ^1.0.8`](https://pub.dev/packages/cupertino_icons) — Cupertino icon set assets.

---

## 📂 Project Architecture & Folder Structure

```text
weather_app/
├── android/                   # Native Android configuration & build files
├── ios/                       # Native iOS configuration & build files
├── linux/                     # Native Linux support files
├── macos/                     # Native macOS support files
├── web/                       # Web platform support files
├── windows/                   # Native Windows support files
├── lib/
│   ├── additional_info_item.dart   # Reusable widget for weather metric cards (humidity, wind, pressure)
│   ├── hourly_forecast_item.dart   # Reusable widget for hourly forecast cards
│   ├── main.dart                   # Application entry point & theme configuration
│   ├── secrets.dart                # Local API key configuration (git-ignored for security)
│   ├── secrets.example.dart        # Safe template for API credentials
│   └── weather_screen.dart         # Core weather dashboard UI & API data fetching
├── test/
│   └── widget_test.dart       # Widget tests
├── .gitignore                 # Configured ignore rules for Flutter & sensitive secrets
├── pubspec.yaml               # Project dependencies and metadata
└── README.md                  # Project documentation
```

---

## 🔑 API Configuration & Setup

This application connects to the OpenWeatherMap API to retrieve weather forecasts.

1. **Get an API Key**:
   - Register or sign in at [OpenWeatherMap](https://home.openweathermap.org/users/sign_up).
   - Navigate to the **API keys** tab and copy your generated key.

2. **Configure your local secrets**:
   - Copy `lib/secrets.example.dart` to `lib/secrets.dart`:
     ```bash
     cp lib/secrets.example.dart lib/secrets.dart
     ```
   - Open `lib/secrets.dart` and insert your actual OpenWeatherMap API key:
     ```dart
     const openWeatherAPIKey = 'YOUR_ACTUAL_API_KEY_HERE';
     ```

> **Security Note:** `lib/secrets.dart` is added to `.gitignore` to prevent confidential credentials from being exposed in public repositories.

---

## 🚀 Getting Started & Installation

### Prerequisites

- Flutter SDK (`>= 3.10.4` or latest stable release)
- Dart SDK installed with Flutter
- Android Studio / VS Code with Flutter extension
- A connected physical device, emulator, or simulator

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/devanshbansal3912/flutter-weather-app.git
   cd flutter-weather-app
   ```

2. **Install Flutter dependencies**:
   ```bash
   flutter pub get
   ```

3. **Configure your API Key**:
   Ensure `lib/secrets.dart` exists and contains your valid API key as described in the [API Configuration](#-api-configuration--setup) section.

4. **Run the application**:
   ```bash
   flutter run
   ```
