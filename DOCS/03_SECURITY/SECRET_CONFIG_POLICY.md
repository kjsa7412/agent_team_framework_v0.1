# 시크릿/설정 정책 (Secret & Config Policy)

## 시크릿 관리 원칙

1. 모든 시크릿은 환경변수로 관리
2. .env 파일은 .gitignore에 포함
3. .env.example 파일로 필요한 변수 목록만 공유
4. CI/CD 환경변수는 플랫폼 설정에서 관리 (Vercel/Railway)

## 필수 시크릿 목록

### Frontend (Vercel)
- NEXT_PUBLIC_SUPABASE_URL
- NEXT_PUBLIC_SUPABASE_ANON_KEY
- NEXT_PUBLIC_API_URL

### Backend (Railway)
- DATABASE_URL
- DATABASE_USER
- DATABASE_PASSWORD
- SUPABASE_JWT_SECRET
- ALLOWED_ORIGINS

## 시크릿 노출 시 대응

1. 즉시 해당 시크릿 무효화/재생성
2. 영향 범위 파악
3. 관리자에게 보고
4. 재배포
