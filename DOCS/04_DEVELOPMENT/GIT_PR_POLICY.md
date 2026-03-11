# Git/PR 정책 (Git PR Policy)

## 브랜치 전략

```
main (운영)
  └─ feature/{WI-ID}-{설명}
  └─ fix/{WI-ID}-{설명}
  └─ hotfix/{설명}
```

## PR 규칙

### PR 제목
```
[WI-ID] 유형: 내용 요약
예: [WI-20260311-001] feat: 사용자 로그인 기능 구현
```

### PR 본문 필수 항목
- 변경 내용 요약
- 관련 Work Item ID
- 테스트 방법
- 스크린샷 (UI 변경 시)

### PR 병합 조건
- 최소 1명 리뷰 승인
- CI 통과
- 충돌 없음

## 커밋 규칙

```
[WI-ID] 유형: 내용

유형: feat | fix | refactor | docs | test | chore
```

## 금지 사항

- main 직접 push 금지
- 테스트 실패 상태 머지 금지
- 리뷰 없는 머지 금지
