# DB 마이그레이션 정책 (DB Migration Policy)

## 기본 정책

Flyway 미사용. SQL 파일 + schema_version 테이블로 관리.

## 파일 위치

```
scripts/db/
  V001__initial_schema.sql
  V002__description.sql
```

## 네이밍 규칙

`V{3자리버전}__{설명}.sql`
예: `V001__create_users_table.sql`

## schema_version 테이블

```sql
CREATE TABLE schema_version (
  id SERIAL PRIMARY KEY,
  version VARCHAR(20) NOT NULL UNIQUE,
  description VARCHAR(200),
  script_name VARCHAR(200) NOT NULL,
  applied_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  applied_by VARCHAR(100),
  checksum VARCHAR(100)
);
```

## 적용 규칙

1. 한번 적용된 SQL은 수정 금지 (새 버전으로 추가)
2. 롤백이 필요한 경우 반드시 롤백 SQL 작성
3. 운영 DB 적용 전 개발 DB에서 검증
4. 적용 후 schema_version 테이블에 기록

## 주의사항

- DROP TABLE, TRUNCATE는 관리자 승인 필수
- 컬럼 삭제는 먼저 deprecated 처리 후 다음 버전에서 삭제
