# 인증/권한 정책 (Auth & Authorization Policy)

## 인증 방식

- **인증 제공자**: Supabase Auth
- **토큰 방식**: JWT (Supabase 발행)
- **토큰 전달**: HTTP Header `Authorization: Bearer {token}`

## 권한 모델

### 기본 역할

| 역할 | 설명 |
|------|------|
| anonymous | 비로그인 사용자 |
| user | 일반 로그인 사용자 |
| admin | 관리자 |

역할 추가는 서비스 요구사항에 따라 확장 가능.

## Backend JWT 검증

```java
// Supabase JWT Secret으로 검증
// Spring Security Filter 에서 처리
// 검증 성공 시 SecurityContext에 사용자 정보 설정
```

## Frontend 인증 상태 관리

```typescript
// Supabase Auth 상태 구독
supabase.auth.onAuthStateChange((event, session) => {
  // 인증 상태 변경 처리
})
```

## 권한 체크 원칙

1. API 레벨에서 권한 체크 (서버사이드)
2. UI 레벨 권한 체크는 보조 수단
3. 권한 없는 접근 시 403 반환
