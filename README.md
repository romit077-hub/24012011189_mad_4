# MAD Practical 4 - Alarm Application

An Android application developed as part of the Mobile Application Development (MAD) Practical 4 assignment. This app demonstrates how to set, display, and cancel alarms using Android's `AlarmManager`, `PendingIntent`, `BroadcastReceiver`, and background `Service`.

---

## 📱 Features

- **Set Alarm Time**: Pick a custom time using `TimePickerDialog`.
- **Alarm Management**: Schedule exact alarms with `AlarmManager.RTC_WAKEUP`.
- **Background Alarm Service**: Plays alarm audio in a background `Service` when triggered.
- **Cancel Alarm**: Easily stop the alarm sound and cancel scheduled pending intents.
- **Live Clock Display**: Uses `TextClock` to display real-time clock updates.
- **Permission Handling**: Checks for `SCHEDULE_EXACT_ALARM` permissions on Android 12 (API 31) and higher.

---

## 🛠 Tech Stack & Architecture

- **Language**: Kotlin
- **UI Framework**: XML Layouts with Material Design Components (`MaterialCardView`, `MaterialButton`, `TextClock`)
- **Core Android Components**:
  - `AlarmManager`: For scheduling background alarms.
  - `PendingIntent`: To deliver alarm triggers to the broadcast receiver.
  - `BroadcastReceiver` (`AlarmBroadcastReceiver`): Receives alarm events and manages service lifecycle.
  - `Service` (`AlarmService`): Uses `MediaPlayer` to handle alarm audio playback.
  - `TimePickerDialog`: Interactive UI component for selecting alarm time.
- **Minimum SDK**: 24 (Android 7.0)
- **Target SDK**: 37

---

## 📁 Project Structure

```
app/src/main/
├── java/com/meshwi/a24012011109_mad_practical_4/
│   ├── MainActivity.kt               # Main activity for picking, setting & cancelling alarms
│   ├── AlarmBroadcastReceiver.kt     # Broadcast receiver for alarm trigger events
│   └── AlarmService.kt               # Service to play audio via MediaPlayer
├── res/
│   ├── layout/activity_main.xml      # Layout with Material Cards, TextClock, and action buttons
│   └── raw/alarm.mp3                 # Alarm sound resource
└── AndroidManifest.xml               # Configured receiver, service, and exact alarm permissions
```

---

## 🚀 Getting Started

### Prerequisites
- [Android Studio](https://developer.android.com/studio) (2023.x or newer recommended)
- Android SDK 37 / Build Tools
- JDK 11 or higher

### Build & Run
1. **Clone the repository**:
   ```bash
   git clone https://github.com/romit077-hub/24012011189_mad_4.git
   ```
2. Open the project in **Android Studio**.
3. Let Gradle sync dependencies.
4. Run the application on an emulator or a connected physical Android device.

---

## 📝 License

This project is created for educational purposes under the Mobile Application Development course curriculum.
