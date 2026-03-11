# 로컬 실행 정책 (Local Run Policy)

## 사전 준비

1. Node.js (LTS) 설치
2. Java 17+ 설치
3. PostgreSQL 또는 Supabase 연결 정보 준비

## Frontend 로컬 실행

```bash
cd front
cp .env.example .env.local
# .env.local에 실제 값 입력

npm install
npm run dev
# http://localhost:3000
```

## Backend 로컬 실행

```bash
cd back
cp src/main/resources/application.yml.example src/main/resources/application-local.yml
# application-local.yml에 실제 값 입력

./mvnw spring-boot:run -Dspring-boot.run.profiles=local
# http://localhost:8080
```

## 환경변수 설정

각 .env.example 파일을 참고하여 로컬 환경변수 설정.
실제 환경변수 값은 관리자에게 문의.

## 주의사항

- .env.local, application-local.yml 파일은 절대 커밋하지 않음
- 로컬에서 운영 DB 사용 금지 (개발 전용 DB 사용)
