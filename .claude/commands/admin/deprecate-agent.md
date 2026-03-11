# /deprecate-agent — 에이전트 퇴역

## 사용법
```
/deprecate-agent [agent-name] [이유]
```

## 처리 절차

1. DOCS/90_ADAPTIVE/DEPRECATION_RULES.md 기준 확인
2. .claude/agents/ 내 파일 이동 (active → candidate 또는 archive)
3. AGENT_CATALOG.md 상태 업데이트
4. EXPERIMENT_LOG.md 에 퇴역 사유 기록
