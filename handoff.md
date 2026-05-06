# HANDOFF · Andrew의 2026년 5월 채용 작업

> 이 문서는 Anthropic 웹 인터페이스에서 Claude Opus 4.7과 진행한 멀티세션 작업을 Claude Code로 이어받기 위한 컨텍스트 primer입니다.
> 작업 종료일 — 2026.05.06 / 다음 인터뷰 — 2026.05.08 (FRI) 16:00 KST

---

## 0. TL;DR for Claude Code

Andrew (도규빈, BAT IT Solutions Analyst, 6년차 PM)의 두 개 포지션 지원 작업을 진행했습니다.

1. **42dot Pleos Playground · Platform Technical Program Manager** — 서류 합격 → **5/8 16:00 1차 기술 인터뷰 예정** (45분)
2. **현대자동차 ICT Service Planner · 글로벌 오너 앱** — 서류 제출 단계, 결과 미정

각 포지션별로 영문 1페이지 resume PDF, 한국어 지원서 텍스트, 그리고 42dot 1차 인터뷰 대비 학습용 정적 웹페이지(`index.html`)까지 만들어 두었습니다. **다음 작업 가능성이 가장 높은 것은 (a) 5/8 인터뷰 직후 회고 → 2차(3시간) 대비, 또는 (b) 학습 페이지의 cross-device sync 추가 (Supabase)** 입니다.

---

## 1. Andrew에 대해 알아두어야 할 것

### 1.1 사람

- **본명** 도규빈 (Kyubin Do, "Andrew") · 1996.10.07 · 한국인 · 영국 University of Sheffield 학사 (BSc IT Management for Business · 2:1)
- **현직** British American Tobacco (BAT) IDT APMEA North · Digital Solutions Analyst (Assistant Manager, 과장)
- **거주지** 평촌 (안양) · 2026년 5월 동일 빌딩 내 이주 예정
- **언어** 한국어 native · 영어 full professional (UK 학위·근무 경험)
- **자격** PSM I, PSPO I

### 1.2 정확한 경력 산정 (이게 어떤 답변이든 영향을 줍니다)

| 회사 | 기간 | 직무 | 비고 |
|---|---|---|---|
| Samsung SDS (런던 구주총괄) | 2018.06 – 2019.06 (1년 1개월) | Project Coordinator (Year-in-Industry 인턴) | **인턴십 — 정규직 경력에서 제외하는 게 맞음** |
| TikTok (ByteDance) Korea | 2020.11 – 2021.12 (1년 2개월) | QA Analyst (Trust & Safety) | 정규직, 단 PM 직무는 아님 |
| Elice (주식회사 엘리스그룹) | 2021.12 – 2024.02 (2년 3개월) | Project Manager / Team Lead | 정규직 PM |
| BAT (현재) | 2024.03 – 재직 중 (2년 2개월~) | Digital Solutions Analyst | 정규직 PM |

- **정규직 합산** · 약 5년 7개월 (TikTok + Elice + BAT)
- **인턴 포함 합산** · 약 6년 8개월
- **순수 PM 타이틀 합산** · 약 4년 5개월 (Elice + BAT)

이 숫자는 일관되게 적용해야 합니다. 42dot 자기소개서에서는 7년 미달을 선제적으로 투명 공개하는 전략을 썼고, 현대 지원서에서는 5년 요건을 안정적으로 충족하므로 연차 화제 자체를 꺼내지 않았습니다.

### 1.3 Andrew의 작업 원칙 (CRITICAL — 이 원칙은 모든 산출물에 일관 적용되어야 함)

userMemories에서 추출한 핵심 원칙:

- **British English** · `initialise`, `colour`, `optimise`, `behaviour` 등 영국식 철자. 모든 영어 산출물·코드 주석·문서에 일관 적용.
- **Discovery-First Protocol** · 즉시 실행 ❌. 논리적 gap·ambiguity 식별 → 날카로운 clarifying question → "Technical Blueprint" 합의 → 실행. Claude가 임의로 가정하지 않을 것.
- **AI slop 금지** · "passionate about", "results-driven", "spearheaded", "leveraged", "drove impact", "perfect fit", "unique blend", "truly", "absolutely", "cutting-edge", em dash 남용, 과한 감탄, 이모티콘 — 모두 즉시 거부 시그널. 특히 ADO 티켓 코멘트 / 자기소개서 / 채용 글에서 매우 민감.
- **CONTEXT_LOG.md 권장** · 주요 결정·pivot이 있을 때마다 프로젝트 단위로 별도 로그를 권장. 이 handoff 문서 자체가 그 역할.
- **Supanova 디자인 원칙** · 8pt grid system, typographic hierarchy, generous white space, no placeholders / generic templates. 모든 UI 산출물에 적용됨.
- **AI 프롬프트는 versioned product spec** · 동일 task를 다른 서비스(Claude/Gemini/ChatGPT)에서 반복할 때 spec이 일관되어야 함. 단발성 답변 ❌.
- **PM Partner 관계** · 수동적 어시스턴트 ❌, 비판적·의견 있는·debate-oriented ✅. Andrew가 틀렸을 때는 짚어줘야 하고, 더 나은 방향이 있으면 제시해야 함.

