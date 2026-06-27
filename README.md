# 🌿 Spandan Eco – Smart Waste Management

<div align="center">

![Eco Vision](https://img.shields.io/badge/EcoVision-AI-00C853?style=for-the-badge&logo=leaf&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-3.0-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Lite-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Auth-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

**AI-Powered Waste Classification & Recycling Assistant**

[🎬 Live Demo](https://qbn5ga2n.mule.page/) • [📱 Get Started](#getting-started) • [📖 Documentation](#features) • [📧 Contact](#contact)

</div>

---

## 🎬 Demo Video

**▶️ [Click here to watch the interactive demo](https://qbn5ga2n.mule.page/)**

<p align="center">
  <a href="https://qbn5ga2n.mule.page/">
    <img src="https://img.shields.io/badge/▶_Watch_Demo-00C853?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch Demo"/>
  </a>
</p>

---

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Screenshots](#screenshots)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [AI Model](#ai-model)
- [Firebase Setup](#firebase-setup)
- [Screens](#screens)
- [Design System](#design-system)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🌍 About

**Spandan Eco** is a smart waste management mobile application that uses artificial intelligence to help users identify waste types and receive proper recycling guidance. Built with Flutter and powered by TensorFlow Lite, the app provides real-time waste classification directly on your device.

The app features a premium dark green AI-inspired design with eco-friendly branding, glassmorphism UI, and smooth animations throughout.

> 🎯 **Mission:** Make recycling accessible, understandable, and rewarding for everyone.

---

## ✨ Features

### Core Features

| Feature | Description |
|---------|-------------|
| 🤖 **AI Waste Scanner** | Capture or upload images for instant waste type identification using TensorFlow Lite |
| 📊 **Confidence Score** | Get a percentage-based confidence level for every classification |
| 📝 **Recycling Instructions** | Receive detailed disposal guidance for each identified waste type |
| 🌎 **Environmental Impact** | See the CO₂ saved and environmental benefit of each recycled item |
| 📍 **Nearby Centers** | Google Maps integration to find recycling centers, smart bins, and collection points |
| 💡 **Smart Tips** | Categorized recycling tips for Plastic, Paper, Glass, Metal, Organic & E-Waste |
| 🏆 **Gamification** | Earn eco points, unlock achievement badges, and build recycling streaks |
| 🔔 **Push Notifications** | Recycling reminders and achievement alerts |
| 📜 **Scan History** | Complete log of all past scans with filtering by category |
| 👤 **User Profile** | Track stats, manage settings, and view achievements |

### Waste Categories Supported

- 🧴 **Plastic** – Bottles, containers, bags, food packaging
- 📄 **Paper** – Newspapers, cardboard, office paper
- 🫙 **Glass** – Bottles, jars, specialty glass
- 🥫 **Metal** – Aluminum cans, steel/tin cans, scrap metal
- 🍎 **Organic** – Food scraps, yard waste, compostable materials
- 💻 **E-Waste** – Phones, tablets, batteries, computers

---

## 📱 Screenshots

<div align="center">

| Splash Screen | Home Dashboard | AI Scanner |
|:---:|:---:|:---:|
| Premium dark green splash with glowing particles | Welcome dashboard with eco stats | Camera & gallery waste scanning |
| **Recycling Tips** | **Nearby Centers** | **User Profile** |
| Categorized tips for all waste types | Google Maps with recycling points | Stats, badges, and settings |

</div>

---

## 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| **Framework** | Flutter 3.x with Material 3 |
| **Language** | Dart |
| **AI/ML** | TensorFlow Lite (on-device classification) |
| **Backend** | Firebase (Authentication, Cloud Firestore) |
| **Maps** | Google Maps Flutter Plugin |
| **State Management** | Provider / Riverpod |
| **Image Handling** | image_picker (Camera & Gallery) |
| **Notifications** | Firebase Cloud Messaging (FCM) |
| **Animations** | Lottie Files |
| **Design** | Glassmorphism, Neon glow effects, Dark theme |

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK >= 3.0.0
- Dart SDK >= 3.0.0
- Android Studio / VS Code
- Firebase account
- Google Maps API key

### Environment Setup

```bash
# Check Flutter installation
flutter doctor

# Clone the repository
git clone https://github.com/spandanparhi/spandan-eco.git

# Navigate to project
cd spandan-eco

# Install dependencies
flutter pub get
```

---

## 📦 Installation

```bash
# Install all dependencies
flutter pub get

# Run the app
flutter run

# Build for Android
flutter build apk --release

# Build for iOS
flutter build ios --release
```

### Firebase Setup

1. Create a Firebase project at [console.firebase.google.com](https://console.firebase.google.com/)
2. Add your Android/iOS apps with the correct package name
3. Download `google-services.json` (Android) and `GoogleService-Info.plist` (iOS)
4. Place files in the respective directories:
   - `android/app/google-services.json`
   - `ios/Runner/GoogleService-Info.plist`
5. Enable **Authentication** (Email/Password, Google Sign-In)
6. Enable **Cloud Firestore** database
7. Enable **Cloud Messaging** for push notifications

### Google Maps Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Enable **Maps SDK for Android** and **Maps SDK for iOS**
3. Create an API key
4. Add the key to:
   - `android/app/src/main/AndroidManifest.xml`
   - `ios/Runner/AppDelegate.swift`

---

## 📁 Project Structure

```
lib/
├── main.dart                    # App entry point & routing
├── screens/
│   ├── splash_screen.dart       # Splash with animations
│   ├── home_screen.dart         # Dashboard & quick actions
│   ├── scan_screen.dart         # AI waste scanner
│   ├── tips_screen.dart         # Recycling tips
│   ├── history_screen.dart      # Scan history log
│   ├── map_screen.dart          # Nearby recycling centers
│   └── profile_screen.dart      # User profile & settings
├── widgets/
│   ├── glass_card.dart          # Glassmorphism card widget
│   ├── feature_card.dart        # Home feature cards
│   ├── scan_result_card.dart    # AI result display
│   ├── tip_card.dart            # Recycling tip cards
│   ├── center_card.dart         # Map center cards
│   ├── bottom_nav.dart          # Custom bottom navigation
│   └── badge_widget.dart        # Achievement badges
├── services/
│   ├── ai_service.dart          # TensorFlow Lite integration
│   ├── auth_service.dart        # Firebase Authentication
│   ├── firestore_service.dart   # Cloud Firestore CRUD
│   ├── maps_service.dart        # Google Maps integration
│   └── notification_service.dart# Push notifications (FCM)
├── models/
│   ├── waste_result.dart        # Waste classification model
│   ├── scan_history.dart        # Scan history model
│   ├── user_profile.dart        # User profile model
│   └── recycling_center.dart    # Center location model
└── assets/
    ├── images/                  # App images & icons
    ├── lottie/                  # Lottie animation files
    └── models/                  # TFLite .tflite model files
```

---

## 🧠 AI Model

The app uses a **TensorFlow Lite** model trained to classify waste into 6 categories:

| Class | Accuracy | Description |
|-------|----------|-------------|
| Plastic | ~94% | Bottles, containers, packaging |
| Paper | ~97% | Cardboard, newspapers, office paper |
| Glass | ~91% | Bottles, jars, containers |
| Metal | ~88% | Cans, foil, scrap metal |
| Organic | ~96% | Food waste, yard waste |
| E-Waste | ~92% | Electronics, batteries, cables |

### Model Details

```
Format: TensorFlow Lite (.tflite)
Input: 224x224 RGB image
Output: 6-class probability distribution
Size: ~4.2 MB (quantized)
Runtime: On-device (no internet required)
```

---

## 🔥 Firebase Setup

### Firestore Collections

```
users/
  └── {userId}/
      ├── name: string
      ├── email: string
      ├── photoUrl: string
      ├── totalScans: number
      ├── ecoPoints: number
      └── badges: array

scan_history/
  └── {userId}/
      └── {scanId}/
          ├── wasteType: string
          ├── confidence: number
          ├── imageUrl: string
          ├── instructions: string
          ├── environmentalImpact: string
          ├── pointsEarned: number
          └── timestamp: DateTime
```

---

## 📱 Screens

| # | Screen | Description |
|---|--------|-------------|
| 1 | **Splash** | Full-screen gradient with glowing particles, logo animation, auto-navigate after 3s |
| 2 | **Home** | Welcome card, eco stats, 4 feature cards, recent activity feed |
| 3 | **AI Scanner** | Camera/gallery input, progress animation, result card with confidence & instructions |
| 4 | **Recycling Tips** | 6 category tabs with scrollable cards and actionable tips |
| 5 | **History** | Filterable scan log with points earned and timestamps |
| 6 | **Nearby Centers** | Google Maps view + list of recycling centers with distance |
| 7 | **Profile** | Avatar, stats grid, achievement badges, settings list, logout |

---

## 🎨 Design System

### Colors

```dart
const Color primaryColor    = Color(0xFF00C853);  // Emerald Green
const Color secondaryColor  = Color(0xFF0B3D2E);  // Dark Green
const Color backgroundColor = Color(0xFF020E08);  // Deep Green/Black
const Color cardColor       = Color(0x730B3D2E);  // Glass card bg
const Color glowColor       = Color(0x6600C853);  // Neon green glow
```

### Typography

| Style | Font | Weight | Usage |
|-------|------|--------|-------|
| Display | Sora | 700-800 | Headings, titles |
| Body | Outfit | 300-600 | Body text, labels |

### UI Components

- **Glassmorphism Cards** – `backdrop-filter: blur(20px)` with green border
- **Neon Glow Effects** – `box-shadow` with primary color at 40% opacity
- **Rounded Corners** – 20–30px border radius throughout
- **Smooth Transitions** – 300ms ease animations on all interactions

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow [Dart best practices](https://dart.dev/guides)
- Use `flutter_lints` for code consistency
- Write unit tests for services and models
- Keep the UI responsive (60fps animations)

---

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 📧 Contact

<div align="center">

**Spandan Parhi**

📧 Email: [spandanparhi7@gmail.com](mailto:spandanparhi7@gmail.com)

🎬 **Live Demo:** [https://qbn5ga2n.mule.page/](https://qbn5ga2n.mule.page/)

</div>

---

<div align="center">

### 🌱 Made with passion for a greener planet

**[🎬 Watch Demo](https://qbn5ga2n.mule.page/)** • **[📧 Email](mailto:spandanparhi7@gmail.com)** • **[⬆ Back to Top](#-spandan-eco--smart-waste-management)**

</div>
