# 👟 스프링 부트 Spring Boot

- 스프링 프레임워크를 사용하는 프로젝트를 아주 간편하게 설정할 수 있는 스프링 프레임워크의 서브프로젝트

## 스프링 부트의 특징

- XML 기반 설정 과정 없이 간단히 프로젝트를 시작할 수 있다.
  - 자연스럽게 생성이 된다.
- 메이븐의 pom.xml 파일에 의존성 라이브러리 버전을 일일이 지정하지 않아도 된다.
  - 스프링 부트가 권장 버전 관리
- 단독 실행되는 스프링 애플리케이션 구현 가능
- 프로젝트 환경 구축에 필요한 서버 외적인 툴들이 내장되어 있어 별도 설치 필요 없음
  - 톰캣 내장되어 있다.

## **✨ 스프링 부트 생성 개요**

### 1. 스프링 부트 프로젝트 생성

- 프로젝트명 / Group / Artifact / pac
- Dependencies 선택
  1. SQL : JDBC API, MyBatis Framework / MySQL Driver
  2. Web : Spring Web

### 2. 프로젝트 생성 후 확인

1. **pom.xml 내용 확인**
   - java.version
   - jdbc
   - mysql-connector
   - tomcat
2. **자동 생성된 클래스 파일 확인**
   - ServletInitializer.java
     - 스프링 부트 애플리케이션을 web.xml 없이 톰캣에서 실행하게 해주는 클래스
     - 따라서 스프링 부트에는 web.xml, context.xml 설정 파일 없음
   - (projectname)\_Application.java
     - @SpringBootApplication 붙어있음
       - 스프링 부트 애플리케이션으로 설정하는 어노테이션
     - main() 메소드 포함
       - 스프링 부트 생성 시 자동으로 생성
       - 스프링 부트 프로젝트에는 반드시 main() 이 있어야 함
       - 스프링 부트 프로젝트 main() 메소드를 시작점으로 실행
       - main() 메소드를 포함하는 java 파일이 필요
       - 이유 : 스프링 부트 웹 애플리케이션을 일반 자바 애플리케이션처럼 개발하려는 의도

### 3. 스프링 설정 파일

- application.properties : 파일 자동 생성
- 내용이 없는 빈 파일로 생성
- 추가할 내용
  - 포트 번호
  - 데이터베이스 연결 정보
  - mapper.xml 위치 지정
    - src/main/resources 파일에 생성할 것
- 여기서 Controller 추가하고 (”/” 매핑) 실행시켜서 오류 있는지 확인
- 오류 없으면 다음 스텝 go

### 4. JSP 뷰 설정

- 스프링 부트는 JSP 뷰가 기본이 아니기 때문에 JSP 뷰를 사용할 경우 추가 설정 필요
  - application.properties 파일에 JSP 설정 추가
  - pom.xml 의존성 라이브러리 추가
  - src/main/webapp 폴더에 WEB-INF/views 폴더 추가
  - hello.jsp 생성하고
  - 컨트롤러에서 @RequestMapping 추가해서 hello.jsp 실행되는지 확인
  - 스프링 부트에서 리소스 파일 경로 확인

### 5. DB 연동 CRUD 기능 구현

- spring_mvc_mybatis 에서 product 코드는 그대로 사용 (일부 경로 수정)
- 파일 위치 주의

# 🔨 스프링 부트 프로젝트 생성

## 1. 스프링부트 프로젝트 생성

### **프로젝트명 / Group / Artifact / 패키지명**

- File - New - Spring Starter Project
- 프로젝트명 (Name) : spring_boot_mybatis
- Type : Maven Project War
- Java Version : 11
- Group : com.spring_boot_mybatis
- Artifact : project
- 패키지명 (Package)
  - com.spring_boot_mybatis.project

### Dependencies 선택

- SQL : JDBC API / MyBatis Framework / MySQL Driver
- Web : Spring Web

## 2. 프로젝트 생성 후 확인

1. pom.xml 내용 확인

- java.version / jdbc / mysql-connector / tomcat

1. 자동 생성된 클래스 파일 확인

