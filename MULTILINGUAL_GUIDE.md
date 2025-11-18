# 다국어 사이트 가이드 (Multilingual Site Guide)

## 개요
이 포트폴리오 사이트는 한국어와 영어를 지원하는 다국어 사이트입니다.

## 주요 기능

### 1. 자동 언어 감지
- 사용자의 브라우저 언어 설정을 자동으로 감지합니다
- 한국어가 아닌 경우 자동으로 영어 버전으로 리다이렉트됩니다
- 세션 스토리지를 사용하여 첫 방문 시에만 감지합니다

### 2. 언어 전환 버튼
- 헤더 네비게이션에 KO/EN 버튼이 있습니다
- 클릭하면 즉시 다른 언어로 전환됩니다
- 현재 페이지에 해당하는 언어 버전으로 이동합니다

### 3. SEO 최적화
- `hreflang` 태그로 언어별 페이지를 검색엔진에 알립니다
- 각 언어별 메타 태그가 자동으로 생성됩니다

## 파일 구조

```
/
├── _data/
│   └── translations.yml       # 모든 번역 텍스트
├── index.html                 # 한국어 홈페이지
├── projects.html              # 한국어 프로젝트 페이지
├── contact.html               # 한국어 연락처 페이지
└── en/
    ├── index.html             # 영어 홈페이지
    ├── projects.html          # 영어 프로젝트 페이지
    └── contact.html           # 영어 연락처 페이지
```

## 번역 수정 방법

### UI 텍스트 번역 수정
`_data/translations.yml` 파일에서 모든 UI 텍스트를 수정할 수 있습니다.

```yaml
ko:
  nav:
    home: "홈"
    projects: "프로젝트"
    contact: "연락처"

en:
  nav:
    home: "Home"
    projects: "Projects"
    contact: "Contact"
```

### 프로젝트 번역 추가
프로젝트 파일(`_projects/*.md`)의 frontmatter에 영어 버전을 추가할 수 있습니다:

```markdown
---
title: 프로젝트 제목
title_en: Project Title
subtitle: 프로젝트 부제목
subtitle_en: Project Subtitle
---
```

## URL 구조

- 한국어: `https://kangjeongmo.github.io/`
- 영어: `https://kangjeongmo.github.io/en/`

각 페이지:
- 홈: `/` (ko), `/en/` (en)
- 프로젝트: `/projects` (ko), `/en/projects` (en)
- 연락처: `/contact` (ko), `/en/contact` (en)

## 로컬 테스트

```bash
# Jekyll 서버 실행
bundle exec jekyll serve

# 브라우저에서 확인
# 한국어: http://localhost:4000/
# 영어: http://localhost:4000/en/
```

## GitHub Pages 배포

변경사항을 commit하고 push하면 자동으로 배포됩니다:

```bash
git add .
git commit -m "Add multilingual support"
git push origin main
```

## Upwork 프로필 활용

영어 버전 URL을 Upwork 프로필에 추가하세요:
```
https://kangjeongmo.github.io/en/
```

이렇게 하면 해외 클라이언트가 영어로 포트폴리오를 확인할 수 있습니다.

## 추가 언어 지원

새로운 언어를 추가하려면:

1. `_data/translations.yml`에 해당 언어 섹션 추가
2. `/[언어코드]/` 디렉토리 생성 (예: `/ja/` for Japanese)
3. 해당 디렉토리에 번역된 페이지 추가
4. `_includes/header.html`에 언어 선택 옵션 추가

## 문제 해결

### 번역이 표시되지 않는 경우
- Jekyll을 재빌드하세요: `bundle exec jekyll clean && bundle exec jekyll build`
- `_data/translations.yml` 파일의 YAML 문법을 확인하세요

### 언어 감지가 작동하지 않는 경우
- 브라우저의 세션 스토리지를 지우고 다시 시도하세요
- 개발자 도구 콘솔에서 JavaScript 에러를 확인하세요

## 참고사항

- 프로젝트 내용은 현재 한국어로만 작성되어 있습니다
- 개별 프로젝트를 영어로 번역하려면 각 프로젝트 파일에 영어 콘텐츠를 추가해야 합니다
- 기술 스택, 날짜 등 언어와 무관한 정보는 그대로 유지됩니다