### 1.4 Andrew의 작업 환경

- **OS** macOS · M2 MacBook Air + iPad Pro (M4 Pro MacBook Pro 이전 검토 중)
- **선호 스택** Python · Next.js · Vite · Supabase (free tier) · British English 코멘트
- **개발 워크플로우** "Vibe coding" with Google Antigravity + Claude Code
- **GitHub** `andrewdho-dev` (DMS 시연 도구 등 기존 프로젝트 호스팅)
- **개인 프로젝트 (관련 시 인지)** Salpan (saju CRM), InvestMate (포트폴리오 관리), Email Intelligence

---

## 2. 두 개 채용 포지션의 컨텍스트

### 2.1 42dot Platform TPM (Pleos Playground)

**JD 핵심**:
- 차종별로 반복되는 검증·인증을 **Platform-level Certification** 체계로 전환
- Jira, Gerrit 활용한 릴리즈/QA 자동화
- 외부 파트너사 기술 협상 단독 창구
- 보안·품질 가이드라인 정의 + 자동 검증 도구 정의
- **요건** 7년 이상 IT/클라우드/모빌리티 TPM 경험, CI/CD/API/자동화 도구 이해, 비즈니스 영어
- **우대** 보안·인증·컴플라이언스 경험, AAOS / IVI 경험, 스타트업 + 대기업 양쪽 경험

**진행 상황**:
- 서류 합격 ✓
- **1차 인터뷰 · 2026.05.08 (FRI) 16:00 KST · 45분 · "기술 인터뷰"로 명시**
- Google Meet · 채용담당자가 4개 회사 리소스 직접 공유 (Pleos 25 키노트 영상, end-to-end 자율주행 영상, Tech blog, LinkedIn)

**전략적 핵심**:
- 7년 미달 → 자기소개서에서 **선제적 투명 공개** + "그럼에도 지원한 이유는 문제 형태가 같기 때문" 논리
- BAT 일본 myGlo 프로젝트 ("로컬 Sitecore → 글로벌 Adobe Commerce 통합") = 42dot의 "차종별 반복 인증 → Platform 표준화" 와 동형 문제
- 회사 자기 정의는 **"Mobility AI Company"** (자율주행 회사 ❌)
- Pleos Playground 그룹 = App Market + 데이터 제품 + 비즈니스 운영 = **플랫폼 비즈니스** (완성차 제조 ❌)
- 양산 일정 · 2026 Q2 첫 신차 → 2030 2,000만 대 (이게 Platform 표준화의 절박성 원천)

### 2.2 현대자동차 ICT Service Planner (글로벌 오너 앱)

**JD 핵심**:
- 글로벌 오너 앱의 통합 기획·운영
- 국내·글로벌·브랜드 간 UX 차이 최소화 → 공통화·표준화 UX 전략
- 데이터 기반 서비스 개선
- 복수 이해관계자 조율
- **요건** 5년 이상 UX/서비스 기획, 비즈니스 영어, 글로벌 서비스 운영 경험

**진행 상황**:
- 지원서 작성 완료, 제출 대기 또는 제출됨 (Andrew 확인 필요)

**전략적 핵심**:
- 5년 요건은 안정적으로 충족 → 연차 화제 꺼내지 않음
- 같은 BAT 일본 프로젝트를 **Platform 표준화가 아닌 "글로벌-로컬 UX 통합"** 각도로 reframing
- TPM 타이틀이 UX/Service Planner 직무엔 약간 어색 → BAT 업무 중 UX·UAT·콘텐츠 부분을 앞으로 끌어냄
- Skills 카테고리도 Service Design 신설, Next.js/Playwright 같은 dev 스택은 의도적 제외

---

## 3. 산출물 인벤토리

### `/mnt/user-data/outputs/` 또는 Andrew의 다운로드 폴더에 있는 파일들

#### 3.1 Resume PDF (영문)