- ServletIn**i**tializer.java
  - 스프링 부트 애플리케이션을 web.xml 없이 톰캣에서 실행하게 해주는 클래스
  - 따라서 스프링 부트에는 web.xml, context.xml 설정 파일 없음
- …….Application.java
  - @SpringBootApplication 붙어 있음
    - 스프링 부트 애플리케이션으로 설정하는 어노테이션
  - main() 메소드 포함
    - 스프링 부트 생성 시 자동으로 생성
    - 스프링 부트 프로젝트에는 반드시 main()이 있어야 함
    - 스프링 부트 프로젝트 main() 메소드를 시작점으로 실행
    - main() 메소드를 포함하는 java 파일이 있어야 함
    - 이유 : 스프링 부트 웹 애플리케이션을 일반 자바 애플리케이션처럼 개발하려는 의도 때문

## 3. 스프링 설정 파일

### application.properties : 파일 자동 생성

- 내용이 없는 빈 파일로 생성
- src/main/resources에 위치

### 추가할 내용 : 포트번호, 데이터베이스 연결 정보, mapper.xml 위치 지정

- 포트 번호 : server.port=8080

- 데이터베이스 연결 정보

  - spring.datasource.driver-class-name=
  - spring.datasource.url=
  - spring.datasource.username=
  - spring.datasource.password=

- mapper.xml 위치 지정

  - src/main/resources 파일에 생성할 것
  - DAO와 mapper 파일 추가한 후에 설정할 것임

- 여기서 Controller 추가하고 (”/” 매핑) 실행시켜서 오류 있는지 확인

  - HelloController 클래스 추가

    - 요청 url : “/”

      - http://localhost:8080

      ```java
      @Controller
      public class HelloController {

      	// test print
      	@ResponseBody
      	@RequestMapping("/")	// 요청 url: http:localhost:8080
      	public String home() {
      		System.out.println("Hello Boot!");
      		return "Hello Boot!";	// jsp 페이지 안만들고, 새 문서에 출력
      	}
      }
      ```

  - 실행 : Run As / Spring Boot App

    - 웹브라우저에 url 직접 입력 : http://localhost:8080

<aside>
🐛 **BUG : 시작 전에 반드시 서버 중단하고 실행하기**

```java
Description:

Web server failed to start. Port 8080 was already in use.

Action:

Identify and stop the process that's listening on port 8080 or configure this application to listen on another port.
```

</aside>

- 오류가 없을 때

  ![Untitled](13%20SpringBoot%2001%208c8a196bfb2a4b8bb6e3f353f601bfd7/Untitled.png)

- 이제 웹브라우저에서 확인하기

  ![Untitled](13%20SpringBoot%2001%208c8a196bfb2a4b8bb6e3f353f601bfd7/Untitled%201.png)

## 4. JSP 설정

### application.properties 파일에 JSP 설정 추가

```java
# jsp view
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp
```

### pom.xml 의존성 라이브러리 추가

- jstl (java.servlet jstl)
- tomcat (org.apache.tomcat.embed tomcat.embeded jasper)

### src/main/webapp 폴더에 WEB-INF/views 폴더 추가

- hello.jsp 생성하고
- 컨트롤러에서 @RequestMapping 추가해서 hello.jsp 실행되는지 확인
- 스프링 부트에서 리소스 파일 경로 확인 : 이미지 출력

  - 리소스 파일 경로 src/main/resources/static 폴더가 기본 위치
  - static 폴더 안에 image 폴더 생성하고
    - apple.png

- 스프링 부트 프로젝트 생성 연습문제
  - spring_boot_mybatis2
  - hello.jsp까지 출력

## 5. DB 연동 CRUD 기능 구현

- spring_mvc_mybatis 에서 product 코드는 그대로 사용 (일부 경로 수정)
- 파일 위치 주의

### (1) 패키지 생성

- controller / dao / model / service
- 클래스 / 인터페이스 파일 (mapper 제외)
  - VO / service / DAO / Controller
- 복사 시 주의! - 이전 패키지 import 삭제할 것

### (2) mapper 파일 폴더 생성

- src/main/resources 폴더에 mappers 폴더 생성하고, 그 안에 product 폴더 생성
- product 폴더 안에 ProductMapper.xml 파일 복사
- application.properties에 mapper 위치 설정

