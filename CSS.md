# CSS Coding Convention

### 1. 코드 스타일

**들여쓰기 및 공백**
- **들여쓰기**: 2 스페이스 사용
- **중괄호 위치**: 여는 중괄호 `{`는 같은 줄에, 닫는 중괄호 `}`는 새로운 줄에 작성
- **속성 구분**: 각 속성은 한 줄에 하나씩 작성
- **선언문 끝 세미콜론**: 항상 세미콜론 사용
- **속성값**: `0`은 단위 없이 사용 (예: `margin: 0;`), `0`이 아닌 값은 단위 포함 (예: `margin: 1rem;`)

**예시:**
```css
.selector {
  property: value;
  another-property: value;
}
```

### 2. 선택자 및 네이밍

**클래스 네이밍**
- **소문자 사용**: 모든 클래스명은 소문자로 작성
- **하이픈 사용**: 단어는 하이픈(`-`)으로 구분 (예: `.main-content`)
- **의미 있는 이름**: 역할을 설명할 수 있는 의미 있는 이름 사용

**아이디 네이밍**
- **소문자 사용**: 모든 아이디명은 소문자로 작성
- **하이픈 사용**: 단어는 하이픈(`-`)으로 구분 (예: `#main-content`)
- 아이디는 유일해야 하므로 필요할 때만 사용

**BEM 방법론**
- **Block**: `.block`
- **Element**: `.block__element`
- **Modifier**: `.block--modifier`

**예시:**
```css
.button {
  /* Block */
}

.button__icon {
  /* Element */
}

.button--primary {
  /* Modifier */
}
```

### 3. 속성 순서

속성은 논리적인 그룹으로 나누어 작성합니다. 예를 들어, 다음과 같은 순서를 따릅니다:

1. **Positioning**: `position`, `top`, `right`, `bottom`, `left`, `z-index`
2. **Box Model**: `display`, `float`, `width`, `height`, `margin`, `padding`, `border`
3. **Typography**: `font`, `line-height`, `text-align`, `color`
4. **Visual**: `background`, `background-color`, `background-image`
5. **Misc**: `transition`, `transform`, `animation`

**예시:**
```css
.selector {
  /* Positioning */
  position: relative;
  top: 10px;

  /* Box Model */
  display: block;
  width: 100px;
  height: 100px;
  margin: 10px;
  padding: 5px;
  border: 1px solid #000;

  /* Typography */
  font-size: 16px;
  line-height: 1.5;
  text-align: center;
  color: #333;

  /* Visual */
  background-color: #f5f5f5;
  background-image: url('image.jpg');

  /* Misc */
  transition: all 0.3s;
  transform: translateX(10px);
}
```

### 4. 주석

**주석 스타일**
- **구조 주석**: 주요 섹션을 설명하는 주석
- **설명 주석**: 특정 블록이나 속성을 설명하는 주석

**예시:**
```css
/* Header section */
.header {
  background-color: #333;
  color: #fff;
}

/* Navigation */
.header__nav {
  display: flex;
  justify-content: space-between;
}

/* Link styles */
.header__nav a {
  color: #fff;
  text-decoration: none;
}
```

### 5. 미디어 쿼리

**미디어 쿼리 위치**
- 관련 CSS 규칙 바로 아래에 작성하여 관련성을 유지
- 모바일 우선 접근법: 기본 스타일을 모바일 기준으로 작성하고, 큰 화면에 대한 스타일을 추가

**예시:**
```css
.button {
  padding: 10px 20px;
  font-size: 16px;
}

@media (min-width: 768px) {
  .button {
    padding: 15px 30px;
    font-size: 18px;
  }
}
```

### 6. 단위 사용

- **rem, em**: 레이아웃과 텍스트 크기
- **%**: 부모 요소에 상대적인 크기
- **px**: 픽셀 단위가 필요한 경우
- **vh, vw**: 뷰포트 단위, 반응형 디자인에 유용

**예시:**
```css
.container {
  width: 80%;
  padding: 1rem;
  font-size: 1.2em;
}

.full-height {
  height: 100vh;
}
```

### 7. 색상 사용

- **HEX 코드**: 색상을 명확하게 정의 (예: `#333`, `#ff0000`)
- **RGBA**: 투명도를 포함한 색상 (예: `rgba(255, 0, 0, 0.5)`)
- **변수 사용**: 색상을 변수로 정의하여 재사용 (CSS Variables)

**예시:**
```css
:root {
  --main-color: #3498db;
  --secondary-color: #2ecc71;
  --text-color: #333;
}

body {
  color: var(--text-color);
  background-color: var(--main-color);
}

.button {
  background-color: var(--secondary-color);
  color: #fff;
}
```
