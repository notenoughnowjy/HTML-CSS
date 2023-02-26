## 2023.02.23

### HTML이란 무엇인가?

***learn from https://github.com/gymcoding/learn-html-css***<br>
***source by https://github.com/gymcoding/learn-html-css***

- HTML 이란? : Hyper Text Markup Language 약자이며, 태그를 이용한 Markup 언어이다.
- HTML Tag : 특징, 구조
- HTML 문서 기본구조 : `doctype`, `html`, `head`, `body`
- HTML 주석 : `<!-- -->`

### Emmet

- 자식노드

```html
<div>
      <ul>
        <li></li>
      </ul>
    </div>

    div>ul>li
```

- 형제 노드

```html
<div>
      <ul>
        <ol>
          <div></div>
        </ol>
      </ul>
    </div>

    div>ul>ol>div
```

- 반복하기

```html
<div>
      <ul>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </div>

    div>ul>li*3
```

- 아이디

```html
<span id="id"></span>
    span#id

    <div id="item"></div>
    #item

    <span class="id"></span>
    span.id

```

- 클래스

```html
<span class="title"></span>
    span.title

    <div class="title"></div>
    .title
```

- 콘텐츠

```html
<p class="container">Hello World~!</p>
    p.container{Hello World~!}
```

- 자동 넘버링

```html
<p class="container">item1</p>
    <p class="container">item2</p>
    <p class="container">item3</p>
    <p class="container">item4</p>
    <p class="container">item5</p>
        p.container{item$}*5
```

## 2023.02.25

### HTML 태그

- 글꼴 태그
- 목록 태그
- 표 태그

- `<i>` (italic) : 텍스트를 이텔릭체로 표시할 때 사용
- `<em>` (Emphasis) : 텍스트를 이텔릭체로 강조할 때 사용
- `<b>` : 텍스트를 진하게 표시할 때 사용
- `<strong>` : 텍스트를 진하게 강조할 때 사용
- b 태그와 strong 태그 모두 진하게 표시할 때 사용하고, i 태그와 em 태그도 모두 이텔릭체로 표시할 때 사용
    
    하지만 이 두 태그의 사용 용도는 크게 다르다.
    
    - b 태그와 i 태그는 **단순히 텍스트를 진하게** 그리고 **이텔릭체로 표시하는 역할**만 함
    - strong 태그와 em태그는 실제로 **페이지 내의 중요한 부분으로 강조하고 싶을 때** 사용
    - strong, em 태그를 용도에 맞게 사용하면 웹 접근성에 큰 기여를 함
        
        브라우저에서 스크린리더(Screen Reader)를 사용하는 경우, 음성 합성(Speech Synthesizer)도구가 페이지를 해석하고 읽어낼 때 ******************************************************strong 태그에 대해 거센 억양으로 음을 낼 수 있도록 하여 실제로 말할 때의 강조******************************************************를 하듯이 재구성할 수 있게 된다.
        
        여기서 스크린리더란 시각장애인이 컴퓨터를 사용할 때 화면에 나타나는 정보들을 음성으로 출력해주는 화면낭독 프로그램
        

---

### 목록 태그

- `<dl>` : (Definition List) : Definition List(정의 목록)의 약자로, ********************************************************************사전처럼 용어를 설명하는 목록********************************************************************을 만듭니다.
ex) A는 B이다.와 같은 Key = value로 사용할 때 유용하다.
- `<dt>` (Definition Term) : Definition Term(정의 용어)의 약자로, 정의되는 **용어의 제목을 넣을 때** 사용한다.
- `<dd>` (Definition Description) : Definition Description(정의 설명)의 약자로, **용어를 설명하는데** 사용합니다.

### 주의 사항

