# CDATA

- 파싱되지 않는 문자 데이터
- 쿼리를 작성할 때 `<`,`>`,`>=`,`&`,`||` 등을 사용해야 하는 xml 태그로 인식해서 오류를 발생할 수 있다.
- XML 파싱 대상이 아닌 단순 문자열로 처리하라는 의미이다.

```html
<select id="listAllProduct" resultMap="prdResult">
    <![CDATA[ SELECT * FROM product WHERE prdPrice >= 1000000 ORDER BY prdNo
   ]]>
</select>
```

## CDATA Syntax

```html
<![CDATA[ code ]]>
```

## 장점

- 가독성을 높인다.

## 주의할 점

- CDATA 영역 안의 모든 `<`,`>`를 문자열로 만들어버리기 때문에 동적 쿼리를 작성할때는 사용하지 않는다.

---

# 참고

- MLP backend 강의
- [CDATA란? (2021)](https://escapefromcoding.tistory.com/372)
