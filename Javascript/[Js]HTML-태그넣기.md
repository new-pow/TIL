# [Javascript] script에서 HTML 태그를 넣는 방법

## 인쇄(document.write)를 하자

* HTML 태그를 프린트하여 화면에 그려준다고 생각하면 덜 헷갈린다.

```javascript
// 따옴표 조합에 유의할 것
document.write("<img src='image/lizard.png'>");

// 혹은 특수문자 사용 가능 \"
document.write("<img src=\"image/lizard.png\">");
```

## 주의사항
- 따옴표 사용에 유의하자. 특수문자 `\"`를 사용하는 방법도 있다.

---
