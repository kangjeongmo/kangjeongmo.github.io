---
title: Jeju 5-Day Market Calendar
subtitle: SwiftUI + AdMob-based traditional Jeju five-day market calendar iOS app
start_date: 2025-07-01
end_date: 2025-07-30
role: iOS Developer
technologies:
  - Swift
  - SwiftUI
  - Google AdMob
  - iOS 14.5+
---

## 📱 Project Overview

A SwiftUI-based native app that provides schedules of traditional five-day markets in Jeju Island in iOS calendar format.

All necessary features including calendar rendering, filtering, detail information sheets, email feedback, and ad monetization were implemented. The entire development was completed 100% independently.

---

## ⭐ Key Features

### 1) Interactive Calendar View
- Monthly five-day market schedule visualization
- Display up to 3 markets per date
- Today's date highlight
- Previous/next month navigation
- LazyVGrid + Geometry-based layout

### 2) Market Filtering & Favorites
- Display only desired items from 9 five-day markets
- ⭐ Favorites system
- Select all/deselect all
- UserDefaults-based user settings storage

### 3) Smart Detail Information Sheet
- List of markets open by date
- One-tap address copy + toast notification
- Information message for markets hidden by filter
- Favorites toggle

### 4) Ad Monetization System
- AdMob interstitial ads + banner ads
- Smart timing considering UX (count + minimum 5-minute interval limit)
- ATT (App Tracking Transparency) compliance
- Automatic ad reload

### 5) Settings & Feedback
- Email feedback
- App review request (StoreKit)
- App information display

---

## 🛠 Core Technical Implementation

### 1) Advanced Calendar Rendering

    // Dynamic cell height calculation based on number of markets per date
    cellHeight = baseLine + CGFloat(maxMarketCount) * lineHeight + padding

- **Calendar grid lines directly implemented** with GeometryReader + Path
- Responsive calendar layout configuration based on LazyVGrid

### 2) Real-Time Date Tracking

    @Environment(\.scenePhase) var scenePhase
    scheduleMidnightUpdate()   // Automatic midnight update

- Date change handling with ScenePhase detection
- Recursive timer-based midnight update

### 3) Efficient Data Filtering

    @Published var selectedMarketNames: Set<String>
    markets.filter { selectedMarketNames.contains($0.name) }

- Set-based O(1) filtering
- Real-time UI reflection with ObservableObject + @Published combination

### 4) SwiftUI ↔ UIKit Bridge

- GADBannerView → UIViewRepresentable
- MFMailComposeViewController → UIViewControllerRepresentable
- Delegate handling through Coordinator pattern

### 5) Smart Ad Management

    viewCount % showEveryNViews == 0 &&
    now - lastAdTime >= minimumInterval

- **Dual condition system** of count limit + time limit
- Optimal ad monetization within the range that doesn't harm UX

### 6) Context-Aware UI

- Distinguish between items hidden due to filtering and actual 'no market on this date'
- Provide guidance messages & CTA tailored to user context

---

## 🏗 Architecture

### MVVM Pattern
- Model: Market, MarketData(JSON)
- View: CalendarView, MarketDetailSheet, FilterSheet
- ViewModel: MarketPreferences, InterstitialAdManager

### State Management
- `@State` → Local UI state
- `@StateObject` → Lifecycle-managed objects
- `@Published` → Reactive data
- `@Environment` → System value access

---

## 💡 Resolved Technical Challenges

1. **Different cell heights per month issue** → Dynamic calculation based on market count
2. **SwiftUI calendar grid line unsupported issue** → Direct implementation with Path
3. **Distinguishing filter hiding vs actually none** → Entire dataset comparison logic
4. **User-friendly ad experience** → Time and count dual restriction
5. **Midnight auto-refresh handling issue** → ScenePhase + recursive timer
6. **Korean calendar format issue resolution** → Custom Calendar based on Locale("ko_KR")

---
