# 📃 Java: ArrayList

# List 컬렉션

## List(인터페이스) 컬렉션의 특징

- 특징
  - 순서가 있는 데이터의 집합
  - 인덱스로 관리
  - 중복해서 객체 저장 가능
- 구현 클래스
  - ArrayList✨
  - Vector
  - LinkedList

## List 컬렉션의 주요 메소드

1. 객체 추가

| 메소드                   | 설명                                             |
| ------------------------ | ------------------------------------------------ |
| boolean add(E e)         | 주어진 객체를 맨 끝에 추가                       |
| void add(int index, E e) | 주어진 인덱스에 객체를 추가                      |
| set(int index, E e)      | 주어진 인덱스에 저장된 객체를 주어진 객체로 대체 |

2. 객체 검색

| 메소드                     | 설명                               |
| -------------------------- | ---------------------------------- |
| boolean contains(Object o) | 주어진 객체가 저장되어 있는지 여부 |
| E get(int index)           | 주어진 인덱스에 저장된 객체를 반환 |
| isEmpty()                  | 컬렉션이 비어 있는지 조사          |
| int size()                 | 저장되어있는 전체 객체수를 반환    |

3. 객체 삭제

| 메소드                   | 설명                               |
| ------------------------ | ---------------------------------- |
| void clear()             | 저장된 모든 객체를 삭제            |
| E remove(int index)      | 주어진 인덱스에 저장된 객체를 삭제 |
| boolean remove(Object o) | 주어진 객체를 삭제                 |

# ArrayList

- List 인터페이스의 구현 클래스
- 크기가 가변적으로 변하는 선형 리스트
- 배열과 유사점
  - 순차 리스트, 인덱스 사용
- 배열과의 차이점
  - 배열 : 크기 고정
  - ArrayList
    - 객체 추가 가능
    - 저장 용량 초과 시 자동 용량 증가
    - 기본 10개
    - new ArrayList(30); // 처음부터 크게 설정 가능

```jsx
// 제네릭을 사용하지 않을 경우

List list = new ArrayList();
list.add("hello");
String str = (String) list.get(0)
```

```jsx
// 제네릭을 사용할 경우

List list = new ArrayList<String>;
list.add("hello");
String str = list.get(0)
```

- ArrayList 객체 생성 시 타입 파라미터로 저장할 객체의 타입을 지정함으로써 강제 타입 변환 **불필요**

- **객체 추가**
  - 인덱스 0부터 차례로 저장
- 객체 제거

  - 제거된 객체의 바로 뒤 인덱스부터 마지막 인덱스까지 앞으로 1씩 당겨짐
  - 따라서 빈번한 객체 삭제와 삽입이 일어나는 경우 ArrayList 사용하는 것이 바람직하지 않음

### 고정된 객체들로 구성된 list 생성

- ArraysList.asList()
- ArraysList.asList()

---

## 참고

- [자바 ArrayList 사용법과 예제 (2022)](https://shpk333.tistory.com/10)
