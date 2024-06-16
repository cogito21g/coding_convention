# Coding Convention

## HTML

1. **문서 구조**
   - `<!DOCTYPE html>` 선언
   - `<html lang="en">` 사용
   - `<meta charset="UTF-8">` 설정
   - `<meta name="viewport" content="width=device-width, initial-scale=1.0">` 설정

2. **코드 스타일**
   - 2 스페이스 들여쓰기
   - 태그명, 속성명, 속성값은 소문자
   - 빈 요소는 자체 종료 태그 사용 (`<img src="image.jpg" alt="Example" />`)

3. **속성 순서**
   - `class`, `id`, `name`, `data-*`, `src`, `title`, `alt`, `role`, `aria-*`, `tabindex`, `style`

4. **주석**
   - `<!-- 주석 내용 -->` 사용

## CSS

1. **코드 스타일**
   - 2 스페이스 들여쓰기
   - 속성은 한 줄에 하나씩, 선언문 끝 세미콜론 사용

2. **선택자 및 네이밍**
   - 클래스명과 아이디명은 소문자와 하이픈(`-`) 사용
   - BEM 방법론: `.block__element--modifier`

3. **속성 순서**
   - `position`, `top`, `right`, `bottom`, `left`, `z-index`, `display`, `width`, `height`, `margin`, `padding`, `border`, `font`, `line-height`, `text-align`, `color`, `background`, `transition`, `transform`

4. **주석**
   - 구조 주석과 설명 주석 사용 (`/* 주석 내용 */`)

5. **미디어 쿼리**
   - 관련 CSS 규칙 바로 아래에 작성, 모바일 우선 접근법

6. **단위 사용**
   - `rem`, `em`, `%`, `px`, `vh`, `vw`

7. **색상 사용**
   - HEX 코드, RGBA, CSS Variables 사용

## Javascript

1. **코드 스타일**
   - **들여쓰기**: 2 스페이스
   - **라인 길이**: 80자 이하
   - **줄 끝 공백**: 허용하지 않음
   - **세미콜론**: 항상 사용
   - **중괄호**: 제어 구문에서 항상 사용

2. **네이밍 규칙**
   - **변수 및 함수명**: camelCase (예: `myVariable`, `myFunction`)
   - **클래스명**: PascalCase (예: `MyClass`)
   - **상수명**: UPPER_CASE (예: `MAX_LIMIT`)

3. **변수 선언**
   - **const와 let 사용**: `const`는 변경되지 않는 값, `let`은 변경될 수 있는 값에 사용
   - **var 사용 지양**

4. **함수 선언**
   - **함수 선언식 선호**: function 키워드 사용
   - **화살표 함수**: 필요한 경우에만 사용

5. **객체 및 배열**
   - **객체와 배열 선언 시 쉼표 사용**: 마지막 요소에 쉼표
   - **속성명은 따옴표 없이 작성**

6. **주석**
   - **단일 행 주석**: `//` 사용
   - **다중 행 주석**: `/* */` 사용
   - **주석 위치**: 함수나 중요한 코드 블록 상단, 복잡한 로직에 주석 작성

7. **공백 및 정렬**
   - **연산자 주위, 콤마 뒤, 중괄호 내부, 블록 사이에 공백 사용**

8. **ES6+ 기능 사용**
   - **템플릿 리터럴**: 문자열 결합 시 사용
   - **디스트럭처링 할당**: 객체와 배열에 사용
   - **모듈 사용**: `import`, `export`로 코드 분리

9. **에러 처리**
   - **try-catch 사용**: 오류가 발생할 가능성이 있는 코드 블록에 사용

## Comment: Jaavascript

1. **파일 주석**
   - 파일의 목적, 작성자, 생성일, 수정 이력을 파일 상단에 기록
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

2. **함수 주석**
   - 함수의 역할, 매개변수, 반환값 등을 함수 상단에 설명
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

3. **블록 주석**
   - 코드 블록의 목적을 설명하거나 중요한 코드 부분을 자세히 설명
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

4. **인라인 주석**
   - 코드 라인 끝에 짧은 설명을 추가하여 특정 코드의 목적을 설명
   ```javascript
   const MAX_LIMIT = 100; // 최대 제한 값
   const count = 0; // 현재 카운트
   ```

5. **TODO 주석**
   - 추후에 수정하거나 추가해야 할 작업을 기록
   ```javascript
   function fetchData() {
     // TODO: 에러 처리 로직 추가
     fetch('/api/data')
       .then(response => response.json())
       .then(data => console.log(data));
   }
   ```

