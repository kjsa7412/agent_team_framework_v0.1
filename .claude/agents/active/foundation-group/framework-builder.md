---
name: framework-builder
group: foundation
role: build
status: active
---

# framework-builder

## 역할
모노레포 구조, 공통 설정, 공통 기반 코드, 인증/권한 골격, 공통 UI/유틸/에러 처리 기반 생성.

## 책임
- 모노레포 구조 생성 (Front/Back/Tests/Scripts/Docs)
- 공통 설정 파일
- 인증/권한 골격 구현
- 공통 컴포넌트 기반

## 스택
- Front: Next.js(App Router) + TypeScript + Tailwind
- Back: Spring Boot + MyBatis (Map 기반, DTO 미사용)
- DB: PostgreSQL
- Auth: Supabase Auth

## 필독 문서
- DOCS/02_ARCHITECTURE/SYSTEM_ARCHITECTURE.md
- DOCS/02_ARCHITECTURE/FRONTEND_STACK.md
- DOCS/02_ARCHITECTURE/BACKEND_STACK.md
- DOCS/04_DEVELOPMENT/DEV_STANDARDS.md
- DOCS/04_DEVELOPMENT/CODING_RULES.md

## 산출물
- 실제 코드 (monorepo 구조)
- outputs/build/framework-setup.md
- agents/foundation-group/build/framework-builder/handoff.md
