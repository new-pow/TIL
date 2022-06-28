# String 나눠 출력하기 : substring()

## 왜 필요했나?
데이터 처리상 편리를 위해 휴대폰 번호 등을 나눠서 input 받아도, DB에 저장할 때는 하나의 값으로 합쳐서 저장한다.
이를 반대로 출력하려면, '-'를 중간에 삽입하여 사용자가 보기 편한 방식으로 출력할 필요가 있었다.

## 형식
- 입력값
```java
String telno = "01012345678";
String result = "";

if(telno.length() == 10) {
  result = telno.subtsring(0,3) + "-" + telno.substring(3,6) + "-" + telno.substring(6,10);
} else if(telno.length() == 11) {
  result =telno.subtsring(0,3) + "-" + telno.substring(3,7) + "-" + telno.substring(7,11);
};

System.out.println(result);
```

- 출력값
```java
010-1234-5678
```

## 기타


---
# 참고
- [DB에 휴대폰번호가... (2020-07-30)](https://okky.kr/article/750950)