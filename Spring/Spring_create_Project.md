# πΒ μ€νλ§ λΆνΈ Spring Boot

- μ€νλ§ νλ μμν¬λ₯Ό μ¬μ©νλ νλ‘μ νΈλ₯Ό μμ£Ό κ°νΈνκ² μ€μ ν  μ μλ μ€νλ§ νλ μμν¬μ μλΈνλ‘μ νΈ

## μ€νλ§ λΆνΈμ νΉμ§

- XML κΈ°λ° μ€μ  κ³Όμ  μμ΄ κ°λ¨ν νλ‘μ νΈλ₯Ό μμν  μ μλ€.
  - μμ°μ€λ½κ² μμ±μ΄ λλ€.
- λ©μ΄λΈμ pom.xml νμΌμ μμ‘΄μ± λΌμ΄λΈλ¬λ¦¬ λ²μ μ μΌμΌμ΄ μ§μ νμ§ μμλ λλ€.
  - μ€νλ§ λΆνΈκ° κΆμ₯ λ²μ  κ΄λ¦¬
- λ¨λ μ€νλλ μ€νλ§ μ νλ¦¬μΌμ΄μ κ΅¬ν κ°λ₯
- νλ‘μ νΈ νκ²½ κ΅¬μΆμ νμν μλ² μΈμ μΈ ν΄λ€μ΄ λ΄μ₯λμ΄ μμ΄ λ³λ μ€μΉ νμ μμ
  - ν°μΊ£ λ΄μ₯λμ΄ μλ€.

## **β¨Β μ€νλ§ λΆνΈ μμ± κ°μ**

### 1. μ€νλ§ λΆνΈ νλ‘μ νΈ μμ±

- νλ‘μ νΈλͺ / Group / Artifact / pac
- Dependencies μ ν
  1. SQL : JDBC API, MyBatis Framework / MySQL Driver
  2. Web : Spring Web

### 2. νλ‘μ νΈ μμ± ν νμΈ

1. **pom.xml λ΄μ© νμΈ**
   - java.version
   - jdbc
   - mysql-connector
   - tomcat
2. **μλ μμ±λ ν΄λμ€ νμΌ νμΈ**
   - ServletInitializer.java
     - μ€νλ§ λΆνΈ μ νλ¦¬μΌμ΄μμ web.xml μμ΄ ν°μΊ£μμ μ€ννκ² ν΄μ£Όλ ν΄λμ€
     - λ°λΌμ μ€νλ§ λΆνΈμλ web.xml, context.xml μ€μ  νμΌ μμ
   - (projectname)\_Application.java
     - @SpringBootApplication λΆμ΄μμ
       - μ€νλ§ λΆνΈ μ νλ¦¬μΌμ΄μμΌλ‘ μ€μ νλ μ΄λΈνμ΄μ
     - main() λ©μλ ν¬ν¨
       - μ€νλ§ λΆνΈ μμ± μ μλμΌλ‘ μμ±
       - μ€νλ§ λΆνΈ νλ‘μ νΈμλ λ°λμ main() μ΄ μμ΄μΌ ν¨
       - μ€νλ§ λΆνΈ νλ‘μ νΈ main() λ©μλλ₯Ό μμμ μΌλ‘ μ€ν
       - main() λ©μλλ₯Ό ν¬ν¨νλ java νμΌμ΄ νμ
       - μ΄μ  : μ€νλ§ λΆνΈ μΉ μ νλ¦¬μΌμ΄μμ μΌλ° μλ° μ νλ¦¬μΌμ΄μμ²λΌ κ°λ°νλ €λ μλ

### 3. μ€νλ§ μ€μ  νμΌ

- application.properties : νμΌ μλ μμ±
- λ΄μ©μ΄ μλ λΉ νμΌλ‘ μμ±
- μΆκ°ν  λ΄μ©
  - ν¬νΈ λ²νΈ
  - λ°μ΄ν°λ² μ΄μ€ μ°κ²° μ λ³΄
  - mapper.xml μμΉ μ§μ 
    - src/main/resources νμΌμ μμ±ν  κ²
- μ¬κΈ°μ Controller μΆκ°νκ³  (β/β λ§€ν) μ€νμμΌμ μ€λ₯ μλμ§ νμΈ
- μ€λ₯ μμΌλ©΄ λ€μ μ€ν go

