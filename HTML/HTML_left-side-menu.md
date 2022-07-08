# 🔧 HTML: 왼쪽 고정 메뉴 만들기

```html
<nav>
  <h1>메인 내비게이션</h1>
  <ul>
    <li><a>메뉴1</a></li>
    <li><a>메뉴2</a></li>
  </ul>
</nav>
```

## `<nav>`

> 목적지로 이동할 수 있도록 링크를 별도로 모아둔 영역

- 링크 중에서 중요도가 높은 링크를 체계적으로 구성해 놓은 것으로 단순 본문 링크와 메뉴(카테고리) 성격의 링크인지 확인이 가능하다.
- ul, li, a 요소들을 여전히 함께 사용해야 한다.
- 브라우저가 네비게이션 영역을 알 수 있게 되면 스크린리더의 내비게이션과 검색엔진의 색인에도 도움을 줄 수 있다.

### css : 좌측 고정을 위한 효과

- position:fixed;
  - 공중에 떠서 공간을 차지하지 않으며, 스크롤을 내려도 고정되어 있다.
- height: 100%;
  - fixed 없으면 적용되지 않는다.

---

## `li a`

### css

- height == line-height
  - 똑같이 지정해서 상하좌우 가운데 정렬이 되도록 한다.
- display:block;
  - a 태그는 기본 display:inline; 이므로, block으로 바꿔준다.
  - 롤오버 효과를 지정할 때 유리하다.

---

# 참고

- [본문 : 섹션(Section) 요소 - BODY, HEADER, NAV, SECTION, ARTICLE, MAIN, ASIDE, FOOTER (2016)](https://webdir.tistory.com/310)

- [[HTML/CSS]Part1-06 (왼쪽 고정 메뉴 만들기, 타겟 기능~) (2017)](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=sora8324&logNo=221025176049)
