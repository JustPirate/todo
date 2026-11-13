# Todo Flutter 📝

> A modern, reactive, local-first Task Management application built with Flutter, Provider, and Hive.

[![Flutter](https://img.shields.io/badge/Flutter-3.x-blue.svg)](https://flutter.dev)
[![State Management](https://img.shields.io/badge/State-Provider-orange.svg)](https://pub.dev/packages/provider)
[![Storage](https://img.shields.io/badge/Storage-Hive%20DB-yellow.svg)](https://pub.dev/packages/hive)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

## 📌 Overview

**Todo** is an intuitive mobile task tracking and productivity app built with Flutter. It combines rapid in-memory reactive updates using `Provider` with persistent offline storage via `Hive`, delivering a seamless, lightning-fast user experience with zero cloud latency.

---

## 🚀 Key Features

- **⚡ Fast Local-First Storage:** Persisted using [Hive](https://pub.dev/packages/hive), a lightweight key-value NoSQL database engineered for Flutter and Dart with sub-millisecond read/write speeds.
- **🔄 Reactive State Management:** Managed with [Provider](https://pub.dev/packages/provider) to cleanly decouple UI presentation from business logic and task lifecycle events.
- **🎯 Smart Task Filters:** Interactive filter chips allowing one-tap switching between:
  - `All` — Complete overview of all created tasks.
  - `Pending` — Focused view of remaining actionable items.
  - `Complete` — History of completed tasks.
- **👆 Interactive Gesture Controls:** Integrated with [flutter_slidable](https://pub.dev/packages/flutter_slidable) for smooth swipe-to-delete and swipe-to-complete actions.
- **🎨 Material 3 Aesthetics:** Clean card-based interface with dynamic theme colors, rounded borders, and customizable task creation modals.

---

## 🏗️ Architecture & Project Structure

```text
lib/
├── data/
│   └── models/               # Hive type adapters and data models
├── pages/
│   └── home_page.dart        # Main dashboard screen with task lists and filter chips
├── providers/
│   └── task_provider.dart    # Task state management, filters, and Hive CRUD operations
├── widget/
│   ├── my_choice_chip.dart   # Filter pill component
│   ├── task_dialog.dart      # Task entry and edit dialog
│   ├── task_slidabelaction.dart # Slidable action buttons
│   └── todo_card.dart        # Individual task card item
└── main.dart                 # Application entrypoint & Hive box initialization
```

---

## 🛠️ Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (`^3.9` or higher)
- Android Studio / VS Code with Flutter extension
- An active Android emulator, iOS simulator, or connected physical device

### Installation & Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/JustPirate/todo.git
   cd todo
   ```

2. **Install Flutter dependencies:**
   ```bash
   flutter pub get
   ```

3. **Generate Hive Adapters (if modifying models):**
   ```bash
   flutter pub run build_runner build --delete-conflicting-outputs
   ```

4. **Launch the application:**
   ```bash
   flutter run
   ```

---

## 🧪 Testing

Run standard Flutter unit and widget tests:

```bash
flutter test
```

---

## 📄 License

This project is open-source and licensed under the [MIT License](https://opensource.org/licenses/MIT).
