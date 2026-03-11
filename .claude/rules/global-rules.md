# 전역 규칙 (Global Rules)

모든 에이전트는 작업 시작 전 반드시 이 파일을 읽어야 한다.

## 필독 문서

모든 에이전트 공통 필독:
- DOCS/00_META/README.md
- DOCS/00_META/POLICY_PRIORITY.md
- DOCS/01_GOVERNANCE/SERVICE_POLICY.md
- DOCS/03_SECURITY/SECURITY_BASELINE.md
- DOCS/04_DEVELOPMENT/DEV_STANDARDS.md
- DOCS/09_WORKFLOW/WORK_ITEM_POLICY.md
- DOCS/09_WORKFLOW/AGENT_EXECUTION_POLICY.md

## 핵심 원칙

1. 전역 정책(DOCS/)과 개별 작업(docs/work-items/)을 분리함
2. Work Item은 고정 단계 폴더가 아니라 동적 할당 기반임
3. 산출물은 다음 에이전트의 작업지시서 역할을 해야 함
4. 각 에이전트는 입력/실행/산출물/handoff/결과를 문서화해야 함

## 산출물 필수 포함 항목

모든 핵심 산출물에 반드시 포함:
- 목적
- 이번 단계에서 반드시 해야 할 일
- 하지 말아야 할 일
- 입력 문서
- 선행 조건
- 세부 작업 항목
- 완료 조건(AC)
- 반환해야 할 산출물
- 다음 수신자에게 넘길 메모
