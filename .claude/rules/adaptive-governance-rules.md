# 적응형 거버넌스 규칙 (Adaptive Governance Rules)

## 핵심 원칙

1. 새 역할과 스킬은 처음부터 정답으로 보지 않음
2. 보정 필요 사항은 DOCS/90_ADAPTIVE/에 기록
3. 반복적으로 유효한 경우에만 승격
4. 자주 쓰지 않거나 중복되는 항목은 deprecated/archive로 이동
5. Work Item 종료 시 학습 로그를 남김

## 상태 정의

- active: 공식 운영 중
- candidate: 유효성 검증 중
- deprecated: 중심 구조에서 밀려난 상태 (아직 삭제 안 함)
- archive: 장기간 미사용 또는 대체재 존재

## 승격 기준

candidate → active: 3회 이상 유효하게 사용된 경우

## 퇴역 기준

active → deprecated: 5개 이상의 Work Item에서 미사용
deprecated → archive: 추가 3개 이상의 Work Item에서 미사용
