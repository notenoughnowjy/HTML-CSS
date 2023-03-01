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
        <td>축지법</td>- .
- .
- .
- .

---

## 2023.02.28

### 폼 태그

`<form>` 요소는 정보를 제출하기 위하여 어디서부터 어디까지가 양식인지 지정하는 역할을 함

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form tag</title>
</head>

<body>
    <form action="/singup" method="post">
        <div class="form-example">
            <label for="name">이름 :</label>
            <input type="text" name="name" id="name" required>
        </div>
        <div class="for-example">
            <label for="email">이메일 :</label>
            <input type="email" name="email" id="email" required>
        </div>
        <div class="for-example">
            <input type="submit" value="제출하기">
        </div>
    </form>
</body>

</html>
```

### 속성

- `action` - 양식 데이터를 처리할 서버 프로그램의 URL
- `method` - 양식을 제출할 때 사용할 HTTP 메서드
    - `post` - 양식 데이터를 요청 본문으로 전송합니다.
    - `get` - 양식 데이터를 URL의 쿼리스트링으로 붙여서 전송

### Input 태그

`<input>` 요소로 데이터를 입력 받을 수 있습니다. `type` 속성을 통하여 다양한 방법으로 데이터를 받을 수 있습니다.

### text

`<input>` 태그의 기본값으로 한줄의 텍스트를 입력 받습니다.

```html
<input type="text" id="name">
```

HTML5 에서는 text 필드가 데이터 용도에 맞게 사용할 수 있도록 다양한 타입이 추가되었습니다.

- `email` - email 데이터를 받기위해 사용됩니다. (이메일 유효성 검증)
- `tel` - 전화번호를 받기위해 사용됩니다. (모바일 접근시 키패드가 다름)
- 더 많은 `type` 은 MDN 사이트에서 참고헤주세요.

### label

`<label>` 레이블 태근느 입력받는 필드를 설명할 때 사용합니다. `웹접근성 준수` 

사용 방법은 <label> 태그 하위에 <input> 태그를 위치시킬 수 있고 `id` 와 `for` 속성을 사용하여 `<input>` 태그와 연결지을 수 있습니다.

```html
<!-- label 태그 하위에 놓는 법 -->
<label>
	<input type="text" id="name">
</label>

<!-- for와 id속성을 사용하여 label 태그와 연결지음 -->
<label for="name">이름 : </label>
<input type="text" id="name">
```

### checkbox

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Input</title>
</head>

<body>
    <form action="">
        <fieldset>
            <legend>개인정보</legend>
            <input type="text">
            <input type="text">
        </fieldset>

        <fieldset>
            <legend>사업자정보</legend>
            <input type="text">
            <input type="text">
        </fieldset>
    </form>
</body>

</html>
```

---

### Form 데이터 태그 속성

- `required` 
입력값이 필수라는 것을 명시할 수 있습니다.
- `readonly`
필드를 읽기전용으로 필드로 만들 수 있습니다.
- `disabled`
비활성화 시킬 수 있으며 해당 필드는 서버로 전송되지 않습니다.
- `autofocus`
초기에 해달 필드에 커서를 위치 시킬 수 있습니다.
- `placeholder`
입력 필드가 비어있을 때 해당 입력값의 설명 또는 가이드 문구를 삽입할 수 있습니다.

### checkbox

여러개의 체크박스 항목 중 2개 이상 선택할 수 있습니다. 그리고 체크박스 선택시 선택된 체크박스의 `value` 값이 서버로 전송됩니다.

```html
<ul>
        <li>
          <label for="apple">사과</label>
          <input type="checkbox" name="" id="apple" value="apple" />
        </li>
        <li>
          <label for="orange">오렌지</label>
          <input type="checkbox" name="" id="orange" value="orange" />
        </li>
        <li>
          <label for="banana">바나나</label>
          <input type="checkbox" name="" id="banana" value="banana" />
        </li>
      </ul>

```

### radio

여러개의 라디오 항목 중 1개를 선택할 수 있습니다. 그리고 라디오 항목 선택시 선택된 항목의 `value` 값이 서버로 전송됩니다.

여러개 중 하나를 선택하게 하려면 그 여러 항목의 `<radio name=””>` `name` 속성 값을 같은 값으로 그룹핑 해줘야 합니다.

