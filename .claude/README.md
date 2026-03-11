# .claude/ — 에이전트 실행 정의 저장소

에이전트, 명령, 스킬, 규칙을 정의하는 실행 레이어.

## 구조

```
.claude/
  agents/         # 에이전트 정의 (active/candidate/archive)
  commands/       # 관리자 명령 세트
  skills/         # 반복 작업 스킬
  rules/          # 전역 규칙
```

## 에이전트 그룹
- foundation-group: 최초 구축 담당
- evolution-group: 운영 중 변경 담당
- intelligence-group: 운영 분석 담당
- test-group: 독립 테스트 담당
