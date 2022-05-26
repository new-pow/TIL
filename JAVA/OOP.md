# Object Oriented Programing

> 객체지향 프로그래밍 (OOP)

* 부품 객체를 만들고 이것들을 하나씩 조립해서 완성된 프로그램을 만드는 기법.
* 프로그램을 작성하는데 필요한 모든 요소를 객체로 표현한다.
* 사람의 사고방식과 비슷한 방식으로 모델링한다.
* __존재하는 모든 것을 객체로 표현__
* __객체 중심 생각__

<br>

## 객체(Object)란?
> an instance of a class that may contain attributes and methods

* 물리적으로 존재하는 것. (물체, 사람 등.)
* 추상적인 것(날짜, 회사 등) 중 자신의 속성과 동작을 가지는 모든 것.
* Java에서 객체는 속성(필드)와 동작(메소드)로 구성된 자바 객체로 모델링 가능.

### 객체의 구성 요소
* 속성 attribute = 필드
    + 데이터
    + 차량번호, 차종, 배기량, 색상 등
* 기능 method  = 메소드
    + 처리작업
    + (차량 정보를) 출력하다. 등

<br>

## 객체 지향 프로그래밍의 특징
### 캡슐화 Encapsulation
* 객체의 필드, 메소드를 하나로 묶고 실제 구현 내용을 감추는 것.
    * 외부 객체는 내부 구조를 알지 못하며 객체가 노출해 제공하는 필드와 메소드만 이용 가능하다.
* 캡슐화하여 보호하는 이유는 외부의 잘못된 사용으로 인해 객체가 손상되지 않도록 **데이터보호** 하기 위함.
* 자바 언어는 캡슐화된 멤버를 노출시킬 것인지, 숨길 것인지 결정하기 위해
    + **접근 제한자**를 사용한다. (public / private)
* 객체간의 관계 __상속__


## Class
### 형식
``` Java
class Animal {

}

// 보통 class는 특수한 경우가 아니라면 파일 단위로 1개씩 작성
```
<br>

## Object와 Instance variable
### Object 객체
``` java
class Animal {

}

public class Sample {
    public static void main(String[] args) {
     Animal dog = new Animal();
     Animal cat = new Animal();
    }
}
```
* 여기서 `dog`과 `cat`은 객체. `Animal`의 instance이다.

<br>

### Instance variable 객체 변수

```java
class Animal {
	String name;
    // 객체 변수 (클래스에 의해 선언된 변수)
}

public class Sample {
	public static void main(String[] args) {
		Animal cat = new Animal();	    // 객체
		System.out.println(cat.name);   // 객체 호출방법 : 객체.객체변수
	}

}
```

## Method

> 클래스 내에 구현된 함수

``` java
class Animal {
	String name;
	public void setName(String name) { // 메소드
		this.name = name;
	}
}

public class Sample {
	public static void main(String[] args) {
		Animal cat = new Animal();
		cat.setName("Woozi");          // 메소드 호출 : 객체.메소드()
		System.out.println(cat.name);
	}

}
```

<br>

## 객체 변수는 공유되지 않는다.
> 클래스에서 가장 중요한 부분은 객체 변수의 값이 독립적으로 유지된다는 점이다.

``` java
class Animal {
	String name;

	public void setName(String name) {
		this.name = name;
	}
}

public class Sample {
	public static void main(String[] args) {
		Animal cat = new Animal();         // 객체 1
		cat.setName("Woozi");
		System.out.println(cat.name);      // 객체변수 1
		
		Animal dog = new Animal();         // 객체 2
		dog.setName("MG");
		System.out.println(dog.name);      // 객체변수 2
	}

}
```

작동 방식은 같지만 서로 다른 두 개의 계산기로 계산값을 저장하고 있는 것과 같다.