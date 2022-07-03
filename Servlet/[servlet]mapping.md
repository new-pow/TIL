# Servlet mapping 방법

## 1. XML이용한 서블릿매핑

> 서블릿 맵핑 이름을 다른 이름으로 추가 (변경의 의미)

1. `src/main/webapp/WEB-INF/web.xml` 열기
2. 하단(`</web-app>`보다 위)에 servlet 태그 추가
   - (1) `<servlet></servlet>`
   - (2) `<servlet-mapping>`
3. `web.xml` 내용 변경했으면 반드시 톰캣 서버 중단했다가 다시 실행

```html
<!-- (1) servlet 추가 -->
<servlet>
  <servlet-name>mySecond</servlet-name>
  <!-- Servlet 이름 -->
  <servlet-class>sec01.SecondServlet</servlet-class>
  <!-- Servlet 이름 -->
</servlet>

<!--  (2) servlet-mapping 추가 -->
<servlet-mapping>
  <servlet-name>mySecond</servlet-name>
  <!-- Servlet 이름 -->
  <url-pattern>/second</url-pattern>
  <!-- 맵핑이름 -->
</servlet-mapping>
```

## 2. 어노테이션을 이용한 서블릿 맵핑

- web.xml에서 여러 서블릿 맵핑 설정시 복잡
- 서블릿 클래스에서 직접 어노테이션으로 서블릿명을 설정하면 가독성도 좋고 편리하다
- @WebServlet을 이용하여 서블릿 맵핑 구현
- 어노테이션이 적용되는 클래스는 반드시 HttpServlet 클래스를 상속받아야 함

### 어노테이션 사용한 서블릿맵핑 예제

    1. 서블릿 생성 : AnnotationServlet.java
    2. 이름 바꾸기
        ```jsx
        // 변경 전
        @WebServlet("/AnnotationServlet")

        // 변경 후
        @WebServlet("/Annot2Servlet")
        ```

---

# 참조

- mlp 강의 정리
