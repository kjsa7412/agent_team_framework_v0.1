# 프론트엔드 스택 (Frontend Stack)

## 기술 스택

- **프레임워크**: Next.js (App Router)
- **언어**: TypeScript
- **스타일링**: Tailwind CSS
- **배포**: Vercel

## 디렉토리 구조 (front/)

```
front/
  app/              # Next.js App Router 페이지
    (auth)/         # 인증 관련 페이지
    (main)/         # 메인 서비스 페이지
    api/            # API Routes (필요 시)
    layout.tsx      # 루트 레이아웃
    page.tsx        # 루트 페이지
  components/       # 공통 컴포넌트
    ui/             # 기본 UI 컴포넌트
    layout/         # 레이아웃 컴포넌트
  lib/              # 유틸리티, 헬퍼
  hooks/            # 커스텀 훅
  types/            # TypeScript 타입 정의
  public/           # 정적 파일
```

## 코딩 규칙

- 컴포넌트: PascalCase
- 파일명: kebab-case
- Server Component 우선, Client Component는 최소화
- 'use client' 필요한 경우만 사용

## 환경변수

```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
NEXT_PUBLIC_API_URL=
```

## Supabase Auth 연동

```typescript
// lib/supabase.ts
import { createClient } from '@supabase/supabase-js'

export const supabase = createClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL!,
  process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY!
)
```
