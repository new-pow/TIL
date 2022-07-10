# JSTL (JSP Standard Tag Library)

## JSTL 이란?

- JSP 표준 태그 라이브러리
- JSP와 HTML을 같이 사용함으로써 가독성이 떨어지는 것을 보완하고자 만들어진 태그 라이브러리
- JSP 페이지 내에서 자바 코드를 사용하지 않고 태그를 사용하도록 하였다.
- JSP 페이지의 로직을 담당하는 부분인 제어문 및 데이터베이스 처리 등을 표준 커스텀 태그 제공
- 사용하기 위해서는 별도의 라이브러리가 필요하다.

```html
<!-- 라이브러리 예시 -->
<%@ taglib uri="..." prefix="" %>
```

## 장점

- 빠름
  - JSP를 단순화하여 빠르게 개발 가능
- 코드 재사용성
  - 다양한 페이지에서 JSTL 태그 사용 가능
- 스크립틀릿 태그를 사용할 필요가 없음

## JSTL 다운로드 하는 방법

- 다운로드 링크 : https://tomcat.apache.org
- Taglibs
- 파일 4개 다운로드
- apache-tomcat-9.0.64\lib 폴더에 저장
- 이클립스 종료했다가 새로 열기

## JSTL 라이브러리

> 5개의 라이브러리로 구성

| 라이브러리              | Prefix | 설명                                      |
| ----------------------- | ------ | ----------------------------------------- |
| [core](jstl_c.md)       | c      | 변수, 제어문, URL 등 처리                 |
| [format](jstl_fmt.md)   | fmt    | 숫자, 날짜, 시간지정, 국제화, 다국어 처리 |
| [sql](jstl_sql.md)      | sql    | 데이터베이스 작업 처리                    |
| [xml](jstl_x.md)        | x      | xml 문서 처리                             |
| [functions](jstl_fn.md) | fn     | 함수 기능                                 |

---

# 참고

- [JSTL (JSP Standard Tag Library) (2020)](https://velog.io/@ye050425/JSP-JSTL-%EC%A0%95%EB%A6%AC)
