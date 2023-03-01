# CSS(Cascading Style Sheets)

## link : https://www.youtube.com/watch?v=N_nVDZSAjq4&list=PLlaP-jSd-nK-ponbKDjrSn3BQG9MgHSKv
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS</title>
    <style>
      .green-text {
        color: green;
      }
      .link {
        text-decoration: none;
      }
      #dark {
        background-color: black;
        color: white;
      }
      .blue {
        color: yellow;
      }
    </style>
  </head>
  <body>
    <h1 style="color: yellowgreen">제목</h1>
    <p class="green-text">
      안녕하세요 실용적인 채널을 만들어가는 박준영입니다.
    </p>
    <hr />
    <a class="link" href="https://www.naver.com">네이버</a>
    <span>이름 : </span><span>박준영</span>
    <ul>
      <li>사과</li>
      <li>바나나</li>
      <li>토마토</li>
      <li>딸기</li>
    </ul>
    <hr />
    <p id="dark">
      <span class="blue">동해</span>물과 <span class="blue">백두산</span>이
      마르고 닳도록<br />
      하느님이 보우하사 우리나라 만세
    </p>
  </body>
</html>
```

## 진행 순서

- CSS란
- Hello CSS!
- CSS 구조
- CSS 적용방법
- CSS 주석
- CSS 출처

### CSS적용 방법

- 인라인 - Inline Style Sheet
- 내부 스타일 - Internal Style Sheet
- 외부 스타일 - External Style Sheet

### CSS 주석

주석은 StyleSheet 내에 메모를 남기는 것을 말합니다.

- 사용법 - `/* 메모내용 */` 메모내용란에 메모할 문자를 작성한다.
- VSCode에서 주석 단축기는 `Ctrl + /` 이다.

## CSS 출처

---

CSS는 브라우저 `기본 스타일`, `브라우저 사용자 스타일`, 우리가 만들 `제작자 스타일`로 분류할 수 있습니다.

### CSS 출처 3가지

- 제작자 스타일 (Author Style)
제작자 스타일은 말 그대로 웹 사이트를 제작하는 `우리가 작성한 스타일 시트`를 말합니다.
- 사용자 스타일(User Style)
사이트를 방문하는 일반 사용자들이 구성한 스타일 시트를 의미함
예를들어 저시력자는 글자를 명확히 읽기 위해 윈도우의 “ 고대비” 설정 기능을 사용할 수 있습니다. 그러한 스타일이 시스템이 저장되게 하는데, 이것이 `사용자 스타일 시트` 입니다.
- 브라우저 스타일(Brower Style)
`브라우저`들마다 기본적으로 지정하고 있는 `스타일` 입니다.
크롬, 사파리, 파이어폭스 등 브라우저 마다 기본 스타일 시트가 다를 수 있습니다.

### CSS 출처 적용 우선순위

`사용자 !important` > `제작자!important`>`제작자`>`사용자`>`브`

`라우저` 

- 주의사항
`!important`는 폭포의 흐름을 깰 수 있으니 주의해서 사용해야 함

### Cascading 뜻

Cascading Style Sheet에서 Cascading은 폭포라는 뜻을 가지고 있습니다.

HTML 문서는

- 제작자 스타일을 우선 적용하고 →
    - 그 다음 브라우저 사용자 스타일 →
        - 마지막으로 브라우저 기본 스타일을 적용

이처럼 Cascading의 뜻인 폭포와 같이 스타일이 우선순위에 맞게 연속적으로 적용됨을 의마

```html
💡 사용자 스타일은 자주 사용하는 개념이 아니기 때문에, "아 그냥 내가 적용한 스타일이 우선 적용되고 그리
고 나서 부라우저 기본 스타일이 적용되는 구나" 정도로 이해하면 편하다
```

### 학습정리

- CSS란 - Cascading Style Sheets
- CSS구조
선택자, 속성명, 속성값
- CSS 적용방법
인라인, 내부, 외부
- CSS 주석/* */
- CSS 출처
브라우저, 사용자, 제작자
우선순위, !important
