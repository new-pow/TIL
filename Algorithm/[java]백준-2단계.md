# 백준 알고리즘 2단계 조건문
> 매일 1시간씩 문제 푸는 감각 키우기

[백준 알고리즘 2단계](https://www.acmicpc.net/step/4)

- 주의
    - main 클래스 생략
    - import 생략
    - `scanner` 객체 `sc`로 사용

## 1330 두 수 비교하기
> 22/6/22

- 두 정수 A와 B가 주어졌을 때, A와 B를 비교하는 프로그램을 작성하시오.

```java
// 정수 받아오기
int a = sc.nextInt();
int b = sc.nextInt();

// 조건문 + 출력
if (a>b) System.out.println(">");
else if (a<b) System.out.println("<");
else System.out.println("==");
```

## 9498 시험성적
> 22/6/22

- 시험 점수를 입력받아 90 ~ 100점은 A, 80 ~ 89점은 B, 70 ~ 79점은 C, 60 ~ 69점은 D, 나머지 점수는 F를 출력하는 프로그램을 작성하시오.

```java
// 점수 입력
int score = sc.nextInt();

// 성적 출력
if(score<=100 && score>=90) System.out.println("A");
else if (score>=80) System.out.println("B");
else if (score>=70) System.out.println("C");
else if (score>=60) System.out.println("D");
else System.out.println("F");
```

## 2753 윤년
> 22/06/22

- 연도가 주어졌을 때, 윤년이면 1, 아니면 0을 출력하는 프로그램을 작성하시오.

```java
// 연도 받아오기
int year = sc.nextInt();

// 윤년 계산
if (year%4==0 && year%100!=0) {
    System.out.println(1);
} else if (year%400==0) {
    System.out.println(1);
} else {System.out.println(0);}
```

## 14681 사분면 고르기
> 22/06/22

- 점 (x, y)의 사분면 번호(1, 2, 3, 4 중 하나)를 출력한다.

```java
// 좌표 입력 받기
int x=sc.nextInt();
int y=sc.nextInt();

// 사분면 위치 찾기
// 문제에는 나오지 않았지만, (0,0) 위치에 있을 경우 0으로 출력하는 것도 추가하였다.
if (x>0 && y>0) System.out.println(1);
else if (x<0 && y>0) System.out.println(2);
else if (x<0 && y<0) System.out.println(3);
else if (x>0 && y<0) System.out.println(4);
else {0}
```

## 2884 알람시계
> 22/06/22

- 첫째 줄에 상근이가 창영이의 방법을 사용할 때, 설정해야 하는 알람 시간을 출력한다. (입력과 같은 형태로 출력하면 된다.)

```java
// 일어나야 할 시간 입력받기
int hour = sc.nextInt();
int min = sc.nextInt();

// 분 계산을 기준으로, 시간 단위가 바뀔때에 대해서 구분
// 23시~0시 경계는 중첩 if문으로 처리
if (min>=45) { min = min-45;}
else if (min<45) {
    hour--;
    min = min+15;
    if (hour<0) { hour=23;};
}

// 출력
System.out.println(hour+" "+min);
```

## 2525 오븐시계
> 22/06/22

- 훈제오리구이를 시작하는 시각과 오븐구이를 하는 데 필요한 시간이 분단위로 주어졌을 때, 오븐구이가 끝나는 시각을 계산하는 프로그램을 작성하시오.

```java
// 현재 시간 입력
int hour = sc.nextInt();
int min = sc.nextInt();
// 요리 시간 입력
int cookTime = sc.nextInt();

// 시간계산 . 2884 문제와 원리는 같다.
// 다만 요리시간이 가변적이라 극단적인(1000분..) 경우 등도 생각해야 했다.
if (min+cookTime < 60) {
    min += cookTime;
} else if (min+cookTime >= 60) {
    hour += (min+cookTime)/60;
    min = (min+cookTime)%60;
}

// 24시간이 넘어가는 경우 처리
if (hour>=24) hour-=24;

// 출력
System.out.println(hour+" "+min);
```

## 2480 주사위 세 개
> 22/6/23

- 주사위 3개를 굴린 후, 상금을 계산하시오.

```java
int dice1 = sc.nextInt();
int dice2 = sc.nextInt();
int dice3 = sc.nextInt();
int price = 0;

if (dice1==dice2 && dice2==dice3) {
    // 눈 3개가 동일 상금 계산
    price = 10000 + (dice1*1000);
} else if (dice1==dice2 || dice2==dice3) {
    // 눈 2개가 동일 case1 상금 계산
    price = 1000 + dice2*100;
} else if (dice1==dice3) {
    // 눈 2개가 동일 case2 상금 계산
    price = 1000 + dice1*100;
} else {
    // 눈 3개가 모두 다를 때, 최대 눈금을 확인하고, 상금 계산
    price = Math.max(Math.max(dice1, dice2),Math.max(dice2, dice3))*100;
}

// 출력
System.out.println(price);
```