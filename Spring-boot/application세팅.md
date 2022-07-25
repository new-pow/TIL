# Spring boot

## application.properties 세팅

```
# portNum
server.port=8080

# auto refresh
server.servlet.session.tracking-modes=cookie

# jsp view
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp

# db connection
# caution!! schema name!!
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/스키마명
spring.datasource.username=root
spring.datasource.password=비밀번호 입력

# xml location
mybatis.mapper-locations=classpath:mappers/**/*.xml

# file upload size
spring.servlet.multipart.max-file-size = 50MB


```