- `<dl>` 태그는 하나 이상의 `<dt>-<dd>` 쌍의 태그를 갖고 있어야 한다.
단, `<dt>-<dd>` 태그가 반드시 하나의 짝으로 지어져야 하는 것은 아니다.
- `<li>` , `<dt>-<dd>` 태그는 밖에서 독립적으로 사용할 수 없다.
- `<ul>` 태그 하위요소로는 `<li>` 태그가 위치해야 한다.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>list-tag</title>
  </head>
  목록 태그
  <body>
    <dl>이건 뭐지</dl>
    <dt>제주도 혼자 여행기</dt>
    <dd>
      제주도의 좋은 추억들이 <br />
      아직도 기억에 남는다
    </dd>
    <dt><strong>제주도 성산의 히든 스테이</strong></dt>
    <dd>
      제일 깔끔하고 냄새도 좋았다. <br />
      한달 살기를 한다면 거기서 하고싶다.
    </dd>
    <dt>제주도 성산의 통발</dt>
    <dd>정말 맛있는 맛집이었다. <br />무조건 또 갈거다</dd>
  </body>
</html>
```
## 2023.02.26

### `Table 태그`

- `<table>`태그 - 표
- `<th>`태그 - 이름
- `<tr>`태그 - 행
- `<td>`태그 - 열

### Table 기본 태그

- `<table>`
표를 만드는 태그로써, 표 전체를 감싸는 데 사용
- `<caption>`
표의 제목이나 설명을 작성하는 태그
- `<tr>`
표의 행을 의미하는 태그, 자식으로 <th>태그나 <td>태그가 반드시 있어야 한다
- `<tr>`
표의 제목 열을 의맣는 태그, 부모 태그인 <tr>태그 안에 있어야 한다.
- `<td>`
표의 일반 열을 의미하는 태그, 부모인 <tr>태그안에 있어야 한다.

### Table 그룹 관련 태그

- `<colorgroup>`
열을 그룹으로 묶을 수 있도록 해주는 태그이다.
- `<col`>
<colgroup>태그의 자식으로 열 단위를 나눌 수 있다. span 속성을 사용하여 열을 그룹으로 묶을지 설정한다.
ex) `<col span=”3”>` → 세 개의 열을 그룹으로 묶음
- `<thead>`
표의 제목 열들을 묶는 그룹 태그
- `<tbody>`
표의 일반적인 데이터들을 묶는 그룹태그.
기본적으로 행그룹태그를 사용하지 않으면 크롬브라우저가 자동으로 tbody 태그로 묶어준다.
- `<tfoot>`
표의 하단 영역을 묶는 그룹태그

### Table 태그 관련 속성

- `<table>` 태그 속성
- border - 테이블이 갖고 있는 테이블과 셀 모두 선을 표시한다. `웹표준X`
- width - 테이블의 가로너비를 설정한다.`웹표준X`
- cellpadding - 셀의 안쪽 여백으로써, 셀과 콘텐츠와의 간격을 조절함.`웹표준X`
- cellspacing - 셀의 바깥쪽 여백으로써, 셀과 셀간의 간격을 조절함.`웹표준X`

위 속성들은 XHTML 1.0에서는 웹 표준이지만 오늘날 HTML5에서는 웹 표준이 아닙니다. → CSS로 대체해야 함.

- `<th>` 태그 속성
    - scope - 웹접근성 관련 속성으로 스크린리더가 데이터를 인식하고 읽는 순서를 결정짓게 합니다.
        - th가 열에 쓰일경우 값을 “col”로 설정합니다. 예)`<th scope=”col">`
        - th가 행에 쓰일경우 값을 “row”로 설정합니다. 예)`<th scope=”row">`
    - `<th>`, `<th>`
        - colspan - 열을 병합하는 속성. 예) <td colspan=”2”>
        - rowspan - 행에 쓰일경우 값은 “row”로 설정합니다. 예) <th scope=”row”>
    - `<th>`, `<td>`
        - colspan - 열을 병합하는 속성. 예) <td colspan=”2”>
        - rowspan - 행을 병합하는 속성. 예) <td rowspan=”2”>
    - `<col>`
        - width - 열의 가로너비를 지정하지만 `웹표준X` → CSS로 대체
        - span - 열을 그룹화 함. 예) <colspan=”3”> → 세 개의 열을 묶음.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Table Tag</title>
    <style>
      table {
        border: 1px solid black;
        border-collapse: collapse;
      }
      th,
      td {
        border: 1px solid black;
        padding: 12px;
      }
      .col1 {
        width: 80px;
      }
      .col2 {
        background-color: beige;
      }
    </style>
  </head>
  <body>
    <h1>Table 기본</h1>
    <table>
      <caption>
        프로필 테이블
      </caption>
      <th>이름</th>
      <th>취미</th>
      <th>이름</th>
      <tr>
        <td>홍길동</td>
        <td>도술</td>
        <td>축지법</td>
      </tr>
      <tr>
        <td>짐코딩</td>
        <td>헬스</td>
        <td>코딩</td>
      </tr>
    </table>
    <table>
      <hr />
      <h1>Table group tag</h1>
      <caption>
        학급 점수
      </caption>
      <colgroup>
        <col class="col1" />
        <col class="col2" />
        <col class="col3" />
        <col class="col4" />
        <col class="col5" />
        <col class="col6" />
      </colgroup>
      <thead>
        <tr>
          <th>반</th>
          <th>이름</th>
          <th>국어</th>
          <th>영어</th>
          <th>수학</th>
          <th>코딩</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>1반</td>
          <td>홍길동</td>
          <td>90</td>
          <td>100</td>
          <td>90</td>
          <td>81</td>
        </tr>
        <tr>
          <td>1반</td>
          <td>짐코딩</td>
          <td>85</td>
          <td>81</td>
          <td>95</td>
          <td>100</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td>1반</td>
          <td>평균</td>
          <td>87.5</td>
          <td>90.5</td>
          <td>92.5</td>
          <td>90.5</td>
        </tr>
      </tfoot>
    </table>
  </body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Table Tag</title>
    <style>
      table {
        border: 1px solid black;
        border-collapse: collapse;
      }
      th,
      td {
        border: 1px solid black;
        padding: 12px;
      }
      .col1 {
        width: 80px;
      }
      .col2 {
        background-color: beige;
      }
      .col11 {
        width: 80px;
      }
      .col12 {
        background-color: gray;
      }
    </style>
  </head>
  <body>
    <h1>Table 기본</h1>
    <table>
      <caption>
        프로필 테이블
      </caption>
      <th>이름</th>
      <th>취미</th>
      <th>이름</th>
      <tr>
        <td>홍길동</td>
        <td>도술</td>
        <td>축지법</td>
      </tr>
      <tr>
        <td>짐코딩</td>
        <td>헬스</td>
        <td>코딩</td>
      </tr>
    </table>
    <table>
      <hr />
      <h1>Table group tag</h1>
      <caption>
        학급 점수
      </caption>
      <colgroup>
        <col class="col1" />
        <col class="col2" />
        <col class="col3" />
        <col class="col4" />
        <col class="col5" />
        <col class="col6" />
      </colgroup>
      <thead>
        <tr>
          <th>반</th>
          <th>이름</th>
          <th>국어</th>
          <th>영어</th>
          <th>수학</th>
          <th>코딩</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td row>1반</td>
          <td>홍길동</td>
          <td>90</td>
          <td>100</td>
          <td>90</td>
          <td>81</td>
        </tr>
        <tr>
          <td>1반</td>
          <td>짐코딩</td>
          <td>85</td>
          <td>81</td>
          <td>95</td>
          <td>100</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td>1반</td>
          <td>평균</td>
          <td>87.5</td>
          <td>90.5</td>
          <td>92.5</td>
          <td>90.5</td>
        </tr>
      </tfoot>
    </table>

    <table>
      <hr />
      <h1>Table group tag</h1>
      <caption>
        학급 점수
      </caption>
      <colgroup>
        <col class="col11" />
        <col class="col12" />
        <col class="col13" />
        <col class="col14" />
        <col class="col15" />
        <col class="col16" />
      </colgroup>
      <thead>
        <tr>
          <th>반</th>
          <th>이름</th>
          <th>국어</th>
          <th>영어</th>
          <th>수학</th>
          <th>코딩</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td rowspan="2">1반</td>
          <td>홍길동</td>
          <td>90</td>
          <td>100</td>
          <td>90</td>
          <td>81</td>
        </tr>
        <tr>
          <td>짐코딩</td>
          <td>85</td>
          <td>81</td>
          <td>95</td>
          <td>100</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td colspan="2">1반</td>
          <td>87.5</td>
          <td>90.5</td>
          <td>92.5</td>
          <td>90.5</td>
        </tr>
      </tfoot>
    </table>
  </body>