```html
<ul>
        <li>
          <label for="strawberry">딸기</label>
          <input
            type="strawberry"
            name="fruit"
            id="strawberry"
            value="strawberry"
          />
        </li>
        <li>
          <label for="grape">포도</label>
          <input type="grape" name="fruit" id="grape" value="grape" />
        </li>
        <li>
          <label for="peach">복숭아</label>
          <input type="peach" name="fruit" id="peach" value="peach" />
        </li>
      </ul>
```

## HTML Form 다루기 2

`<input>` 태그에서 주로 한줄 데이터를 `type` 에 의해 다양한 방 입력 받아습니다.

`<form>` 양식을 전송할 때는 `<input>` 태그 말고 다양한 요소를 사용할 수 있습니다.

Textarea

Select

detalist

Button

type

### Textarea

---

`<Textarea>` 는 여러줄의 데이터를 입력받을 수 있습니다.

```html
<textarea id="story" name="story" rows="5" cols="33">
It was a dark and stromy night...
</textarea>
```

속성

- rows - 화면에 표시되는 행수를 지정합니다
- cols - 화면에 표시되는 컬럼 수를 지정합니다.

### Select

---

`<select>` 태그는 옵션 메뉴를 제공합니다. `<option>` 태그로 각 항목을 나타내면 `<select>` 태그는 `<option>` 태그를 감싸줍니다.

```html
<fieldset>
      <legend>주문 상품을 선택해주세요</legend>
      <ul>
        <li>
          <select name="goods" id="goods" multiple>
            <option value="apple_10kg">사과10kg</option>
            <option value="apple_20kg" selected>사과20kg</option>
            <option value="apple_30kg">사과30kg</option>
            <option value="apple_40kg">사과40kg</option>
          </select>
        </li>
      </ul>
    </fieldset>
```

### datalist

다른 컨트롤에서 고를 수 있는 가능한, 혹은 추천하는 선택지를 나타내는 `<option>` 요소 여럿을 담습니다.

```html
<li>
        <label for="ice-cream-choice">맛을 선택하세요</label>
        <input
          list="ice-cream-flavors"
          name="ice-cream-choice"
          id="ice-cream-choice"
        />
        <datalist id="ice-cream-flavors">
          <option value="Chocolate"></option>
          <option value="Coconut"></option>
          <option value="Mint"></option>
          <option value="Strawberry"></option>
          <option value="Vanilla"></option>
        </datalist>
      </li>
```

### Button

`<button>` 요소는 클릭 가능한 버튼을 나타냅니다. `<form>` 내부는 물론이고 버튼기능이 필요한 곳 이라면 어디에나 배치할 수 있습니다.

```html
<button type="button">
추가하기
</button>
```

### `type`

버튼의 행동 방식을 선언합니다.

- `submit` : 버튼이 서버로 양식 데이터를 제출합니다. (기본값)
- `reset` : `<input type=”reset”>` 처럼, 모든 입력 필드를 초기값으로 되돌립니다.
- `button` : 기본 행동이 없으며 주로 클릭 한 후 자바스크립트 측 코드를 명령할 때 사용합니다.

```html
<button>제출하기</button>
      <button type="submit">제출하기</button>
      <button type="reset">리셋하기</button>
      <button type="button" onclick="alert('Hello World~!')">버튼</button>
<!-- 자바 스크립트 등을 추가로 설정하거나 할때 사용 -->

```

### 학습정리

- Form
양식을 정의하는 구획
- input
데이터를 입력받는 태그이며 다양한 타입들이 존재
ex) number, date, email, password, checkbox, radio
- textarea, select, datalist, button

---
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
`h1~h6`, `p`, `hr`, `br`, `i`, `em`, `b`, `strong`
- 목록 태그
`ol`, `ul`, `li`, `dl`, `dt`, `dd`
- 표 태그
`table`, `tr`, `th`, `td`
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

### `Block Element`

블록 레벨 요소는 부모 요소의 전체 공간을 차지하여 “블록을” 만든다. `<h1>~<h6><ol><ul><li><p>` 태그 등이 블록 요소에 속한다.
      
- 화면 구성이나 레이아웃을 짤 때는 블록 레벨 요소를 사용합니다.
- 블록 레벨 요소는 한칸을 모두 차지하기 때문에 세로로 나열 됩니다.
- width, height, margin 소성이 적용됨

### `Inline Element`

인라인 레벨 요소는 콘텐츠의 흐름을 끊지 않고(줄바꿈X), 요소를 구성하는 태그에 할당된 공간만 차지합니다.
`<a>``<em>``<img>``<span>` 태그 등이 인라인 요소에 속한다.

