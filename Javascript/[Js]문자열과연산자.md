# Javascript 문자열에 연산자 활용법

> 별 생각 안해봤는데, 이렇게도 쓸 수 있다고?! 싶어서 얼른 정리해본다. 아마 java에서도 가능하지 않을까?

## 문자열과 +
- 연산자 +은 숫자와 숫자 사이에 있을 때, 덧셈으로 연산한다.
- 그러나 `문자열+숫자열` 혹은 `문자열+문자열`일때는 붙여 쓴 효과를 가진다.

```javascript
function sayHello(name) {
    let msg = "Hello!"
    msg = "Hello! "+name;
}
```

- 내가 써보고 싶었던 것은 이것이다. 왜 아직까지 생각하지 못했지!?

```javascript
function sayHello(name) {
    let msg = "Hello!"
    msg += " "+name;
}
```

- 백틱 `을 활용하면 다음처럼 사용도 가능하다.

```javascript
function sayHello(name) {
    let msg = "Hello!"
    msg += ` ${name}`;
}
```

- 어떤 표현 방식이 가장 효율적일지 선택해보자.