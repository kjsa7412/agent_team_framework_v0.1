# /work-start — Work Item 실행 시작

## 사용법
```
/work-start [WI-ID]
```

## 처리 절차

1. _analysis/work-classification.md 분류 실행
2. _analysis/level-routing.md 라우팅 결정
3. _analysis/agent-assignment.md 에이전트 할당
4. 해당 그룹 오케스트레이터 실행
5. _meta/status.md 상태를 IN_PROGRESS로 변경

## 분류 유형
- evolution-small
- evolution-large
- foundation-rebuild
- hybrid-foundation-evolution
- intelligence-only
