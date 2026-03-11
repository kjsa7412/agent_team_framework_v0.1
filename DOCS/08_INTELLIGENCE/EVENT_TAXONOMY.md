# 이벤트 분류 체계 (Event Taxonomy)

## 이벤트 명명 규칙

```
{명사}_{동사}
예: user_signup, post_created, button_clicked
```

## 기본 이벤트 (MVP)

### 인증
- user_signup: 회원가입
- user_login: 로그인
- user_logout: 로그아웃

### 서비스 핵심
- (서비스별 핵심 이벤트 정의)

## 이벤트 속성

모든 이벤트 공통 속성:
- timestamp: 발생 시각
- user_id: 사용자 ID (비로그인 시 anonymous)
- session_id: 세션 ID
