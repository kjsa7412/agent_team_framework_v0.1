# 롤백 정책 (Rollback Policy)

## 롤백 조건

- 배포 후 서비스 장애 발생
- 핵심 기능 오작동
- 보안 취약점 발견

## 롤백 절차

### Frontend (Vercel)
1. Vercel 대시보드 → Deployments
2. 이전 배포 선택 → Promote to Production

### Backend (Railway)
1. Railway 대시보드 → Deployments
2. 이전 배포 선택 → Rollback

### Database
- DB 롤백은 별도 롤백 SQL 실행
- 반드시 사전에 롤백 SQL 준비 필요
- 데이터 손실 가능성 검토 후 실행

## 롤백 기록

롤백 실행 후:
1. 관리자에게 보고
2. docs/00_admin/decision-log.md에 기록
3. 원인 분석 후 수정 버전 준비
