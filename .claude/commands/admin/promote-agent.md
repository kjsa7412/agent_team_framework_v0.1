# /promote-agent — 에이전트 승격

## 사용법
```
/promote-agent [agent-name] [from-status] [to-status]
```

예: `/promote-agent data-analyst candidate active`

## 처리 절차

1. DOCS/90_ADAPTIVE/AGENT_CATALOG.md 에서 에이전트 확인
2. DOCS/90_ADAPTIVE/PROMOTION_RULES.md 기준 충족 여부 확인
3. .claude/agents/ 내 파일 이동 (candidate → active)
4. DOCS/90_ADAPTIVE/AGENT_CATALOG.md 업데이트
5. DOCS/90_ADAPTIVE/EXPERIMENT_LOG.md 에 기록
