# 릴레이션(테이블)의 특징

## 1. 속성은 단일 값을 가진다.
- 각 속성의 값은 도메인에 정의된 값만을 가지며, 그 값은 모두 단일한 값이어야 한다.
- 한 속성은 2개 이상의 값을 가질 수 없다.

<br>

## 2. 속성은 서로 다른 이름을 가진다.
---

<br>

## 3. 한 속성의 값은 모두 같은 도메인 값을 가진다.
---
* 한 속성에 속한 열은 모두 그 속성에서 정의한 도메인값만 가질 수 있다.

<br>

## 4. 속성의 순서는 상관없다.
---
- 열의 순서를 변경하더라도 이 관계의 내용은 전혀 변하지 않는다.

<br>

## 5. 릴레이션 내의 중복된 튜플은 허용하지 않는다.
---
* 하나의 릴레이션 인스턴스 내에서는 서로 중복된 값을 가질 수 없다.
* 모든 튜플은 서로 값이 달라야 한다. (전체 행이 같으면 안된다.)
* 각 튜플(행)을 서로 다르게 구별짓는 속성을 갖는다. (기본키)

<br>

## 6. 튜플의 순서는 상관없다.
---
* 행의 순서가 달라도 같은 릴레이션이다.
* 관계 데이터 모델의 행은 실제적인 값을 가지고 있다.
* 이 값은 시간이 지남에 따라 삭제, 수정, 삽입으로 인해 순서가 바뀔 수 있다.

<br>

> - 속성 = 열, colmn
> - 도메인 = 하나의 속성이 취할 수 있는 동일한 타입의 원자값들의 합.
> - 튜플 = 행, row