</html>
```

### 학습 정리

- 글꼴 태그
h1~h6, p, hr, br, i, em, b, strong
- 목록 태그
ol, ul, li, dl, dt, dd
- 표 태그
table, tr, th, td
---

### Semantic

- 이점
    - 검색엔진 최적화
    - 웹 접근성 향상
    - 가독성 향상

### HTML Sementic Elements

- `<header>` : 페이지에 대한 정보를 담는 태그로, 페이지 상단에 위치함
- `<nav>` : 다른 페이지나 같은 페이지 안에 다른 부분으로 이어주는 네비게이션 링크로 구성된 섹션을 표현함
- `<aside>` : 페이지 전체 내용과는 어느정도 관련성이 있지만, 주요 내용과는 직접적인 연관성은 없는 분리된 내용을 담고 있음
- `<main>` : 문서의 body 요소의 주 콘텐츠 (main contents)를 정의할 때 사용함
- `<article>` : article은 여러가지 아이템들을 묶어 재사용 가능하게 그룹화함
- `<footer>` : 주로 저작관 정보나 서비스 제공자 정보등을 나타내며 사이트 하단에 위치함
- `<details>` : 추가적인 정보를 나타내거나 사용자가 요청하는 정보를 나타냄
- `<figcaption>` : 부모요소인 figure 요소의 내용들에 대한 캡션, 혹은 제목을 나타냄
- `<figure>` : 일러스트, 다이어그램, 사진, 코드등에 주석을 다는 용도로 사용
- `<mark>` : 하나의 문서 내에서 다른 문맥과의 관련성을 나타내기 위해서 참조 목적으로 마킹되거나 하이라이트된 텍스트를 표현
- `<time>` : 24시간에서의 시간 혹은 [그레고리력](https://ko.wikipedia.org/wiki/%EA%B7%B8%EB%A0%88%EA%B3%A0%EB%A6%AC%EB%A0%A5)에서의 정밀한 날짜를 나타냄

- Non-Semantic

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Non Semantic</title>
    <style>
      * {
        text-align: center;
      }
      .header {
        border: 2px solid red;
        line-height: 55px;
        height: 55px;
      }
      .nav {
        border: 2px solid blue;
        height: 110px;
      }
      .main {
        border: 2px solid green;
        height: 300px;
        line-height: 300px;
      }
      .footer {
        border: 2px solid black;
        height: 55px;
        line-height: 55px;
      }
      ul {
        list-style: none;
        padding-left: 0px;
      }
    </style>
  </head>
  <body>
    <div class="header">Header 영역</div>
    <div class="nav">
      <ul>
        <li>Menu1</li>
        <li>Menu2</li>
        <li>Menu3</li>
        <li>Menu4</li>
      </ul>
    </div>
    <div class="main">Content 영역</div>
    <div class="footer">Footer 영역</div>
  </body>
</html>
```

