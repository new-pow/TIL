# ALTER
---
> 

#### 목차
1. [RENAME](#rename)
2. [ADD](#테이블-table)
3. [MODIFY](#modify)
4. [CHANGE](#change)
5. [DROP](#drop)
6. [CHECK](#check)

<br>


## RENAME
---
> 이름 변경
### 단일 테이블 이름 변경
* `ALTER`와 `RENAME`의 차이점
    1. `RENAME`은 다수의 테이블 이름을 한 번에 변경할 수 있다.
    2. 테이블을 다른 데이터베이스로 이동시킬 수 있다.

### 형식
```sql
RENAME TABLE oldTable to newTable;
```
* ALTER 사용시 형식
```SQL
ALTER TABLE oldTable RENAME newTable;
```

* 다수의 테이블 이름 변경
```SQL
RENAME TABLE oldTable1 TO newTable1,
             oldTable2 TO newTable2,
             oldTable3 TO newTable3,
```

### 열 이름 변경
+ 주의! 데이터 타입을 같이 적으면 오류 발생
```sql
alter table student rename column stdTel to stdHP;
ALTER TABLE department RENAME COLUMN majorCode to dptNo;
ALTER TABLE department RENAME COLUMN majorName to dptName;
ALTER TABLE department RENAME COLUMN majorCont to dptTel;
```

## ADD
### 테이블에 열 추가
#### 형식
* 단일 열 추가
```sql
alter table 테이블명 add 열이름 타입(크기);
```

* 여러 개의 열 추가
    + 괄호 안에 열이름 타입, 크기 삽입
```sql
alter table student add(stdAge varchar(2), atdaddress2 varchar(50));
```

## MODIFY

## CHANGE

## DROP

## CHECK

## SET