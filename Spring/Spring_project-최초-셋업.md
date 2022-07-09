# Spring project 생성시 환경설정

## 1. 프로젝트 생성

1. Select a wizard - Spring Legacy Project 선택
2. Templates - Spring MVC Project 선택

## 2. Java Compiler

-

## 3. Java Build Path

1. 프로젝트 Properties 👉 Java Build Path 👉 Libraries 탭
2. JRE System Library 클릭 👉 Edit... 클릭
3. 내 JDK 버전에 맞추어 선택
4. Apply

## 4. Project Facets

1. 프로젝트 Properties 👉 Project Facets 👉 Java Version
2. 내 Java 버전에 맞추어 선택
3. Runtimes 탭
4. tomcat 선택 (실행 서버)

## 5. pom.xml

1. java-version 👉 내 버전에 맞게 설정
2. springframework-version 👉 내 버전에 맞게 설정
3. Maven compiler 👉 내 버전에 맞게 설정

```
// 예시
Java Version : 11
Spring Framework : 5.2.22.RELEASE
Maven compiler : 1.8
```

## 그 외 확인 사항

### 전체 구조 파악

- src
  - /main
    - /java : 자바 코드 (Controller, model, Service)
    - /resources : 자바 코드에서 참조하는 리소스 파일들 (sqlMapConfig.xml ...)
    - /webapp : 웹 서비스 루트 디렉터리 (외부에서 접근 가능)
      - /resources : js, css, image 등의 웹 리소스 파일
      - /WEB-INF
        - /classes : 컴파일된 클래스
        - /spring : 스프링의 설정 파일 (root-context.xml, servlet-context.xml)
        - /views : html, jsp 페이지 (보안상 외부에서 접근 불가능. 컨트롤러를 경유해야만 접근 가능)
  - /test
    - /java
    - resources

### servlet-context.xml

- ViewResolver 확인

### web.xml

- DispatcherServlet
- 스프링 컨테이너 설정 파일 위치

### url 에서 context 명 확인

- 프로젝트에서 패키지명 : com.spring_mvc.project
- 나중에 url 명 : http://localhost:8080/project/
- `server.xml`에서 `<Context path=”/project” … />`

---

# 참조

- MLP Back-end Spring
