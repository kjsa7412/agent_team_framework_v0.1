# Work Item 정책 (Work Item Policy)

## Work Item 정의

Work Item = 하나의 요청/문제를 해결하기 위한 실행 단위

Work Item은 다음을 담는 컨테이너:
- 작업 기본 정보
- 요청 원문
- 분석/분류 결과
- 할당 에이전트 목록
- 에이전트별 실행 기록
- 에이전트별 산출물
- 상태 기록
- 의사결정 기록
- 최종 결과 요약

## Work Item ID 형식

```
WI-YYYYMMDD-XXX-slug
예: WI-20260311-001-user-login
```

## 폴더 구조

```
docs/work-items/WI-{ID}/
  README.md           # 작업 개요
  _meta/              # 작업 메타 정보
  _analysis/          # 분석/분류/라우팅
  agents/             # 실제 투입된 에이전트만
  outputs/            # 실제 생성된 산출물만
```

## 핵심 원칙

1. 폴더 구조를 고정 단계형으로 확정하지 않음
2. 실제 투입된 에이전트 기준으로 폴더 생성
3. 각 에이전트는 입력/실행/산출물/handoff/결과를 문서화
4. 관리자가 Work Item을 열었을 때 현황을 바로 볼 수 있어야 함

## 필수 관리 정보

1. 이 작업이 무엇인지
2. 왜 들어왔는지
3. 누가 요청했는지
4. Foundation/Evolution/Intelligence/Hybrid 중 무엇인지
5. 어떤 에이전트들이 투입되었는지
6. 각 에이전트가 무엇을 만들었는지
7. 현재 어떤 상태인지
8. 완료 조건은 무엇인지
9. 어떤 결정이 내려졌는지
10. 후속 작업이 필요한지

## 상태 값

- OPEN: 작업 접수
- IN_PROGRESS: 진행 중
- REVIEW: 검토 중
- APPROVED: 승인됨
- CLOSED: 완료
- BLOCKED: 차단됨
