# 강정모 - 프리랜서 개발자 포트폴리오

Jekyll 기반 1인 개발자 프리랜서 홍보 페이지입니다.

## 기능

- 프로젝트 포트폴리오
- 기술 블로그
- 경력 및 이력서
- 연락처 및 문의 폼

## 로컬 실행 방법

### 1. 사전 요구사항

- Ruby 2.7 이상
- Bundler

### 2. 의존성 설치

```bash
bundle install
```

### 3. 로컬 서버 실행

```bash
bundle exec jekyll serve
```

브라우저에서 `http://localhost:4000` 접속

### 4. 실시간 자동 빌드

```bash
bundle exec jekyll serve --livereload
```

## GitHub Pages 배포

1. GitHub에 `kangjeongmo.github.io` 저장소 생성
2. 코드를 main 브랜치에 푸시
3. Settings > Pages에서 Source를 main 브랜치로 설정
4. 몇 분 후 `https://kangjeongmo.github.io`에서 확인

## 설정 변경

`_config.yml` 파일에서 다음 정보를 수정하세요:

- `title`: 사이트 제목
- `email`: 이메일 주소
- `description`: 사이트 설명
- `author`: 작성자 정보 (이름, GitHub, LinkedIn 등)

## 컨텐츠 추가

### 새 블로그 글 작성

`_posts/` 디렉토리에 `YYYY-MM-DD-title.md` 형식으로 파일 생성:

```markdown
---
layout: post
title: "글 제목"
date: 2023-11-01 10:00:00 +0900
author: 강정모
tags: [React, JavaScript]
---

글 내용...
```

### 새 프로젝트 추가

`_projects/` 디렉토리에 `project-name.md` 파일 생성:

```markdown
---
title: 프로젝트 제목
subtitle: 프로젝트 부제목
date: 2023-09-15
role: 역할
technologies:
  - React
  - Node.js
image: /assets/images/projects/image.jpg
links:
  demo: https://example.com
  github: https://github.com/username/repo
---

프로젝트 설명...
```

## 디렉토리 구조

```
.
├── _config.yml          # Jekyll 설정
├── _layouts/            # 레이아웃 템플릿
├── _includes/           # 재사용 컴포넌트
├── _posts/              # 블로그 글
├── _projects/           # 프로젝트 포트폴리오
├── assets/
│   ├── css/            # 스타일시트
│   └── images/         # 이미지 파일
├── index.html          # 메인 페이지
├── projects.html       # 프로젝트 목록
├── blog.html           # 블로그 목록
├── resume.html         # 이력서
└── contact.html        # 연락처
```

## 커스터마이징

### 디자인 수정

`assets/css/main.css` 파일에서 CSS 변수를 수정하여 색상 테마를 변경할 수 있습니다:

```css
:root {
    --primary-color: #2c3e50;
    --secondary-color: #3498db;
    --text-color: #333;
    /* ... */
}
```

### 네비게이션 메뉴 수정

`_includes/header.html` 파일에서 메뉴 항목을 추가/수정할 수 있습니다.

## 문의 폼 설정

`contact.html`의 form action을 [Formspree](https://formspree.io/) 또는 다른 폼 서비스로 설정하세요:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

## 라이선스

MIT License

## 연락처

- Email: your.email@example.com
- GitHub: https://github.com/kangjeongmo
