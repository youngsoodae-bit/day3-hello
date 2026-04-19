# Landing Page Design Spec

## Overview

전문 서비스(디자인/컨설팅)를 소개하는 미니멀한 싱글 페이지 랜딩 페이지. GitHub Pages에 배포 가능한 단일 `index.html` 파일.

## Requirements

- 정적 HTML + Tailwind CSS CDN (빌드 도구 없음)
- 한국어 콘텐츠
- 모바일 반응형
- JavaScript 불필요

## Page Structure

### 1. Hero Section
- 큰 타이포그래피로 서비스 한 줄 소개
- CTA 버튼 ("상담 신청")
- 흰색 배경, 포인트 컬러 버튼

### 2. Service Cards Section
- 3개 카드 그리드 레이아웃
- 각 카드: 아이콘 + 서비스명 + 설명
- 모바일에서는 세로 스택

### 3. Features Section
- 체크마크 아이콘 + 특징 텍스트 리스트
- 서비스 차별점 4-5개 항목

### 4. CTA Section
- 하단 행동 유도 배너
- "지금 시작하기" 버튼
- 배경색으로 시각적 분리

### 5. Footer
- 연락처 정보
- 저작권 문구

## Design Tokens

- Primary color: 슬레이트 계열 (#1e293b)
- Accent: 인디고 (#4f46e5)
- Background: white (#ffffff)
- Text: slate-800, slate-600
- Font: 시스템 폰트 (Tailwind default)
- Spacing: 넉넉한 여백 (py-16 ~ py-24)

## Tech Stack

- HTML5
- Tailwind CSS v3 CDN
- GitHub Pages 배포
- 파일 1개: `index.html`

## Scope

- 싱글 파일, 빌드 없음
- 폼 제출 기능 없음 (CTA 버튼은 `#` 링크)
- 이미지 없음 (아이콘은 SVG 인라인 또는 이모지)
