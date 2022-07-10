# [JSP/JSTL] Core Tags

## OVERVIEW

```html
<!-- 다음을 태그에 추가 후 사용 가능 -->
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
```

- URI : http://html.sun.com/jsp/jstl/core
- prefix : c
- 제공 기능
  - 변수의 선언 및 삭제 등의 변수와 관련된 작업
  - if, for 문 등과 같은 제어문
  - url 처리 및 그밖에 예외처리 및 화면 출력

## Cor 태그

| 종류                              | 설명                                                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`<c:set>`](#cset-태그)           | - JSP의 setAttribute()와 같은 역할.<br>(page, request, session, application) 범위의 변수(속성)를 설정                                                   |
| `<c:remove>`                      | - JSP의 removeAttribute()와 같은 역할.<br>(page, request, session, application) 범위의 변수(속성)를 제거                                                |
| `<c:out>`                         | - 화면 출력. JSP의 표현식 대체                                                                                                                          |
| [`<c:redirect>`](#credirect-태그) | - response.sendRedirect()를 대체하는 태그로 지정한 다른 페이지로 이동                                                                                   |
| [`<c:if>`](#cif-태그)             | - 조건문을 사용할 때 씀 : else문 없을 때                                                                                                                |
| [`<c:choose>`](#cchoose-태그)     | - 자바의 switch 문과 같지만, 조건에 문자열 비교도 가능하고 쓰임의 범위가 넓음. <br>서브 태그로 `<when>`과 `<otherwise>`를 가짐 <br> - else 가 필요할 때 |
| `<c:when>`                        | - choose의 서브 태그로 조건의 비교 시에 조건을 만족한 경우에 사용                                                                                       |
| `<c:otherwise>`                   | - 조건을 만족하지 못한 경우에 사용                                                                                                                      |
| [`<c:forEach>`](#cforeach-태그✨) | - 객체 전체에 걸쳐 반복 실행을 할 때 사용                                                                                                               |
| `<c:forToken>`                    | - 자바의 StringTokenizer 클래스를 사용하는 것과 같음                                                                                                    |
| `<c:catch>`                       | - body 위치에서 실행되는 코드의 예외를 잡아내는 역할을 담당                                                                                             |
| `<c:import>`                      | - 웹 애플리케이션 내부의 자원 접근은 물론이고, <br>http, ftp 같은 외부에 있는 자원(html, jsp등)을 가져옴                                                |
| `<c:param>`                       | - 파라미터사용시 필요. `<import>`태그의 URL뒤에 파라미터로 붙여서 사용되기도 함                                                                         |
| [`<c:url>`](#curl-태그)           | - 쿼리 파라미터로 부터 URL을 생성                                                                                                                       |

## `<c:set>` 태그

- 변수 선언

```html
<c:set var="변수명" value="변수값" [scope] />
```

## `<c:if>` 태그

- 조건문을 사용할 때 씀 : else 문이 없을 때

```html
<c:if test="”${조건식}”" /> <c:if test="”${조건식}”" [scope] />
```

## `<c:choose>` 태그

- 자바의 switch 문과 같지만, 조건에 문자열 비교도 가능하고 쓰임의 범위가 넓음. 서브 태그로 <when>과 <otherwise>를 가짐
- else 가 필요할 때

```html
<c:choose>
  <c:when test="조건식">내용1</c:when>
  <c:when test="조건식2">내용2</c:when>
  <c:otherwise>내용n</c:otherwise></c:choose
>
```

## `<c:forEach>` 태그✨

- 반복문 수행

```html
<c:forEach
  var="변수명"
  begin="시작값"
  end="마지막값"
  step="증가값"
  varStatus="반복상태변수명"
></c:forEach>
```

```java
// 컨트롤러
// 데이터를 List 형태로 가져와 modelAndView 객체에 담아줌
ModelAndView modelAndView = new ModelAndView();
modelAndView.addObject("myQst", service.getMyQst());
modelAndView.setViewName("mypage/activity");
return modelAndView;
```

```html
<!-- 태그 예시 : 테이블로 출력 -->
<table class="table">
  <thead>
    <tr>
      <th>번호</th>
      <th>제목</th>
      <th>작성일</th>
    </tr>
  </thead>

  <c:forEach items="${myQst}" var="qst" varStatus="status">
    <tr>
      <td>${ status.count }</td>
      <td>${ qst.q_title }</td>
      <td>${ qst.q_regdate }</td>
    </tr>
  </c:forEach>
</table>
```

- varStatus : 반복 상태 속성 지정

  - index
    - items에서 정의한 항목을 가르키는 index 번호
    - 0부터 시작한다.
    - begin=1로 하면 index도 1부터 시작
  - count : 몇 번째인지 표시. 1부터 시작
  - first : 첫번째이면 true
  - last : 마지막 반복이면 true

## `<c:url>` 태그

- url 정보 저장

```html
<c:url var="변수명" value="url 경로" />
```

## `<c:redirect>` 태그

- response.sendRedirect() 기능과 동일
- 매개변수 전달 가능
- <c:redirect url=”redirect할 url”>

```html
<c:param name=”id” value=”홍길동” />
</c:redirect>
```
