# Comment: HTML

### 1. 파일 주석

파일의 상단에 파일의 목적, 작성자, 생성일, 수정 이력 등을 기록합니다. 이는 파일 전체에 대한 정보를 제공하여 다른 개발자가 파일의 목적과 내용을 쉽게 이해할 수 있도록 합니다.

**예시:**
```html
<!-- 
  파일명: index.html
  작성자: 홍길동
  생성일: 2024-06-16
  설명: 이 파일은 메인 페이지의 구조를 정의합니다.
  수정 이력:
    - 2024-06-17: 비밀번호 암호화 기능 추가 (작성자: 이몽룡)
-->
```

### 2. 섹션 주석

HTML 문서를 구조화하기 위해 주요 섹션의 시작과 끝을 주석으로 표시합니다. 이는 문서의 구조를 명확히 하여 유지보수성을 높입니다.

**예시:**
```html
<!-- Header section starts -->
<header>
  <h1>My Website</h1>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>
<!-- Header section ends -->

<!-- Main content starts -->
<main>
  <section id="home">
    <h2>Welcome to My Website</h2>
    <p>This is the home section.</p>
  </section>
</main>
<!-- Main content ends -->
```

### 3. 블록 주석

코드 블록의 목적을 설명하거나 중요한 코드 부분에 대한 자세한 설명을 제공하기 위해 사용합니다. 주석은 해당 코드 블록의 상단에 작성합니다.

**예시:**
```html
<!--
  사용자 데이터 처리 섹션
  - 사용자 데이터를 검증하고 데이터베이스에 저장합니다.
  - 데이터 검증 실패 시, 오류 메시지를 반환합니다.
-->
<section id="user-data">
  <!-- 사용자 데이터 검증 폼 -->
  <form action="/submit" method="POST">
    <label for="name">Name:</label>
    <input id="name" type="text" name="name" required>
    
    <label for="email">Email:</label>
    <input id="email" type="email" name="email" required>
    
    <button type="submit">Submit</button>
  </form>
</section>
```

### 4. 인라인 주석

특정 코드 라인의 목적이나 기능을 설명하기 위해 코드 라인 끝에 주석을 추가합니다. 이는 주로 간단한 설명이나 추가 정보를 제공할 때 사용됩니다.

**예시:**
```html
<img src="image.jpg" alt="Example Image" /> <!-- Example image for the home section -->
<p>Welcome to my website.</p> <!-- Welcome message -->
```

### 5. TODO 주석

추후 수정하거나 추가해야 할 작업을 기록하는 데 사용합니다. 이는 개발 중에 놓칠 수 있는 작업을 나중에 쉽게 찾을 수 있도록 도와줍니다.

**예시:**
```html
<!-- TODO: Add more sections to the main content -->
<main>
  <section id="home">
    <h2>Welcome to My Website</h2>
    <p>This is the home section.</p>
  </section>
</main>
```

### 6. 주석 사용 예시

아래는 위의 모든 주석 양식을 포함한 예시 HTML 코드입니다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- 
    파일명: index.html
    작성자: 홍길동
    생성일: 2024-06-16
    설명: 이 파일은 메인 페이지의 구조를 정의합니다.
    수정 이력:
      - 2024-06-17: 비밀번호 암호화 기능 추가 (작성자: 이몽룡)
  -->
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Header section starts -->
  <header>
    <h1>My Website</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
  <!-- Header section ends -->

  <!-- Main content starts -->
  <main>
    <!-- Home section starts -->
    <section id="home">
      <h2>Welcome to My Website</h2>
      <p>This is the home section.</p>
      <img src="image.jpg" alt="Example Image" /> <!-- Example image for the home section -->
    </section>
    <!-- Home section ends -->

    <!-- About section starts -->
    <section id="about">
      <h2>About Us</h2>
      <p>Information about us.</p>
    </section>
    <!-- About section ends -->

    <!-- Contact section starts -->
    <section id="contact">
      <h2>Contact Us</h2>
      <form action="/submit" method="POST">
        <label for="name">Name:</label>
        <input id="name" type="text" name="name" placeholder="Enter your name" required>
        
        <label for="email">Email:</label>
        <input id="email" type="email" name="email" placeholder="Enter your email" required>
        
        <button type="submit">Submit</button>
      </form>
    </section>
    <!-- Contact section ends -->
  </main>
  <!-- Main content ends -->

  <!-- Footer section starts -->
  <footer>
    <p>&copy; 2024 My Website</p>
  </footer>
  <!-- Footer section ends -->
</body>
</html>
```
