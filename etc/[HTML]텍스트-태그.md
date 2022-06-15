# [HTML] 텍스트 관련 태그

## `<h1>`,`</h1>` 제목 태그

```html
<h1>h1 제목 출력</h1> 
<h2>h2 제목 출력</h2>
<h3>h3 제목 출력</h3>
<h4>h4 제목 출력</h4>
<h5>h5 제목 출력</h5>
<h6>h6 제목 출력</h6>
```

<h1>h1 제목 출력</h1>
<h2>h2 제목 출력</h2>
<h3>h3 제목 출력</h3>
<h4>h4 제목 출력</h4>
<h5>h5 제목 출력</h5>
<h6>h6 제목 출력</h6>

<br>

## `<p>` `</p>` 문단 태그

+ 문단(paragraph)을 나누는 태그
+ `<br>` 태그를 2번 사용한 만큼의 간격이 분리된다.
+ `<p>` 태그를 여러 번 연속적으로 사용하더라도 행 간격이 더 벌어지지 않는다.

```html
<p>
    문단1
</p>
<p>
    문단2
</p>
```

### 출력값
<p>
    문단1
</p>
<p>
    문단2
</p>

<br>

## `<hr>` 수평선
    + `<hr/>`로도 사용 가능

<br>

# HTML 텍스트 장식효과 태그 종류

## `<b>` 텍스트 강조
    ```html
    <b>텍스트</b>
    <br>
    <strong>텍스트</strong>
    ```
    <b>텍스트</b><br>
    <strong>텍스트</strong>

<br>

## `<i>` 이탤릭체
```html
<i>텍스트</i>
<br>
<em>텍스트</em>
```
<i>텍스트</i><br>
<em>텍스트</em>

<br>

## `<sub>`,`<sup>` 첨자
```html
텍스트<sub>텍스트</sub>
<br>
텍스트<sup>텍스트</sup>
```

텍스트<sub>텍스트</sub><br>
텍스트<sup>텍스트</sup>

<br>

## `<big>`, `<small>` 텍스트 크기 조절
```html
<big>크게</big>
<br>
<small>작게</small>
```
<big>크게</big>
<br>
<small>작게</small>

<br>

## `<ins>` 밑줄 표시
```html
<ins>텍스트</ins>
```
<ins>텍스트</ins>

<br>

## `<del>` 취소선 표시
```html
<del>취소할 텍스트</del>
<br>
<strike>취소할 텍스트</strike>
```
<del>취소할 텍스트</del>
<br>
<strike>취소할 텍스트</strike>

<br>

## `<pr>`,`</pre>` 입력한 그대로 출력
* 공백이나 코드 등을 작성할 때, 입력창에 작성한 내용을 그대로 출력한다.
* HTML은 공백처리, 줄바꿈 표시가 불편하기 때문에 유용
```html
안           녕
<br>
<pre>안        녕</pre>
```
안           녕
<br>
<pre>안        녕</pre>

