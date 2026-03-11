# 퇴역 기준 (Deprecation Rules)

## 에이전트 퇴역

### active → deprecated
- 연속 5개 Work Item에서 미사용
- 다른 에이전트로 대체 가능
- 관리자 판단

### deprecated → archive
- 추가 3개 Work Item에서도 미사용
- 또는 명시적 대체재 존재

## 스킬 퇴역

에이전트 퇴역과 동일한 기준 적용.

## 퇴역 절차

1. /deprecate-agent 또는 /deprecate-skill 명령 실행
2. .claude/ 내 파일 이동
3. AGENT_CATALOG.md / SKILL_CATALOG.md 상태 업데이트
4. EXPERIMENT_LOG.md에 퇴역 사유 기록

## 주의사항

- 퇴역 파일은 즉시 삭제하지 않음
- deprecated: 1개월 보관 후 archive 검토
- archive: 3개월 보관 후 삭제 검토
