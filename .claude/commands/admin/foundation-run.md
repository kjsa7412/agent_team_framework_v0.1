# /foundation-run — Foundation Group 실행

## 사용법
```
/foundation-run [WI-ID]
```

## 처리 절차

1. foundation-orchestrator 실행
2. planning-agent → design-agent 순서로 진행
3. 설계 완료 후 build 에이전트 할당 (framework-builder / feature-builder / integration-builder)
4. devops-agent 운영 준비
5. 각 에이전트 산출물을 outputs/ 에 저장

## 투입 에이전트
- foundation-orchestrator
- planning-agent
- design-agent
- framework-builder / feature-builder / integration-builder
- devops-agent