- 인라인 레벨 요소는 콘텐츠 영역 만큼 차지하기 때문에 가로로 나열됩니다.
- `amrgin-top`, `margin-bottom` 적용되지 않습니다. 대신에 `line-height` 이용
- `width`, `height` 속성이 적용되지 않습니다.
- 태그가 콘텐츠의 할당 된 공간만 갖고 있기 때문에 `text-align`과 같은 속성은 사용할 수 없습니다.

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
### 이미지 & 멀티미디어

- 이미지 <img>
- 절대경로 vs 상대경로
- 오디오 <audio>
- 비디오 <video>
- 하이퍼링크 <a>

### 이미지 태그

<img> 태그는 HTML 문서에 이미지를 넣습니다.

```html
<img src="images/apple.jpg" alt="사과">
```

위의 예제를 통해 `<img>` 요소의 사용법을 알 수 있습니다.

### 속성

- `src`
필수이며, 이미지로의 경로를 지정합니다.
- `alt`
이미지의 텍스트 설명이며 필수는 아니지만, 스크린 리더가 `alt` 의 값을 읽어 사용자에게 이미지를 설명하므로, 웹 접근성 차원에서 매우 유용합니다. 또한 네트워크 오류, 콘텐츠 차단, 죽은 링크 등 이미지를 표시할 수 없는 경우에도 이 속성의 값을 대신 보여줍니다.
- `height` 
픽셀 단위의 이미지의 고유 크기, 단위 없는 정수여야 합니다.
- `width` 
이미지의 픽셀 기준 고유 너비, 단위 없는 정수여야 합니다.

### 절대경로 vs 상대경로

### 절대경로

리소스(이미지)의 절대경로는 말 그대로 절대적인 고유한 경로를 지정하는 것입니다.

- 웹 이미지 절대경로 예) - http://www.naver.com/apple.png
http 프로토콜로 시작해서 전체 경로를 입력함
- 웹 이미지 절대경로 예) - /apple.png
루트(’/’) 디렉터리 부터 시작하는 경우 현재 도메인이 자동으로 앞에 붙음
- PC 컴퓨터 절대경로 예) - C:/user/박준영/cat.png

그러나 절대경로를 이용하면 웹에서 사라지거나 내 컴퓨터에서 만든 파일을 다른 곳으로 옮길 때 해당 절대 경로를 다시 수정해야 하는 불편함이 있습니다.

그래서 작업중인 폴더에 이미지를 옮기고 상대적인 위치를 가리킴으로써 이러한 불편함을 해소할 수 있습니다.

### 상대경로

상대경로는 현재 문서를 기준으로 경로를 인식하는 방법입니다.

- `index.html` 에서 동일한 위치에 있는 apple.png를 가져오는 방법 → `src=”apple.png”` 또는 `src=”./apple.png”`
- `index.html` 의 상위 폴더에 이미지가 있는 경우 → `src=”../apple.png”`
- `index.html` 의 하위 폴더에 이미지가 있는 경우 → `src=”하위폴더/apple.png”`

---
## 2023.02.27
### 오디오 태그

`<audio>` 태그는 HTML 문서에 소리 콘텐츠를 넣을 때 사용합니다.

`src` 속성 또는 `<source>` Elements를 사용하여 한 개 이상의 오디오 소스를 지정할 수 있으며, 다수를 지정한 경우 가장 적절한 소스를 브라우저가 선택합니다.

```html
<!-- src 속성을 사용 -->
<audio controls src=""></audio>

<!-- source 요소를 사용 -->
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg" />
  <source src="myAudio.ogg" type="audio/ogg" />
</audio>
```

### 비디오 태그

`<video>` 태그는 영상 콘텐츠를 HTML 문서에 삽입할 때 사용함

`src` 속성 또는 `<source>` Element를 사용하여 한 개 이상의 오디오 소스를 지정할 수 있으며, 다수를 지정한 경우 가장 적절한 소스를 브라우저가 선택합니다.

### Form

- Form
- Input
- textarea, selec, button

### 오디오&비디오 태그 속성

