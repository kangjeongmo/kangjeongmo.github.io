---
title: Kids Age Calculator
subtitle: SwiftUI + SwiftData-based iOS utility app
start_date: 2024-11-01
end_date: 2024-12-28
role: iOS Developer
technologies:
  - Swift
  - SwiftUI
  - SwiftData
---

## 📱 Project Overview

A **personal iOS utility app** developed to accurately calculate nieces and nephews' ages and conveniently manage birthday and growth information.

Designed with focus on actual user experience including age calculation accuracy, sorting UX, and deletion recovery features. **100% independently developed** from planning through design, development, and deployment.

Built with latest architecture based on SwiftData and SwiftUI, with complete support for 3 languages: Korean, English, and Japanese.

---

## ⭐ Key Features

### 1) Multi-Sort List Management
- Drag-and-drop-based **manual sorting**
- **Name / Age / Birthday** automatic sorting
- **Real-time search** reflected immediately upon input

### 2) Precise Age Calculation
- **Detailed age expression** in format `"12 years (9 months 15 days)"`
- Automatic **🎂 display** for today's birthday
- **D-day notification** provided for birthdays within 7 days

### 3) Soft Delete System
- **Recently Deleted Items bin** provided like Photos app
- Auto-delete after 30 days
- **Remaining days (D-day) countdown** display
- Deletion undo (restore) support

### 4) Memo Feature
- 200-character text limit
- Real-time character counter UI
- **📝 icon display** in list for items with memos

### 5) 3-Language Support
- Complete support for Korean / English / Japanese
- Total **1,598 lines of localization files**
- **Context-based UI/UX localization**, not simple translation

---

## 🛠 Core Technical Implementation

### Architecture
- **Latest structure based on SwiftUI + SwiftData**
- Clear separation of view and logic with MVVM pattern
- Screen navigation structure designed with NavigationStack (iOS 16+)

### State Management
- `@Query` → SwiftData-based automatic data fetching
- `@Bindable` → Bidirectional data binding
- `@State` → UI-level lightweight state management

### Data Model
- **Automatic persistence support** with `@Model` macro
- **Type-safe** queries with Predicate-based
- Built-in soft delete logic (deletion date storage, 30-day countdown)
- Index-based data structure considering sorting/search features

### SwiftData Utilization
- Actively utilized lightweight persistence + query features provided by SwiftData
- Data flow for D-day calculation, birthday events, sorting, etc.
  structured to handle without performance degradation

---

## 💡 Achievements

- Accumulated latest architecture experience based on SwiftUI + SwiftData
- Actual user-centered feature design (sorting, search, birthday notifications, deletion bin, etc.)
- Prepared for global user base through 3-language support
- Achieved iOS system app-level UX completeness despite being a personal project

---
