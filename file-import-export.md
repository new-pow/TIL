# my.cnf 파일 수정 for Mac

- my.cnf 파일

  > - MySQL 서버는 단 하나의 설정파일만 사용한다. my.cnf는 Unix 계열의 mysql 설정파일이다. Windows 계열은 my.ini 파일로 관리된다.
  > - 서버가 시작될 때, 디렉토리에서 가장 먼저 발견된 my.cnf 파일을 사용한다.

- 하나의 my.cnf 파일은 여러 개의 설정 그룹을 담을 수 있다.
- 아래는 기본 설정으로 흔히 볼 수 있다. (커넥션을 localhost만 허용함.)

- 일반적으로 Unix 및 Unix 계열 시스템에서 MySQL / MariaDB 프로그램은 다음 위치에서 지정된 순서대로 구성 / 시작 파일을 읽는다.
  - /etc/my.cnf -글로벌
  - /etc/mysql/my.cnf -글로벌
  - SYSCONFDIR/my.cnf -글로벌

```SQL
# Default Homebrew MySQL server config
[mysqld]
# Only allow connections from localhost bind-address = 127.0.0.1
mysqlx=bind-address = 127.0.0.1
```

## 경로 확인

1. 터미널에서 다음 명령어로 확인 가능하다.

```
$ mysql --help | grep my.cnf
```

## 적용

- MySQL 서버를 다시 시작함으로서 변경사항을 적용할 수 있다.

```
$ mysql.server restart
```

혹은

```
$ mysql.server stop
$ mysql.server start
```
