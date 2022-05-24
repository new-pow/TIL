# Object Oriented Programing

## Class
### 형식
``` Java
class Animal {

}

// 보통 class는 특수한 경우가 아니라면 파일 단위로 1개씩 작성
```
<ㅠㄱ

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
