# [HTML] 하이퍼링크 태그

## `<a>`

* 앵커태그라고도 부른다. 하이퍼링크로 문서와 문서를 연결한다.

<br>

## 이동경로에 따른 태그
### 다른 웹페이지로 이동

```html
<a href=”http:www.naver.com”>네이버 사이트로 이동></a>
```
<br>

### 다른 문서로 이동
- 다른 폴더로 이동해야 할 경우 문서명 앞에 경로를 적어준다.

```html
<!-- 같은 폴더 내 -->
<a href=”newMember.html”>회원가입</a>

<!-- 하위 폴더 -->
<a href=”folder/newMember.html”>회원가입</a>

<!-- 상위 폴더 -->
<a href=”../newMember.html”>회원가입</a>
```

<br>

### 문서 내 다른 영역으로 이동
    
```html
<a href=”#jQuery”>id가 jQuery인 영역으로 이동</a>

<!-- 문서 내에 id=”jQuery”인 영역으로 이동 -->
<h3 id=”jQuery”>jQuery 영역입니다</h3>
```

<br>

### target 타겟
+ 하이퍼링크의 대상인 문서를 어디에서 보여줄지 지정한다.

```html
<!-- 새창에서 출력 -->
<a href=”http:www.naver.com” target="_blank">
    플로그 새창에서 열기</a>

<!-- iFrame에서 출력 -->
<a href=”http:www.naver.com” target="iFrame">
```
