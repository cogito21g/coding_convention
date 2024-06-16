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


## Comment: HTML

1. **파일 주석**
   - 파일의 목적, 작성자, 생성일 등을 파일 상단에 기록
   ```html
   <!-- 
     파일명: index.html
     작성자: 홍길동
     생성일: 2024-06-16
     설명: 이 파일은 메인 페이지의 구조를 정의합니다.
   -->
   ```

2. **섹션 주석**
   - 주요 섹션을 구분하기 위해 섹션 상단에 주석 추가
   ```html
   <!-- Header section starts -->
   <header>
     <h1>My Website</h1>
   </header>
   <!-- Header section ends -->
   ```

3. **블록 주석**
   - 특정 블록의 목적을 설명하기 위해 주석 추가
   ```html
   <!-- Main content starts -->
   <main>
     <section id="home">
       <h2>Welcome to My Website</h2>
       <p>This is the home section.</p>
     </section>
   </main>
   <!-- Main content ends -->
   ```

4. **인라인 주석**
   - 특정 코드 라인의 목적이나 기능을 설명하기 위해 주석 추가
   ```html
   <img src="image.jpg" alt="Example Image" /> <!-- Example image for the home section -->
   ```

5. **TODO 주석**
   - 추후 수정이나 추가할 작업을 기록
   ```html
   <!-- TODO: Add more sections to the main content -->
   <main>
     <section id="home">
       <h2>Welcome to My Website</h2>
       <p>This is the home section.</p>
     </section>
   </main>
   ```

## Comment: CSS

1. **주석 기본 형태**
   - 단일 행 주석: `/* This is a single-line comment */`
   - 다중 행 주석: 
     ```css
     /*
       This is a multi-line comment
       You can use it to explain more complex logic or sections
     */
     ```

2. **주석 용도**

   **1. 섹션 주석**
   - 파일을 주요 섹션으로 나누어 각 섹션의 시작 부분에 주석 추가
     ```css
     /* ==========================================================================
        Base Styles
        ========================================================================== */
     ```

   **2. 블록 주석**
   - 특정 스타일 블록의 목적이나 기능을 설명하는 주석
     ```css
     /* Primary Button Styles */
     .button-primary {
       background-color: #007bff;
       color: white;
       border: none;
       padding: 10px 20px;
       cursor: pointer;
     }
     ```

   **3. 인라인 주석**
   - 특정 속성의 목적이나 기능을 설명하기 위해 인라인으로 작성하는 주석
     ```css
     .button-primary {
       background-color: #007bff; /* Main button color */
       color: white; /* Text color */
       border: none; /* Remove border */
     }
     ```

   **4. TODO 주석**
   - 추후 수정하거나 추가해야 할 작업을 기록
     ```css
     /* TODO: Add responsive styles for mobile */
     @media (max-width: 600px) {
       .button-primary {
         width: 100%;
       }
     }
     ```


## Git Commit Message

#### Commit Message 구조
1. **제목 (subject)**: `<타입>(<범위>): <변경 사항 요약>`
   - 50자 이내
   - 대문자로 시작, 마침표 사용 금지
2. **본문 (body)**: (선택 사항)
   - 한 줄 비워두고 작성
   - 한 줄당 72자 이내
   - 변경 이유와 주요 변경 사항 설명
3. **푸터 (footer)**: (선택 사항)
   - 한 줄 비워두고 작성
   - 관련된 이슈 번호나 참고 정보

#### Commit Message 타입
- **feat**: 새로운 기능 추가
- **fix**: 버그 수정
- **docs**: 문서 수정
- **style**: 코드 포맷팅, 세미콜론 누락 등 (기능 변화 없음)
- **refactor**: 코드 리팩토링 (기능 변화 없음)
- **test**: 테스트 추가 또는 수정
- **chore**: 빌드 작업, 패키지 매니저 설정 등 (기타 변경 사항)

#### 예시
**간단한 예시:**
```
fix(button): correct typo in class name
```

**자세한 예시:**
```
feat(auth): add JWT authentication

Implemented JSON Web Token (JWT) authentication to enhance security. 
Users can now log in using their credentials and receive a token for 
subsequent requests. This update also includes unit tests for the 
authentication module.

Resolves: #456
```

#### 작성 규칙
1. 현재 시제 사용 (예: "Add feature")
2. 명령형 사용 (예: "Fix bug")
3. 적절한 타입 사용 (feat, fix, docs, etc.)
4. 관련 이슈 번호 포함
5. 일관성 유지


## Git Strategy

#### 1. Git 브랜치 전략

**1.1 Git Flow**
- **브랜치 종류**: `main`, `develop`, `feature/*`, `release/*`, `hotfix/*`, `bugfix/*`
- **워크플로우**: 
  1. `develop`에서 `feature` 브랜치 생성
  2. `feature` 완료 후 `develop`에 병합
  3. 릴리스 준비 시 `release` 브랜치 생성
  4. 릴리스 후 `release`를 `main`과 `develop`에 병합
  5. 긴급 수정은 `hotfix` 브랜치에서 수행 후 `main`과 `develop`에 병합

**1.2 GitHub Flow**
- **브랜치 종류**: `main`, 기능 브랜치 (예: `feature/short-description`)
- **워크플로우**: 
  1. `main`에서 기능 브랜치 생성
  2. 기능 개발 완료 후 Pull Request 생성
  3. 코드 리뷰 및 테스트 후 `main`에 병합
  4. `main` 브랜치에서 배포

**1.3 GitLab Flow**
- **브랜치 종류**: `main`, `develop`, 기능 브랜치, 환경 브랜치 (예: `staging`, `production`)
- **워크플로우**:
  1. `develop`에서 기능 브랜치 생성
  2. 기능 완료 후 `develop`에 병합
  3. `develop`에서 환경 브랜치로 병합 (예: `staging`)
  4. 환경 브랜치에서 최종 테스트 후 `main`에 병합

#### 2. 커밋 메시지 전략

**규칙:**
1. **제목 (subject)**: 50자 이내, 대문자로 시작, 마침표 금지
2. **본문 (body)**: 72자 이내 줄, 한 줄 비워두고 작성, 변경 이유와 주요 변경 사항 설명
3. **푸터 (footer)**: 관련 이슈 번호나 참고 정보

**타입:**
- `feat`: 새로운 기능
- `fix`: 버그 수정
- `docs`: 문서 수정
- `style`: 코드 포맷팅
- `refactor`: 코드 리팩토링
- `test`: 테스트 추가
- `chore`: 기타 변경 사항

#### 3. 코드 리뷰 및 병합 전략

**코드 리뷰:**
- 모든 Pull Request는 적어도 한 명 이상의 리뷰어가 리뷰
- 코드 리뷰 시 피드백 제공 및 토론
- 주요 기능 변경 시 팀 전체 논의

**병합 전략:**
- **Squash and Merge**: 커밋 히스토리를 하나로 합쳐 깔끔하게 유지
- **Rebase and Merge**: 커밋 히스토리를 재배열하여 깔끔하게 유지, 충돌 해결 필요
- **Merge Commit**: 모든 커밋을 유지하며 병합, 히스토리가 복잡해질 수 있음