### 4. JSP λ·° μ€μ 

- μ€νλ§ λΆνΈλ JSP λ·°κ° κΈ°λ³Έμ΄ μλκΈ° λλ¬Έμ JSP λ·°λ₯Ό μ¬μ©ν  κ²½μ° μΆκ° μ€μ  νμ
  - application.properties νμΌμ JSP μ€μ  μΆκ°
  - pom.xml μμ‘΄μ± λΌμ΄λΈλ¬λ¦¬ μΆκ°
  - src/main/webapp ν΄λμ WEB-INF/views ν΄λ μΆκ°
  - hello.jsp μμ±νκ³ 
  - μ»¨νΈλ‘€λ¬μμ @RequestMapping μΆκ°ν΄μ hello.jsp μ€νλλμ§ νμΈ
  - μ€νλ§ λΆνΈμμ λ¦¬μμ€ νμΌ κ²½λ‘ νμΈ

### 5. DB μ°λ CRUD κΈ°λ₯ κ΅¬ν

- spring_mvc_mybatis μμ product μ½λλ κ·Έλλ‘ μ¬μ© (μΌλΆ κ²½λ‘ μμ )
- νμΌ μμΉ μ£Όμ

# π¨Β μ€νλ§ λΆνΈ νλ‘μ νΈ μμ±

## 1. μ€νλ§λΆνΈ νλ‘μ νΈ μμ±

### **νλ‘μ νΈλͺ / Group / Artifact / ν¨ν€μ§λͺ**

- File - New - Spring Starter Project
- νλ‘μ νΈλͺ (Name) : spring_boot_mybatis
- Type : Maven Project War
- Java Version : 11
- Group : com.spring_boot_mybatis
- Artifact : project
- ν¨ν€μ§λͺ (Package)
  - com.spring_boot_mybatis.project

### Dependencies μ ν

- SQL : JDBC API / MyBatis Framework / MySQL Driver
- Web : Spring Web

## 2. νλ‘μ νΈ μμ± ν νμΈ

1. pom.xml λ΄μ© νμΈ

- java.version / jdbc / mysql-connector / tomcat

1. μλ μμ±λ ν΄λμ€ νμΌ νμΈ

- ServletIn**i**tializer.java
  - μ€νλ§ λΆνΈ μ νλ¦¬μΌμ΄μμ web.xml μμ΄ ν°μΊ£μμ μ€ννκ² ν΄μ£Όλ ν΄λμ€
  - λ°λΌμ μ€νλ§ λΆνΈμλ web.xml, context.xml μ€μ  νμΌ μμ
- β¦β¦.Application.java
  - @SpringBootApplication λΆμ΄ μμ
    - μ€νλ§ λΆνΈ μ νλ¦¬μΌμ΄μμΌλ‘ μ€μ νλ μ΄λΈνμ΄μ
  - main() λ©μλ ν¬ν¨
    - μ€νλ§ λΆνΈ μμ± μ μλμΌλ‘ μμ±
    - μ€νλ§ λΆνΈ νλ‘μ νΈμλ λ°λμ main()μ΄ μμ΄μΌ ν¨
    - μ€νλ§ λΆνΈ νλ‘μ νΈ main() λ©μλλ₯Ό μμμ μΌλ‘ μ€ν
    - main() λ©μλλ₯Ό ν¬ν¨νλ java νμΌμ΄ μμ΄μΌ ν¨
    - μ΄μ  : μ€νλ§ λΆνΈ μΉ μ νλ¦¬μΌμ΄μμ μΌλ° μλ° μ νλ¦¬μΌμ΄μμ²λΌ κ°λ°νλ €λ μλ λλ¬Έ

## 3. μ€νλ§ μ€μ  νμΌ

### application.properties : νμΌ μλ μμ±

- λ΄μ©μ΄ μλ λΉ νμΌλ‘ μμ±
- src/main/resourcesμ μμΉ

### μΆκ°ν  λ΄μ© : ν¬νΈλ²νΈ, λ°μ΄ν°λ² μ΄μ€ μ°κ²° μ λ³΄, mapper.xml μμΉ μ§μ 

