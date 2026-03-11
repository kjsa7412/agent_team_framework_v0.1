# skill: work-intake

## 목적
새 작업 요청을 Work Item으로 변환하고 초기 정보를 수집.

## 입력
- 관리자 요청 텍스트

## 처리 단계
1. 요청 파싱 (제목, 내용, 요청자, 우선순위)
2. Work Item ID 생성
3. 폴더 구조 생성
4. _meta/request.md 작성
5. _meta/status.md OPEN으로 설정
6. work-classifier 스킬 호출

## 출력
- Work Item 초기 구조
- docs/00_admin/work-item-index.md 업데이트
