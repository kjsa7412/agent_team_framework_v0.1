# 백엔드 스택 (Backend Stack)

## 기술 스택

- **프레임워크**: Spring Boot
- **ORM**: MyBatis
- **언어**: Java
- **배포**: Railway

## 핵심 설계 결정

### DTO 미사용
- Controller, Service, Mapper 간 데이터 전달에 Map 사용
- `Map<String, Object>` 기반으로 통일

### MyBatis 설정
- XML Mapper 파일 사용
- resultType: `java.util.Map`
- parameterType: `java.util.Map`

## 디렉토리 구조 (back/)

```
back/
  src/main/java/
    controller/   # REST 컨트롤러
    service/      # 비즈니스 로직
    mapper/       # MyBatis 매퍼 인터페이스
    config/       # 설정 클래스 (Security, CORS 등)
    filter/       # JWT 필터 등
  src/main/resources/
    mapper/       # MyBatis XML 파일
    application.yml
  src/test/
```

## 환경변수

```yaml
spring:
  datasource:
    url: ${DATABASE_URL}
    username: ${DATABASE_USER}
    password: ${DATABASE_PASSWORD}

supabase:
  jwt-secret: ${SUPABASE_JWT_SECRET}
```

## JWT 인증

Supabase JWT 토큰을 서버에서 검증.
`Authorization: Bearer {supabase-jwt-token}` 헤더 사용.

## API 응답 형식

```json
{
  "success": true,
  "data": {},
  "message": "성공"
}
```

에러 응답:
```json
{
  "success": false,
  "error": "에러 메시지",
  "code": "ERROR_CODE"
}
```
