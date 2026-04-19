# Landing Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 전문 서비스를 소개하는 미니멀한 싱글 페이지 랜딩 페이지를 `index.html` 하나로 구현한다.

**Architecture:** 단일 `index.html` 파일에 Tailwind CSS CDN을 로드하여 Hero → 서비스 카드 → 특징 → CTA → Footer 순서의 세로 스크롤 랜딩 페이지를 구성한다. JavaScript 없이 순수 HTML + CSS만 사용한다.

**Tech Stack:** HTML5, Tailwind CSS v3 CDN, GitHub Pages

---

## File Structure

| File | Responsibility |
|------|---------------|
| `index.html` | 전체 랜딩 페이지 (Hero, Services, Features, CTA, Footer) |

---

### Task 1: HTML 기본 구조 + Hero Section

**Files:**
- Overwrite: `index.html`

- [ ] **Step 1: HTML 기본 구조와 Hero Section 작성**

`index.html` 전체를 아래 내용으로 덮어쓴다:

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>프로웍스 | 전문 컨설팅 서비스</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-white text-slate-800">

    <!-- Hero Section -->
    <section class="min-h-screen flex items-center justify-center px-6">
        <div class="max-w-3xl text-center">
            <h1 class="text-4xl md:text-6xl font-bold text-slate-900 mb-6">
                비즈니스의<br>다음 단계를 만듭니다
            </h1>
            <p class="text-lg md:text-xl text-slate-600 mb-10">
                전문 컨설팅으로 성장 전략을 설계하고, 실행을 지원합니다.
            </p>
            <a href="#contact" class="inline-block bg-indigo-600 text-white px-8 py-4 rounded-lg text-lg font-semibold hover:bg-indigo-700 transition-colors">
                무료 상담 신청
            </a>
        </div>
    </section>

</body>
</html>
```

- [ ] **Step 2: 브라우저에서 Hero Section 확인**

로컬 서버를 실행하고 브라우저에서 Hero가 화면 중앙에 큰 타이포와 CTA 버튼으로 표시되는지 확인한다.

- [ ] **Step 3: 커밋**

```bash
git add index.html
git commit -m "feat: add Hero section"
```

---

### Task 2: Services Section

**Files:**
- Modify: `index.html` (Hero Section 뒤에 Services Section 삽입)

- [ ] **Step 1: Services Section 추가**

`</section>` (Hero 닫는 태그) 바로 뒤, `</body>` 앞에 아래 섹션을 삽입한다:

```html

    <!-- Services Section -->
    <section class="py-20 px-6 bg-slate-50">
        <div class="max-w-5xl mx-auto">
            <h2 class="text-3xl font-bold text-center mb-12">서비스</h2>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="bg-white p-8 rounded-xl shadow-sm">
                    <div class="text-3xl mb-4">&#x1f4ca;</div>
                    <h3 class="text-xl font-semibold mb-3">전략 컨설팅</h3>
                    <p class="text-slate-600">시장 분석과 경쟁사 연구를 기반으로 맞춤형 성장 전략을 수립합니다.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-sm">
                    <div class="text-3xl mb-4">&#x1f4c8;</div>
                    <h3 class="text-xl font-semibold mb-3">운영 최적화</h3>
                    <p class="text-slate-600">업무 프로세스를 분석하고 효율적인 운영 체계를 구축합니다.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-sm">
                    <div class="text-3xl mb-4">&#x1f91d;</div>
                    <h3 class="text-xl font-semibold mb-3">디지털 전환</h3>
                    <p class="text-slate-600">디지털 도구 도입과 데이터 기반 의사결정 체계를 지원합니다.</p>
                </div>
            </div>
        </div>
    </section>
