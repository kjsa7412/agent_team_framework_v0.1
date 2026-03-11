# 배포 정책 (Deploy Policy)

## 배포 환경

| 서비스 | 플랫폼 | 배포 방식 |
|--------|--------|----------|
| Frontend | Vercel | Git 연동 자동 배포 |
| Backend | Railway | Git 연동 자동 배포 |
| Database | Supabase | SQL 스크립트 수동 적용 |

## 배포 절차

### Frontend (Vercel)
1. main 브랜치에 머지
2. Vercel 자동 감지 및 배포
3. 배포 완료 확인 (Vercel 대시보드)
4. 스모크 테스트 실행

### Backend (Railway)
1. main 브랜치에 머지
2. Railway 자동 감지 및 배포
3. 배포 완료 확인 (Railway 대시보드)
4. 헬스체크 확인

### Database (Supabase)
1. SQL 파일 준비
2. 개발 DB에 먼저 적용 및 검증
3. Supabase SQL 에디터에서 운영 DB 적용
4. schema_version 테이블에 기록
5. 적용 결과 확인

## 배포 전 체크리스트

- [ ] QA 게이트 통과
- [ ] 관리자 승인
- [ ] 환경변수 설정 확인
- [ ] 롤백 계획 준비
- [ ] DB 마이그레이션 계획 (있는 경우)

## 배포 후 확인

- [ ] 서비스 정상 동작 확인
- [ ] 에러 로그 확인
- [ ] 핵심 기능 스모크 테스트
