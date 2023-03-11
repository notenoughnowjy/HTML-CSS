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
### 안쪽 여백 Padding

- `padding` 속성은 HTML 요소의 안쪽 여백을 지정합니다.
- `padding-top` `padding-bottom` `padding-left` `padding-right` 속성을 사용하여 각각 지정할 수도 있습니다.
- 예시

```css
padding: 20px;
padding: 10px 20px;
padding: 4px 2px 2px 4px;
padding-top: 20px;
```

### 바깥 여백 Margin

- `margin` 속성은 HTML 요소의 바깥 여백을 지정합니다.
- `margin-top` `margin-bottom` `margin-left` `margin-right` 속성을 사용하여 각각 지정할 수도 있습니다.
- 예시

```css
margin: 20px;
margin: 10px 20px;
margin: 4px 2px 2px 4px;
margin-top: 20px;
```

### 마진 중첩

HTML 요소를 세로로 배치할 경우 `margin` 과 `margin` 이 만날 때 `margin` 값이 큰 쪽으로 겹쳐지는 것, 요소를 가로로 배치할 경우에는 상관없지만 세로로 배치할 경우에는 값이 큰 `margin` 만 적용 된다.

### 테두리 Border

CSS `border` `border-width` `border-style` `border-color` 속성으로 요소의 테두리를 설정

- `border-style`
    - 어떤 형태의 테두리 스타일을 지정할지 나타냅니다.
    - 4개 방향을 값을 한꺼번에 지정할 때는 방향 순서를 지켜야 합니다. top → right → bottom → left
    - 테두리 스타일 종류 MDN
    - 예시
    
    ```css
    border-style: solid;
    border-style: dotted solid dashed solid;
    border-left-style: solid;
    ```
    
- `border-width`
    - 테두리 두께를 지정합니다.
    - 값으로 `<크기>` 또는 키워드 `thin` `medium` `thick` 가 올 수 있습니다.
    - 예시
    
    ```css
    border-width: 1px;
    border-width: thin thin;
    border-width: thin thin thin; /* 이 경우는 잘 사용 안함 */
    border-width: 8px 4px 4px 8px;
    border-left-width: 2px;
    ```
    
- `border-color`
    - 테두리 색상을 지정합니다
    - 예시
    
    ```css
    border-color: blue;
    border-color: yellow red;
    ```
    
- `border`
    - 단축 속성으로서 다음의 하위 속성을 포함합니다. `border-width` `border-style` `border-color`
    - 즉, 테두리 두께, 스타일, 색상을 한꺼번에 표기할 수 있습니다.
    - `border-top` `border-right` `border-left` `border-bottom` 을 사용하여 스타일을 각각 지정할 수 있습니다.
    - 예시
    
    ```css
    border: 1px solid red;
    border: 4px dashed green;
    ```
    
- border-radius
    - 테두리 꼭짓점을 둥글게 만듭니다.
    - 예시
    
    ```css
    border-radius: 30px;
    border-radius 10% 20%;
    ```
    

### Box Sizing

Box Sizing 속성은 HTML 요소의 너비와 높이를 계산하는 방법을 지정

CSS 박스 모델에서 지정한 너비(width)와 높이(height)는 HTML 요소의 Content 크기에 적용됩니다. 요소에 테두리(Border)나 안쪽 여백(Padding)이 있으면 너비와 높이에 더해서 화면에 그립니다. 따라서 크기를 설정할 때 원하는 크기를 얻으려면 테두리나 안쪽 여백을 고려해야 합니다.

이때 `box-sizing` 속성을 사용해 이 방식을 변경할 수 있습니다.

- `box-sizing` 값
    - `content-box` - 기본 CSS 박스 크기 결정법 입니다. 요소의 너비를 100px로 설정하면 콘텐츠 영역이 100px 너비를 가지고, 테두리와 안쪽 여백은 이에 더해집니다.
    - `border-box` - 테두리와 안쪽 여백도 요소의 크기(width, height)로 고려합니다. 너비를 100px로 설정하고 테두리와 안쪽 여백을 추가하면, 콘텐츠 영역이 줄어들어 총 너비 100px을 유지합니다. 대부분의 경우 이 편이 크기를 조절할 때 쉽습니다.
    
    ```css
    box-sizing: content-box;
    box-sizing: border-box;
    ```
    

