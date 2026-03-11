# 코딩 규칙 (Coding Rules)

## Frontend (Next.js + TypeScript)

### 네이밍
- 컴포넌트: PascalCase (UserProfile.tsx)
- 함수/변수: camelCase (getUserData)
- 파일명: kebab-case (user-profile.tsx)
- 상수: UPPER_SNAKE_CASE (MAX_RETRY_COUNT)
- 타입/인터페이스: PascalCase (UserData)

### 컴포넌트 규칙
- Server Component 기본, Client Component 최소화
- 'use client' 필요한 경우만 사용
- props 타입 명시 필수

### API 호출
- fetch 또는 axios 사용
- 에러 처리 필수
- 로딩 상태 처리 필수

## Backend (Spring Boot + MyBatis)

### DTO 미사용
```java
// 금지
public UserDto getUserById(Long id) { ... }

// 올바른 방법
public Map<String, Object> getUserById(Long id) { ... }
```

### MyBatis 규칙
```xml
<!-- 파라미터 바인딩: #{} 사용, ${} 사용 금지 -->
<select id="getUserById" resultType="java.util.Map">
  SELECT * FROM users WHERE id = #{id}
</select>
```

### 네이밍
- 클래스: PascalCase
- 메서드/변수: camelCase
- 상수: UPPER_SNAKE_CASE
- 패키지: lowercase

### 예외 처리
- 전역 예외 핸들러 사용
- 비즈니스 예외는 커스텀 예외 클래스
- 에러 코드 표준화

## Database

- 테이블명: snake_case 복수형
- 컬럼명: snake_case
- 인덱스: idx_{테이블}_{컬럼}
