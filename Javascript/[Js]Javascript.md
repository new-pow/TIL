# 자바스크립트 Javascript
> 정식 명칭 ECMAScript. Ecma International이 ECMA-262 기술 규격에 따라 정의하고 있는 표준화된 스크립트 프로그래밍 언어

## 특징
- 동적인 웹페이즈를 작성하기 위해 사용하는 언어
- 웹의 표준 프로그램 언어로 모든 웹브라우저에서 자바스크립트를 지원한다.
- 전 세계적으로 가장 많이 사용하는 언어 1위
- 웹 브라우저 뿐 아니라, 스마트폰용 어플리케이션 개발 등 각종 분야에서 능력과 가치를 인정받고 있다.
- 초기에는 브라우저에 내장되어 제한된 기능만 지원하였으나, 현재 Ajax(Asynchronous Javascript and XML)라는 기술과 함께 영향력이 증가

## 기능
- HTML이 지원하지 못하는 다양한 기능 지원
    + 동적인 움직임
    + 이벤트 발생처리
    + 경고 메시지 출력
    + etc...
- Ajax를 이용하여 새로운 내용을 동적으로 로딩하거나, 서버에 전송하여 동적인 페이지 생성

## 실행형식
- 스크립트 언어이기 때문에 컴파일되지 않는다.
- 웹 브라우저에서 위에서 아래로 한 줄씩 바로 실행된다.
- 비동기식 처리

> 인터프리팅 언어(스크립트 언어란?
>> - 독자적으로 실행되지 않고, 다른 프로그램에 내장되어 사용된다.
>> - 소스코드를 컴파일 하지 않고, 한줄씩 인터프리터를 통해 바로 실행된다.

> 비동기식 처리란?
>> 서버 측에 데이터를 요청한 후에 데이터 수신이 완료될 때까지 기다리지 않고 다른 작업을 진행한다.

## 기본 구조 및 사용 방법
### Internal 방식
- HTML 문서 `<head>` 부분에 `<script>`, `</script>` 태그 삽입
```html
<script type = "text/javascript">
    // 소스 코드
</script>
```

### External 방식
- 대부분 이 방식을 사용함
- 별도의 자바스크립트 파일(~.js)로 작성하여, HTML 문서에서 소스 지정
```html
<script src="js/fileName.js"></script>
```

### Inline 방식
- 작성할 스크립트가 소량일 때 주로 사용
- HTML 태그의 이벤트 핸들러 속성을 이용하여 사용
```html
<body onLoad = "start()">
```