- **`Kyubin_Do_Resume_42dot.pdf`** · 42dot 타게팅 · 1페이지 · "Technical Programme Manager" 헤더 · TPM/Platform 표준화 narrative
- **`Kyubin_Do_Resume_Hyundai.pdf`** · 현대 타게팅 · 1페이지 · "Digital Service Planner" 헤더 · UX/Service Design narrative · Skills 카테고리 재편 (Service Design 신설, dev 스택 제외)

**기술 스택**: Python WeasyPrint, HTML+CSS, Fraunces (display) + Pretendard (body) + IBM Plex Mono (label) 폰트.

**HTML 소스는 outputs에 저장하지 않음** (PDF만 export). 만약 수정이 필요하면 Andrew의 자기소개서·이력서 메모리 또는 이 handoff에서 구조 복원해서 재생성하는 게 빠름.

#### 3.2 지원서 텍스트 (한국어)

- **`42dot_Application_Texts_A.md`** · 42dot 최종 버전 (A안) · Additional Information + Why Interested 두 필드 · Andrew가 검토하고 첫 단락 복원 요청한 버전이 최종
- **`42dot_Application_Texts.md`** · 42dot 초기 버전 (예전 7년 어필 논리 포함, **DEPRECATED** — 참고용)
- **`Hyundai_Application_Texts.md`** · 현대 4개 필드 모두 포함 · 직장 경력 (각 1,000자 이내) / 프로젝트 5개 / 영문 논문란 / 자기소개서 (2,000자 이내)

**글자수 검증 완료** (모든 필드 한도 내, 250자 이상 여유).

#### 3.3 42dot 1차 인터뷰 학습 도구

- **`index.html`** · 단일 HTML 파일 (~70KB) · GitHub Pages 즉시 호스팅 가능
- **`DEPLOY.md`** · GitHub Pages 배포 가이드
- **`42dot_Interview_Prep.md`** · 학습 도구의 원본 markdown (참고용, 실제 학습은 HTML로)

**기술 스택**:
- 외부 의존성 · Google Fonts CDN만 (Fraunces, Pretendard, IBM Plex Mono)
- 데이터 · localStorage (key: `'42dot-prep-v2'`)
- 빌드 도구 없음 — HTML 그대로 호스팅

**기능**:
- 3개 학습 모드 (Browse / Q&A / Cheatsheet) 탭 전환
- D-day 카운터 (1분마다 자동 갱신, 5/8 16:00 KST 타겟)
- 회사 제공 리소스 4개 시청 체크리스트
- Q&A 12개 카드 (펼침 인터랙션, 카테고리 필터, 학습 완료 토글)
- 다크/라이트 토글 (auto-persist)
- 모바일 하단 nav (768px 미만)
- 한국어 콘텐츠 + 영문 키워드 (Pretendard + IBM Plex Mono)

**구조 (Q&A 데이터)**:
```javascript
{
  id: 'q1',  // q1 ~ q12
  cat: 'A',  // A=자기소개, B=BAT검증, C=JD갭/기술깊이, D=TPM사고
  catLabel: 'A · 자기소개',
  q: '질문 텍스트',
  strategy: '답변 전략 (HTML)',
  a: `<p>모범 답변 골격 (HTML)</p>`,
  keypoints: ['키 포인트 1', ...]
}
```

#### 3.4 이전 작업 산출물 (참고)

`/mnt/user-data/outputs/42dot-interview-prep/` 디렉토리는 빈 폴더이거나 이전 산출물의 잔재. 사용 안 함.

---

## 4. 향후 작업 가능성 (확률 높은 순)

### 4.1 인터뷰 직후 회고 → 2차 (3시간) 대비

**트리거** · 5/8 16:00 인터뷰 종료 직후, Andrew가 실제 받은 질문·답변·면접관 반응을 공유.

**작업**:
1. 1차 면접에서 잘 답한 부분 / 어색했던 부분 식별
2. 2차 인터뷰 (3시간 구성) 시뮬레이션 — 1차와 다른 면접관 가정, 더 깊은 기술 깊이
3. 가능하면 동일 design system 위에 새 페이지 추가 (`/index.html`은 1차용 그대로 두고 `/round2.html` 생성, 또는 같은 페이지에 "1차/2차" 토글)

**참고할 것**:
- userMemories의 PM Partner 원칙 (debate-oriented)
- 1차에서 검증된 narrative는 2차에서도 일관 유지
- 2차는 보통 hiring manager 외 chapter lead/senior IC가 들어와서 더 디테일 검증

### 4.2 학습 페이지의 cross-device sync (Supabase)

**트리거** · Andrew가 폰↔맥북 진행도 동기화 원함.

