---
title: 개 나이 계산기 (Dog Age Calculator)
subtitle: SwiftUI 기반 13개국어 지원 반려견 나이 변환 iOS 앱
start_date: 2025-10-01
end_date: 2025-11-30
role: iOS 개발자
technologies:
  - Swift
  - SwiftUI
  - AdMob
  - Combine
  - UMP SDK (GDPR)
  - iOS 14.5+
---

## 📱 프로젝트 개요

반려견의 나이를 과학적 공식에 따라 사람 나이로 변환해주는  
SwiftUI 기반 iOS 유틸리티 앱입니다.  

UC San Diego의 연구 논문에 따라 **로그 공식 기반 나이 계산**을 적용했으며,  
전 세계 사용자에게 제공하기 위해 **13개 언어를 완전 지원**합니다.  
ATT·GDPR 등 개인정보보호 규정도 준수하여 프로덕션 수준의 안정성을 확보했습니다.

전체 개발은 100% 단독으로 진행되었습니다.

---

## ⭐ 주요 기능

### 1) 과학 기반 나이 계산
- UC San Diego 성인견 변환 공식 적용  
  - `human_age = 16 × ln(dog_age) + 31`
- 견종 크기별 조정  
  - 소형 / 중형 / 대형 / 초대형견  
- 생애 주기 자동 분류  
  - 강아지 / 청소년 / 성견 / 중년 / 노견 / 초고령  

### 2) 직관적인 UI/UX
- SwiftUI 기반 반응형 화면 구성  
- Stepper + Segmented Picker로 간편 나이 입력  
- 실시간 계산 결과 카드 표시  
- iPhone · iPad 완전 지원 (유니버설 앱)  

### 3) 13개 언어 완전 지원
- 한국어, 영어, 일본어  
- 중국어(간체/번체), 스페인어, 프랑스어, 독일어  
- 이탈리아어, 포르투갈어, 러시아어  
- 아랍어, 힌디어  
- **String Catalog 기반 전체 인터페이스 국제화**  

### 4) AdMob 광고 통합
- iPhone/iPad 대응 반응형 배너 광고  
- 실제 프로덕션 광고 단위 ID 적용  
- 광고 표시 정책을 준수한 인앱 광고 구조  

---

## 🛠 핵심 기술 구현

### 1) 개인정보보호 규정 준수
- **ATT(App Tracking Transparency)**  
  - iOS 14.5+ 환경에서 추적 권한 요청 절차 적용  
- **GDPR(유럽 개인정보보호법)**  
  - Google UMP SDK로 EU 지역 동의 관리  
- **동의 흐름 제어 로직**  
  - GDPR → ATT → 광고 초기화 순으로 안전하게 처리  

### 2) 현대적 SwiftUI 아키텍처
- `@main` 매크로 기반 앱 진입점 구성  
- `async/await` 구조적 동시성 적용  
- `@MainActor` 로 UI 업데이트 스레드 안전성 확보  
- Combine 기반 반응형 상태 관리 (`@Published`, `@StateObject`)  

### 3) UIKit - SwiftUI 통합
- AdMob 배너: `UIViewRepresentable` 로 래핑  
- 네이티브 기능: `UIApplicationDelegateAdaptor` 통해 AppDelegate 활용  
- Safe Area Inset으로 광고영역 + UI 요소 충돌 방지  

### 4) 성능 및 메모리 최적화
- `@StateObject` 로 ConsentManager 싱글톤 관리  
- `@Published` 최소 데이터 변경만 반영  
- 조건부 렌더링으로 불필요한 UI 업데이트 제거  
- 메모리 사용량을 최소화한 경량 아키텍처  

---

## 💡 해결한 기술 과제

1. **다양한 견종 크기별 나이 계산 정밀화**  
   - UCSD 공식을 기반으로 크기별 가중치 적용  
2. **13개 언어 국제화 처리**  
   - String Catalog로 모든 UI 문구 시스템화  
3. **GDPR & ATT 규정 준수 흐름 충돌 문제 해결**  
   - 지역·환경별 조건문으로 정확한 순서 제어  
4. **AdMob + SwiftUI 레이아웃 충돌 문제 해결**  
   - Safe Area Inset 및 UIViewRepresentable 조합  
5. **iPad·iPhone 대응 반응형 UI 구현**  
   - Dynamic Type + GeometryReader 기반 레이아웃  
6. **고정 FPS 유지 및 뷰 재렌더링 최소화**  
   - Combine 기반 최소 상태 변경 구조 설계  

---