- `controls` - 플레이어 화면에 컨트롤 바(재생막대)를 표시합니다.
- `autoplay` - 오디오나 비디오를 자동으로 실행합니다.
단, 크롬, 파이어폭스 브라우저는 자동 재생을 지원하지 않습니다. 만약 자동 재생을 하고 싶다면 `muted` 속성을 사용하여 소리를 제거해야 합니다.
- `loop` - 오디오나 비디오를 반복 재생합니다.
- `muted` - 오디오나 비디오의 소리를 제거합니다.
- `preload` - 페이지를 불러올 때 오디오나 비디오 파일을 어떻게 로딩할 것인지 지정합니다. 사용할 수 있는 값은 `auto` `metadata` `none` 입니다.
기본적으로 `preload=”auto”` 가 사용됩니다.
- `width` `height` - 비디오 플레이어의 너비와 높이를 지정합니다. `width` 나 `height` 의 값 중에서 하나만 지정하면 나머지는 자동으로 계산해서 표시합니다.
- `poster=”파일이름”` - `<video>` 태그에서 사용하는 속성으로, 비디오가 재생되기 전까지 화면에 표시될 포스터 이미지를 지정합니다.

### 하이퍼링크 태그

`<a>` 태그는 `href` 속성을 사용하여 다른 페이지나 같은 페이지의 특정위치, 파일, 이메일 주소 그 외 다른 URL로 연결할 수 있는 하이퍼링크를 만듭니다.

`target=”_blank”`속성을 사용하여 새탭에서 화면을 열 수 있다.

- 같은 폴더안에 있는 다른페이지로 이동
- 이미지에 하이퍼링크 걸기
- ID 속성이 apple인 특정위치로 이동하는 하이퍼링크

### 속성

- `href` 
하이퍼링크가 가리키는 URL 링크는 HTTP 기반 URL일 필요는 없고, 브라우저가 지원하는 모든 URL 스킴을 사용할 수 있습니다.
    - 페이지 구획을 가리키는 프래그먼트 URL
    - 미디어 파일 일부를 가리키는 미디어 프래그먼트
    - `tel:` URL을 사용하는 전화번호
    - `mailto:` URL을 사용하는 이메일 주소
    - 웹 브라우저는 다른 URL 스킴을 지원하지 않지만, 웹사이트는 `Navigator.registerProtocolHandler()` 를 통해 지원할 수 있습니다.
- `target`
    - `_self` : URL을 현재 브라우징 맥락에 표시합니다. 기본값.
    - `_blank` : URL을 새로운 브라우징 맥락에 표시합니다. 보통 새 탭이지만, 사용자가 브라우저 설정을 통해 새 창으로 바꿀 수 있습니다.
    - `_parent` : URL을 현재 브라우징 맥락의 부모에 표시합니다. 부모가 존재하지 않으면 `_self` 와 동일하게 행동합니다.
    - `_top` : URL을 최상단 브라우징 맥락(현재 맥락의 부모면서 자신의 부모가 존재하지 않는, 제일 높은 맥락)에 표싷바니다. 부모가 존재하지 않으면 `_self` 와 동일하게 행동합니다.

### 학습정리

- 이미지 <img>
src, alt
- 절대경로 vs 상대경로
절대 : http~, /~
상대 : ./ ../
- 오디오 <audio>
- 비디오 <video>
- 하이퍼링크 <a>
- href, target=”_blank”
### Form

- Form
- Input
- textarea, selec, button

### HTML Form 다루기 1

HTML에서 Form은 웹에서 사용자의 정보를 입력받기 위해 사용
예를들면 로그인, 회원가입, 게시판 글쓰기 등 우리는 사용자의 데이터를 입력받아 데이터를 입력받는다.
이때 입력받은 데이터들의 묶을 폼(Form)그리고 데이터를 폼 데이터(Form Data) 또는 필드(Field)라고 함.

즉, 폼(Form)은 사용자의 정보를 입력받을 수 있게 만들어 놓은 형식

- 폼태그


---

## 2023.02.28

### 폼 태그

`<form>` 요소는 정보를 제출하기 위하여 어디서부터 어디까지가 양식인지 지정하는 역할을 함

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form tag</title>
</head>

<body>
    <form action="/singup" method="post">
        <div class="form-example">
            <label for="name">이름 :</label>
            <input type="text" name="name" id="name" required>
        </div>
        <div class="for-example">
            <label for="email">이메일 :</label>
            <input type="email" name="email" id="email" required>
        </div>
        <div class="for-example">
            <input type="submit" value="제출하기">
        </div>
    </form>
</body>