### 학습정리

- Box Model
- Content - width, height
- Padding - padding-방향 또는 padding
- Margin - margin-방향 또는 margin, 마진중첩
- Border
border-방향, ㅠorder, border-color, border-radius, border-style, border-width
- Box Sizing
---

## 2023.03.07

### Display속성

`display` 속성은 HTML 요소를 어떻게 표시할지를 결정합니다
HTML 요소마다 기본적으로 갖고 있는 display 속성 값이 다름

이 기본값이 `display: block` 이면 Block Level Element 이며, `display: inline` 일 경우 Inline Level Element 입니다.

그리고 display 속성은 주로 4가지 속성 값이 쓰입니다.

### 기본 4가지 값

### `none`

요소를 보이지 않게 설정합니다. visibility 속성을 hidden으로 설정한 것과 달리, 영역도 차지하지 않습니다.

### `block`

기본적으로 가로 영역을 모두 채우며, block 요소 다음에 등장하는 태그는 줄바꿈이 된 것처럼 보입니다. 문서에서 문단을 표시할 때 주로 사용합니다.

`width`, `height` 속성을 지정할 수 있습니다.

`div` `p` `h1~h6` 태그 등이 이에 해당됩니다.

### `Inline`

컨텐츠만큼 영역을 차지합니다.

block과 달리 줄 바꿈이 되지 않고, `width`와 `height`를 지정할 수 없습니다.

word 같은 문서에서 볼드, 이탤릭, 색상, 밑줄 등 글자나 문장에 효과를 주기 위해 존재하는 단위라고 할 수 있습니다.

### `Inline-block`

block과 inline의 중간 형태로 요소는 inline인데 내부는 block처럼 표시함

inline처럼 컨텐츠 만큼 영역을 차지하여 가로로 배치되지만 block처럼 내부 속성인 width, height등과 같은 값을 변경할 수 있습니다.
---
## 2023.03.08

### Float “뜨다”

### Float 속성

`float` 의 사전적인 의미는 ‘뜨다’라는 뜻

만약 HTML 요소에 float이 적용되면 HTML 요소는 원래의 흐름에서 벗어나 둥둥 떠다니듯 배치가 됩낟,

그리하여 인접한 텍스트 또는 인라인 요소가 그 주위를 자연스럽게 감싸게 합니다.

자주 사용하는 `float` 속성 값은

- `none` - 기본적으로 요소를 띄우지 않음
- `left` - 왼쪽에 띄움
- `right` - 오른쪽에 띄움
- `inherit` - 부모 요소로부터 상속함
- `initial` - 기본적으로 설정함

### Clear 속성

clear는 취소하다 라는 뜻으로 `float: left;` 혹은 `float: right;` 값을 취소합니다.

`clear: none;` - 기본값

`clear: left;` - 왼쪽을 취소

`clear: right` - 오른쪽을 취소

`clear: both` - 왼쪽 오른쪽 둘 다 취소
```css
float 속성으로 과거에는 레이아웃을 적용
최근에는 CSS flex box를 활용
```
---

## 2023.03.10

### Position

### position 속성

`position` 속성은 HTML 요소를 배치하는 방법을 지정합니다.

- `static` (기본값)
static은 요소가 HTML 문서에서 일반적인 흐름을 따라 배치가 되게하며, 기본값
- `relative` (상대적인)
`static` 과 마찬가지로 요소가 문서의 일반적인 흐름에 따라 배치되게 합니다. static과 차이점은 요소가 자신의 `static` 위치에서 `top` `right` `bottom` `left` 와 같은 속성에 의한 상대적인 위치에 배치된다는 점입니다.
- `absolute` 
`absolute` 는 요소가 문서의 일반적인 흐름을 따르지 않음. `absolute` 는 position: static 속성을 가지고 있지 않은 부모를 기준으로 움직입니다. 만약 부모중에 포지션이 relative, absolute, fixed인 태그가 없다면 가장 위의 태그(body)가 기준이 됩니다.
- `fixed` 
`fixed` 역시 `absolute` 와 마찬가지로 요소가 문서의 일반적인 흐름에서 제거됩니다. 대신, 스크린의 뷰포트(viewport)를 기준으로 한 위치에서 배치됩니다. 즉, 스크롤되어도 움직이지 않는 고정된 자리를 갖게 됩니다.
    
    ```jsx
    💡 뷰포트(viewport)란? 웹 페이지가 브라우저 화면상에서 실제로 표시되는 영역이다.
    ```
    
