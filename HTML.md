# HTML Coding Convention

### 1. 문서 구조

- **DOCTYPE 선언**: 모든 HTML 문서는 `<!DOCTYPE html>` 선언으로 시작해야 합니다.
  ```html
  <!DOCTYPE html>
  ```

- **언어 속성**: `<html>` 태그에는 `lang` 속성을 명시합니다.
  ```html
  <html lang="en">
  ```

- **문서 인코딩**: `<meta charset="UTF-8">`을 사용하여 문서의 인코딩을 설정합니다.
  ```html
  <meta charset="UTF-8">
  ```

- **뷰포트 설정**: 모바일 반응형 디자인을 위해 `<meta name="viewport" content="width=device-width, initial-scale=1.0">`을 설정합니다.
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```

### 2. 코드 스타일

- **들여쓰기**: 2 스페이스를 사용합니다.
  ```html
  <html>
    <head>
      <title>Document</title>
    </head>
    <body>
      <h1>Hello, World!</h1>
    </body>
  </html>
  ```

- **소문자 사용**: 태그명, 속성명, 속성값은 모두 소문자로 작성합니다.
  ```html
  <img src="image.jpg" alt="Example">
  ```

- **자체 종료 태그**: 빈 요소는 자체 종료 태그를 사용합니다.
  ```html
  <img src="image.jpg" alt="Example" />
  ```

### 3. 속성 순서

속성은 다음 순서대로 작성합니다:
1. `class`
2. `id`
3. `name`
4. `data-*`
5. `src`, `for`, `type`, `href`, `value`, `max-length`, `max`, `min`, `pattern`, `placeholder`, `required`, `readonly`, `disabled`
6. `title`, `alt`
7. `role`, `aria-*`, `tabindex`
8. `style`

예시:
```html
<input class="form-input" id="username" type="text" name="username" placeholder="Enter your username" required>
```

### 4. HTML 주석

주석을 사용하여 코드의 주요 부분을 설명합니다.
```html
<!-- Main content starts here -->
<main>
  <h1>Welcome to our website</h1>
  <p>Enjoy your stay!</p>
</main>
<!-- Main content ends here -->
```

### 5. 코드 예시

아래는 위 규칙들을 적용한 예시 HTML 코드입니다.

```html
<!DOCTYPE html>
<html lang="en">
<head>
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
    <section id="home">
      <h2>Welcome to My Website</h2>
      <p>This is the home section.</p>
      <img src="image.jpg" alt="Example" />
    </section>

    <section id="about">
      <h2>About Us</h2>
      <p>Information about us.</p>
    </section>

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

### 6. 추가 규칙

**접근성 준수:**
- ARIA 속성을 사용하여 접근성을 높입니다.
- 이미지에는 항상 `alt` 속성을 추가합니다.
- 링크에는 명확한 텍스트를 포함시킵니다.

**네이밍 규칙:**
- 클래스명은 소문자와 하이픈(`-`)을 사용하여 작성합니다.
  ```html
  <div class="main-content"></div>
  ```

**섹션 요소 사용:**
- 의미에 맞는 HTML5 섹션 요소를 사용합니다.
  ```html
  <header></header>
  <nav></nav>
  <main></main>
  <section></section>
  <article></article>
  <aside></aside>
  <footer></footer>
  ```