- Semantic

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Semantic</title>
    <style>
      * {
        text-align: center;
      }
      header {
        border: 2px solid red;
        line-height: 55px;
        height: 55px;
      }
      nav {
        border: 2px solid blue;
        height: 110px;
      }
      main {
        border: 2px solid green;
        height: 300px;
        line-height: 300px;
      }
      footer {
        border: 2px solid black;
        height: 55px;
        line-height: 55px;
      }
      ul {
        list-style: none;
        padding-left: 0px;
      }
    </style>
  </head>
  <body>
    <header>Header 영역</header>
    <nav>
      <ul>
        <li>Menu1</li>
        <li>Menu2</li>
        <li>Menu3</li>
        <li>Menu4</li>
      </ul>
    </nav>
    <main>Content 영역</main>
    <footer>Footer 영역</footer>
  </body>
</html>
```

- 적극적으로 사용해야함


---

### Inline Level Element / Block Level Element

- `<div>`와<`span>`
    - `<div>` - 컨테이너 역할
    display : block
    - `<span>` - 특정 아이템
    display : inline
        - display 요소에 따라 나뉘어진다.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Inline Block 1</title>
    <style>
      div {
        background-color: beige;
      }
      span {
        background-color: red;
      }
    </style>
  </head>
  <body>
    <div>
      동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리나라 만세 무궁화
      삼천리 화려 강산 대한사람 대한으로 길이 보전하세 남산 위에 저 소나무
      철갑을 두른듯 바람서리 불변함은 우리 기상일세 무궁화 삼천리 화려 강산
      대한사람 대한으로 길이 보전하세 가을 하늘 공활한데 높고 구름 없이 밝은
      달은 우리 가슴 일편단심일세 무궁화 삼천리 화려 강산 대한사람 대한으로 길이
      보전하세 이 기상과 이 마음으로 충성을 다하여 괴로우나 즐거우나
      나라사랑하세 무궁화 삼천리 화려 강산 대한사람 대한으로 길이 보전하세 접기
    </div>

    <span>
      동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리나라 만세 무궁화
      삼천리 화려 강산 대한사람 대한으로 길이 보전하세 남산 위에 저 소나무
      철갑을 두른듯 바람서리 불변함은 우리 기상일세 무궁화 삼천리 화려 강산
      대한사람 대한으로 길이 보전하세 가을 하늘 공활한데 높고 구름 없이 밝은
      달은 우리 가슴 일편단심일세 무궁화 삼천리 화려 강산 대한사람 대한으로 길이
      보전하세 이 기상과 이 마음으로 충성을 다하여 괴로우나 즐거우나
      나라사랑하세 무궁화 삼천리 화려 강산 대한사람 대한으로 길이 보전하세 접기
    </span>

    <hr />

    <div>Hello</div>
    <span> Hello </span>
  </body>
</html>
```

