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
