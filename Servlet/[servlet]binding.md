# 바인딩

- 수십 개 또는 많은 양의 회원 정보나 상품 정보를 전달해야 할 경우, 포워딩 방식만 사용할 경우, 문제가 된다.
- 서블릿에서 다른 서블릿 또는 JSP로 다량의 데이터를 공유하거나 전달할 때 바인딩(binding) 기능 사용

## 바인딩 방법

- 포워딩 할 때 setAttribute(”바인딩이름”,데이터) 메소드 사용
- 바인딩 이름과 데이터를 묶어서 설정한 후
- 포워딩된 문서에서 getAtrribute(”바인딩이름") 메소드 사용하여 바인딩된 데이터를 추출하여 사용
- redirect 방식으로는 전송 안 되고, dispatch 포워딩 방식 사용

- 바인딩 예제1
  - [firstServlet06.java](http://firstServlet06.java) : /first06 : setAttribute()
  - [SecondServlet06.java](http://SecondServlet06.java) : /second06 : getAttribute()
- 바인딩 예제2
  - 좀 더 많은 양의 데이터 바인딩
  - DB연동 없이 VO와 ArrayList 사용해서 DB연동했다고 가정하고
  - 조회한 회원 정보를 ArrayList 객체에 저장한 후 바인딩 (setAttribute())
  - ViewServlet에서 getAttribute() 사용해서 회원 정보 출력
  - [MemberVO.java](http://MemberVO.java) (멤버 DTO)
  - 서블릿 생성
    - **MemberBindingServlet.java**
      - DB 연동 가정 : MemberVO를 ArrayList에 저장
      - memList로 데이터 바인딩 : setAttribute()
    - **MemberViewServlet.java**
      - getAttribute() : ArrayList로 반환
      - for문 사용해서 MemberVO 값 추출 (Getter 사용)
  ### DTO와 VO의 차이
  1. DTO (Data Transfer Object)
     1. 데이터 저장 담당 클래스(Model)
     2. Controller, Service, View 등 계층간 데이터 교환을 위해 사용되는 객체
     3. 비즈니스 로직을 갖지 않는 순수한 데이터 객체
     4. Getter / Setter 메소드만 포함
     5. 가변의 성격 (Setter : 값을 설정==값이 바뀜)
  2. VO (Value Object)
     1. 데이터 저장 담당 클래스 (Model)
     2. DTO와 혼용해서 사용되지만
     3. VO는 값(value)을 위해 사용되는 객체로 불변(read only)의 속성
     4. 보통 Getter의 기능만 포함
     5. 그러나 일반적으로 스프링에서 VO로 사용되지만 Getter/Setter 기능 다 사용하는 경우도 있다.
