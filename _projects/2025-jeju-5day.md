---
title: 제주 오일장 달력 (Jeju 5-Day Market Calendar)
subtitle: SwiftUI + AdMob 기반 제주 전통 오일장 캘린더 iOS 앱
start_date: 2025-07-01
end_date: 2025-07-30
role: iOS 개발자
technologies:
  - Swift
  - SwiftUI
  - Google AdMob
  - iOS 14.5+
---

## 📱 프로젝트 개요

제주도 전통 오일장의 일정을 iOS 캘린더 형태로 제공하는  
SwiftUI 기반 네이티브 앱입니다.  

캘린더 렌더링, 필터링, 상세 정보 시트, 이메일 피드백, 광고 수익화 등  
필요 기능을 모두 구현했으며 전체 개발을 100% 단독으로 진행했습니다.

---

## ⭐ 주요 기능

### 1) 인터랙티브 캘린더 뷰
- 월별 오일장 일정 시각화  
- 날짜별 최대 3개 장터 표시  
- 오늘 날짜 하이라이트  
- 이전/다음 달 전환  
- LazyVGrid + Geometry 기반 레이아웃  

### 2) 장터 필터링 & 즐겨찾기
- 9개 오일장 중 원하는 항목만 표시  
- ⭐ 즐겨찾기 시스템  
- 전체 선택/해제  
- UserDefaults 기반 사용자 설정 저장  

### 3) 스마트 상세 정보 시트
- 날짜별 열리는 장터 목록  
- 주소 원탭 복사 + 토스트 알림  
- 필터로 숨겨진 장터 안내 메시지  
- 즐겨찾기 토글  

### 4) 광고 수익화 시스템
- AdMob 전면광고 + 배너광고  
- UX 고려한 스마트 타이밍(횟수 + 최소 5분 간격 제한)  
- ATT(App Tracking Transparency) 대응  
- 자동 광고 재로드  

### 5) 설정 & 피드백
- 이메일 피드백  
- 앱 리뷰 요청(StoreKit)  
- 앱 정보 표시  

---

## 🛠 핵심 기술 구현

### 1) 고급 캘린더 렌더링

    // 날짜별 장터 수에 따른 동적 셀 높이 계산
    cellHeight = baseLine + CGFloat(maxMarketCount) * lineHeight + padding

- GeometryReader + Path 로 **캘린더 격자선 직접 구현**  
- LazyVGrid 기반 반응형 달력 레이아웃 구성  

### 2) 실시간 날짜 추적

    @Environment(\.scenePhase) var scenePhase
    scheduleMidnightUpdate()   // 자정 자동 업데이트

- ScenePhase 감지로 날짜 변경 처리  
- 재귀 타이머 기반 midnight update  

### 3) 효율적인 데이터 필터링

    @Published var selectedMarketNames: Set<String>
    markets.filter { selectedMarketNames.contains($0.name) }

- Set 기반 O(1) 필터링  
- ObservableObject + @Published 조합으로 실시간 UI 반영  

### 4) SwiftUI ↔ UIKit 브릿지

- GADBannerView → UIViewRepresentable  
- MFMailComposeViewController → UIViewControllerRepresentable  
- Coordinator 패턴을 통한 Delegate 처리  

### 5) 스마트 광고 관리

    viewCount % showEveryNViews == 0 &&
    now - lastAdTime >= minimumInterval

- 횟수 제한 + 시간 제한의 **이중 조건 시스템**  
- UX을 해치지 않는 범위에서 최적의 광고 수익화  

### 6) 컨텍스트 인지 UI

- 필터링 때문에 숨겨진 항목과 실제 '해당 날짜 장터 없음'을 구분  
- 사용자 상황에 맞춘 안내 메시지 & CTA 제공  

---

## 🏗 아키텍처

### MVVM 패턴
- Model: Market, MarketData(JSON)  
- View: CalendarView, MarketDetailSheet, FilterSheet  
- ViewModel: MarketPreferences, InterstitialAdManager  

### 상태 관리
- `@State` → 로컬 UI 상태  
- `@StateObject` → 생명주기 관리 객체  
- `@Published` → 반응형 데이터  
- `@Environment` → 시스템 값 접근  

---

## 💡 해결한 기술 과제

1. **월마다 다른 셀 높이 문제** → 장터 수 기반 동적 계산  
2. **SwiftUI 캘린더 격자선 미지원 문제** → Path 기반 직접 구현  
3. **필터 숨김 vs 실제 없음 구분** → 전체 데이터셋 비교 로직  
4. **사용자 친화적 광고 경험** → 시간·횟수 이중 제한  
5. **자정 자동 갱신 처리 문제** → ScenePhase + 재귀 타이머  
6. **한국어 달력 포맷 문제 해결** → Locale("ko_KR") 기반 커스텀 Calendar  

---
