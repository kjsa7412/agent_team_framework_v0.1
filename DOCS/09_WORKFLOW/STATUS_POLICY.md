# 상태 정책 (Status Policy)

## Work Item 상태

| 상태 | 설명 | 전환 조건 |
|------|------|----------|
| OPEN | 작업 접수 | /work-new 실행 시 |
| IN_PROGRESS | 진행 중 | /work-start 실행 시 |
| REVIEW | 검토 중 | /work-review 실행 시 |
| APPROVED | 승인됨 | /work-approve 실행 시 |
| CLOSED | 완료 | /work-close 실행 시 |
| BLOCKED | 차단됨 | 블로커 발생 시 |

## 에이전트 상태

| 상태 | 설명 |
|------|------|
| WAITING | 입력 대기 |
| IN_PROGRESS | 작업 중 |
| DONE | 완료 |
| BLOCKED | 차단됨 |
| SKIPPED | 이번 Work Item에서 불필요 |

## 상태 기록

모든 상태 변경은 _meta/status.md에 타임스탬프와 함께 기록.
