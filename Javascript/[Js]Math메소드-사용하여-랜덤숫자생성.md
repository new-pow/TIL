# [Javascript] Math.random() 사용하여 1~n 랜덤 숫자 생성

## Math.random()
> Javascript의 내장 객체 중 하나로, 수학적 계산에 필요한 함수 또는 상수를 제공한다. Java에서도 똑같이 사용된다.

```
Math.random()
```

<br>

## 기능
- **0 이상 1 미만**의 부동소숫점 의사 난수를 반환한다.
- 0.345823 이런 식

<br>

## 사용
* 주로 난수에 숫자를 곱하여 랜덤 숫자를 생성하는 데 사용한다.

<br>

### 예시1 : 1~10 중 랜덤 숫자 생성
* 0~9까지 난수가 생성되므로 마지막에 `+1`을 붙여 사이값을 보정해준다.

```java
(Math.floor(Math.random())*10)+1
```

### 예시2 : 1~5 중 랜덤 숫자 생성

```java
(Math.floor(Math.random())*5)+1
```

### 예시3 : 1~n 중 랜덤 숫자 생성

```java
(Math.floor(Math.random())*n)+1
```