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





