# UX/UI 정책 (UX UI Policy)

## 기본 원칙

1. 단순하고 명확한 UI
2. 일관된 디자인 시스템
3. 반응형 레이아웃
4. 접근성 고려

## 기술 기준

- Tailwind CSS 유틸리티 클래스 활용
- 모바일 우선(Mobile First) 접근
- 다크 모드: 서비스 요구사항에 따라 결정

## UI 컴포넌트 원칙

- 공통 컴포넌트는 components/ui/에 모아서 관리
- props로 스타일 변형 가능하게 설계
- 접근성(aria-label 등) 기본 적용

## 피해야 할 패턴

- 인라인 스타일 사용 (Tailwind 클래스 사용)
- 하드코딩된 색상 (Tailwind 팔레트 사용)
- 접근성 무시
