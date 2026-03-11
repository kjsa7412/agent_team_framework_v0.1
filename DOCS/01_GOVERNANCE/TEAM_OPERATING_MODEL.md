# 팀 운영 모델 (Team Operating Model)

## 그룹 체계

### Foundation Group
- 역할: 최초 기획안을 받아 서비스 뼈대 구축
- 핵심: "처음 만드는 힘"
- 오케스트레이터: foundation-orchestrator

### Evolution Group
- 역할: 운영 중인 서비스에 요구사항 반영, 기능 개선
- 핵심: "계속 바꾸는 힘"
- 오케스트레이터: evolution-orchestrator

### Intelligence Group
- 역할: 운영 데이터, 트래픽, 사용자 행동, VOC 분석
- 핵심: "보고 판단하는 힘"
- 오케스트레이터: intelligence-orchestrator

### Test Group (독립)
- 역할: 구축/운영/구조 재편 모두 검증
- 핵심: "테스트 자산 기반 품질 통제"
- 오케스트레이터: test-orchestrator

## 기본 운영 흐름

1. 관리자 작업 지시
2. Work Item 생성 (/work-new)
3. 오케스트레이터 분류 및 라우팅
4. 에이전트 동적 할당
5. 에이전트별 실행 및 산출물 생성
6. Test Group 시나리오 선택 및 테스트
7. 결과 검토 및 승인
8. 종료 또는 후속 Work Item 생성
9. 적응형 보정 항목 기록
