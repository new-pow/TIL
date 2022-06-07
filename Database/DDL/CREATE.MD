# CREATE
---
> 테이블, 도메인, 뷰, 인덱스, 스키마의 구조를 정의한다.

#### 목차
1. [SCHEMA](#schema-스키마)
2. [TABLE](#테이블-table)
3. [KEY](#키-keyuserssaehimdesktoptildatabasekeymd)
    * [PRIMARY KEY](#기본키-primary-key)
    * [FOREIGN KEY](#외래키-foreign-key)

<br>

## SCHEMA 스키마
> 데이터 테이블의 합. 데이터베이스

* 데이터베이스 생성
``` sql
CREATE DATABASE sqldb1;
```
```sql
CREATE SCHEMA sqldb DEFAULT CHARACTER SET utf8;
```
```sql
CREATE SCHEMA sqldb DEFAULT CHARACTER SET utf8mb4;
```

* 데이터베이스 삭제
``` sql
DROP DATABASE sqldb1;
```
```sql
DROP SCHEMA sqldb2;
```

* 데이터베이스 확인
```sql
SHOW DATABASE sqldb1;
```
```sql
SHOW SCHEMA sqldb2;
```

* 사용 데이터베이스 변경
```sql
USE sqldb;
```

<br>

## 테이블 Table
* 테이블 생성
``` sql
CREATE TABLE product(
	prdNo char(10) not null primary key,
    prdName varchar(30) not null,
    prdPrice int,
    prdCompany varchar(30)
);
```
### [키 KEY](/Users/saehim/Desktop/TIL/Database/Key.md)

#### 기본키 PRIMARY KEY
> 데이터를 구분하는 고유한 열. 다른 행과 중복되지 않고, NULL일 수 없다.

* 기본키 제약조건 설정방법 1
```sql
CREATE TABLE product(
	-- 기본키 : prdNo, NOT NULL
	prdNo char(10) not null primary key,
    prdName varchar(30) not null,
    prdPrice int,
    prdCompany varchar(30)
);
```

* 기본키 제약조건 설정방법 2
```sql
CREATE TABLE product2(
	-- 기본키 : prdNo, NOT NULL
	prdNo char(10) not null,
    prdName varchar(30) not null,
    prdPrice int,
    prdCompany varchar(30),
    primary key (prdNo)
);
```

* 기본키 제약조건 설정방법 3
    + 복합키의 경우
```sql
CREATE TABLE product3(
-- 제약 조건
	-- 기본키 : prdNo, NOT NULL
	prdNo char(10) not null,
    prdName varchar(30) not null,
    prdPrice int,
    prdCompany varchar(30),
    CONSTRAINT PK_product_prdNo PRIMARY KEY (prdNo,prdName)
);
```

#### 외래키 FOREIGN KEY
* 외래키 제약조건 설정 방법1 --
```SQL
CREATE TABLE publisher(
	pubNo char(10) NOT NULL,
    pubName varchar(20) not null,
    PRImARY KEY (pubNo)
);
```
```SQL
Create table book (
	bookNo char(10) not null primary key,
    bookName varchar(30) not null,
    bookPrice int default 10000 check(bookPrice>1000),
    bookDate date,
    pubNo char(10) not null,
    constraint fk_book_publisher foreign key (pubNo) references publisher (pubNo)	--
);
```

* 외래키 제약조건 설정 방법2 --
```SQL
Create table book2 (
	bookNo char(10) not null primary key,
    bookName varchar(30) not null,
    bookPrice int default 10000 check(bookPrice>1000),
    bookDate date,
    pubNo char(10) not null,
    foreign key (pubNo) references publisher (pubNo)	-- 지정한 이름이 없으므로 임의 이름으로 설정
);
```

* 외래키 제약조건 설정 방법3
```SQL
create table scores (
	majorCode char(10),
    courNo char(10) Not null,
    profNo char(10) Not null,
    stuNo char(10) not null,
    scorResult int default 70 check(scorResult>0 and scorResult<101),
    constraint db_scores primary key (courNo, profNo, stuNo),							-- 한번에 설정해주어야 함. 오류남.
    constraint db_scoresMajor foreign key (majorCode) references major (majorCode),
    constraint db_scoresCour foreign key (courNo) references course (courNo),
    constraint db_scoresProf foreign key (profNo) references professor (profNo),
    constraint db_scoresStu foreign key (stuNo) references student (stuNo)
);
```

### DESCRIBE
```SQL
describe book;
```