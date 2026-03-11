# skill: work-classifier

## 목적
Work Item을 분류하여 라우팅 결정.

## 분류 유형
- evolution-small
- evolution-large
- foundation-rebuild
- hybrid-foundation-evolution
- intelligence-only

## 판단 기준 (DOCS/09_WORKFLOW/WORK_ITEM_POLICY.md 참조)
- 기존 구조 위에서 처리 가능 → Evolution
- 구조 재설계 필요 → Foundation
- 코드 변경보다 분석 중심 → Intelligence
- 구조 + 기능 동시 → Hybrid

## 출력
- _analysis/work-classification.md
- _analysis/level-routing.md
