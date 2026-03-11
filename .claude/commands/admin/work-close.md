# /work-close — Work Item 종료

## 사용법
```
/work-close [WI-ID]
```

## 처리 절차

1. _meta/closure-summary.md 작성
2. DOCS/90_ADAPTIVE/EXPERIMENT_LOG.md 에 학습 로그 기록
3. _meta/status.md 를 CLOSED로 변경
4. docs/00_admin/work-item-index.md 업데이트
5. 후속 Work Item 필요 여부 판단

---

## 종료 후 결과 검증 체크리스트

Work Item 종료 시 아래 항목을 확인하고 결과를 관리자에게 보고함.

### 1. 폴더 구조
- [ ] `docs/work-items/WI-{ID}/` 폴더가 존재하는가
- [ ] `_meta/`, `_analysis/`, `agents/`, `outputs/` 하위 폴더가 있는가
- [ ] `agents/`에 실제 투입된 에이전트 폴더만 생성됐는가 (미투입 에이전트 폴더 없어야 함)
- [ ] `outputs/`에 실제 산출물 폴더만 생성됐는가

### 2. 분석 문서
- [ ] `_analysis/work-classification.md` — 분류 결과 기록됐는가
- [ ] `_analysis/level-routing.md` — Foundation/Evolution/Hybrid 라우팅 판단 기록됐는가
- [ ] `_analysis/agent-assignment.md` — 투입 에이전트 목록과 역할 기록됐는가

### 3. 에이전트 실행 기록
- [ ] 각 에이전트 폴더에 `execution.md`, `inputs.md`, `outputs.md` 있는가
- [ ] 각 에이전트 `handoff.md`에 다음 수신자와 넘길 내용이 명시됐는가
- [ ] 각 에이전트 `result.md`에 실행 결과가 기록됐는가

### 4. 산출물
- [ ] `outputs/`에 실제 파일(코드, 설계 문서 등)이 쌓였는가
- [ ] 완료 조건(AC)이 모두 충족됐는가

### 5. 종료 문서
- [ ] `_meta/closure-summary.md` 작성됐는가
- [ ] `DOCS/90_ADAPTIVE/EXPERIMENT_LOG.md`에 학습 로그 기록됐는가

위 체크리스트 결과를 요약하여 관리자에게 보고함.
