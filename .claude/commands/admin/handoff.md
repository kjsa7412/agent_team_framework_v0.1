# /handoff — 에이전트 간 Handoff 처리

## 사용법
```
/handoff [WI-ID] [from-agent] [to-agent]
```

## 처리 절차

1. from-agent의 handoff.md 확인
2. 필수 산출물 완료 여부 확인
3. to-agent의 inputs.md 에 handoff 내용 기록
4. _meta/status.md 업데이트
5. to-agent 실행 트리거
