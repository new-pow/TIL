# 서블릿 요청 API

- 서블릿의 기본 기능
  1. 클라이언트로부터 요청을 받기
  2. 데이터베이스 연동과 같은 비즈니스 로직을 처리
  3. 처리된 결과를 클라이언트에 응답

## 1. 클라이언트로부터 요청 받기

- 서블릿 요청과 응답 수행 API
- javax.servlet.http 패키지에 포함
- 요청과 관련된 API

  ```java
  import javax.servlet.http.HttpServletRequest;
  ```

- 응답과 관련된 API

  ```java
  import javax.servlet.http.HttpServletResponse;
  ```

### 서블릿에서 클라이언트 요청 받는 방법

- HttpServletRequest 클래스의 여러 가지 메소드를 이용해서 전송된 데이터를 받는다.
- <form>태그로 전송된 데이터를 받아오는 메소드
    - 그 안에 있는 모든 값을 서버로 보낸다.

## 2. 태그로부터 요청

### `<form>` 태그로 서블릿 요청

- 서블릿 데이터를 웹 브라우저를 통해 전송하는 방법
- <form>태그를 사용해서 브라우저에서 서블릿으로 사용자의 요청이나 데이터를 전송

### `<form>` 태그

- action 속성 : 서블릿 또는 jsp 이름 지정
- method : get 또는 post(디폴트 get)

### `<input>` 태그

- 데이터 입력 받아서 전송
- name : 속성 사용
  - jQuery에서는 id였지만, 지금은 name을 사용.
  - name 속성명과 속성값 쌍으로 전송