**작업**:
- Supabase free tier 프로젝트 생성 (Andrew 계정)
- 간단한 user_progress 테이블 (anonymous user_id 기반, 또는 이메일 magic link)
- localStorage → Supabase 양방향 sync
- 실패 시 localStorage fallback

**원칙 적용**:
- 짧은 휴대용 도구이므로 over-engineering 금지
- Supanova 8pt grid · 기존 디자인 시스템 그대로 유지
- British English 코멘트

### 4.3 현대 인터뷰 대비 (서류 통과 시)

**트리거** · 현대 측 1차 인터뷰 통보.

**작업**:
- 42dot용 `index.html` 디자인 시스템을 거의 그대로 재사용
- 콘텐츠는 Service Planner 직무에 맞게 새로 작성
- 별도 디렉토리 (`/hyundai-prep/` 또는 별도 저장소)

### 4.4 추가 포지션 지원

**트리거** · Andrew가 새 JD 공유.

**작업**:
- 기존 두 resume PDF (42dot, 현대) 중 가까운 쪽을 base로 분기
- 자기소개서·지원서 텍스트는 새로 작성
- 모든 산출물에 동일 톤·동일 narrative 일관성 유지

---

## 5. 작업 시 반드시 지킬 것

### 5.1 Andrew와의 상호작용 패턴

- **Discovery-First** · 즉시 코드/산출물 만들지 말 것. 1~3개의 sharp clarifying question 먼저.
- **PM Partner** · Andrew가 잘못 판단했거나, 더 나은 방향이 있으면 즉시 짚어줄 것. 동의·아부 ❌.
- **검증된 사실만 기재** · Andrew의 경력 숫자·프로젝트 디테일·기간 등은 이 handoff의 1.2 섹션 또는 userMemories에서 확인. 추측·과장 금지.

### 5.2 산출물 톤·스타일

- 영어 산출물 → British English (`-ise`, `-our`, `-yse`)
- 한국어 산출물 → 직접적·구체적·AI slop 없는 톤
- 이력서·자기소개서 → 사실 + 숫자 + 고유명사 (Cognizant, ITC Infotech, Adobe Commerce, 9억, MAU 150만 등)
- 코드·UI → Supanova 원칙 (8pt grid, generous spacing, typographic hierarchy)

### 5.3 컨텍스트 일관성

- 42dot은 "**Mobility AI Company**", 자율주행 회사 ❌
- Pleos Playground는 "**플랫폼 비즈니스**", 자동차 제조 ❌
- BAT 일본 myGlo MAU = **약 1.5M**, 한국 myGlo MAU = **약 200K** (자기소개서·이력서 일관)
- Elice AI LMS 연구과제 = **9억 원** (절대 9백만 원 / 90억 원 금지)
- 디지털새싹캠프 = **12억 원** / **17개 시도교육청**

### 5.4 금지 사항

- **AI slop 표현** — 5.1에 나열된 거부 시그널 단어들
- **Andrew의 경력 연수를 7년이라고 표기** — 숫자 안 맞음
- **"열정", "기여하고 싶습니다"로 끝나는 closing** — Andrew가 명시적으로 거부한 패턴
- **이력서·자기소개서를 그대로 말로 옮기는 답변** — 면접 답변은 trade-off / 의사결정으로 들어가야 함
- **회사가 검색하면 나오는 정보를 묻는 역질문** — 자살

---

## 6. 다음 Claude Code 인스턴스가 처음 받을 만한 요청 예시

Andrew가 5/8 인터뷰 종료 후 보낼 가능성 높은 메시지 예시와 권장 응답:

### 시나리오 A · "면접 끝났어. 받은 질문 정리해서 줄게..."

**권장 응답 흐름**:
1. 받은 질문 정리에서 패턴 추출 (어떤 카테고리가 깊게 들어왔는지, 면접관 reaction)
2. 1차 학습 도구 (`index.html`)의 Q&A 12개 중 실제 적중한 것 / 빗나간 것 / 안 나온 것 분류
3. 2차 인터뷰 시뮬레이션을 위한 Discovery 질문 1~3개
4. 동의 받은 후 2차 학습 페이지 작업 시작

### 시나리오 B · "학습 도구를 폰이랑 맥북이랑 동기화하고 싶어"

**권장 응답 흐름**:
1. Andrew의 Supabase 프로젝트 상태 확인 (기존 InvestMate / Salpan 프로젝트 활용 가능?)
2. 인증 방식 결정 (anonymous user_id / 이메일 magic link)
3. localStorage 데이터 schema → Supabase 테이블 매핑
4. 합의 후 `index.html` 수정 + 환경변수 처리

### 시나리오 C · "다른 회사 지원하려고 하는데 [JD]"

