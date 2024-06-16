# Comment: CSS

### CSS 주석의 기본 형태

CSS 주석은 `/* ... */` 형태로 작성합니다. 주석 안의 내용은 브라우저에 의해 무시되며, 코드의 설명이나 주석을 남길 수 있습니다.

**기본 예시:**
```css
/* This is a single-line comment */
```

**다중 행 주석:**
```css
/*
  This is a multi-line comment
  You can use it to explain more complex logic or sections
*/
```

### 주석의 사용 용도

#### 1. 섹션 주석

파일을 주요 섹션으로 나누어 각 섹션의 시작 부분에 주석을 추가합니다. 이는 파일의 구조를 명확하게 하고, 각 섹션의 목적을 설명하는 데 유용합니다.

**예시:**
```css
/* ==========================================================================
   Base Styles
   ========================================================================== */
```

#### 2. 블록 주석

특정 스타일 블록의 목적이나 기능을 설명하는 주석입니다. 이는 해당 블록이 무엇을 하는지 명확히 하기 위해 사용합니다.

**예시:**
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

#### 3. 인라인 주석

특정 속성의 목적이나 기능을 설명하기 위해 인라인으로 작성하는 주석입니다. 이는 간단한 설명이 필요할 때 유용합니다.

**예시:**
```css
.button-primary {
  background-color: #007bff; /* Main button color */
  color: white; /* Text color */
  border: none; /* Remove border */
}
```

#### 4. TODO 주석

추후 수정하거나 추가해야 할 작업을 기록합니다. 이는 개발 중에 놓칠 수 있는 작업을 나중에 쉽게 찾을 수 있도록 도와줍니다.

**예시:**
```css
/* TODO: Add responsive styles for mobile */
@media (max-width: 600px) {
  .button-primary {
    width: 100%;
  }
}
```

### 주석 사용 예시

아래는 위의 모든 주석 양식을 포함한 예시 CSS 코드입니다.

```css
/* ==========================================================================
   Global Styles
   ========================================================================== */

/* Base styles for the entire document */
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  background-color: #f4f4f4; /* Background color */
  color: #333; /* Text color */
}

/* ==========================================================================
   Header Styles
   ========================================================================== */

/* Header section styles */
header {
  background-color: #333;
  color: #fff;
  padding: 10px 0;
  text-align: center;
}

/* Header title */
header h1 {
  margin: 0;
  font-size: 2em;
}

/* ==========================================================================
   Main Content Styles
   ========================================================================== */

/* Main content container */
main {
  padding: 20px;
}

/* Section styles */
section {
  padding: 20px;
  margin: 10px 0;
  background-color: #fff;
  border-radius: 5px; /* Rounded corners */
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Subtle shadow */
}

/* ==========================================================================
   Button Styles
   ========================================================================== */

/* Primary Button Styles */
.button-primary {
  background-color: #007bff; /* Main button color */
  color: white; /* Text color */
  border: none; /* Remove border */
  padding: 10px 20px;
  cursor: pointer;
}

/* TODO: Add hover effect for primary button */
.button-primary:hover {
  background-color: #0056b3; /* Darker blue on hover */
}

/* ==========================================================================
   Footer Styles
   ========================================================================== */

/* Footer section styles */
footer {
  background-color: #333;
  color: #fff;
  padding: 10px 0;
  text-align: center;
}
```
