
# Blueprint: Quran App

This document outlines the plan, style, design, and features of the Quran App.

## 1. Overview

The Quran App is a mobile application designed for Muslims, providing easy access to the Holy Quran, prayer times, Islamic radio, and video content. The app will feature a modern, user-friendly interface with both light and dark modes, offline capabilities, and customizable notifications.

## 2. Style and Design

*   **Theme:** Modern, clean, and intuitive dark-themed UI as per the user's request.
*   **Color Palette:**
    *   Primary Background: Dark blue/charcoal (`#1E2A3B`)
    *   Card Backgrounds: Slightly lighter shade of blue-gray (`#2A3A4D` and `#4A5A6D`)
    *   Accent/Highlight Color: A warm, gold-like color for highlights and important elements (`#D4AF37`) and a light green (`#A8D5BA`).
    *   Text Color: White and light gray for readability.
*   **Typography:**
    *   Arabic Text: A clean, traditional Arabic font for Quranic verses (e.g., Uthmanic font).
    *   UI Text: A modern, readable sans-serif font like `GoogleFonts.cairo()`.
    *   Font Sizes: A clear hierarchy will be used for titles, subtitles, and body text to improve readability.
*   **Iconography:** Modern and simple icons for navigation and actions (e.g., play, pause, download, settings).

## 3. Implemented Features

*(This section will be updated as features are implemented.)*

## 4. Current Plan: Initial Setup & Home Screen

### Step 1: Project Setup (Done)
- Add necessary dependencies:
  - `adhan`: For prayer time calculations.
  - `flutter_local_notifications`: For Adhan notifications.
  - `path_provider`: For finding local storage paths.
  - `dio`: For downloading Surah audio files.
  - `video_player`: For in-app video playback.
  - `permission_handler`: To manage user permissions for notifications, location, and storage.
  - `google_fonts`: For custom typography.

### Step 2: Asset and Theme Configuration
- Create `assets/images` and `assets/fonts` directories.
- Add asset paths to `pubspec.yaml`.
- Configure the main theme in `lib/main.dart`, focusing on the dark theme specified in the design.

### Step 3: Application Structure
- Create the main navigation structure with a `BottomNavigationBar`.
- Create placeholder screen files for the main tabs:
  - `lib/screens/home_screen.dart`
  - `lib/screens/search_screen.dart`
  - `lib/screens/my_quran_screen.dart`
  - `lib/screens/radio_screen.dart`
  - `lib/screens/settings_screen.dart`

### Step 4: Home Screen UI
- Implement the UI for `home_screen.dart` based on the provided screenshot.
- Create static widgets for:
  - Prayer Times Card
  - Audio Player Card
  - Radio Card
  - Live Stream Card

### Step 5: Prayer Times Logic
- Create a service `lib/services/prayer_times_service.dart`.
- Implement logic to fetch prayer times using the `adhan` package (using a fixed location for now).
- Integrate the prayer times into the UI.

### Step 6: Audio & Video Services
- Create placeholder services for audio and video playback to be integrated later.
  - `lib/services/audio_service.dart`
  - `lib/services/video_service.dart`

### Step 7: Surah Reader UI
- Create `lib/screens/surah_detail_screen.dart`.
- Implement the UI for reading a Surah as shown in the second screenshot, with placeholder data.
