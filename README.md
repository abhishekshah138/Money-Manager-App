# 📈 Money Manager App

A highly intuitive, cross-platform personal finance and money management ecosystem designed to bring clarity, control, and convenience to your daily financial activities.

Whether you're looking to gain simple insights into your monthly spending, efficiently track borrowed or lent money, or quickly scan UPI QR codes securely on the go, the **Money Manager App** unites an easy-to-use interface with powerful underlying technologies. The ecosystem is thoughtfully divided into a hyper-native iOS client and a versatile Android client to ensure an uncompromised user experience on any device.

---

## 🌟 Vision & Overview

Managing finances shouldn't be a tedious chore; it should be an empowering habit. The philosophy behind this project is to eliminate the friction from tracking personal wealth. By providing a clean interface infused with real-time analytics, rapid entry mechanisms, and a centralized hub for tracking both standard spending and peer-to-peer debts, users can finally achieve complete financial awareness without the typical spreadsheet overhead.

---

## 🚀 Key Features & Capabilities

### 1. Smart Dashboard & Analytics
The intelligent **Dashboard** acts as the command center for your financial life.
* **Instant Overviews:** View your current balances, total expenses, and monthly income at a single glance.
* **Granular Analytics (`AnalyticsView.swift`):** Interactive visual representations and charts provide a deep understanding of where your money is going over custom time periods.
* **Category Breakdown (`CategoryDetailView.swift`):** Group expenses automatically. Dive into specific categories to see exactly what takes up the majority of your budget, enabling you to identify cutback opportunities immediately.

### 2. Comprehensive Transaction History
A robust history ledger ensures that no penny slips through the cracks.
* **Continuous Logging (`HistoryView.swift`):** Search, sort, and filter through your entire timeline of financial events.
* **Payment Views (`PaymentView.swift`):** Detailed screens for every transaction context you might encounter, whether it's recording digital payments, cash expenditures, or salary deposits.

### 3. Advanced Lending & Borrowing Tracker
Managing the money you owe or the money owed to you has never been easier.
* **Dedicated IOUs (`LendBorrowView.swift`):** Actively monitor ongoing liabilities or assets involving friends, family, and colleagues.
* **Person-Specific Ledgers (`PersonDetailView.swift` & `ContactPickerView.swift`):** Pick a contact directly from your device's native address book. Tap on a specific person to see a consolidated history of all transactions, loans, and split costs associated directly with them.

### 4. Seamless UPI QR Code Scanning
A frictionless approach to standard payments.
* **Hardware-accelerated Parsing (`QRScannerView.swift`):** Securely ties into the device camera to instantly read printed or digital UPI QR tags.
* **Automatic Auto-Fill:** Dramatically reduces manual data entry time by automatically extracting recipient IDs and integrating them effortlessly into the next step of the payment/logging flow.

### 5. Configurable Settings & Theme Control
Personalization is at the core of heavy daily usage.
* **Customization Settings (`SettingsView.swift`):** Modify app behaviors, default currencies, and notification preferences.
* **Dynamic Theming (`Theme.swift`):** Thoughtfully designed color palettes and typographies that adapt dynamically, ensuring the application remains beautiful and accessible in both light and dark environments.

---

## 🛠 Architecture & Tech Stack

This project takes a "best of both worlds" approach by rejecting a pure write-once-run-anywhere compromise in favor of optimized, platform-appropriate clients.

### The iOS Client (Native Performance First)
Engineered for raw performance, smooth animations, and deep system integration on Apple devices. 
* **Language:** `Swift 5.9` utilizing the latest concurrent and safe coding paradigms.
* **User Interface:** Written entirely in declarative **SwiftUI**, targeting a minimum of `iOS 16.0` to leverage the newest collection views, navigation stacks, and custom charting tools.
* **Project Generation:** Instead of dealing with messy `.xcodeproj` git conflicts, the project leverages **XcodeGen**. The repository contains a single declarative `project.yml` that cleanly defines targets, asset paths (`Assets.xcassets`), and `Info.plist` properties, drastically simplifying open-source collaboration.

### The Android Client (Rapid Cross-Platform Scale)
Built with web-first technologies aimed directly at feature parity and rapid iterative deployment on Android devices.
* **Language:** Strongly typed **TypeScript** (`tsx` / `ts`) to enforce predictability at compile time.
* **Framework:** Powered by **React Native** and managed by the robust **Expo** (`app.json`, `eas.json`) ecosystem for streamlined over-the-air updates and simple hardware bridging.
* **State & Navigation:** 
  * Centralized, highly scalable state-management localized inside the `store/` directory.
  * Native-feeling screen transitions and navigation hierarchies powered by `React Navigation` (`Navigation.tsx` / `screens/` directory).
  * Highly reusable UI components stored independently in the `components/` directory.

---

## 🔮 Future Scope & Roadmap

While the application natively handles standard tracking and ledger management, the future roadmap involves extending the core `Models.swift` and `index.ts` data definitions to support:
- Cloud-based synchronization to sync ledgers between iOS and Android instances simultaneously.
- Recurring transaction schedules to auto-log monthly bills and rent.
- Machine Learning categorization allowing the app to predict the category of an expense based on the merchant's name and past interactions.
- Export options to convert logs into CSV/PDF reports for tax purposes.

---

## 📜 License & Open Source

This repository is maintained as an open-source project designed to aid personal financial independence. Feel free to explore the structure, fork the repository, or even submit pull requests to add new charts, localizations, or improved cross-platform functionalities.
