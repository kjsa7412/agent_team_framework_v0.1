# 시스템 아키텍처 (System Architecture)

## 모노레포 구조

```
project-root/
  front/          # Next.js (App Router) + TypeScript + Tailwind
  back/           # Spring Boot + MyBatis
  tests/          # 테스트 코드
  scripts/        # 유틸리티 스크립트
  docs/           # 서비스 문서
  DOCS/           # 프레임워크 전역 정책
  .claude/        # 에이전트 실행 정의
```

## 기술 스택 요약

| 영역 | 기술 |
|------|------|
| Frontend | Next.js (App Router) + TypeScript + Tailwind CSS |
| Backend | Spring Boot + MyBatis |
| Database | PostgreSQL (Supabase) |
| Auth | Supabase Auth |
| 배포 - Front | Vercel |
| 배포 - Back | Railway |
| 배포 - DB/Auth | Supabase |

## 데이터 흐름

```
사용자 → Next.js (Vercel)
           ↓ API 호출
       Spring Boot (Railway)
           ↓ DB 쿼리
       PostgreSQL (Supabase)

인증 흐름:
사용자 → Supabase Auth → JWT 토큰 → Spring Boot 검증
```

## 주요 설계 결정

1. DTO 미사용 — MyBatis에서 Map 기반으로 처리
2. Flyway 미사용 — SQL 파일 + schema_version 테이블로 이력 관리
3. 모노레포 — Front/Back/Tests/Scripts/Docs 한 곳 관리
