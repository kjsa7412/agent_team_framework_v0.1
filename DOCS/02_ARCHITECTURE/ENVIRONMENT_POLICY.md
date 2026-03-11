# 환경 정책 (Environment Policy)

## 환경 구분

| 환경 | 설명 |
|------|------|
| local | 개발자 로컬 환경 |
| production | 운영 환경 |

## 환경변수 관리

- `.env` 파일은 절대 커밋하지 않음
- `.env.example` 파일로 필요한 변수 목록만 커밋
- 실제 값은 Vercel/Railway 환경변수 설정에서 관리

## Frontend 환경변수 (.env.local)

```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
NEXT_PUBLIC_API_URL=
```

## Backend 환경변수

```
DATABASE_URL=
DATABASE_USER=
DATABASE_PASSWORD=
SUPABASE_JWT_SECRET=
ALLOWED_ORIGINS=
```

## 로컬 실행 설정

참조: DOCS/06_OPERATIONS/LOCAL_RUN_POLICY.md
