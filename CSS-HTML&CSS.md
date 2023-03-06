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

---

## 2023.03.02

### Chapter02_1. 선택자(Selector)

### 진행 순서

- 기본선택자
전체, 타입, 클래스. ID, 속성
- 그룹선택자
- 결합자
자손, 자식, 일반형제, 인접형제

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Selector Basic</title>
    <style>
      /* *(전체 선택자)는 브라우저가 가지고 있는 기본 스타일을 초기화할 때 사용 */
      /* * {
        margin: 0;
        padding: 0;
      } */
      /* Type 선택자 */
      h2 {
        color: green;
      }
      p {
        color: blue;
        text-align: center;
        font-size: 20px;
        font-weight: 600;
      }

      /* Class 선택자 */
      .blue {
        color: blue;
      }
      .red {
        color: red;
      }
      /* ID 선택자 */
      #title {
        font-size: 40px;
        color: darkgray;
        background-color: yellow;
      }
    </style>
  </head>
  <body>
    <h1 id="title">애국가</h1>
    <hr />
    <h2>1절</h2>
    <p>
      <span class="blue">동해</span>물과 <span class="red">백두산</span>이
      마르고 닳도록 <br />
      하느님이 보우하사 우리나라 만세 <br />
    </p>
    무궁화 삼천리 화려강산 대한사람 <br />
  </body>
</html>
```

---

### Chapter02_2. 선택자(Selector)

### 속성 선택자 (Attribute selector)

주어진 속성을 가진 모든 요소를 검색합니다.

- 문법
`[attr]` `[attr=value]` `[attr~=value]` `[attr|=value]` `[attr^=value]` `[attr$=value]`
`[attr*=value]`
- 예제

```css
/* <a>태그에 title tㅗㄱ성이 존재하는 모든 요소, 예) <a href="https://example.org">exam</a> */

      a[href] {
        color: purple;
      }
      /* <a>태그에 href 속성이 "https://example.org" 해당 값과 일치하는 요소 */
      a[href="https://example.org"]
      {
        color: green;
      }
      /* <a>태그의 href 속성에 "example" 문자열을 포함하는 요소 */
      a[href*='example'] {
        font-size: 2em;
      }
      /* <a>태그의 href 속성이 "www"로 시작하는 요소. */
      a[href^='www'] {
        font-style: italic;
      }
      /* <a>태그의 href 속성이 ".org로 끝나는 요소." */
      a[href$='.org'] {
        font-style: italic;
      }

```

- 존재 : class만 명시
- 포함 : *=
- 일치 : =
- 시작 : ^=
- 끝 : $=
- 단어가 포함 : ~=

```css
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Selector Attribute</title>
    <style>
      /* 속성이 존재하는 요소 */
      h2[class] {
        font-size: 30px;
      }
      /* a태그 안의 target 속성의 글자색만 변경 가능 */
      /* a태그를 제외하고 속성명만 사용해도 가능 */
      /* [target]{
        color: green;
      } */
      a[target] {
        color: green;
      }

      /* 속성 값과 일치하는 요소 */
      h2[class='naver-title'] {
        color: green;
      }
      /* 속성 값을 포함하는 요소 */
      a[href*='www'] {
        text-decoration: none;
      }
      /* 일치는 =을 넣어주고 포함은 *=를 해준다. */

      /* 속성 값으로 시작하는 요소 */
      h2[class^='google'] {
        color: blue;
      }
      /* 속성 값으로 끝나는 요소 */
      a[href$='facebook.com'] {
        color: red;
      }
      /* 속성에 단어가 포함하는 요소 */
      h2[class~='title'] {
        color: blue;
        font-weight: 300;
      }
    </style>
  </head>
  <body>
    <h2 class="naver-title">네이버</h2>
    <a href="http://www.naver.com">네이버</a>
    <h2 class="google-title">구글</h2>
    <a href="http://www.google.com" target="_blank">구글</a>
    <h2 class="facebook-title">페이스북</h2>
    <a href="http://www.facebook.com">페이스북</a>
    <h2>박준영</h2>
    <h2 class="text title pjy">감사합니다</h2>
  </body>
