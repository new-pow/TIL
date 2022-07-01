# 서블릿 응답 처리

## 서블릿의 응답처리 방법

- doGet()이나 doPost() 메소드 안에서 처리함
- javax.servlet.http.HttpServletResponse객체를 이용함
- 클라이언트에게 전송할 데이터 타입 인코딩
- MIME-TYPE
  - HTML로 전송 시 : text/html
    - 일반적으로 사용
  - 일반 텍스트 전송 : text/plain
  - XML 데이터로 전송 : application/xml
  ```java
  response.setContentType(”text/html;charset=utf-8”)
  ```
- 클라이언트(웹 브라우저)와 서블릿의 통신은 자바 입출력 스트림 I/O의 스트림 이용
  - PrintWriter 클래스 사용
  ```java
  PrintWriter out = response.getWriter();
  out.print(data);
  // data : 웹 브라우저로 보내는 데이터
  ```

### 서블릿의 응답 처리 순서

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/01b2bb86-a1b1-4e67-8f5e-611984e3154e/Untitled.png)

## doGet() / doPost() 방식 둘 다 처리

- 일반적으로 doHandle() 또는 doProcess() 메소드를 새로 추가해서
- doGet() / doPost() 방식 둘다 처리
- doGet() 혹은 doPost() 방식으로 요청이 들어오면
- doGet() 또는 doPost() 메소드에서 doHandle() 호출하고 request와 response 객체 전달
- doHandle() 메소드에서 처리

# Get 방식과 Post 방식

## 1. Get 방식

- 데이터를 전송할 때 데이터가 URL 뒤에 name=value 형태로 전송
- 여러 개의 데이터를 전송할 때는 &로 구분해서 전송
- 전송 데이터 노출 : 보안 취약
  - _그래서 데이터 전송할때는 사용하지 않는다._
- 전송 데이터 길이 제한 : 최대 255자
- 기본 전송 방식
- 웹 브라우저에서 직접 url 입력해서 doGet() 메소드 호출 가능
- 서블릿에서는 doGet() 이용해서 데이터 처리
- 웹 브라우저에서 직접 url에 입력해서 doGet() 메소드 호출 가능

## 2. Post 방식

- 데이터를 전송할 때 TCP/IP 프로토콜 데이터의 HEAD 영역에 숨겨서 전송됨
- 보안에 유리
  - 데이터 전송에 주로 사용한다!
- 전송 데이터 길이 : 무제한
- 서블릿에서는 doPost() 메소드 이용해서 데이터 처리
- get방식 보다 속도가 느린 편
  - 그래서 일반 사용에는 get방식을 사용한다.

---

💡 **[ 주의 ]**

- 폼에 입력되어 서버로 전송되는 값들은 모두 문자열로 전송된다. <br>
  연산이 필요한 경우, 숫자로 형변환 필요

- 1개의 값을 받을 경우 : `getParameter()` 메소드 사용
- 여러 개의 값을 받을 경우 (동일한 name 값이 여러개인 경우 : checkbox 등) `getParameterValues()` 메소드 사용
- radio 버튼의 경우, 한 그룹의 radio 버튼 이름이 동일해도, 1개의 값만 전송되므로 `getParameter()` 메소드 사용

---