**권장 응답 흐름**:
1. JD를 42dot / 현대 두 narrative 중 어디에 더 가까운지 분석
2. 가장 가까운 base resume + 자기소개서를 출발점으로 제안
3. JD-Andrew 핏 / 갭 분석 (Discovery)
4. 합의 후 산출물 작업

---

## 7. 부록 · 자주 참조하는 사실

### 7.1 BAT 프로젝트 디테일

**myGlo / Velo Japan 차세대 이커머스 (Experience PM)**
- 기간 · 2025.04 – 2025.10 (진행 중)
- MAU · 약 1.5M
- 스택 · Sitecore (legacy) → Adobe Commerce + AEM (target)
- 작업 · PRD 작성, 40+ 커스텀 컴포넌트 스펙, 500+ 페이지 콘텐츠 최적화, UAT 리드
- 핵심 의사결정 · "일본 고유 vs 다른 시장 재사용 가능 패턴" 분류 → 후자만 글로벌 표준 컴포넌트 가이드로 문서화

**BAT Korea 신규 이커머스 플랫폼 (PM)**
- 기간 · 2024.03 – 2026 Q1 (진행 중)
- 작업 · 비즈니스 케이스 분석, gap 식별, E2E 아키텍처 제안, T-shirt sizing
- 스택 · Adobe Commerce + Salesforce Service/Marketing Cloud + Kakao 메시징 + EDA/OMS/WMS
- ⚠️ Andrew 본인이 아키텍처를 "리드"한 게 아니라 **제안**한 것. 표현 주의.

**bat-ly**
- @bat.com-gated URL shortener · BAT Korea 마케팅팀 전체 사용
- 직접 풀스택 빌드 (사이드 프로젝트 아닌 업무 산출물)
- 데이터 거버넌스 risk 제거 + 100% UTM attribution 보존

### 7.2 회사 컨텍스트

**42dot**:
- 2019 자율주행 스타트업 창업 → 2022 현대차·기아 완전 인수 → 그룹 글로벌 SW 센터
- 2024.07 제2 판교테크노밸리 이전 (1,500명)
- 2025.12 송창현 CEO 사임 → 2026.01 박민우 사장 (AVP 본부장 겸직)
- 자체 LLM (42dot LLM 1.3B), Active Learning, Transformer 기반 perception
- 자기 정의 · "**We Are A Mobility AI Company**"

**Pleos 제품 패밀리**:
- Pleos Vehicle OS (HPVC + Zone Controller + SDV OS)
- Pleos Connect (AAOS 기반 인포테인먼트, 2026 Q2 첫 신차)
- **Pleos Playground** ← Andrew 지원 그룹 (SDK·API·디자인 가이드·App Market)
- Atria AI (자율주행 모델)
- Gleo AI (음성 에이전트)
- Pleos Fleet (차량 관제, 기아 PV5 탑재)

**양산 일정**:
- 2026 Q2 · Pleos Connect 첫 신차 출시
- 2030 · 2,000만 대 확대 목표
- 글로벌 파트너 · 구글 (AAOS), 삼성 (SmartThings), 네이버, 우버, 쏘카, 유니티

### 7.3 도메인 키워드 (Andrew가 면접 전 외워둬야 할 것)

- AAOS (Android Automotive OS)
- HPVC (High-Performance Vehicle Computer)
- SDV (Software-Defined Vehicle)
- ASPICE (자동차 SW 프로세스 평가)
- ISO 26262 (차량용 SW 기능안전 표준)
- E&E Architecture (Electrical & Electronic)
- OTA (Over-The-Air)
- NPU (Neural Processing Unit)

---

## 8. 이 handoff 문서의 한계

- **5/6 시점 기준** · 5/8 인터뷰 결과 미반영. 인터뷰 후 회고가 추가되면 이 문서 업데이트 권장.
- **Andrew의 voice·tone에 대한 외부 검증 부족** · 이력서·자기소개서를 Andrew가 최종 사용했는지 확인 필요. 일부 표현은 그가 톤다운하거나 재작성했을 수 있음.
- **회사 측 정보의 시점성** · 42dot 박민우 사장 체제, 양산 일정 등은 2026.05 시점 기준. 이후 변경 가능.
- **Resume HTML 소스 미보존** · PDF만 export됨. 재수정 필요 시 처음부터 빌드 필요. (DEPLOY.md에 디자인 시스템 명세는 있음)

---

*Last updated · 2026.05.06 · by Claude Opus 4.7 (Anthropic web interface)*
*Handoff to · Claude Code (any version)*
*Andrew의 작업 원칙은 모든 후속 작업에 일관 적용되어야 함.*