# Javascript 데이터 입력과 출력
- 목차
    1. 

## 데이터를 출력하는 기본 방법
### window.alert(*contents*);
- 출력 내용을 알림창(팝업 경고창)으로 출력하는 방법
- window 객체는 기본 객체이기 때문에 생략 가능하다.

```javascript
window.alert("hi");
alert("hi");
```

### console.log(*contents*);
- 출력 내용을 콘솔창에 출력

```javascript
console.log("hi");
```

### document.write(*contents*);
- HTML 문서에 내용 출력

```javascript
document.write("hi");
```

### DOM(문서 객체 모델) 사용
- 태그에 출력
- 최종적으로 주로 활용하게 될 방법

---

## javascript 코드 입력시 주의할 점
- 대소문자를 구별한다.
- 문장 끝에 세미콜론 ; 사용한다.
- 문자열에서 따옴표 겹침 오류를 주의한다.
    - 홑따옴표와 겉따옴표의 열고 닫음을 잘 챙겨주자
- 괄호 짝이 잘 맞아야 한다.

---

## 데이터 입력
### confirm()
- 자바스크립트 내장 함수
- 확인과 취소가 있는 대화상자를 출력한다.
- `확인` return true; `취소` return false;

### promp()
- 자바스크립트 내장 함수
- 사용자로부터 입력 받은 값을 반환한다.

```jsx
prompt(”출력 메세지”);
prompt(”출력 메세지”,”기본 메세지”);
```

### 주석문
- // 한줄주석
- /* 여러 줄 주석 */

### DOM
### <input> 태그와 value 속성