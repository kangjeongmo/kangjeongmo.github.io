---
title: Dog Age Calculator
subtitle: SwiftUI-based iOS app with 13-language support for dog age conversion
start_date: 2025-10-01
end_date: 2025-11-30
role: iOS Developer
technologies:
  - Swift
  - SwiftUI
  - AdMob
  - Combine
  - UMP SDK (GDPR)
  - iOS 14.5+
---

## 📱 Project Overview

A SwiftUI-based iOS utility app that converts dog age to human age based on scientific formulas.

The app applies **logarithmic formula-based age calculation** according to research from UC San Diego, and provides **complete support for 13 languages** to serve users worldwide. It achieves production-level stability by complying with privacy regulations including ATT and GDPR.

The entire development was completed 100% independently.

---

## ⭐ Key Features

### 1) Science-Based Age Calculation
- UC San Diego adult dog conversion formula applied
  - `human_age = 16 × ln(dog_age) + 31`
- Adjustments by breed size
  - Small / Medium / Large / Giant breeds
- Automatic life stage classification
  - Puppy / Adolescent / Adult / Middle-aged / Senior / Geriatric

### 2) Intuitive UI/UX
- SwiftUI-based responsive screen design
- Easy age input with Stepper + Segmented Picker
- Real-time calculation result card display
- Full support for iPhone and iPad (Universal app)

### 3) Complete 13-Language Support
- Korean, English, Japanese
- Chinese (Simplified/Traditional), Spanish, French, German
- Italian, Portuguese, Russian
- Arabic, Hindi
- **String Catalog-based complete interface internationalization**

### 4) AdMob Ad Integration
- Responsive banner ads for iPhone/iPad
- Production ad unit IDs applied
- In-app ad structure compliant with ad display policies

---

## 🛠 Core Technical Implementation

### 1) Privacy Regulation Compliance
- **ATT (App Tracking Transparency)**
  - Tracking permission request procedure for iOS 14.5+ environment
- **GDPR (European Privacy Law)**
  - EU region consent management with Google UMP SDK
- **Consent Flow Control Logic**
  - Safely processed in GDPR → ATT → Ad initialization order

### 2) Modern SwiftUI Architecture
- App entry point configured with `@main` macro
- Structured concurrency with `async/await`
- UI update thread safety with `@MainActor`
- Reactive state management with Combine (`@Published`, `@StateObject`)

### 3) UIKit - SwiftUI Integration
- AdMob banner: Wrapped with `UIViewRepresentable`
- Native features: AppDelegate utilized through `UIApplicationDelegateAdaptor`
- Ad area + UI element collision prevention with Safe Area Inset

### 4) Performance and Memory Optimization
- ConsentManager singleton management with `@StateObject`
- Minimal data change reflection with `@Published`
- Unnecessary UI update removal with conditional rendering
- Lightweight architecture minimizing memory usage

---

## 💡 Resolved Technical Challenges

1. **Precision age calculation by various breed sizes**
   - Applied size-specific weights based on UCSD formula
2. **13-language internationalization processing**
   - Systematized all UI text with String Catalog
3. **Resolved GDPR & ATT compliance flow conflict**
   - Precise sequence control with region/environment conditionals
4. **Resolved AdMob + SwiftUI layout conflict**
   - Combination of Safe Area Inset and UIViewRepresentable
5. **Responsive UI for iPad and iPhone**
   - Dynamic Type + GeometryReader-based layout
6. **Maintained stable FPS and minimized view re-rendering**
   - Minimal state change structure design with Combine

---
