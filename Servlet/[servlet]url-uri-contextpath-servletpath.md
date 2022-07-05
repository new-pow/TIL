# Servlet의 URL, URI, ContextPath, ServletPath 개념

- URL : 전체 주소
  - `http://localhost:8080/second`
  - 프토토콜(http://) + IP(localhost) + 포트번호(8080) + URI(second)
- URI : ContextPath + ServletPath
  - `/Servlet01/first`
  - 프로젝트명 + 서블릿 매핑 이름
- ContextPath : 프로젝트명
  - `/Servlet01`
- ServletPath
  - `/second`

## URI (Uniform Resource Identifier : 통합 자원 식별자)

- 특정 리소스를 구분하는 식별자
- 논리적 또는 물리적 리소스 (접근할 리소스 위치를 알 수 있다.)
- 인터넷, 모바일 기기 등 다양한 곳에서 사용

## URL (Uniform Resource Locator) : 웹주소

- 리소스 위치
- URI가 서브넷
