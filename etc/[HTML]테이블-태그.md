# [HTML] 테이블 태그

## 테이블 구조 정의
- `<table>`, `</table>` 테이블 선언
- `<caption>` 테이블 제목, 설명시 사용

<br>

+ `<tr>` Table Row 테이블 내 한 행을 정의
+ `<td>` Table Data 테이블 내 하나의 셀을 정의

<br>

- `<thead>`, `<tbody>`, `<tfoot>`
    + 표의 제목과 본문 등 구분
    + 필수적이지는 않으나, 그룹을 지어 놓으면 접근성 향상의 효과가 있다.
    + CSS를 사용하여 테이블의 각 부분에 다른 스타일을 적용할 수 있어 편리하다.
    + 종류
        1. `<thead>`, `</thead>` 테이블 상단부
        2. `<tbody>`, `</tbody>` 테이블의 내용이 주로 여기에 정의
        3. `<tfoot>`, `</tfoot>` 테이블 하단부



<br>    

## 기본 형식

```html
<table>
    <thead>
        <tr>
            <th>번호</th><th>2열 머리</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1행 1열</td><td>1행 2열</td>
        </tr>
        <tr>
            <td>2행 2열</td><td>1행 2열</td>
        </tr>
    </tbody>
</table>
```
<table>
    <thead>
        <tr>
            <th>번호</th><th>2열 머리</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1행 1열</td><td>1행 2열</td>
        </tr>
        <tr>
            <td>2행 2열</td><td>1행 2열</td>
        </tr>
    </tbody>
</table>

<br>

## `<table>` 속성
- `align` 테이블 정렬 방식 (left/right/center)
- `border` 테이블 테두리, 생략하면 테두리 없음
- `bordercolor` 테두리 색상
- `width`,`height` 테이블 너비, 높이
- `bgcolor` 테이블 배경색
- `background` 테이블에 배경 이미지 넣기
- `cellspacing` 셀과 셀 사이 여백
- `cellpadding` 텍스트와 셀 사이의 여백

<br>

## `<tr>` 태그 속성
- `align` 행 전체 수평 정렬 (left/right/center)
- `width` 행의 가로 길이
- `height` 행의 세로 길이
- `bgcolor` 행의 배경색

<br>

## `<td>` 태그 속성
- `valign` 셀의 수직 정렬 (top/middle/bottom)
- `align` 셀의 수평 정렬 (left/right/center)
- `width`, `height` 셀의 가로, 세로 길이
- `bgcolor` 셀의 배경색
- `background` 셀의 배경 이미지
- **`rowspan` 행 합치기**
- **`colspan` 열 합치기**

<br>

## 예시

```html
<table border="1px">
<caption>휴양림 객실 정보</caption>
    <thead align="center">
        <tr>
            <th>방 이름</th>><th>크기</th><th>가격</th>
        </tr>
    </thead>
    <tbody align="center">
        <tr>
            <th>종달새방</th> <td>2인실</td><td rowspan="4">1인 30,000원</td>
        </tr>
        <tr>
            <th rowspan="2">진달래방</th><td rowspan="3">4인실</td>
        </tr>
        <tr>
            <td>가족</td>
        </tr>
    </tbody>
    <tfoot align="center">
        <tr><td colspan="4">휴가철 성수기 기준</td></tr>
    </tfoot>
</table>
```
<table border="1px">
<caption>휴양림 객실 정보</caption>
    <thead align="center">
        <tr>
            <th>방 이름</th>
            <th>대상</th>
            <th>크기</th>
            <th>가격</th>
        </tr>
    </thead>
    <tbody align="center">
        <tr>
            <th>종달새방</th>
            <td>여성</td>
            <td>2인실</td>
            <td rowspan="4">1인 30,000원</td>
        </tr>
        <tr>
            <th rowspan="2">진달래방</th>
            <td>남성</td>
            <td rowspan="3">4인실</td>
        </tr>
        <tr>
            <td>가족</td>
        </tr>
    </tbody>
    <tfoot align="center">
        <tr><td colspan="4">휴가철 성수기 기준</td></tr>
    </tfoot>
</table>


