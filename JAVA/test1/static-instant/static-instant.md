# static과 instant

## 인스턴스 멤버
- non-static 멤버
- 객체를 통해서 접근
- 지금까지 우리가 만들었던 객체 멤버
- 객체가 생성될 때 각 객체 내부에 하나씩 생성
- 객체마다 자신의 고유 멤버 공간을 가짐
- 다른 객체들과 공유하지 않음
- 객체가 사라지면 함께 사라짐

## static멤버
- 클래스에 고정된 필드와 메소드
- 클래스에 소속된 멤버 (클래스당 하나만 생성)
- 객체를 생성하지 않고 클래스로 바로 접근해서 사용
- 클래스 내의 모든 객체들이 공유
- 프로그램이 시작될 때 이미 생성 (객체보다 먼저 생성됨)
- 프로그램이 종료될 때 사라짐

```java
public class Test {
	static int width, height;
	static void sum() {
		System.out.print("면적 : "+width*height);
	}
}
```