</html>
```

### 속성

- `action` - 양식 데이터를 처리할 서버 프로그램의 URL
- `method` - 양식을 제출할 때 사용할 HTTP 메서드
    - `post` - 양식 데이터를 요청 본문으로 전송합니다.
    - `get` - 양식 데이터를 URL의 쿼리스트링으로 붙여서 전송

### Input 태그

`<input>` 요소로 데이터를 입력 받을 수 있습니다. `type` 속성을 통하여 다양한 방법으로 데이터를 받을 수 있습니다.

### text

`<input>` 태그의 기본값으로 한줄의 텍스트를 입력 받습니다.

```html
<input type="text" id="name">
```

HTML5 에서는 text 필드가 데이터 용도에 맞게 사용할 수 있도록 다양한 타입이 추가되었습니다.

- `email` - email 데이터를 받기위해 사용됩니다. (이메일 유효성 검증)
- `tel` - 전화번호를 받기위해 사용됩니다. (모바일 접근시 키패드가 다름)
- 더 많은 `type` 은 MDN 사이트에서 참고헤주세요.

### label

`<label>` 레이블 태근느 입력받는 필드를 설명할 때 사용합니다. `웹접근성 준수` 

사용 방법은 <label> 태그 하위에 <input> 태그를 위치시킬 수 있고 `id` 와 `for` 속성을 사용하여 `<input>` 태그와 연결지을 수 있습니다.

```html
<!-- label 태그 하위에 놓는 법 -->
<label>
	<input type="text" id="name">
</label>

<!-- for와 id속성을 사용하여 label 태그와 연결지음 -->
<label for="name">이름 : </label>
<input type="text" id="name">
```

### checkbox

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Input</title>
</head>

<body>
    <form action="">
        <fieldset>
            <legend>개인정보</legend>
            <input type="text">
            <input type="text">
        </fieldset>

        <fieldset>
            <legend>사업자정보</legend>
            <input type="text">
            <input type="text">
        </fieldset>
    </form>
</body>

</html>
```

---

### Form 데이터 태그 속성

- `required` 
입력값이 필수라는 것을 명시할 수 있습니다.
- `readonly`
필드를 읽기전용으로 필드로 만들 수 있습니다.
- `disabled`
비활성화 시킬 수 있으며 해당 필드는 서버로 전송되지 않습니다.
- `autofocus`
초기에 해달 필드에 커서를 위치 시킬 수 있습니다.
- `placeholder`
입력 필드가 비어있을 때 해당 입력값의 설명 또는 가이드 문구를 삽입할 수 있습니다.

### checkbox

여러개의 체크박스 항목 중 2개 이상 선택할 수 있습니다. 그리고 체크박스 선택시 선택된 체크박스의 `value` 값이 서버로 전송됩니다.

```html
<ul>
        <li>
          <label for="apple">사과</label>
          <input type="checkbox" name="" id="apple" value="apple" />
        </li>
        <li>
          <label for="orange">오렌지</label>
          <input type="checkbox" name="" id="orange" value="orange" />
        </li>
        <li>
          <label for="banana">바나나</label>
          <input type="checkbox" name="" id="banana" value="banana" />
        </li>
      </ul>

```

### radio

여러개의 라디오 항목 중 1개를 선택할 수 있습니다. 그리고 라디오 항목 선택시 선택된 항목의 `value` 값이 서버로 전송됩니다.

여러개 중 하나를 선택하게 하려면 그 여러 항목의 `<radio name=””>` `name` 속성 값을 같은 값으로 그룹핑 해줘야 합니다.

```html
<ul>
        <li>
          <label for="strawberry">딸기</label>
          <input
            type="strawberry"
            name="fruit"
            id="strawberry"
            value="strawberry"
          />
        </li>
        <li>
          <label for="grape">포도</label>
          <input type="grape" name="fruit" id="grape" value="grape" />
        </li>
        <li>
          <label for="peach">복숭아</label>
          <input type="peach" name="fruit" id="peach" value="peach" />
        </li>
      </ul>
```

## HTML Form 다루기 2

`<input>` 태그에서 주로 한줄 데이터를 `type` 에 의해 다양한 방 입력 받아습니다.

`<form>` 양식을 전송할 때는 `<input>` 태그 말고 다양한 요소를 사용할 수 있습니다.

Textarea

Select

detalist

Button

type

### Textarea

---

`<Textarea>` 는 여러줄의 데이터를 입력받을 수 있습니다.

```html
<textarea id="story" name="story" rows="5" cols="33">
It was a dark and stromy night...
</textarea>
```