```

- [ ] **Step 2: 브라우저에서 Services Section 확인**

3개 카드가 가로로 나란히 표시되고, 모바일에서는 세로로 스택되는지 확인한다.

- [ ] **Step 3: 커밋**

```bash
git add index.html
git commit -m "feat: add Services section with 3 cards"
```

---

### Task 3: Features Section

**Files:**
- Modify: `index.html` (Services Section 뒤에 Features Section 삽입)

- [ ] **Step 1: Features Section 추가**

Services Section의 닫는 `</section>` 바로 뒤에 아래 섹션을 삽입한다:

```html

    <!-- Features Section -->
    <section class="py-20 px-6">
        <div class="max-w-3xl mx-auto">
            <h2 class="text-3xl font-bold text-center mb-12">왜 프로웍스인가</h2>
            <ul class="space-y-5">
                <li class="flex items-start gap-3">
                    <span class="text-indigo-600 font-bold text-xl mt-0.5">&#10003;</span>
                    <span class="text-lg text-slate-700">10년 이상의 산업별 컨설팅 경험</span>
                </li>
                <li class="flex items-start gap-3">
                    <span class="text-indigo-600 font-bold text-xl mt-0.5">&#10003;</span>
                    <span class="text-lg text-slate-700">삼성, LG 등 대기업 프로젝트 수행</span>
                </li>
                <li class="flex items-start gap-3">
                    <span class="text-indigo-600 font-bold text-xl mt-0.5">&#10003;</span>
                    <span class="text-lg text-slate-700">데이터 기반의 객관적 분석 방법론</span>
                </li>
                <li class="flex items-start gap-3">
                    <span class="text-indigo-600 font-bold text-xl mt-0.5">&#10003;</span>
                    <span class="text-lg text-slate-700">프로젝트 완료 후 6개월 무료 후속 지원</span>
                </li>
            </ul>
        </div>
    </section>
```

- [ ] **Step 2: 브라우저에서 Features Section 확인**

체크마크가 있는 4개 항목이 세로 리스트로 표시되는지 확인한다.

- [ ] **Step 3: 커밋**

```bash
git add index.html
git commit -m "feat: add Features section with checklist"
```

---

### Task 4: CTA + Footer Section

**Files:**
- Modify: `index.html` (Features Section 뒤에 CTA와 Footer 삽입)

- [ ] **Step 1: CTA Section과 Footer 추가**

Features Section의 닫는 `</section>` 바로 뒤에 아래를 삽입한다:

```html

    <!-- CTA Section -->
    <section id="contact" class="py-20 px-6 bg-indigo-600">
        <div class="max-w-3xl mx-auto text-center">
            <h2 class="text-3xl font-bold text-white mb-6">지금 시작하세요</h2>
            <p class="text-indigo-100 text-lg mb-10">
                첫 상담은 무료입니다. 비즈니스 과제를 함께 해결해 보세요.
            </p>
            <a href="mailto:hello@proworks.kr" class="inline-block bg-white text-indigo-600 px-8 py-4 rounded-lg text-lg font-semibold hover:bg-indigo-50 transition-colors">
                hello@proworks.kr 로 문의
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-8 px-6 bg-slate-900 text-slate-400 text-center text-sm">
        <p>&copy; 2026 프로웍스. All rights reserved.</p>
    </footer>
```

- [ ] **Step 2: 브라우저에서 전체 페이지 확인**

Hero → Services → Features → CTA → Footer가 순서대로 잘 표시되고, CTA 버튼 클릭 시 메일 링크가 동작하는지 확인한다.

- [ ] **Step 3: 커밋**

```bash
git add index.html
git commit -m "feat: add CTA and Footer sections"
```

---

### Task 5: 최종 검증 및 푸시

- [ ] **Step 1: 전체 페이지 최종 확인**

브라우저에서 새로고침 후 모든 섹션이 정상 표시되는지, 모바일 크기에서 반응형이 동작하는지 확인한다.

- [ ] **Step 2: 원격 저장소에 푸시**

```bash
git push origin main
```

- [ ] **Step 3: GitHub Pages에서 배포 확인**

`https://youngsoodae-bit.github.io/day3-hello/` 접속 후 페이지가 정상 표시되는지 확인한다.