### (3) …Application.java 클래스에 추가

- 컴포넌트 Controller와 Service 클래스에 대해 추가
  - @ComponentScan
  - @MapperScan
- DAO, Service, Controller 마다 모두 추가해 주어야 한다.
  - 추가하지 않으면 bean이 없다는 오류 발생

```java
@SpringBootApplication
@ComponentScan(basePackageClasses=ProductController.class)
@ComponentScan(basePackageClasses=ProductService.class)
@MapperScan(basePackageClasses=IProductDAO.class)
public class SpringBootMybatisApplication {

	public static void main(String[] args) {
		SpringApplication.run(SpringBootMybatisApplication.class, args);
	}

}
```

```java
// 줄였을 때
@SpringBootApplication
@ComponentScan(basePackages= {"com.spring_boot_mybatis.book"})
@MapperScan(basePackageClasses=IBookDAO.class)
public class SpringBootMybatisBookApplication {

	public static void main(String[] args) {
		SpringApplication.run(SpringBootMybatisBookApplication.class, args);
	}

}
```

### (4) view 페이지 복사

-
- product 폴더 복사
- index.jsp 복사

### **(5) HelloController 필요 없음 (삭제 또는 내용 주석 처리)**

### **(6) js 폴더 생성**

- **src/main/resources/static 폴더에 js 폴더 복사**

### **(7) 외부 경로 설정 : 상품 이미지 출력**

- WebConfig 클래스 생성 (WebMvcConfigurer 인터페이스 구현)
  - MVC 프로젝트에서 spring-context.xml에 설정한 내용 추가
  - <resources mapping="/images/**" location="file:///C:/springWorkspace/product_images/" />

```java
@Configuration
public class WebConfig implements WebMvcConfigurer {

	@Override
	public void addResourceHandlers(ResourceHandlerRegistry registry) {
		registry.addResourceHandler("/images/**")
		.addResourceLocations("file:/Users/newp/workSpace/springWorkSpace/product_images/");
	}

}
```

- 스프링 부트 프로젝트 연습문제
  - 도서관리 프로그램 작성
    - spring_boot_mybatis_book
  - CRUD 기능 구현
  - 중복 체크, 검색, 외부 파일 경로 설정 (이미지 출력)

# 스프링 부트 프로젝트에 파일 업로드

- MultipartFile 클래스 사용

  - 스프링 부트에서는 의존성 라이브러리 추가 필요 없음
  - 자동으로 MultipartConfigElement 클래스를 빈으로 등록

- HTML

  - <form enctype=”multipart/form-data”>

  - <input type="file">

- 업로드되는 파일 크기 제한 변경 가능

  - maxFileSize
    - 업로드하는 파일 1개의 크기 : 디폴트 1M
  - maxRequestSize
    - 요청 크기 제한
    - 모든 파일의 크기를 합한 크기 값 제한

- 파일 업로드 예제

  1. 파일명이 중복되지 않게 해서 업로드

  - 동일한 파일명으로 업로드 되는 경우 앞의 파일 덮어쓰게 되는 문제
  - 파일명이 중복되지 않도록 파일명을 변경해서 업로드
  - UUID : 식별자 표준
    - 16 옥텟(128비트)의 수
    - 총 36개의 문자 (32개 문자와 4개의 하이픈)
    - 8-4-4-4-12
    - 8e1a2153-edfa-436f-bd72-23b6b7e5cd6b\_원본파일명
    - 자바 UUID 클래스의 randomUUID() 메소드를 사용해서 유일한 식별자 생성

  1. 여러 개의 파일 업로드
  2. 파일명 변경하지 않고 파일 업로드

  파일 다운로드 예제

  - 폴더 내 모든 파일 목록 출력하고
  - 목록에서 파일 선택해서 다운로드
  - 파일명에 한글 들어 있는 경우 한글 출력 안 됨
    - 다운로드 컨트롤러에서 인코딩

