# [템플릿] 설계 문서

> 파일 위치: docs/work-items/{WI-ID}/outputs/design/

---

## API 설계

### POST /api/v1/{리소스}

**목적**:

**요청**:
```json
{
  "field1": "string",
  "field2": "number"
}
```

**응답**:
```json
{
  "success": true,
  "data": {}
}
```

**에러 코드**:
- 400: 잘못된 요청
- 401: 인증 필요

---

## DB 설계

### 테이블: {table_name}

| 컬럼 | 타입 | NULL | 기본값 | 설명 |
|------|------|------|--------|------|
| id | SERIAL | NOT NULL | - | PK |
| created_at | TIMESTAMP | NOT NULL | NOW() | 생성일 |
| updated_at | TIMESTAMP | NOT NULL | NOW() | 수정일 |
| is_deleted | BOOLEAN | NOT NULL | FALSE | 삭제 여부 |

---

## 프로세스 흐름

```
사용자 요청 → (검증) → (비즈니스 로직) → DB → (응답)
```

---

## 다음 수신자

→ framework-builder / feature-builder
**전달 내용**: 위 설계를 기반으로 구현 시작
