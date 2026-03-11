# 에이전트 팀 프레임워크 v0.1

## 프로젝트 개요

웹서비스 MVP를 구축하고 운영하기 위한 에이전트 팀 프레임워크.

## 기술 스택

| 영역 | 기술 |
|------|------|
| Frontend | Next.js (App Router) + TypeScript + Tailwind |
| Backend | Spring Boot + MyBatis (Map 기반, DTO 미사용) |
| Database | PostgreSQL (Supabase) |
| Auth | Supabase Auth |
| 배포 - Front | Vercel |
| 배포 - Back | Railway |
| 배포 - DB/Auth | Supabase |

## 핵심 설계 결정

- **DTO 미사용**: MyBatis에서 Map 기반으로 처리
- **Flyway 미사용**: SQL 파일 + schema_version 테이블로 이력 관리
- **모노레포**: Front/Back/Tests/Scripts/Docs 한 곳 관리

## 저장소 구조

```
DOCS/           # 전역 정책 저장소 (모든 에이전트 공통 참조)
docs/           # 작업 실행 저장소
  00_admin/     # 전역 작업 운영 관리
  work-items/   # Work Item 단위 실행 기록
.claude/        # 에이전트 실행 정의
  agents/       # 에이전트 정의 (active/candidate/archive)
  commands/     # 관리자 명령 세트
  skills/       # 반복 작업 스킬
  rules/        # 전역 규칙
```

## 에이전트 그룹

| 그룹 | 역할 | 핵심 |
|------|------|------|
| Foundation Group | 최초 구축 | 처음 만드는 힘 |
| Evolution Group | 운영 중 변경 | 계속 바꾸는 힘 |
| Intelligence Group | 운영 분석 | 보고 판단하는 힘 |
| Test Group (독립) | 품질 검증 | 테스트 자산 기반 품질 통제 |

## 기본 운영 흐름

1. `/work-new` — 새 Work Item 생성
2. `/work-start` — 분류 및 에이전트 할당
3. 에이전트 실행 (Foundation/Evolution/Intelligence)
4. Test Group 검증
5. `/work-approve` — 승인
6. `/work-close` — 종료 및 학습 기록

## 필독 문서 (작업 시작 전 필수)

- DOCS/00_META/README.md
- DOCS/00_META/POLICY_PRIORITY.md
- DOCS/01_GOVERNANCE/SERVICE_POLICY.md
- DOCS/03_SECURITY/SECURITY_BASELINE.md
- DOCS/04_DEVELOPMENT/DEV_STANDARDS.md
- DOCS/09_WORKFLOW/WORK_ITEM_POLICY.md
- DOCS/09_WORKFLOW/AGENT_EXECUTION_POLICY.md

## 적응형 원칙

이 프레임워크는 완성된 정답이 아니라 운영하며 보정되는 적응형 시스템.
보정 필요 사항은 DOCS/90_ADAPTIVE/에 누적.
