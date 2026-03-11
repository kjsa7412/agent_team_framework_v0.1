# 운영 정책 (Operations Policy)

## 운영 원칙

1. 운영 환경 직접 수정 금지 — 반드시 배포 프로세스를 통해 변경
2. 장애 발생 시 즉시 관리자 보고
3. 롤백 계획 없이 배포 금지
4. 운영 DB 직접 접근 최소화

## 운영 환경

| 서비스 | 플랫폼 |
|--------|--------|
| Frontend | Vercel |
| Backend | Railway |
| Database | Supabase (PostgreSQL) |
| Auth | Supabase Auth |

## 모니터링

- 서비스 상태: 각 플랫폼 대시보드 확인
- 에러 모니터링: 로그 기반
- 성능 모니터링: 필요 시 추가

## 긴급 연락 체계

장애 발생 → 관리자 즉시 보고 → 롤백 또는 핫픽스 결정
