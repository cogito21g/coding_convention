# Coding Convention

## Index
1. [HTML](#html)
2. [CSS](#css)
3. [Javascript](#javascript)
4. [Python](#python)
5. [C++](#c-plus-plus)   

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


## Communication

#### 1. 커뮤니케이션 도구 및 방법
- **도구**: Slack/Teams, Trello/Jira, GitHub/GitLab, Google Meet/Zoom
- **방법**:
  - **일일 스탠드업 미팅**: 매일 진행 상황 공유
  - **주간 스프린트 회의**: 목표 설정 및 회고
  - **비동기 커뮤니케이션**: 이메일, 슬랙 채널

#### 2. 브랜치 및 워크플로우
- **브랜치 전략**:
  - `main` 또는 `master`: 배포 가능한 코드
  - `develop`: 개발 중인 코드
  - `feature/feature-name`: 기능 개발 브랜치
  - `bugfix/bug-name`: 버그 수정 브랜치
  - `release/release-version`: 릴리스 준비 브랜치
  - `hotfix/hotfix-name`: 긴급 수정 브랜치
- **워크플로우**:
  1. 기능 브랜치 생성
  2. 로컬 브랜치에서 작업 및 커밋
  3. Pull Request 생성
  4. 코드 리뷰 및 병합

#### 3. 코드 리뷰
- **절차**:
  - PR 생성 → 리뷰어 지정 → 피드백 제공 → 수정 및 재검토 → 최종 승인 및 병합
- **가이드라인**:
  - 일관된 스타일, 테스트 포함, 명확한 커밋 메시지, 최적화 및 성능 고려

#### 4. 테스트 및 배포
- **테스트**: 단위 테스트, 통합 테스트, 종단 간 테스트
- **배포**: CI/CD 도구 사용, 스테이징 환경 테스트, 배포 승인 절차

#### 5. 문서화
- **코드 주석**: 파일 주석, 함수 주석, 블록 주석, 인라인 주석
- **README**: 프로젝트 개요, 설치 방법, 사용 방법, 기여 방법

#### 6. 협업 문화
- **코드 스타일 가이드 준수**: eslint, prettier 사용
- **주기적인 회고**: 스프린트 회고, 피드백 문화
- **지식 공유**: 위키/노션 운영, 기술 세미나


## Git

#### 1. Git 설치 및 설정
- **설치**: [Git 공식 사이트](https://git-scm.com/)에서 다운로드
- **설정**:
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  ```

#### 2. Git 저장소 초기화 및 클론
- **저장소 초기화**:
  ```bash
  git init
  ```
- **저장소 클론**:
  ```bash
  git clone <repository_url>
  ```

#### 3. 파일 상태 및 작업 관리
- **상태 확인**:
  ```bash
  git status
  ```
- **파일 스테이징**:
  ```bash
  git add <file_name>
  git add .
  ```
- **변경 사항 보기**:
  ```bash
  git diff
  git diff --staged
  ```

#### 4. 커밋
- **커밋 생성**:
  ```bash
  git commit -m "Commit message"
  ```
- **커밋 메시지 수정**:
  ```bash
  git commit --amend -m "New commit message"
  ```

#### 5. 브랜치
- **브랜치 생성 및 이동**:
  ```bash
  git checkout -b <branch_name>
  ```
- **브랜치 목록 확인**:
  ```bash
  git branch
  ```
- **브랜치 전환**:
  ```bash
  git checkout <branch_name>
  ```
- **브랜치 삭제**:
  ```bash
  git branch -d <branch_name>
  git branch -D <branch_name>
  ```

#### 6. 병합 및 충돌 해결
- **브랜치 병합**:
  ```bash
  git merge <branch_name>
  ```
- **충돌 해결**:
  ```bash
  git add <resolved_file>
  git commit -m "Resolve merge conflict"
  ```

#### 7. 원격 저장소
- **원격 저장소 추가**:
  ```bash
  git remote add origin <repository_url>
  ```
- **원격 저장소 확인**:
  ```bash
  git remote -v
  ```
- **변경 사항 가져오기**:
  ```bash
  git fetch origin
  ```
- **원격 저장소와 동기화**:
  ```bash
  git pull origin <branch_name>
  ```
- **변경 사항 푸시**:
  ```bash
  git push origin <branch_name>
  ```

#### 8. 되돌리기 및 리셋
- **파일 되돌리기**:
  ```bash
  git checkout -- <file_name>
  ```
- **커밋 되돌리기**:
  ```bash
  git revert <commit_hash>
  ```
- **리셋**:
  ```bash
  git reset --soft HEAD^
  git reset --mixed HEAD^
  git reset --hard HEAD^
  ```

#### 9. 기타 유용한 명령어
- **로그 보기**:
  ```bash
  git log
  git log --oneline
  ```
- **태그**:
  ```bash
  git tag <tag_name>
  git push origin <tag_name>
  git push origin --tags
  ```

  
## Python

#### 1. 코드 레이아웃

- **들여쓰기**: 4칸의 스페이스를 사용합니다.
- **최대 줄 길이**: 79자로 제한합니다.
- **빈 줄**: 최상위 함수 및 클래스 정의 사이에는 두 줄, 클래스 내부 메서드 사이에는 한 줄을 띄웁니다.

#### 2. 공백 사용

- **연산자 주변**: 연산자 앞뒤에 한 칸의 공백을 둡니다.
- **콤마 뒤**: 인자 목록의 콤마 뒤에 한 칸의 공백을 둡니다.
- **괄호 내부**: 괄호, 대괄호, 중괄호 내부에는 공백을 두지 않습니다.

#### 3. 주석

- **블록 주석**: 여러 줄에 걸쳐 작성하며, 각 줄 앞에 `#`을 붙입니다.
- **인라인 주석**: 코드의 오른쪽에 위치하며, 코드와 주석 사이에 최소 두 칸의 공백을 둡니다.
- **독스트링 (Docstring)**: 함수, 클래스, 모듈에 대한 설명을 제공하며, 삼중 따옴표(`"""`)로 묶습니다.

#### 4. 이름 규칙

- **변수와 함수 이름**: 소문자와 밑줄을 사용합니다. (예: `my_variable`, `my_function`)
- **클래스 이름**: CamelCase를 사용합니다. (예: `MyClass`)
- **상수 이름**: 모두 대문자를 사용하고, 단어 사이는 밑줄로 구분합니다. (예: `PI`, `MAX_SIZE`)

#### 5. 문자열

- **따옴표**: 작은 따옴표(`'`) 또는 큰 따옴표(`"`) 중 하나를 선택하여 일관되게 사용합니다.
- **멀티라인 문자열**: 삼중 따옴표(`"""` 또는 `'''`)를 사용합니다.

#### 6. import문

- **위치**: import문은 항상 파일의 최상단에 위치합니다.
- **순서**: 표준 라이브러리, 서드 파티 라이브러리, 로컬 라이브러리 순으로 정렬합니다.

```python
import os
import sys

import numpy as np
import pandas as pd

from my_module import my_function
```


## Comment: Python

#### 1. 블록 주석
- 코드 블록에 대한 설명을 제공합니다.
- 각 줄 앞에 `#`을 붙여 여러 줄로 작성할 수 있습니다.

```python
# 이 함수는 두 수를 더하고 결과를 반환합니다.
# 인자:
#     a (int): 첫 번째 숫자
#     b (int): 두 번째 숫자
# 반환값:
#     int: 두 수의 합
def add(a, b):
    return a + b
```

#### 2. 인라인 주석
- 코드 라인에 대한 설명을 제공합니다.
- 코드와 주석 사이에 최소 두 칸의 공백을 둡니다.

```python
x = x + 1  # x에 1을 더합니다.
```

#### 3. 독스트링 (Docstring)
- 함수, 클래스, 모듈에 대한 설명을 제공합니다.
- 삼중 따옴표(`"""` 또는 `'''`)로 묶습니다.
- Google 스타일 또는 NumPy 스타일을 사용합니다.

##### Google 스타일
```python
def fetch_data(path: str) -> dict:
    """
    데이터 파일에서 데이터를 로드합니다.

    Args:
        path (str): 데이터 파일의 경로

    Returns:
        dict: 로드된 데이터
    """
    pass
```

##### NumPy 스타일
```python
def fetch_data(path: str) -> dict:
    """
    데이터 파일에서 데이터를 로드합니다.

    Parameters
    ----------
    path : str
        데이터 파일의 경로

    Returns
    -------
    dict
        로드된 데이터
    """
    pass
```

#### 4. 주석 작성 가이드라인
- **명확성**: 주석은 명확하고 이해하기 쉽게 작성해야 합니다.
- **간결성**: 불필요한 내용을 피하고 간결하게 작성합니다.
- **관련성**: 주석은 관련된 코드 블록에 대한 설명만 포함해야 합니다.
- **업데이트**: 코드가 변경될 때마다 주석도 함께 업데이트해야 합니다.


## C Plus Plus

1. **파일 조직 및 네이밍**
   - 파일 이름: 소문자와 언더스코어(`_`) 사용. 예: `my_class.cpp`, `my_class.h`
   - 클래스 이름: CamelCase 사용. 예: `MyClass`

2. **인덴테이션 및 공백**
   - 인덴테이션: 공백 4칸 또는 탭 1칸
   - 연산자 양쪽에 공백. 예: `a + b`

3. **네이밍 컨벤션**
   - 변수: 소문자와 언더스코어. 예: `my_variable`
   - 상수: 대문자와 언더스코어. 예: `MY_CONSTANT`
   - 함수: CamelCase 사용. 예: `MyFunction`

4. **함수**
   - 길이: 20~30줄 이하
   - 이름: 명확한 동사로 시작. 예: `CalculateTotal()`
   - 매개변수: 적게 유지, 필요시 구조체나 클래스 사용

5. **클래스**
   - 멤버 변수: `m_` 접두사 사용. 예: `m_variable`
   - 접근 지정자: `public`, `protected`, `private` 순서로 작성

6. **포인터와 레퍼런스**
   - 포인터: `int* ptr`
   - 레퍼런스: `int& ref`
   - 스마트 포인터 사용 권장

7. **조건문과 루프**
   - 중괄호 항상 사용. 예: `if (condition) { // code }`

8. **에러 처리**
   - 표준 예외 클래스 사용, 필요시 사용자 정의 예외 클래스 작성

## Comment: C Plus Plus

1. **파일 주석**
   ```cpp
   /**
    * @file filename.h
    * @brief Brief description.
    * @author Author Name
    * @date YYYY-MM-DD
    */
   ```

2. **클래스 주석**
   ```cpp
   /**
    * @class ClassName
    * @brief Brief description.
    */
   ```

3. **함수 주석**
   ```cpp
   /**
    * @brief Brief description.
    * @param[in] param Description.
    * @return Description.
    */
   ```

4. **멤버 변수 주석**
   ```cpp
   /**
    * @brief Description of the member variable.
    */
   int m_memberVariable;
   ```

5. **인라인 주석**
   ```cpp
   int value = 42;  // Initialize value
   ```

6. **TODO 주석**
   ```cpp
   // TODO: Implement this function.
   ```
