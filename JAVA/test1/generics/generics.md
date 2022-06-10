# 제네릭 / 제네릭 타입

- 클래스(인터페이스나 메소드를 타입파라미터를 이용하는 기법
- 클래스 설계시에 타입 <T>가 아직 결정되지 않음
- 총칭해서 제네릭 타입
- public class *class name<T> {}*

```java
class Gen<T> {
 private T value;
```

```java
Gen<String> gen = new gen<String();
```

```java
Gen<Integer> gen2 = new Gen<Integer>();
```

## <>

기본 데이터 타입은 올 수 없음

- <int> : X
- <Integer> : Wrapper 클래스 사용
    - 기본 데이터 타입에 대응되는 클래스
    - 기본 데이터 타입을 객체로 포장

## 제네릭 사용하는 코드의 이점

- 컴파일시 강한 타입 체크 가능
    - 실행 시 타입 에러가 나는 것 방지
    - 컴파일 시에 미리 타입을 강하게 체크해서 에러를 사전에 방지
- 강제 타입 변환 제거 가능 (프로그램 성능 향상)

```java
// 제네릭을 사용하지 않을 경우
List list = new ArrayList();
list.add(“hello”);
String str = (String) list.get(0); // 강제 타입 변환
Object -> String
```

```java
// 제네릭 사용할 경우
List<String> list = new ArrayList<String>();
list.add(“hello”);
String str = list.get(0);  // 강제 타입 변환 불필요
```

## 제네릭 정리

- 클래스나 인터페이스를 설계할 때
- 구체적인 타입을 명시하지 않고 타입 파라미터로 대체했다가
- 실제 클래스 사용될 때 구체적인 타입을 지정하여
- 타입 변환을 최소화시킴으로써 프로그램 성능을 향상시킬 수 있고
- 컴파일 시에 미리 타입을 강하게 체크해서 에러를 사전에 방지