</html>
```

---

### Chapter02-3. 선택자(Selector)

### 그룹선택자

선택자를 쉼표(,)로 구분해 여러 선택자를 나열함.

같은 스타일을 여러 선택자에 한꺼번에 정의할 수 있다.

- 문법
`선택자1, 선택자2 {스타일 규칙}`
- 예제

```css
h1, p{
	text-align: center;
}
```

```css
/* 그룹 선택지 */
      h1,
      h2 {
        text-align: center;
      }
```

---

### 결합자

자손 결합자

자손 ``(공백)결합자는 첫 번째 요소의 자손인 태그를 선택합니다.

- 문법
`A` `B` A선택자의 하위에 있는 B선택자를 모두 선택함.
- 예제

```css
/* <div>태그 하위에 있는 모든 <span>요소 */
div span{
	color: blue;
}
```

### 자식 결합자

자식`>` 결합자는 첫 번째 요소의 바로 아래 자식인 태그를 선택합니다.

- 문법

`A>B` 

- 예제

```css
/* <div> 태그 하위에 있는 모든 <span>요소 */
ul > li{
	color: blue;
}
```

### 일반 형제 결합자

일반 형제`~` 결합자는 형제, 즉 첫 번째 요소를 뒤따르면서 같은 부모를 공유하는 두 번째 요소를 선택합니다.

- 문법
`A~B`
- 예제

```css
/* <p>태그의 뒤에(아래) 나오는 모든 <span>요소 */
p ~ span {
	color: blue;
}
```

### 인접 형제 결합자

인접 형제`+` 결합자는 형제, 즉 첫 번째 요소의 바로 뒤에 위치하면서 같은 부모를 공유하는 두 번째 요소를 선택합니다.

- 문법
`A+B`
- 예제

```css
/* <h2>태그 바로 뒤에 위치하는 <p>요소 */
h2 + p{
	color : blue;
}
```

### 학습 정리

- 기본선택자
전체, 타입, 클래스, ID, 속성
- 그룹선택자
- 결합자
자손, 자식, 일반형제, 인접형제
---
## 2023.03.03

### CSS 속성 - 폰트

### 진행순서

- 폰트 관련 속성
- 웹폰트
- 단위 - px, rem, em, vw, vh
- 색상
- 그 외 글꼴 관련 속성

### 글꼴 관련 속성 MDN

- `font-family` - 글꼴 종류를 지정합니다.
기본값 : 웹브라우저 기본 글꼴
- `font-size` - 글자 크기를 지정합니다.
- `font-style` - 글자를 이텔릭체로 표시할지 지정합니다.
- `font-weight` - 글자 굵기를 지정합니다.
- `font-variant` - 소문자를 작은 대문재로 바꾸는 속성
---
## 2023.03.05

### 글자 색상

글자 색상은 `color` 속성으로 지정하며 색상 값으로는 `16진수 값` `rgb 값` `hsl 값` `색상 이름`이 사용된다.

### `색상 키워드` 표기법

색상 키워드는 대소문자를 구분하지 않는 식별자로, red, blue, black, lightseagreen처럼 특정 생을 나타냅니다. 이름이 표현하는 색을 그럭저럭 가리키고 있긴 하지만 모든 키워드의 본질은 인위적이며 어떤 특정한 규칙을 따르거나 하지 않습니다.

- 예시
blue, red, yellow 등 색상 키워드
- `transparent` 키워드
transparent 키워드는 완전히 투명한 색으로, “색”을 입힌 항목의 뒷편이 모두 보입니다. 기술적으로 transparent는 rgba(0,0,0,0)의 짧은 이름입니다.
- `currentColor` 키워드
`currentColor` 키워드는 요소의 `color` 속성값을 나타냅니다. 이를 통해 다른 속성이 `color` 속성값을 따라가도록 설정할 수 있습니다.

### `RGB/RGBA` 표기법

RGB 색상 모델은 빨강, 초록, 파랑을 통해 특정 색을 표현합니다. `선택사항으로 색의 투명도`를 알파 채널로 표현할 수 있습니다. 함수형 표기법(`rgb()`, `rgba()`)으로 표현할 수 있습니다.

- 예시
rgb(0,0,0), rgba(0,0,0,0)

### `16진수` 표기법

RGB 색상 모델은 빨강, 초록, 파랑을 통해 특정 색을 표현합니다. 선택사항으로 색의 투명도를 알파 채널로 표현할 수 있습니다.# 뒤의 16진수 표기법으로 표현할 수 있습니다.

- 예시
#ff0000, #ff00ff, #808000 등 16진수

### `hsl/hsla` 표기법

HSL 색상 모델은 색상, 채도, 명도를 통해 특정 색상을 표현합니다. 선택사항으로 색의 투명도를 알파 채널로 표현할 수 있습니다.

HSL 색상은 함수형 `hsl()` 과 `hsla()` 표기법을 사용합니다.

- 예시
hsl(H, S, L[, A]), hela(H,, S, L, A)
자세한 값은 MDN-Color속성을 참고할 수 있다.

### 학습정리

- 폰트 관련 속성
font-family, font-size, font-style, font-weight, font-vaiant
- 웹폰트
구글웹폰트 적용
- 단위 - px, rem, em. vw, vh
- 색상
16진수, RGB
- 그 외 글꼴 관련 속성
---

## 2023.03.06

### Box Model

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4f676170-cf42-471e-bc82-7f68b3877fa1/Untitled.png)

모든 HTML 요소는 웹 페이지에서 일정 공간을 차지하게 됩니다. 그리고 이러한 공간을 CSS에서는 박스 모델(Box Model)로 정의하고 있습니다

HTML 요소의 박스 모델은 Content, Padding, Border, Margin으로 구성되어 있습니다.

마진(margin)

테두리(border)

패딩(padding)

콘텐츠(content)

- `content` - 텍스트나 이미지가 들어있는 HTML 요소의 실질적인 내용
- `Padding` - Content와 Border 사이의 영역으로 쉽게 말해 안쪽 여백
- `Border` - Content를 감싸는 테두리
- `Margin` - 테두리와 이웃하는 요소 사이의 간격으로 쉽게 말해 바깥쪽 여백

모든 HTML요소의 박스모델은 이렇게 구성되어 있으며, 웹 브라우저 > 개발자도구 > Computed 탭에서 박스모델을 확인할 수 있습니다.

### Box Model CSS 속성

박스 모델은 속서을 지정하지 않으면 브라우저가 선언한 기본값으로 셋팅되며, 우리는 CSS 속성으로 박스모델 값을 변경할 수 있습니다. 여기에서는 간단히만 알아보고 밑에서 더 자세히 알아보자.

### Content

- `width` - Content 영역은 `width` 값을 이용하여 가로 너비를 지정할 수 있다.
- `height` - Content 영역은 `height` 값을 이용하여 세로 너비를 지정할 수 있다.

```css
width: 200px;
height: 200px;
```

```css
💡인라인 레벨 요소(Inline Level Element)에는 width, height가 적용되지 않습니다. 왜냐하면 인라인 요소는 콘텐츠 만큼의 영역을 갖기 때문 입니다.(displayL inlie)
만약 인라인 요소에 width, height를 변경하고 싶다면 display: inline-block으로 변경해야 합니다.
- inline-block - block과 inline의 중간 형태로 요소는 inline인에 내부는 block처럼 표시함
```

### Padding

- `padding` - `padding` 값을 조절하여 안쪽 여백을 지정할 수 있습니다.
- `padding-{direction}` - `padding-top` `padding-left` `padding-right` `padding-bottom` 속성을 사용하여 각각 지정할 수도 있습니다.