- ν¬νΈ λ²νΈ : server.port=8080

- λ°μ΄ν°λ² μ΄μ€ μ°κ²° μ λ³΄

  - spring.datasource.driver-class-name=
  - spring.datasource.url=
  - spring.datasource.username=
  - spring.datasource.password=

- mapper.xml μμΉ μ§μ 

  - src/main/resources νμΌμ μμ±ν  κ²
  - DAOμ mapper νμΌ μΆκ°ν νμ μ€μ ν  κ²μ

- μ¬κΈ°μ Controller μΆκ°νκ³  (β/β λ§€ν) μ€νμμΌμ μ€λ₯ μλμ§ νμΈ

  - HelloController ν΄λμ€ μΆκ°

    - μμ²­ url : β/β

      - http://localhost:8080

      ```java
      @Controller
      public class HelloController {

      	// test print
      	@ResponseBody
      	@RequestMapping("/")	// μμ²­ url: http:localhost:8080
      	public String home() {
      		System.out.println("Hello Boot!");
      		return "Hello Boot!";	// jsp νμ΄μ§ μλ§λ€κ³ , μ λ¬Έμμ μΆλ ₯
      	}
      }
      ```

  - μ€ν : Run As / Spring Boot App

    - μΉλΈλΌμ°μ μ url μ§μ  μλ ₯ : http://localhost:8080

<aside>
π **BUG : μμ μ μ λ°λμ μλ² μ€λ¨νκ³  μ€ννκΈ°**

```java
Description:

Web server failed to start. Port 8080 was already in use.

Action:

Identify and stop the process that's listening on port 8080 or configure this application to listen on another port.
```

</aside>

- μ€λ₯κ° μμ λ

  ![Untitled](13%20SpringBoot%2001%208c8a196bfb2a4b8bb6e3f353f601bfd7/Untitled.png)

- μ΄μ  μΉλΈλΌμ°μ μμ νμΈνκΈ°

  ![Untitled](13%20SpringBoot%2001%208c8a196bfb2a4b8bb6e3f353f601bfd7/Untitled%201.png)

## 4. JSP μ€μ 

### application.properties νμΌμ JSP μ€μ  μΆκ°

```java
# jsp view
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp
```

### pom.xml μμ‘΄μ± λΌμ΄λΈλ¬λ¦¬ μΆκ°

- jstl (java.servlet jstl)
- tomcat (org.apache.tomcat.embed tomcat.embeded jasper)

### src/main/webapp ν΄λμ WEB-INF/views ν΄λ μΆκ°

- hello.jsp μμ±νκ³ 
- μ»¨νΈλ‘€λ¬μμ @RequestMapping μΆκ°ν΄μ hello.jsp μ€νλλμ§ νμΈ
- μ€νλ§ λΆνΈμμ λ¦¬μμ€ νμΌ κ²½λ‘ νμΈ : μ΄λ―Έμ§ μΆλ ₯

  - λ¦¬μμ€ νμΌ κ²½λ‘ src/main/resources/static ν΄λκ° κΈ°λ³Έ μμΉ
  - static ν΄λ μμ image ν΄λ μμ±νκ³ 
    - apple.png

- μ€νλ§ λΆνΈ νλ‘μ νΈ μμ± μ°μ΅λ¬Έμ 
  - spring_boot_mybatis2
  - hello.jspκΉμ§ μΆλ ₯

## 5. DB μ°λ CRUD κΈ°λ₯ κ΅¬ν

- spring_mvc_mybatis μμ product μ½λλ κ·Έλλ‘ μ¬μ© (μΌλΆ κ²½λ‘ μμ )
- νμΌ μμΉ μ£Όμ

### (1) ν¨ν€μ§ μμ±

- controller / dao / model / service
- ν΄λμ€ / μΈν°νμ΄μ€ νμΌ (mapper μ μΈ)
  - VO / service / DAO / Controller
- λ³΅μ¬ μ μ£Όμ! - μ΄μ  ν¨ν€μ§ import μ­μ ν  κ²

### (2) mapper νμΌ ν΄λ μμ±

