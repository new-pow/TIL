# 백준 알고리즘 3단계 반복문
> 매일 1시간씩 문제 푸는 감각 키우기

[백준 알고리즘 2단계](https://www.acmicpc.net/step/4)

- 주의
    - main 클래스 생략
    - import 생략
    - `scanner` 객체 `sc`로 사용



## 2739 구구단 출력
> 22/6/23

- 단 수를 입력받아 해당 단의 구구단을 출력하시오.

```java
// 단 입력
int num = sc.nextInt();

// 출력
for(int i=1; i<10; i++) {
    System.out.println(num+" * "+i+" = "+num*i);
}
```
