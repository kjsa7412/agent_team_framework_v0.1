# /evolution-run — Evolution Group 실행

## 사용법
```
/evolution-run [WI-ID]
```

## 처리 절차

1. evolution-orchestrator 실행
2. 변경 규모 판단 (evolution-small / evolution-large)
3. change-planning-agent → change-design-agent 순서
4. change-builder / change-integration-builder / bug-fixer 할당
5. 각 에이전트 산출물을 outputs/ 에 저장

## 투입 에이전트
- evolution-orchestrator
- change-planning-agent
- change-design-agent
- change-builder / change-integration-builder / bug-fixer
