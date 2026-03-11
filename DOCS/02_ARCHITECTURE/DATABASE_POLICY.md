# 데이터베이스 정책 (Database Policy)

## 기술 스택

- **DB**: PostgreSQL
- **호스팅**: Supabase
- **마이그레이션 도구**: 미사용 (Flyway 미사용)

## 마이그레이션 정책

### Flyway 미사용
- SQL 파일 + `schema_version` 테이블로 적용 이력 관리

### schema_version 테이블 구조

```sql
CREATE TABLE schema_version (
  id SERIAL PRIMARY KEY,
  version VARCHAR(20) NOT NULL,
  description VARCHAR(200),
  script_name VARCHAR(200) NOT NULL,
  applied_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  applied_by VARCHAR(100),
  checksum VARCHAR(100)
);
```

### SQL 파일 명명 규칙

```
scripts/db/
  V001__initial_schema.sql
  V002__add_users_table.sql
  V003__add_posts_table.sql
```

형식: `V{버전번호}__{설명}.sql`

### 적용 절차

1. SQL 파일 작성
2. 개발 DB에 적용 및 검증
3. schema_version 테이블에 기록
4. 스테이징 → 운영 순서로 적용

## 네이밍 규칙

- 테이블명: snake_case 복수형 (예: users, board_posts)
- 컬럼명: snake_case (예: created_at, user_id)
- 인덱스명: idx_{테이블명}_{컬럼명}
- 외래키: fk_{테이블명}_{참조테이블명}

## 공통 컬럼

모든 테이블에 포함:
```sql
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
created_by VARCHAR(100),
is_deleted BOOLEAN DEFAULT FALSE
```
