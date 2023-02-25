## 2023.02.23

### HTML이란 무엇인가?

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

# 꿀팁 : 멀티셀렉터 기능

## Windows → Ctrl + Alt

## Mac → cmd + option
