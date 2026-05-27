# nontech-product-page-builder

> 비전공자도 쉽게 — 제품 사진 한 장으로 브랜드 맞춤형 상세페이지를 만드는 Claude 스킬

---

## 한국어

### 이 스킬이 하는 일

제품 사진, 회사명, 홈페이지 주소만 있으면 AI가 단계별 질문을 통해 스마트스토어·카페24·Shopify에 바로 올릴 수 있는 단일 HTML 파일을 만들어 줍니다.

HTML, CSS, 디자인을 전혀 몰라도 사용할 수 있습니다.

### 주요 기능

- **단계별 질문 흐름** — 어려운 용어 없이 사장님 말투로 질문
- **브랜드 분위기 자동 반영** — 홈페이지를 분석해 색상·레이아웃·톤 자동 추출
- **정보 분류** — 확정 정보 / AI 추정 정보 / 확인 필요 정보를 명확히 구분
- **가격 절대 임의 생성 금지** — 모르면 "가격 문의"로 처리
- **고품질 디자인** — 4개의 Claude 디자인 스킬(ui-ux-pro-max, frontend-design, make-interfaces-feel-better, emil-design-eng)을 자동 적용
- **최종 검수 체크리스트** 제공

### 설치 방법

1. 아래 파일을 다운로드합니다.

   **[`nontech-product-page-builder.skill` 다운로드](https://github.com/bongjunpyo/nontech-product-page-builder/raw/main/nontech-product-page-builder.skill)**

2. Claude Code를 열고 채팅창에 다운받은 파일을 드래그합니다.

3. 아래 문장을 입력합니다.

   ```
   제품 상세페이지 만들어줘
   ```

4. AI의 질문에 답하다 보면 HTML 파일이 완성됩니다.

### 사용 흐름

```
제품 사진 업로드
    ↓
회사명 · 홈페이지 입력
    ↓
페이지 언어 선택 (한국어 / 영어 등)
    ↓
제품 정보 입력 (모르면 건너뛰기 가능)
    ↓
AI 분석 결과 확인 · 승인
    ↓
HTML 파일 생성 + 검수 체크리스트
```

### 필수 입력

| 항목 | 설명 |
|---|---|
| 제품 사진 | 1장 이상 |
| 회사명 | 브랜드명 |
| 홈페이지 URL | 브랜드 분위기 분석에 사용 |

### 선택 입력 (몰라도 건너뛸 수 있음)

제품명 · 가격 · 핵심 장점 · 타깃 고객 · 판매 채널 · 금지 표현 · 특허증 · 인증서 · 상장 · 로고 · 리뷰 이미지 · 사용 장면 · 전후 비교 이미지

### 지원 언어

한국어 · 영어 · 일본어 · 중국어 간체 · 중국어 번체 · 베트남어 · 태국어 · 아랍어

### 주의 사항

- AI가 추정한 정보(보온 시간, 소재 등)는 게시 전 반드시 실제 수치로 확인·교체하세요.
- 가격은 사용자가 직접 입력하지 않는 한 절대 자동 생성하지 않습니다.
- 생성된 HTML은 초안입니다. 제공된 체크리스트를 확인한 후 스토어에 올리세요.

---

## English

### What this skill does

Give it a product photo, a company name, and a website URL — the AI walks you through simple questions and generates a single self-contained HTML file ready to upload to Shopify, Cafe24, Smart Store, or any other platform.

No HTML, CSS, or design knowledge required.

### Features

- **Step-by-step question flow** — plain language, no technical terms
- **Automatic brand matching** — fetches the company website and extracts colors, layout, and tone
- **Information classification** — clearly separates confirmed facts, AI inferences, and items needing verification
- **Never invents a price** — uses "Contact for pricing" if the price is unknown
- **Production-grade design** — automatically applies 4 Claude design skills (ui-ux-pro-max, frontend-design, make-interfaces-feel-better, emil-design-eng)
- **Final review checklist** included

### Installation

1. Download the file below.

   **[Download `nontech-product-page-builder.skill`](https://github.com/bongjunpyo/nontech-product-page-builder/raw/main/nontech-product-page-builder.skill)**

2. Open Claude Code and drag the downloaded file into the chat.

3. Type:

   ```
   Make a product detail page
   ```

4. Answer the AI's questions — your HTML file will be ready at the end.

### Flow

```
Upload product photo(s)
    ↓
Enter company name & website URL
    ↓
Choose page language
    ↓
Enter product info (skip anything you don't know)
    ↓
Review & approve AI analysis
    ↓
HTML file + review checklist
```

### Required inputs

| Field | Description |
|---|---|
| Product photo | At least one image |
| Company name | Brand name |
| Website URL | Used to analyze brand atmosphere |

### Optional inputs (all skippable)

Product name · Price · Key benefits · Target customer · Sales platform · Prohibited phrases · Patent certificates · Certifications · Awards · Logo · Review images · Usage photos · Before/after comparison images

### Supported languages

Korean · English · Japanese · Simplified Chinese · Traditional Chinese · Vietnamese · Thai · Arabic

### Important notes

- AI-inferred information (e.g. insulation time, materials) must be verified and replaced with official specs before publishing.
- Prices are never invented — if unknown, the page will show "Contact for pricing."
- The generated HTML is a draft. Review it against the provided checklist before uploading to your store.

---

## License

MIT