속성

- rows - 화면에 표시되는 행수를 지정합니다
- cols - 화면에 표시되는 컬럼 수를 지정합니다.

### Select

---

`<select>` 태그는 옵션 메뉴를 제공합니다. `<option>` 태그로 각 항목을 나타내면 `<select>` 태그는 `<option>` 태그를 감싸줍니다.

```html
<fieldset>
      <legend>주문 상품을 선택해주세요</legend>
      <ul>
        <li>
          <select name="goods" id="goods" multiple>
            <option value="apple_10kg">사과10kg</option>
            <option value="apple_20kg" selected>사과20kg</option>
            <option value="apple_30kg">사과30kg</option>
            <option value="apple_40kg">사과40kg</option>
          </select>
        </li>
      </ul>
    </fieldset>
```

### datalist

다른 컨트롤에서 고를 수 있는 가능한, 혹은 추천하는 선택지를 나타내는 `<option>` 요소 여럿을 담습니다.

```html
<li>
        <label for="ice-cream-choice">맛을 선택하세요</label>
        <input
          list="ice-cream-flavors"
          name="ice-cream-choice"
          id="ice-cream-choice"
        />
        <datalist id="ice-cream-flavors">
          <option value="Chocolate"></option>
          <option value="Coconut"></option>
          <option value="Mint"></option>
          <option value="Strawberry"></option>
          <option value="Vanilla"></option>
        </datalist>
      </li>
```

### Button

`<button>` 요소는 클릭 가능한 버튼을 나타냅니다. `<form>` 내부는 물론이고 버튼기능이 필요한 곳 이라면 어디에나 배치할 수 있습니다.

```html
<button type="button">
추가하기
</button>
```

### `type`

버튼의 행동 방식을 선언합니다.

- `submit` : 버튼이 서버로 양식 데이터를 제출합니다. (기본값)
- `reset` : `<input type=”reset”>` 처럼, 모든 입력 필드를 초기값으로 되돌립니다.
- `button` : 기본 행동이 없으며 주로 클릭 한 후 자바스크립트 측 코드를 명령할 때 사용합니다.

```html
<button>제출하기</button>
      <button type="submit">제출하기</button>
      <button type="reset">리셋하기</button>
      <button type="button" onclick="alert('Hello World~!')">버튼</button>
<!-- 자바 스크립트 등을 추가로 설정하거나 할때 사용 -->

```

### 학습정리

- Form
양식을 정의하는 구획
- input
데이터를 입력받는 태그이며 다양한 타입들이 존재
ex) number, date, email, password, checkbox, radio
- textarea, select, datalist, button

---
## 2023.03.01

### Head

### head 안에 배치할 수 있는 요소

- `<title>`
브라우저의 제목 표시줄이나 페이지 탭에 보이는 문서 제목을 정의합니다. 텍스트만 포함할 수 있으며 태그를 포함하더라도 무시함

```html
<title>NAVER</title>
```

- `<base>`
문서 안의 모든 상대 URL이 사용할 기준 URL을 지정합니다. **문서에는 하나의 `<base>` 요소만 존재**할 수 있습니다.

```html
<base href="/assets/images/" />
```

- `<link>` 
요소는 현재 문서와 외부 리소스의 관계를 명시합니다. <link>는 스타일 시트를 연결할 때 제일 많이 사용하지만, 사이트 아이콘(”파비콘”과 홈 화면 아이콘>. 연결 등 여러가지로 쓰일 수 있습니다.

```html
<!--파비콘 설정-->
<link rel="shortcut icon" href="./favicon.ico" />

<!-- Style 시트 연결 -->
<link href="/style.css" rel="stylesheet">
```

- `<style>`
스타일 규칙을 담고 있습니다.

```html
<style>
.tile {
	color: blue;
}
</style>
```

- `<meta>
<base>` `<link>` `<script>` `<style>` `<title>` 과 같은 다른 메타관련 요소로 나타낼 수 없는 메타데이터를 나타냅니다.

```html
<meta property="og:image" content="https://example.com/image.jpg">
```

- `<script>` 
데이터나 자바스크립터 코드를 웹 문서에 포함할 때 사용합니다.

```html
<script src="javascriopt"></script>
```

---

## 오픈그래프 Open Graph

---

콘텐츠의 요약내용이 SNS에 게시되는데 최적화된 데이터를 가지고 갈 수 있도록 설정하는 것            
