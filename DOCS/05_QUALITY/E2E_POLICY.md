# E2E 테스트 정책 (E2E Policy)

## E2E 테스트 범위

핵심 사용자 플로우에 대한 End-to-End 테스트.

## 최소 E2E 시나리오 (MVP)

1. 회원가입 → 로그인 → 핵심 기능 사용 → 로그아웃
2. 로그인 실패 시나리오
3. 권한 없는 접근 차단 확인

## 도구

프로젝트 특성에 맞게 선택:
- Playwright (권장)
- Cypress

## 실행 시점

- foundation-rebuild: E2E 필수
- evolution-large: 핵심 플로우 E2E 권장
- evolution-small: E2E 선택
