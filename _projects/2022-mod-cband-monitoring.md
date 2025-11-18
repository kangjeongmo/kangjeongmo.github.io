---
title: 트래픽 체커
subtitle: Electron 기반 mod_cband 트래픽 모니터링 Windows 프로그램
start_date: 2022-08-01
end_date: 2022-08-31
role: 개발자
technologies:
  - Electron
  - Node.js
  - Axios
  - Cheerio
  - TailwindCSS
---

## 프로젝트 개요

서버의 **mod_cband 상태 페이지**에서 제공하는 트래픽 사용량 정보를  
자동으로 크롤링하고, Windows 데스크톱 환경에서 보기 쉽게 시각화하는  
**트래픽 모니터링 프로그램(Traffic Checker)**을 단독 개발했습니다.

Electron을 사용해 Windows 앱 형태로 제공하며,  
Node.js 환경에서 Axios·Cheerio를 활용하여 mod_cband 상태 페이지를 파싱합니다.  
TailwindCSS를 사용해 UI를 직관적이고 빠르게 구성했습니다.

## 핵심 기능

- mod_cband 상태 페이지 자동 크롤링  
- 트래픽 사용량(업로드/다운로드/현재 사용량) 파싱  
- Electron 기반 Windows 프로그램 제공  
- TailwindCSS 기반 간결한 UI  
- 실시간 조회/새로고침 기능  
- 여러 서버를 등록해 모니터링할 수 있는 확장성 있는 구조  

## 기술 구현

### 데이터 수집 / 크롤링

- **Axios**로 mod_cband 상태 페이지 요청  
- **Cheerio**로 HTML 구조 파싱 → 트래픽 사용량 추출  
- HTML 구조가 정형화되어 있지 않은 특성을 고려하여  
  문자열 기반 파싱 + 예외 처리 로직을 병행  

### Electron 기반 Windows 앱

- Electron 메인 프로세스에서 Node.js 크롤러 실행  
- 렌더러 프로세스에서 UI와 데이터 표시  
- IPC 통신으로 크롤링 결과를 UI에 전달  
- Windows 사용자를 위한 간편 실행(.exe) 앱으로 패키징  

### UI / 디자인

- TailwindCSS로 빠르고 가볍게 UI 스타일 구성  
- 실시간 트래픽 상태를 한 눈에 확인할 수 있도록  
  색상 기반 Highlight 적용 (예: 사용량 높을 때 경고 색상 표시)  
- 여러 서버를 등록해 모니터링할 수 있는 리스트 구성  

## 성과

- 서버 트래픽 상태를 매번 웹 브라우저로 열 필요 없이  
  **Windows 앱에서 실시간으로 확인 가능**  
- Electron 기반으로 누구나 설치·실행할 수 있는 형태 제공  
- 서버 관리자들의 업무 효율 증가  
- mod_cband 상태 페이지의 불편한 텍스트 형태 데이터를  
  사용자 친화적인 UI로 변환  

## 기술적 도전과 해결

mod_cband 페이지는 표준화되지 않은 HTML 텍스트 구조라  
정확한 트래픽 숫자를 추출하는 것이 가장 까다로웠습니다.

이를 해결하기 위해:

- Cheerio로 HTML을 DOM처럼 파싱 후  
  패턴 분석을 통해 필요한 숫자만 안정적으로 추출  
- Axios 요청 실패 대비 예외처리 및 재시도 로직 추가  
- Electron의 메인 프로세스와 렌더러 간 IPC 구조를 이용해  
  데이터 흐름을 명확히 분리해 유지보수성 확보  

그 결과, 복잡한 HTML에서 필요한 데이터만 깨끗하게 추출하여  
Windows UI로 안정적으로 제공할 수 있는  
경량 트래픽 체크 프로그램을 구축했습니다.
