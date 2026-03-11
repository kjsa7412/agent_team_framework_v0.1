# /work-new — 새 Work Item 생성

## 사용법
```
/work-new [제목] [요청 내용]
```

## 처리 절차

1. Work Item ID 생성: WI-YYYYMMDD-XXX-slug
2. docs/work-items/WI-{ID}/ 폴더 생성
3. _meta/work-item-master.md 작성
4. _meta/request.md 에 요청 원문 기록
5. _meta/status.md 상태를 OPEN으로 설정
6. docs/00_admin/work-item-index.md 에 등록
7. 오케스트레이터에게 분석 요청

## 산출물
- Work Item 폴더 구조
- work-item-master.md
- request.md
- status.md (OPEN)

---

## 프리셋

제목만 입력하면 아래 내용이 자동 적용됨.

### 웹서비스 개발을 위한 프로젝트 초기 프레임워크 구성

```
분류: foundation-rebuild

작업 범위:
- 모노레포 폴더 구조 생성 (front/back/tests/scripts/docs)
- Next.js(App Router) + TypeScript + Tailwind 초기 세팅
- Spring Boot + MyBatis 초기 세팅
- Supabase Auth 연동 골격
- 환경변수 구조 (.env.example)
- 로컬 실행 기준 README

완료 조건:
- 로컬에서 front/back 각각 기동 가능한 상태
- Supabase Auth 로그인 흐름 동작 확인 가능한 수준

제외 범위:
- 기능 구현 없음. 뼈대만.
```

사용 예:
```
/work-new "웹서비스 개발을 위한 프로젝트 초기 프레임워크 구성"
```
