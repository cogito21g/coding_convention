# Comment: Javascript

### 1. 파일 주석

파일 상단에 파일의 목적, 작성자, 생성일, 수정 이력 등을 기록합니다.

**예시:**
```javascript
/**
 * 파일명: example.js
 * 작성자: 홍길동
 * 생성일: 2024-06-16
 * 설명: 이 파일은 사용자 로그인 기능을 포함하고 있습니다.
 * 수정 이력:
 *   - 2024-06-17: 비밀번호 암호화 기능 추가 (작성자: 이몽룡)
 */
```

### 2. 함수 주석

함수 상단에 함수의 역할, 매개변수, 반환값 등을 설명합니다.

**예시:**
```javascript
/**
 * 사용자 로그인 함수
 * @param {string} email - 사용자 이메일
 * @param {string} password - 사용자 비밀번호
 * @returns {boolean} - 로그인 성공 여부
 */
function login(email, password) {
  // 로그인 로직...
}
```

### 3. 블록 주석

코드 블록의 목적을 설명하거나, 중요한 코드 부분에 대한 자세한 설명을 제공합니다.

**예시:**
```javascript
/**
 * 사용자 데이터 처리 블록
 * - 사용자 데이터를 검증하고 데이터베이스에 저장합니다.
 * - 데이터 검증 실패 시, 오류 메시지를 반환합니다.
 */
try {
  validateUserData(userData);
  saveToDatabase(userData);
} catch (error) {
  console.error('데이터 처리 중 오류 발생:', error);
}
```

### 4. 인라인 주석

코드 라인 끝에 짧은 설명을 추가하여 특정 코드의 목적을 설명합니다.

**예시:**
```javascript
const MAX_LIMIT = 100; // 최대 제한 값
const count = 0; // 현재 카운트
```

### 5. TODO 주석

추후에 수정하거나 추가해야 할 작업을 기록합니다.

**예시:**
```javascript
function fetchData() {
  // TODO: 에러 처리 로직 추가
  fetch('/api/data')
    .then(response => response.json())
    .then(data => console.log(data));
}
```

### 주석 사용 예시

**파일 전체 주석 및 함수 주석:**
```javascript
/**
 * 파일명: userAuth.js
 * 작성자: 홍길동
 * 생성일: 2024-06-16
 * 설명: 사용자 인증 관련 기능을 포함하고 있습니다.
 * 수정 이력:
 *   - 2024-06-17: 이메일 인증 추가 (작성자: 이몽룡)
 */

/**
 * 사용자 로그인 함수
 * @param {string} email - 사용자 이메일
 * @param {string} password - 사용자 비밀번호
 * @returns {boolean} - 로그인 성공 여부
 */
function login(email, password) {
  // 이메일과 비밀번호를 검증
  if (!email || !password) {
    return false; // 이메일 또는 비밀번호가 없으면 실패
  }

  // TODO: 비밀번호 암호화 로직 추가

  // 로그인 성공
  return true;
}

/**
 * 사용자 로그아웃 함수
 * @returns {void}
 */
function logout() {
  // 세션 데이터 삭제
  sessionStorage.removeItem('user');
  console.log('사용자가 로그아웃되었습니다.');
}
```
