# Javascript Coding Convention

### 1. 코드 스타일

**들여쓰기 및 공백**
- **들여쓰기**: 2 스페이스 사용
- **라인 길이**: 80자 이하 유지
- **줄 끝 공백**: 허용하지 않음
- **파일 끝**: 항상 빈 줄 추가

**중괄호 사용**
- 모든 제어 구문(if, else, for, while, try 등)에서 중괄호 사용
- 여는 중괄호는 같은 줄에, 닫는 중괄호는 새로운 줄에 작성

**세미콜론**
- 세미콜론을 항상 사용

**예시:**
```javascript
if (condition) {
  // code block
} else {
  // code block
}
```

### 2. 네이밍 규칙

**변수명 및 함수명**
- **camelCase** 사용 (예: `myVariable`, `myFunction`)
- 의미 있는 이름 사용, 축약형 사용 자제

**클래스명**
- **PascalCase** 사용 (예: `MyClass`)

**상수명**
- **UPPER_CASE** 사용 (예: `MAX_LIMIT`)

**예시:**
```javascript
const MAX_LIMIT = 100;

function calculateSum(a, b) {
  return a + b;
}

class MyClass {
  constructor(name) {
    this.name = name;
  }
}
```

### 3. 변수 선언

**const와 let 사용**
- 변경되지 않는 값은 `const` 사용
- 변경될 수 있는 값은 `let` 사용
- `var` 사용 지양

**예시:**
```javascript
const MAX_LIMIT = 100;
let count = 0;
```

### 4. 함수 선언

**함수 표현식과 선언식**
- 함수 표현식 사용 지양, 함수 선언식 선호
- 화살표 함수 사용 시, 필요한 경우에만 사용

**예시:**
```javascript
// 함수 선언식
function calculateSum(a, b) {
  return a + b;
}

// 화살표 함수
const calculateSum = (a, b) => a + b;
```

### 5. 객체 및 배열

**객체와 배열 선언**
- 객체와 배열 선언 시, 마지막 요소에 쉼표 사용
- 속성명은 따옴표 없이 작성

**예시:**
```javascript
const person = {
  firstName: 'John',
  lastName: 'Doe',
};

const numbers = [1, 2, 3, 4, 5];
```

### 6. 주석

**주석 스타일**
- 단일 행 주석: `//` 사용
- 다중 행 주석: `/* */` 사용

**주석 위치**
- 함수나 중요한 코드 블록 상단에 주석 작성
- 복잡한 로직이 있는 라인에 주석 작성

**예시:**
```javascript
// This function calculates the sum of two numbers
function calculateSum(a, b) {
  return a + b; // Return the sum
}
```

### 7. 공백 및 정렬

**공백**
- 연산자 주위, 콤마 뒤, 중괄호 내부, 블록 사이에 공백 사용

**예시:**
```javascript
const result = a + b;

if (condition) {
  // code block
}

const array = [1, 2, 3];

function myFunction() {
  const obj = { key: 'value' };
}
```

### 8. ES6+ 기능 사용

**템플릿 리터럴**
- 문자열 결합 시, 템플릿 리터럴 사용

**예시:**
```javascript
const name = 'John';
const greeting = `Hello, ${name}!`;
```

**디스트럭처링 할당**
- 객체와 배열의 디스트럭처링 할당 사용

**예시:**
```javascript
const person = { firstName: 'John', lastName: 'Doe' };
const { firstName, lastName } = person;

const numbers = [1, 2, 3, 4, 5];
const [first, second, ...rest] = numbers;
```

**모듈 사용**
- 모듈 시스템을 사용하여 코드를 분리하고 재사용성 높이기

**예시:**
```javascript
// module.js
export const MAX_LIMIT = 100;

export function calculateSum(a, b) {
  return a + b;
}

// main.js
import { MAX_LIMIT, calculateSum } from './module';
```

### 9. 에러 처리

**try-catch 사용**
- 오류가 발생할 가능성이 있는 코드 블록에는 `try-catch` 사용
- 에러 메시지를 명확히 작성

**예시:**
```javascript
try {
  // code that may throw an error
} catch (error) {
  console.error('An error occurred:', error.message);
}
```