<aside>
🚧 <c:url 사용시> jsessionid 붙는 이유
- 처음 접속 시 cooke 사용하지 못하는 경우를 위해 자동으로 붙여준다.
- 경로를 못 차즌 경우 발생
- jsessionid 제거 [application.properties](http://application.properties) 파일에서 설정

```java
server.servlet.session.tracking-modes=cookie
```

</aside>

### index.jsp 분할 : top/bottom/index

- top.jsp

  - <head>

  - <header>

  - <nav>

- bottom.jsp

  - <footer>

- index.jsp

  - **<div id="wrap">**
    - **<section></section>**

</div>

- index.jsp에 top과 bottom include 시키는 방법
  - **(1) <jsp:include>**
  - **(2) <c:import>**

# 로그인 처리

## 쿠키와 세션

- 클라이언트와 서버 간에 정보를 교환하는데
- 클라이언트 PC 또는 서버의 메모리에 저장해두고 사용하면
- 프로그램 속도를 향상시킬 수 있음

## 웹페이지를 연결하기 위한 방법 요약

- 페이지간에 정보를 교환하거나 데이터를 공유하기 위한 방법

### 1) <input type="hidden"> 태그 사용

- 현재 페이지에 데이터를 숨겨놓고
- 연결된 다음 페이지로 데이터를 보내는 방법
- 두 웹페이지가 데이터를 공유

### 2) URL Rewriting

- Get 방식으로 전송할 때 데이터가 URL enldp qnxjdtj
- 다음 페이지로 전송

### 3) 쿠키

- 클라이언트의 PC의 Cookie 파일에 정보를 저장한 후 웹페이지가 공유

### 4) 세션

- 서버 메모리에 정보를 저장한 후 웹 페이지 공유

## 쿠키 (Cookie)

- 서버 측에서 클라이언트 측에 상태 정보를 저장하고 추출하기 위한 매커니즘
- 서버에서 생성하여, 클라이언트 측에 저장됨
- 서버에 요청할 때마다 쿠키의 속성값을 참조하거나 변경
- 크기는 4kb로 용량제한
- 클라이언트에 저장되므로 보안상의 문제 발생
- 따라서 민감한 정보는 쿠키 내에 저장하지 않음
- 쿠키는 사용자가 거부할 수 있으며 256문자 이하의 text 데이터만 저장

## 세션 (Session) ⭐

- 클라이언트와 웹 서버간에 네트워크로 연결이 지속적으로 유지되고 있는 상태

- 쿠키와 마찬가지로 서버와의 관계를 유지하기 위한 수단

- 쿠키와 달리 클라이언트에 저장되는 것이 아니라 서버 상에 객체로 존재

- 따라서 세션은 서버에서만 접근이 가능하여 보안이 좋음

- 서버에서 사용자의 정보를 유지 관리하는데 사용

- 사용자 인증 후 여러 페이지에 걸쳐 정보를 공유해서 사용할 수 있도록 해 줌

- 객체형을 포함한 거의 모든 형태의 데이터 저장도 가능

- Session은 서버측에서만 설정이 가능

  ```java
  HttpSession session;
  ```

- 세션은 브라우저 당 한개씩 생성

### 세션 ID

- 클라이언트가 처음 접속하면 서버(컨테이너)로부터 유일한 ID를 부여받게 되는데 이를 세션 ID라고 한다.
- 클라이언트가 재 접속했을 때 클라이언트 구분하기 위한 수단

### 세션 관련 메소드

- setAttribute(이름, 값) : 세션 이름과 값 설정
  - session.setAttribute(”sid”,memId);
- getAttribute(이름) : 이름에 해당되는 값 반환
- invalidate() : 실행중인 세션 종료. 모든 데이터 삭제
  - 로그아웃 시 사용
- 세션 설정
  - 컨트롤러에서 session.setAttribute(”sid”, memId);
- 세션 값 알아오기
  - JSP 페이지에서 ${sessionScope.sid}
- 세션 종료 (무효화)

  - session.invalidate()
  - 웹브라우저 종료
  - 또는 설정된 유효 기간이 만료되면 종료

- 로그인 예제
  - new 스키마 : projectdb
  - create member table
  - create package
    - controller / dao / service / model
  - create member class & interface file
    - MemberVO
    - IMemberDAO
    - IMemberService / MemberService
    - MemberController