- src/main/resources ν΄λμ mappers ν΄λ μμ±νκ³ , κ·Έ μμ product ν΄λ μμ±
- product ν΄λ μμ ProductMapper.xml νμΌ λ³΅μ¬
- application.propertiesμ mapper μμΉ μ€μ 

### (3) β¦Application.java ν΄λμ€μ μΆκ°

- μ»΄ν¬λνΈ Controllerμ Service ν΄λμ€μ λν΄ μΆκ°
  - @ComponentScan
  - @MapperScan
- DAO, Service, Controller λ§λ€ λͺ¨λ μΆκ°ν΄ μ£Όμ΄μΌ νλ€.
  - μΆκ°νμ§ μμΌλ©΄ beanμ΄ μλ€λ μ€λ₯ λ°μ

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
// μ€μμ λ
@SpringBootApplication
@ComponentScan(basePackages= {"com.spring_boot_mybatis.book"})
@MapperScan(basePackageClasses=IBookDAO.class)
public class SpringBootMybatisBookApplication {

	public static void main(String[] args) {
		SpringApplication.run(SpringBootMybatisBookApplication.class, args);
	}

}
```

### (4) view νμ΄μ§ λ³΅μ¬

-
- product ν΄λ λ³΅μ¬
- index.jsp λ³΅μ¬

### **(5) HelloController νμ μμ (μ­μ  λλ λ΄μ© μ£Όμ μ²λ¦¬)**

### **(6) js ν΄λ μμ±**

- **src/main/resources/static ν΄λμ js ν΄λ λ³΅μ¬**

### **(7) μΈλΆ κ²½λ‘ μ€μ  : μν μ΄λ―Έμ§ μΆλ ₯**

- WebConfig ν΄λμ€ μμ± (WebMvcConfigurer μΈν°νμ΄μ€ κ΅¬ν)
  - MVC νλ‘μ νΈμμ spring-context.xmlμ μ€μ ν λ΄μ© μΆκ°
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

- μ€νλ§ λΆνΈ νλ‘μ νΈ μ°μ΅λ¬Έμ 
  - λμκ΄λ¦¬ νλ‘κ·Έλ¨ μμ±
    - spring_boot_mybatis_book
  - CRUD κΈ°λ₯ κ΅¬ν
  - μ€λ³΅ μ²΄ν¬, κ²μ, μΈλΆ νμΌ κ²½λ‘ μ€μ  (μ΄λ―Έμ§ μΆλ ₯)

# μ€νλ§ λΆνΈ νλ‘μ νΈμ νμΌ μλ‘λ

- MultipartFile ν΄λμ€ μ¬μ©

  - μ€νλ§ λΆνΈμμλ μμ‘΄μ± λΌμ΄λΈλ¬λ¦¬ μΆκ° νμ μμ
  - μλμΌλ‘ MultipartConfigElement ν΄λμ€λ₯Ό λΉμΌλ‘ λ±λ‘

- HTML

  - <form enctype=βmultipart/form-dataβ>

  - <input type="file">

- μλ‘λλλ νμΌ ν¬κΈ° μ ν λ³κ²½ κ°λ₯

  - maxFileSize
    - μλ‘λνλ νμΌ 1κ°μ ν¬κΈ° : λν΄νΈ 1M
  - maxRequestSize
    - μμ²­ ν¬κΈ° μ ν
    - λͺ¨λ  νμΌμ ν¬κΈ°λ₯Ό ν©ν ν¬κΈ° κ° μ ν

- νμΌ μλ‘λ μμ 

  1. νμΌλͺμ΄ μ€λ³΅λμ§ μκ² ν΄μ μλ‘λ

  - λμΌν νμΌλͺμΌλ‘ μλ‘λ λλ κ²½μ° μμ νμΌ λ?μ΄μ°κ² λλ λ¬Έμ 
  - νμΌλͺμ΄ μ€λ³΅λμ§ μλλ‘ νμΌλͺμ λ³κ²½ν΄μ μλ‘λ
  - UUID : μλ³μ νμ€
    - 16 μ₯ν(128λΉνΈ)μ μ
    - μ΄ 36κ°μ λ¬Έμ (32κ° λ¬Έμμ 4κ°μ νμ΄ν)
    - 8-4-4-4-12
    - 8e1a2153-edfa-436f-bd72-23b6b7e5cd6b\_μλ³ΈνμΌλͺ
    - μλ° UUID ν΄λμ€μ randomUUID() λ©μλλ₯Ό μ¬μ©ν΄μ μ μΌν μλ³μ μμ±

  1. μ¬λ¬ κ°μ νμΌ μλ‘λ
  2. νμΌλͺ λ³κ²½νμ§ μκ³  νμΌ μλ‘λ

  νμΌ λ€μ΄λ‘λ μμ 

  - ν΄λ λ΄ λͺ¨λ  νμΌ λͺ©λ‘ μΆλ ₯νκ³ 
  - λͺ©λ‘μμ νμΌ μ νν΄μ λ€μ΄λ‘λ
  - νμΌλͺμ νκΈ λ€μ΄ μλ κ²½μ° νκΈ μΆλ ₯ μ λ¨
    - λ€μ΄λ‘λ μ»¨νΈλ‘€λ¬μμ μΈμ½λ©

<aside>
π§ <c:url μ¬μ©μ> jsessionid λΆλ μ΄μ 
- μ²μ μ μ μ cooke μ¬μ©νμ§ λͺ»νλ κ²½μ°λ₯Ό μν΄ μλμΌλ‘ λΆμ¬μ€λ€.
- κ²½λ‘λ₯Ό λͺ» μ°¨μ¦ κ²½μ° λ°μ
- jsessionid μ κ±° [application.properties](http://application.properties) νμΌμμ μ€μ 

```java
server.servlet.session.tracking-modes=cookie
```

</aside>

### index.jsp λΆν  : top/bottom/index

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

- index.jspμ topκ³Ό bottom include μν€λ λ°©λ²
  - **(1) <jsp:include>**
  - **(2) <c:import>**

# λ‘κ·ΈμΈ μ²λ¦¬

## μΏ ν€μ μΈμ

- ν΄λΌμ΄μΈνΈμ μλ² κ°μ μ λ³΄λ₯Ό κ΅ννλλ°
- ν΄λΌμ΄μΈνΈ PC λλ μλ²μ λ©λͺ¨λ¦¬μ μ μ₯ν΄λκ³  μ¬μ©νλ©΄
- νλ‘κ·Έλ¨ μλλ₯Ό ν₯μμν¬ μ μμ

## μΉνμ΄μ§λ₯Ό μ°κ²°νκΈ° μν λ°©λ² μμ½

- νμ΄μ§κ°μ μ λ³΄λ₯Ό κ΅ννκ±°λ λ°μ΄ν°λ₯Ό κ³΅μ νκΈ° μν λ°©λ²

### 1) <input type="hidden"> νκ·Έ μ¬μ©

- νμ¬ νμ΄μ§μ λ°μ΄ν°λ₯Ό μ¨κ²¨λκ³ 
- μ°κ²°λ λ€μ νμ΄μ§λ‘ λ°μ΄ν°λ₯Ό λ³΄λ΄λ λ°©λ²
- λ μΉνμ΄μ§κ° λ°μ΄ν°λ₯Ό κ³΅μ 

### 2) URL Rewriting

- Get λ°©μμΌλ‘ μ μ‘ν  λ λ°μ΄ν°κ° URL enldp qnxjdtj
- λ€μ νμ΄μ§λ‘ μ μ‘

### 3) μΏ ν€

- ν΄λΌμ΄μΈνΈμ PCμ Cookie νμΌμ μ λ³΄λ₯Ό μ μ₯ν ν μΉνμ΄μ§κ° κ³΅μ 

### 4) μΈμ

- μλ² λ©λͺ¨λ¦¬μ μ λ³΄λ₯Ό μ μ₯ν ν μΉ νμ΄μ§ κ³΅μ 

## μΏ ν€ (Cookie)

- μλ² μΈ‘μμ ν΄λΌμ΄μΈνΈ μΈ‘μ μν μ λ³΄λ₯Ό μ μ₯νκ³  μΆμΆνκΈ° μν λ§€μ»€λμ¦
- μλ²μμ μμ±νμ¬, ν΄λΌμ΄μΈνΈ μΈ‘μ μ μ₯λ¨
- μλ²μ μμ²­ν  λλ§λ€ μΏ ν€μ μμ±κ°μ μ°Έμ‘°νκ±°λ λ³κ²½
- ν¬κΈ°λ 4kbλ‘ μ©λμ ν
- ν΄λΌμ΄μΈνΈμ μ μ₯λλ―λ‘ λ³΄μμμ λ¬Έμ  λ°μ
- λ°λΌμ λ―Όκ°ν μ λ³΄λ μΏ ν€ λ΄μ μ μ₯νμ§ μμ
- μΏ ν€λ μ¬μ©μκ° κ±°λΆν  μ μμΌλ©° 256λ¬Έμ μ΄νμ text λ°μ΄ν°λ§ μ μ₯

## μΈμ (Session) β­

- ν΄λΌμ΄μΈνΈμ μΉ μλ²κ°μ λ€νΈμν¬λ‘ μ°κ²°μ΄ μ§μμ μΌλ‘ μ μ§λκ³  μλ μν

- μΏ ν€μ λ§μ°¬κ°μ§λ‘ μλ²μμ κ΄κ³λ₯Ό μ μ§νκΈ° μν μλ¨

- μΏ ν€μ λ¬λ¦¬ ν΄λΌμ΄μΈνΈμ μ μ₯λλ κ²μ΄ μλλΌ μλ² μμ κ°μ²΄λ‘ μ‘΄μ¬

- λ°λΌμ μΈμμ μλ²μμλ§ μ κ·Όμ΄ κ°λ₯νμ¬ λ³΄μμ΄ μ’μ

- μλ²μμ μ¬μ©μμ μ λ³΄λ₯Ό μ μ§ κ΄λ¦¬νλλ° μ¬μ©

- μ¬μ©μ μΈμ¦ ν μ¬λ¬ νμ΄μ§μ κ±Έμ³ μ λ³΄λ₯Ό κ³΅μ ν΄μ μ¬μ©ν  μ μλλ‘ ν΄ μ€

- κ°μ²΄νμ ν¬ν¨ν κ±°μ λͺ¨λ  ννμ λ°μ΄ν° μ μ₯λ κ°λ₯

- Sessionμ μλ²μΈ‘μμλ§ μ€μ μ΄ κ°λ₯

  ```java
  HttpSession session;
  ```

- μΈμμ λΈλΌμ°μ  λΉ νκ°μ© μμ±

### μΈμ ID

- ν΄λΌμ΄μΈνΈκ° μ²μ μ μνλ©΄ μλ²(μ»¨νμ΄λ)λ‘λΆν° μ μΌν IDλ₯Ό λΆμ¬λ°κ² λλλ° μ΄λ₯Ό μΈμ IDλΌκ³  νλ€.
- ν΄λΌμ΄μΈνΈκ° μ¬ μ μνμ λ ν΄λΌμ΄μΈνΈ κ΅¬λΆνκΈ° μν μλ¨

### μΈμ κ΄λ ¨ λ©μλ

- setAttribute(μ΄λ¦, κ°) : μΈμ μ΄λ¦κ³Ό κ° μ€μ 
  - session.setAttribute(βsidβ,memId);
- getAttribute(μ΄λ¦) : μ΄λ¦μ ν΄λΉλλ κ° λ°ν
- invalidate() : μ€νμ€μΈ μΈμ μ’λ£. λͺ¨λ  λ°μ΄ν° μ­μ 
  - λ‘κ·Έμμ μ μ¬μ©
- μΈμ μ€μ 
  - μ»¨νΈλ‘€λ¬μμ session.setAttribute(βsidβ, memId);
- μΈμ κ° μμμ€κΈ°
  - JSP νμ΄μ§μμ ${sessionScope.sid}
- μΈμ μ’λ£ (λ¬΄ν¨ν)

  - session.invalidate()
  - μΉλΈλΌμ°μ  μ’λ£
  - λλ μ€μ λ μ ν¨ κΈ°κ°μ΄ λ§λ£λλ©΄ μ’λ£

- λ‘κ·ΈμΈ μμ 
  - new μ€ν€λ§ : projectdb
  - create member table
  - create package
    - controller / dao / service / model
  - create member class & interface file
    - MemberVO
    - IMemberDAO
    - IMemberService / MemberService
    - MemberController
