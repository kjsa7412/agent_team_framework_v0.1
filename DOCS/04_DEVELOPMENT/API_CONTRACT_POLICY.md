# API 계약 정책 (API Contract Policy)

## API 설계 원칙

1. RESTful 설계 원칙 준수
2. 버전 관리: `/api/v1/...`
3. 일관된 응답 구조

## URL 규칙

```
GET    /api/v1/users          # 목록 조회
GET    /api/v1/users/{id}     # 단건 조회
POST   /api/v1/users          # 생성
PUT    /api/v1/users/{id}     # 전체 수정
PATCH  /api/v1/users/{id}     # 부분 수정
DELETE /api/v1/users/{id}     # 삭제
```

## 응답 구조

### 성공
```json
{
  "success": true,
  "data": {},
  "message": "성공"
}
```

### 목록
```json
{
  "success": true,
  "data": {
    "items": [],
    "total": 100,
    "page": 1,
    "size": 20
  }
}
```

### 에러
```json
{
  "success": false,
  "error": "에러 메시지",
  "code": "ERROR_CODE"
}
```

## HTTP 상태 코드

| 코드 | 사용 시점 |
|------|----------|
| 200 | 성공 |
| 201 | 생성 성공 |
| 400 | 잘못된 요청 |
| 401 | 인증 필요 |
| 403 | 권한 없음 |
| 404 | 리소스 없음 |
| 500 | 서버 오류 |
