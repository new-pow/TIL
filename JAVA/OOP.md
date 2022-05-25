# Object Oriented Programing

> 객체지향 프로그래밍

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