# HTML
> Hyper Text Markup Language

* 웹 브라우저에서 하이퍼텍스트 기능을 구현하는 웹페이지 작성언어

## 하이퍼텍스트
* 문서 간에 서로 링크가 설정되어 있어, 링크 설정 부분을 클릭하면 해당 문서로 이동하는 기능
* 일반문서는 위에서 아래로 순서대로 읽지만, 하이퍼텍스트는 링크된 문서로 이동(페이지 변경)한다.

## 언어 구성
* 태그
    * HTML에서 사용하는 명령어로 문자열과 기호로 이루어졌다.
    * 원하는 모양과 형태로 브라우저에게 명령을 내릴 수 있다.
* 문서 내용

## 태그의 종류
### 1. [HTML 문서 구조 태그]([HTML]문서구조-태그.md)
### 2. [텍스트 관련 태그]([HTML]텍스트-태그.md)
### 3. [하이퍼링크 태그]([HTML]하이퍼링크-태그.md)
### 4. [목록 태그]([HTML]목록-태그.md)
### 5. [테이블 태그]([HTML]테이블-태그.md)
### 6. [이미지/이미지맵 태그]([HTML]이미지-이미지맵-태그.md)
### 7. [문서 삽입 태그]([HTML]문서삽입-태그.md)
### 8. [입력 양식 태그]([HTML]입력양식-태그.md)
### 9. [공간 분할 태그]([HTML]공간분할-태그.md)

```html
<!-- 형식 -->
<!-- <시작태그명>출력내용</태그명> -->

<p>안녕하세요</p>

<!-- 속성이 있는 경우의 형식 -->
<!-- <태그명 속성명="속성값">출력내용</태그명> -->
<a href="a.html" target="iFarm">이동</a>

<!-- 종료 태그 없이 혼자 사용하는 태그 -->
<br> : 줄바꿈
<img rct="a.jpg"> : 이미지 삽입
<hr> : 수평선 삽입
```



## 문서 구성
### `<head>` 부분
* 문서의 기본 정보를 작성하는 부분
    + 제목, 문자열 처리 방식
    + 외부 파일 연결
    + CSS 정리
    + 자바스크립트 정리