# Work Item 규칙 (Work Item Rules)

## 생성 규칙

1. Work Item ID 형식: WI-YYYYMMDD-XXX-slug
2. 모든 작업은 Work Item으로 관리됨
3. Work Item 폴더 구조는 고정하지 않음 (동적 생성)
4. 실제 투입된 에이전트 폴더만 생성함

## 필수 문서

Work Item 내 _meta/ 필수:
- work-item-master.md
- request.md
- status.md
- output-index.md

## 상태 값

- OPEN: 작업 접수
- IN_PROGRESS: 진행 중
- REVIEW: 검토 중
- APPROVED: 승인됨
- CLOSED: 완료
- BLOCKED: 차단됨

## 참조
DOCS/09_WORKFLOW/WORK_ITEM_POLICY.md
