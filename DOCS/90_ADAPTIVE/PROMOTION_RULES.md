# 승격 기준 (Promotion Rules)

## 에이전트 승격

### candidate → active
- 3개 이상의 Work Item에서 유효하게 사용됨
- 중복 역할 없음
- 관리자 승인

### active 유지 기준
- 10개 Work Item 중 최소 3개 이상에서 사용

## 스킬 승격

### candidate → active
- 3개 이상의 Work Item에서 유효하게 사용됨
- 명확한 목적과 범위 정의
- 관리자 승인

## 정책 승격

### policy_candidates → 공식 DOCS/
- 2개 이상의 Work Item에서 유효성 확인
- 기존 정책과 충돌 없음
- 관리자 승인

## 승격 절차

1. /promote-agent 또는 /promote-skill 명령 실행
2. 승격 기준 충족 여부 확인
3. AGENT_CATALOG.md / SKILL_CATALOG.md 업데이트
4. .claude/agents/ 또는 .claude/skills/ 파일 이동
5. EXPERIMENT_LOG.md에 승격 기록
