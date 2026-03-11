# 관측성 정책 (Observability Policy)

## 기본 관측 항목

### 서비스 가용성
- Vercel/Railway 상태 대시보드 활용
- 서비스 다운 시 즉시 알림

### 에러 모니터링
- Backend: 로그 기반 에러 추적
- Frontend: Next.js 에러 경계

### 성능 지표
- API 응답 시간
- 페이지 로딩 시간

## 로그 접근

| 서비스 | 로그 위치 |
|--------|----------|
| Frontend | Vercel 대시보드 → Functions |
| Backend | Railway 대시보드 → Logs |
| Database | Supabase 대시보드 → Logs |

## 알림 설정

MVP 단계 최소 알림:
- 서비스 다운 알림 (각 플랫폼 기본 제공)
- 에러율 급증 알림 (선택)