- `sticky
sticky` 는 요소가 HTML 문서안에서 `static` 과 같이 일반적인 흐름에 따라가다가 스크롤 위치가 임계점에 이르면 `fixed` 와 같이 박스를 화면에 고정할 수 있는 속성입니다.

### 위치 속성

`position` 속성이 배치하는 방법이라면 `top` `left` `bottom` `right` 속성은 요소를 원하는 곳으로 최종적으로 위치 시키는 속성이다. 이 속성은 `position: static;` 에서는 적용되지 않는다.

- `top`
- `left`
- `bottom`
- `right`

### 관련 속성

- `z-index`
어느 객체가 앞으로 나오고, 뒤에 나올지 배치 순서를 결정하는 속성입니다.
`z-index`는 `position` (`relative`, `absolute`, `fixed`)속성이 적용된 요소에서만 작동합니다.
---

## 2023.03.11

### Background

### `background-color`

HTML 요소의 배경 색을 지정합니다.

```html
/* 키워드 값 */
background-color: red;
/* 16진수 값 */
background-color: #bbff00;
/* RGB 값 */
background-color: rgb(255,255,128);
/* 특별 키워드 값 */
background-color: currentcolor;
/* 전역 값 */
background-color: inherit;
```

### `background-image`

HTML요소에 배경 이미지를 한 개 또는 여러 개를 지정할 수 있습니다.

```html
background-image: url("../../media/examples/lizard.png");
background-image: url("../../media/examples/lizard.png"),
									url("../../media/examples/lizard.png");
```

### `background-repeat`

배경 이미지의 반복 방법을 지정합니다. 가로축 및 세로축을 따라 반복할 수 있고, 아예 반복하지 않을 수도 있습니다.

- `repeat` : 가로,세로 반복
- `no-repeat` : 반복하지 않음
- `repeat-x` : 가로 반복
- `repeat-y` : 세로 반복

### `background-position`

배경 이미지의 초기 위치를 설정합니다.

```html
/* Keyword values */
background-position: top;
background-position: left;
background-position: center;
/* <percentage> values */
background-position: 25% 75%;
/* Edge offsets values */
background-position: bottom 10px right 20px;
```

### `background-attachment`

배경 이미지를 뷰포트 내에서 고정할지 말지를 지정하는 속성입니다.

- `scroll` : 선택한 요소와 같이 움직입니다. 내용을 스크롤하면 배경 이미지는 스크롤되지 않습니다. (기본값)
- `fixed` : 움직이지 않습니다.
- `local` : 선택한 요소와 같이 움직입니다. 내용을 스크롤하면 배경 이미지도 스크롤됩니다.
- `initial` : 기본값으로 설정합니다.
- `inherit` : 부모 요소의 속성값을 상속받습니다.

```html
/* 키워드 값 */
background-attachment: scroll;
background-attachment: fixed;
background-attachment: local;

/* 전역 값 */
background-attachment: inherit;
background-attachment: initial;
background-attachment: unset;

```

### `background`

`background-image` `background-repeat` `background-position` `background-attachment` 속성을 한꺼번에 선언할 수 있습니다.

```html
background: url('images/bg.png') no-repeat top right fixed;
```

보통 이렇게 background 속성으로 많이 사용합니다.

### `background-size`

요소 배경 이미지의 크기를 설정합니다. 그대로 두거나, 늘리고 줄이거나, 공간에 맞출 수 있습니다.

- `contain` - 이미지가 잘리거나 찌그러지지 않는 한도 내에서 제일 크게 설정
- `cover` - 이미지가 찌그러지지 않는 한도 내에서 제일 크게 설정. 이미지의 가로세로비가 요소와 다르다면 이미지를 세로 또는 가로방향으로 잘라내어 빈 공간이 생기지 않도록 설정합니다. (많이 사용함)
- `auto` - 배경 미지이의 원본 크기를 유지.
- `<length>` - 원본 크기의 너비/높이를 주어진 값으로 늘리거나 줄임. 음수는 유효하지 않습니다.
- `<percentage>` - 배경 위치 지정 영역의 지정된 백분율에 해당되는 크기로 이미지를 늘립니다.
