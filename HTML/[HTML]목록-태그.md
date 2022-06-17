# 목록 태그

- 목차
    1. [기본 목록 태그](#기본-목록)
        + [순서가 없는 목록](#순서가-없는-목록)
        + [순서가 있는 목록](#순서가-있는-목록)
    2. [정의 목록 태그](#정의-목록-태그)
    3. [중첩 목록 태그](#중첩-목록-태그)

<br>

---

<br>

## 기본 목록
### 순서가 없는 목록

* `<ul>` Unordered List
* `<li>` List Item

```html
<ul>FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
    <li>Peach</li>
</ul>
```

<ul>FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
    <li>Peach</li>
</ul>
<br>

* 속성 `type`
    + `disc` 검은 원(기본값)
    + `circle` 흰 원
    + `square` 사각형

```html
<ul type="square">FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
    <li>Peach</li>
</ul>
```
<ul type="square">FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
    <li>Peach</li>
</ul>
<br>
    
### 순서가 있는 목록

* `<ol>` Ordered List
* `<li>` List Item

```html
<ol>FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
    <li>Peach</li>
</ol>
```
<ol>FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
    <li>Peach</li>
</ol>
<br>

* 속성 `type`
    + `1` 숫자(기본값)
    + `a` 영어 소문자
    + `A` 영어 대문자
    + `i` 소문자 로마 숫자
    + `I` 대문자 로마 숫자
* 속성 `start`
    + `숫자` 시작 라벨 지정
* `reversed` 역순으로 표시

```html
<ol type="i" start="4" reversed>My Favorite Food
    <li>Pizza</li>
    <li>Hot dog</li>
    <li>Ice cream</li>
    <li>Chicken</li>
</ol>
```
<ol type="i" start="4" reversed>My Favorite Food
    <li>Pizza</li>
    <li>Hot dog</li>
    <li>Ice cream</li>
    <li>Chicken</li>
</ol>
<br>

## 정의 목록 태그
* `<dl>` 정의 목록 Definition List
* `<dt>` 정의 용어 Definition Term
* `<dd>` 정의 설명 Definition Description

```html
<dl>
    <dt>정의 제목1</dt>
    <dt>정의 제목2</dt>
    <dd>정의 설명1</dd>
    <dd>정의 설명2</dd>
</dl>
```
<dl>
    <dt>정의 제목1</dt>
    <dt>정의 제목2</dt>
    <dd>정의 설명1</dd>
    <dd>정의 설명2</dd>
</dl>
<br>

## 중첩 목록 태그

- 다양한 목록 형식을 섞어서 사용 가능하다.

```html
<ol>FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
        <ul type="1">
        <li>This is red</li>
        <li>and sweet!</li>
        </ul>
    <li>Peach</li>
</ol>
```
<ol>FRUITS
    <li>Apple</li>
    <li>Banana</li>
    <li>Strawberry</li>
        <ul type="1">
        <li>This is red</li>
        <li>and sweet!</li>
        </ul>
    <li>Peach</li>
</ol>
<br>