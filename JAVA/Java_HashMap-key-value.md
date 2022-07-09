# Java: HashMap에서 키(Key)와 값(Value)

## 1. HashMap 선언

```java
Map<String, Integer> map = new HashMap<String, integer>();
```

- HashMap은 key-value의 형태로 쌍의 데이터로 저장되는 구조를 가지고 있다.
- key 값은 중복 저장되지 않는다. (value는 중복되어도 된다.)

## 2. 데이터 넣기

```java
map.put("수학", 90);
map.put("국어", 80);
map.put("영어", 50);
```

- 선언한 hashmap에 위와 같이 값을 넣어 줄 수 있다.

## 3. 데이터 가져오기

```java
map.keySet();   // key 값 가져오기
map.values();   // value 값 가져오기

```

## 4. 키 값으로 데이터 찾기

```java

```
