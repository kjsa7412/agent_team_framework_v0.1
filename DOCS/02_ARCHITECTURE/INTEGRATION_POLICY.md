# 연동 정책 (Integration Policy)

## Supabase Auth 연동

### Frontend
```typescript
// 로그인
const { data, error } = await supabase.auth.signInWithPassword({
  email, password
})

// JWT 토큰을 API 요청 헤더에 포함
const token = (await supabase.auth.getSession()).data.session?.access_token
```

### Backend
- Supabase JWT Secret으로 토큰 검증
- Spring Security Filter에서 처리

## API 통신

- Frontend → Backend: REST API
- 인증 헤더: `Authorization: Bearer {jwt-token}`
- Content-Type: `application/json`
- CORS: Backend에서 Vercel 도메인 허용 설정

## 환경별 API URL

| 환경 | URL |
|------|-----|
| 로컬 | http://localhost:8080 |
| 운영 | Railway 배포 URL |
