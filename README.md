# OroTrack - Jewellery Shop Management Software
<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?size=28&duration=3000&color=00F7FF&center=true&vCenter=true&width=600&lines=Hi+I'm+Hridoy+Dhar;Flutter+Developer;QA+Engineer;AI+Enthusiast;Building+Real+World+Apps" />
</p>
<img width="1472" height="939" alt="Screenshot 2026-01-31 at 6 19 07 PM" src="https://github.com/user-attachments/assets/32cc6f41-3ef4-446e-8b9d-da1cc276bb0c" />

A comprehensive Flutter-based application for managing gold shop operations, inventory, and  transactions. Built with Firebase backend and real-time notifications.

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

**OroTrack** is a sophisticated gold shop management and e-commerce application designed to streamline operations, inventory tracking, and customer transactions. The platform provides end-to-end solutions for gold retailers including sales management, mortgage tracking, employee management, and comprehensive financial reporting.

**Project Name:** OroTrack
**Platforms:** Android

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




## 🔒 Security

### Best Practices Implemented
- Firebase App Check for integrity verification
- Secure authentication flows
- Encrypted local storage (Hive)
- HTTPS for all API calls
- Environment-based configuration

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
