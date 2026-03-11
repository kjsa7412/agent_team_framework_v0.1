# 에러 처리 정책 (Error Handling Policy)

## Frontend 에러 처리

### API 에러
```typescript
try {
  const response = await fetch('/api/v1/...')
  if (!response.ok) {
    throw new Error(`HTTP error! status: ${response.status}`)
  }
  const data = await response.json()
} catch (error) {
  // 사용자에게 적절한 에러 메시지 표시
  console.error('API 호출 실패:', error)
}
```

### Next.js Error Boundary
- app/error.tsx: 전역 에러 처리
- 각 라우트 세그먼트에 error.tsx 추가 가능

## Backend 에러 처리

### 전역 예외 핸들러
```java
@RestControllerAdvice
public class GlobalExceptionHandler {
  @ExceptionHandler(Exception.class)
  public ResponseEntity<Map<String, Object>> handleException(Exception e) {
    Map<String, Object> response = new HashMap<>();
    response.put("success", false);
    response.put("error", e.getMessage());
    response.put("code", "INTERNAL_ERROR");
    return ResponseEntity.status(500).body(response);
  }
}
```

## 에러 코드 체계

```
AUTH_001: 인증 실패
AUTH_002: 토큰 만료
AUTH_003: 권한 없음
VALID_001: 필수값 누락
VALID_002: 유효하지 않은 형식
DATA_001: 데이터 없음
DATA_002: 중복 데이터
SYS_001: 시스템 오류
```