### Block Elemnet

블록 레벨 요소는 부모 요소의 전체 공간을 차지하여 “블록을” 만든다. <h1>~<h6><ol><ul><li><p> 태그 등이 블록 요소에 속한다.

- 화면 구성이나 레이아웃을 짤 때는 블록 레벨 요소를 사용합니다.
- 블록 레벨 요소는 한칸을 모두 차지하기 때문에 세로로 나열 됩니다.
- width, height, margin 소성이 적용됨

### Inline Element

인라인 레벨 요소는 콘텐츠의 흐름을 끊지 않고(줄바꿈X), 요소를 구성하는 태그에 할당된 공간만 차지합니다.
<a><em><img><span> 태그 등이 인라인 요소에 속한다.

- 인라인 레벨 요소는 콘텐츠 영역 만큼 차지하기 때문에 가로로 나열됩니다.
- amrgin-top, margin-bottom 적용되지 않습니다. 대신에 line-height 이용
- width, height 속성이 적용되지 않습니다.
- 태그가 콘텐츠의 할당 된 공간만 갖고 있기 때문에 text-align과 같은 속성은 사용할 수 없습니다.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Inline Block Element</title>
    <style>
      div {
        background-color: red;
        width: 100px;
        height: 100px;
        border: 1px solid black;
      }

      span {
        background-color: blue;
        border: 1px solid gray;
      }
    </style>
  </head>
  <body>
    <div>1</div>
    <div>2</div>
    <div>3</div>
    <span>3</span><span>3</span><span>3</span>
  </body>
</html>
```



### 학습정리

- div, span
div, span 둘 다 영역태그이다.
div는 영역을 분할 하며, 컨테이너의 역할도 한다.
span은 영역태그이며, 특정 아이템을 꾸밀 때 사용한다.
- block vs inline
div는 block leven element 이다. (전체공간, 세로배치, width&height 적용 O)
span은 inline level element 이다. (콘텐츠만큼, 가로배치, width&height 적용X)

---
# 꿀팁 : 멀티셀렉터 기능
      
## Windows → Ctrl + Alt

## Mac → cmd + option
