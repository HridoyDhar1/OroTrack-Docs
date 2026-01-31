# Goold - Gold Shop Management & E-Commerce Platform

A comprehensive Flutter-based application for managing gold shop operations, inventory, and e-commerce transactions. Built with Firebase backend and real-time notifications.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Key Features & Modules](#key-features--modules)
- [Firebase Setup](#firebase-setup)
- [Push Notifications](#push-notifications)
- [PDF Generation](#pdf-generation)
- [Database](#database)
- [Testing](#testing)
- [Deployment](#deployment)
- [Documentation](#documentation)
- [Contributing](#contributing)

---

## 🎯 Overview

**Goold** is a sophisticated gold shop management and e-commerce application designed to streamline operations, inventory tracking, and customer transactions. The platform provides end-to-end solutions for gold retailers including sales management, mortgage tracking, employee management, and comprehensive financial reporting.

**Project Name:** goldshop  
**Version:** 1.0.0  
**Minimum SDK:** Flutter 3.7.0+  
**Platforms:** Android, iOS, Web

---

## ✨ Features

### Core Business Features
- **Sales Management** - Track and manage gold sales with detailed invoices
- **Inventory Management** - Real-time product inventory tracking
- **Mortgage Management** - Handle gold mortgage operations
- **Employee Management** - Manage employee records and work assignments
- **Pricing Management** - Dynamic gold price management and updates
- **Income Dashboard** - Comprehensive financial analytics and reporting
- **Subscription Management** - Handle customer subscriptions
- **Calculator** - Built-in gold weight and price calculator

### User Features
- **Authentication** - Firebase Auth with Google & Facebook sign-in
- **User Profiles** - Detailed user profile management
- **Push Notifications** - Real-time FCM notifications
- **Offline Support** - Local data persistence with Hive
- **Multi-language Support** - Bangla/Bengali language support

### Technical Features
- **PDF Generation** - Full Bangla support for PDF exports
- **QR Code Scanning** - Mobile scanner integration
- **Geolocation** - GPS-based location services
- **Map Integration** - Google Maps integration
- **Video Support** - In-app video playback
- **Image Management** - Gallery and camera integration
- **Ad Support** - Google Mobile Ads integration
- **Data Sync** - Real-time Firestore synchronization

---

## 🏗 Architecture

The project follows **Clean Architecture** principles with clear separation of concerns:

```
lib/
├── core/                      # Core utilities & configuration
│   ├── config/               # App routes and configuration
│   ├── constant/             # App-wide constants
│   ├── controller/           # Global controllers
│   ├── helper/               # Helper utilities
│   ├── services/             # Core services (auth, database, etc.)
│   ├── utils/                # Utility functions
│   └── widgets/              # Reusable widgets
│
└── feature/                  # Feature modules (modular architecture)
    ├── Auth/                # Authentication feature
    ├── HomePage/            # Home screen
    ├── ProductList/         # Product listing
    ├── SellList/            # Sales management
    ├── MortgageList/        # Mortgage operations
    ├── NewBuy/              # Purchase management
    ├── NewSell/             # Sales operations
    ├── EmployeeList/        # Employee management
    ├── GiveWork/            # Work assignment
    ├── GoldPrice/           # Price management
    ├── IcomeDashboard/      # Financial dashboard
    ├── Calculator/          # Calculation utilities
    ├── PayList/             # Payment tracking
    ├── Pay/                 # Payment processing
    ├── Notifications/       # Notification system
    ├── ProfileDetails/      # User profiles
    ├── Subscription/        # Subscription management
    ├── Tutorial/            # User onboarding
    ├── admin/               # Admin features
    └── ... (other features)
```

### Architecture Pattern: MVVM + MVC
- **Model** - Data structures and Firestore models
- **View** - UI screens and widgets
- **ViewModel/Controller** - Business logic and state management
- **Services** - Firebase, Authentication, Notifications

---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose |
|-----------|---------|
| **Flutter** | Cross-platform UI framework |
| **GetX** | State management & routing |
| **Flutter ScreenUtil** | Responsive design |
| **Google Fonts** | Typography |
| **Flutter SVG** | Vector graphics |

### Backend & Database
| Technology | Purpose |
|-----------|---------|
| **Firebase Core** | Backend infrastructure |
| **Cloud Firestore** | Real-time NoSQL database |
| **Firebase Auth** | User authentication |
| **Firebase Storage** | File storage |
| **Firebase Messaging (FCM)** | Push notifications |
| **Firebase App Check** | Security & integrity |
| **Firebase Remote Config** | Remote configuration |

### Features & Plugins
| Technology | Purpose |
|-----------|---------|
| **Image Picker** | Camera & gallery access |
| **Hive & Hive Flutter** | Local data persistence |
| **Shared Preferences** | Simple key-value storage |
| **Permission Handler** | Runtime permissions |
| **Geolocator & Geocoding** | Location services |
| **Google Maps Flutter** | Map integration |
| **Mobile Scanner** | QR code scanning |
| **Firebase Local Notifications** | Local notifications |
| **PDF & Bangla PDF** | PDF generation with Bangla support |
| **Barcode Widget** | Barcode generation |
| **Video Player** | In-app video playback |
| **Lottie** | Animations |

### Social & Ads
| Technology | Purpose |
|-----------|---------|
| **Google Sign-In** | Google authentication |
| **Facebook Auth** | Facebook authentication |
| **Google Mobile Ads** | AdMob integration |
| **Share Plus** | Social sharing |
| **URL Launcher** | Deep linking |

### Backend Functions
| Technology | Purpose |
|-----------|---------|
| **Node.js/TypeScript** | Cloud Functions |
| **Firebase Functions** | Serverless backend |

---

## 📁 Project Structure

### Main Directories

```
Goold-main/
├── lib/                          # Flutter app source code
│   ├── firebase_options.dart    # Firebase configuration
│   ├── main.dart                # App entry point
│   ├── navigation.dart          # Navigation configuration
│   ├── core/                    # Core functionality
│   └── feature/                 # Feature modules
├── android/                      # Android native code
│   ├── app/                     # Android app configuration
│   ├── gradle/                  # Gradle build files
│   └── firebase-admin/          # Firebase Admin SDK
├── ios/                          # iOS native code
├── macos/                        # macOS native code
├── web/                          # Web platform code
├── windows/                      # Windows platform code
├── linux/                        # Linux platform code
├── functions/                    # Firebase Cloud Functions
│   ├── src/                     # TypeScript source
│   └── lib/                     # Function definitions
├── dataconnect/                  # Firebase Data Connect config
├── assets/                       # Static resources
│   ├── icons/                   # App icons
│   ├── images/                  # Images
│   ├── videos/                  # Videos
│   └── fonts/                   # Custom fonts (Bangla support)
├── scripts/                      # Build and utility scripts
├── test/                         # Test files
├── build/                        # Build output
└── pubspec.yaml                 # Flutter dependencies
```

---

## 🚀 Getting Started

### Prerequisites
- Flutter SDK (3.7.0 or higher)
- Dart SDK
- Xcode (for iOS development)
- Android Studio (for Android development)
- Firebase CLI
- Node.js (for Cloud Functions)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/goold.git
   cd goold
   ```

2. **Install Flutter dependencies**
   ```bash
   flutter pub get
   ```

3. **Get packages**
   ```bash
   flutter pub get
   ```

4. **Configure Firebase**
   ```bash
   flutterfire configure
   ```
   This will set up `firebase_options.dart` with your Firebase project credentials.

5. **Install Cloud Functions dependencies**
   ```bash
   cd functions
   npm install
   cd ..
   ```

6. **Run the app**
   ```bash
   flutter run
   ```

### Development Environment Setup

**Android:**
```bash
flutter run -d <android-device-id>
```

**iOS:**
```bash
flutter run -d <ios-device-id>
```

**Web:**
```bash
flutter run -d chrome
```

---

## ⚙️ Configuration

### Firebase Configuration
1. Create a Firebase project at [firebase.google.com](https://firebase.google.com)
2. Enable the following services:
   - Authentication (Email, Google, Facebook)
   - Cloud Firestore
   - Firebase Storage
   - Cloud Messaging
   - Remote Config
   - App Check

3. Run `flutterfire configure` to generate `firebase_options.dart`

### Google Maps Setup

**Android:**
1. Get Google Maps API key
2. Add to `android/app/src/main/AndroidManifest.xml`:
   ```xml
   <meta-data
       android:name="com.google.android.geo.API_KEY"
       android:value="YOUR_API_KEY"/>
   ```

**iOS:**
1. Add API key to `ios/Runner/GoogleService-Info.plist`

### AdMob Setup
1. Create AdMob account
2. Get App ID and Ad Unit IDs
3. Update in app configuration

---

## 🎨 Key Features & Modules

### 1. Authentication Module (`feature/Auth/`)
- Firebase Authentication integration
- Email/Password login
- Google Sign-In
- Facebook Login
- Password recovery
- OTP verification

### 2. Inventory Management
- Real-time product tracking
- Stock management
- Price updates
- Inventory reports

### 3. Sales Management (`feature/SellList/`)
- Create and manage sales transactions
- Invoice generation with Bangla PDF support
- Sales history
- Sales analytics

### 4. Mortgage System (`feature/MortgageList/`)
- Mortgage creation and tracking
- Mortgage redemption
- Mortgage history
- Interest calculation

### 5. Employee Management (`feature/EmployeeList/`)
- Employee database
- Work assignment
- Attendance tracking
- Salary management

### 6. Financial Dashboard (`feature/IcomeDashboard/`)
- Income tracking
- Expense management
- Profit/Loss analysis
- Financial reports

### 7. Notification System (`feature/Notifications/`)
- Firebase Cloud Messaging (FCM)
- Local notifications
- Push notification handling
- Notification history

---

## 📱 Firebase Setup

### Cloud Firestore Collections

Key collections in Firestore:

- **users** - User profiles and data
- **products** - Product inventory
- **sales** - Sales transactions
- **mortgages** - Mortgage records
- **employees** - Employee information
- **notifications** - Notification logs
- **payments** - Payment records

### Security Rules
Configure Firestore security rules to control access:
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

### Firebase Authentication
- Enable Email/Password authentication
- Configure Google OAuth credentials
- Set up Facebook app configuration

---

## 🔔 Push Notifications

### FCM Integration
1. Notification Service (`feature/Notifications/data/service/`)
   - `notification_service.dart` - Main notification handler
   - `fcm_notification_service.dart` - FCM integration
   - `admin_notification.dart` - Admin notifications

2. Features:
   - Real-time push notifications
   - Local notifications
   - Notification routing
   - Deep linking support

### Configuration
1. Enable Cloud Messaging in Firebase Console
2. Configure notification channels for Android
3. Set up FCM service account

### Sending Notifications
Notifications can be sent via:
- Firebase Console
- Cloud Functions
- Admin SDK

---

## 📄 PDF Generation

### Bangla PDF Support
The app includes full Bangla (Bengali) language support for PDF generation:

**File:** `lib/core/utils/bangla_pdf_generator.dart`

**Features:**
- Bangla text rendering
- Professional invoice layout
- Automatic file saving
- Print functionality
- A4 size formatting

**Usage:**
```dart
BanglaPdfGenerator().generateAndSavePDF(
  title: 'বিক্রয় চালান',
  data: saleData,
  fileName: 'invoice_bn.pdf'
);
```

---

## 📊 Database

### Local Storage
- **Hive** - Local NoSQL database for offline data
- **Shared Preferences** - Key-value storage for settings

### Remote Storage
- **Cloud Firestore** - Real-time NoSQL database
- **Firebase Storage** - File storage for images, PDFs, videos

### Data Models
All models support serialization:
- `toMap()` - Convert to JSON
- `fromMap()` - Create from JSON
- Firebase integration

---

## 🧪 Testing

### Widget Tests
```bash
flutter test
```

### Integration Tests
```bash
flutter test integration_test/
```

### Test Files Location
- Unit tests: `test/`
- Integration tests: `integration_test/`

---

## 📦 Deployment

### Android Deployment
1. Build APK:
   ```bash
   flutter build apk --release
   ```

2. Build App Bundle (for Google Play):
   ```bash
   flutter build appbundle --release
   ```

3. Upload to Google Play Console

### iOS Deployment
1. Build iOS:
   ```bash
   flutter build ios --release
   ```

2. Open in Xcode:
   ```bash
   open ios/Runner.xcworkspace
   ```

3. Upload to App Store

### Web Deployment
```bash
flutter build web --release
```

Deploy the `build/web/` directory to a hosting service.

---

## 📚 Documentation

Additional documentation files in the project:

| Document | Purpose |
|----------|---------|
| `NOTIFICATION_ARCHITECTURE.md` | Notification system design |
| `README_NOTIFICATIONS.md` | Notification setup guide |
| `PUSH_NOTIFICATION_GUIDE.md` | Push notification implementation |
| `OTP_VERIFICATION_GUIDE.md` | OTP authentication flow |
| `FCM_QUICK_REFERENCE.md` | FCM quick reference |
| `firebase.json` | Firebase configuration |
| `analysis_options.yaml` | Linter configuration |

---

## 🤝 Contributing

### Code Style
- Follow Dart style guide
- Use meaningful variable names
- Add comments for complex logic
- Keep methods small and focused

### Naming Conventions
- Classes: `PascalCase`
- Variables/Methods: `camelCase`
- Constants: `CONSTANT_CASE`
- Files: `snake_case.dart`

### Git Workflow
1. Create a feature branch: `git checkout -b feature/feature-name`
2. Commit changes: `git commit -m "Add feature"`
3. Push to branch: `git push origin feature/feature-name`
4. Create a Pull Request

### Code Review
- All PRs require review
- Tests must pass
- Code style must comply with guidelines

---

## 🔒 Security

### Best Practices Implemented
- Firebase App Check for integrity verification
- Secure authentication flows
- Encrypted local storage (Hive)
- HTTPS for all API calls
- Environment-based configuration

### Secrets Management
- Firebase credentials in `firebase_options.dart` (auto-generated)
- API keys in secure configuration
- Never commit sensitive data

---

## 📝 Environment Files

### Firebase Configuration
- `lib/firebase_options.dart` - Auto-generated by `flutterfire configure`
- Contains platform-specific Firebase credentials

### Build Configuration
- `android/key.properties` - Android signing configuration
- `android/gradle.properties` - Gradle settings
- `ios/Podfile` - CocoaPods configuration

---

## 🐛 Troubleshooting

### Common Issues

**Flutter pub get fails:**
```bash
flutter clean
flutter pub get
```

**Build issues:**
```bash
flutter clean
flutter pub cache repair
flutter pub get
flutter build (platform)
```

**Firebase connection issues:**
- Verify Firebase credentials
- Check internet connection
- Restart app

**Notification not working:**
- Check FCM setup
- Verify notification permissions
- Check Firebase console

---

## 📞 Support

For issues, feature requests, or contributions:
- Open an issue on GitHub
- Contact the development team
- Check existing documentation

---

## 📄 License

This project is proprietary. All rights reserved.

---

## 👥 Team

**Developed by:** Goold Development Team  
**Last Updated:** January 31, 2026  
**Version:** 1.0.0

---

## 🎉 Key Achievements

- ✅ Full Flutter cross-platform support
- ✅ Real-time Firebase integration
- ✅ Bangla language support (PDF & UI)
- ✅ Push notification system
- ✅ Employee & inventory management
- ✅ Comprehensive financial dashboard
- ✅ Multi-authentication methods
- ✅ Production-ready code

---

**Happy Coding! 🚀**
