# DOCS — 전역 정책 저장소

모든 에이전트가 공통으로 참조하는 상위 규칙 집합.

## 폴더 구조

| 폴더 | 내용 |
|------|------|
| 00_META | 메타 정보 (이 파일, 정책 우선순위, 변경 이력, 용어사전) |
| 01_GOVERNANCE | 거버넌스 (서비스 정책, 팀 운영 모델, 승인 정책, 문서 정책) |
| 02_ARCHITECTURE | 아키텍처 (시스템, 프론트, 백엔드, DB, 연동, 환경) |
| 03_SECURITY | 보안 (기준선, 인증/권한, 시크릿, 개인정보, 감사로그) |
| 04_DEVELOPMENT | 개발 (표준, 코딩 규칙, API 계약, DB 마이그레이션, 에러 처리, PR 정책) |
| 05_QUALITY | 품질 (테스트 정책, QA 게이트, E2E, 릴리즈 가능 상태) |
| 06_OPERATIONS | 운영 (운영 정책, 로컬 실행, 배포, 롤백, 관측, 장애 대응) |
| 07_PRODUCT | 제품 (MVP 범위, RFP, UX/UI, 콘텐츠 정책) |
| 08_INTELLIGENCE | 인텔리전스 (지표, 이벤트 체계, 실험, VOC, 리포팅) |
| 09_WORKFLOW | 워크플로우 (Work Item, Handoff, 상태, 에이전트 실행, 명령 세트) |
| 90_ADAPTIVE | 적응형 (에이전트/스킬/정책 후보, 실험, 승격/퇴역) |
| 99_ARCHIVE | 아카이브 |
| 99_TEMPLATES | 템플릿 |

## 필독 규칙

모든 에이전트는 작업 시작 전 반드시 읽어야 함:
1. DOCS/00_META/README.md (이 파일)
2. DOCS/00_META/POLICY_PRIORITY.md
3. DOCS/01_GOVERNANCE/SERVICE_POLICY.md
4. DOCS/03_SECURITY/SECURITY_BASELINE.md
5. DOCS/04_DEVELOPMENT/DEV_STANDARDS.md
6. DOCS/09_WORKFLOW/WORK_ITEM_POLICY.md
7. DOCS/09_WORKFLOW/AGENT_EXECUTION_POLICY.md
