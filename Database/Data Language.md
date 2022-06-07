# 데이터베이스 언어 Data Language


> 데이터베이스를 구축하고 이용하기 위한 데이터베이스 관리 시스템과의 통신수단
## 언어로 다룰 부분 3가지
- [데이터 정의어 DDL](/Users/saehim/Desktop/TIL/Database/SQL/DDL.md) : Data Definition Language
- [데이터 조작어 DML](/Users/saehim/Desktop/TIL/Database/SQL/DML.md) : Data Manipulation Language
- [데이터 제어어 DCL](/Users/saehim/Desktop/TIL/Database/SQL/DCL.md) : Data Control Language

<br>

### 데이터 정의어 <br> DDL : Data Definition Language
> 데이터베이스 구조 정의를 위한 언어
* 데이터베이스 구조, 데이터 형식, 접근방식 등 데이터베이스 구축 및 변경
* 데이터베이스의 논리적, 물리적 구조 정의 및 변경
* 스키마 Schema 에 사용되는 제약 조건 정의
    - 스키마 : 데이터베이스의 전체 구조 명시
- 데이터의 물리적 순서 규정
- 물리적 구조 정의 방법
    - CREATE / ALTER / DROP

- 데이터 조작어 DML : Data Manipulation Language
    - 실제 데이터 처리를 위해 응용프로그램과 데이터베이스 관리 시스템 간의 인터페이스를 위한 언어
    - 데이터 처리 연산 가능 : 검색, 삽입, 삭제, 갱신 연산 등
    - INSERT / DELETE / UPDATE / SELECT
    - CRUD
        - Create / Read / Update / Delete
- 데이터 제어어 DCL : Data Control Language
    - 보안 및 권한 제어, 데이터 무결성, 복구, 병행 제어 등을 위한 언어
    - 데이터 보안 : 권한이 없는 접근으로부터 보호
    - 데이터 무결성 : 데이터의 정확성, 안정성 보장
    - 데이터 복구(회복) : 시스템오류 등으로부터 회복
    - 병행 제어 : 다수 사용자가 공유
    - GRANT / REVOKE / COMMIT / ROLLBACK