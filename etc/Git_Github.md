# Git and Github

## why Git & Github?

### Git

- 분산 버전 관리 프로그램
- 백업 / 복구 / 협업을 용이하게 하기 위해 사용한다.
- [Git 공식문서](https://git-scm.com/book/ko/v2)


### Github

- Git을 사용하는 프로젝트의 협업을 위한 웹호스팅 서비스
- 포트폴리오를 전시 / 공유할 수 있다.



## Git 기초

### 초기 설정 : 작성자 입력

> 최초 1회 설정하고 매번 설정할 필요가 없습니다.

1. 이름 / 이메일을 설정해준다.

```bash
git config --global user.name "이름"
git config --global user.email "메일주소"
```
* 메일주소, 이름은 github와 일치시키는 것이 좋다.


2. 확인해본다.

```bash
git config --global -l

#또는

git config --global --list
```


### Git 저장소

#### Git 저장소 만들기 (로컬 저장소)
> Git 저장소는 3가지 영역으로 나뉘어져 있다.

**Working Directory (Working Tree)** : 사용자의 일반적인 작업이 일어나는 곳

▼

**Staging Area (Index)** : 커밋을 위한 파일 및 폴더가 추가되는 곳

▼

**Commits (Repository)** : staging area에 있던 파일 및 폴더의 변경사항 commit을 저장하는 곳


1. 버전을 만들 폴더를 만든다. (일반 폴더)


2. `git init` 명령어 입력으로 폴더를 Git으로 관리하는 것을 명령한다.
  * <master> 표시가 위치 옆에 표시된다.
  (Mac은 처음에 표시가 안되는데 이는 추가 설정이 필요하다.)


3. `git add` 명령어로 폴더를 WD에서 SA로 추가한다.

   ```bash
   # file 추가
   git add a.txt
   
   # folder 추가
   git add my_folder/
   
   # Directory 현재 디렉토리 추가
   git add .
   ```


4. `git commit` 명령어로 SA에서 Commits에 저장.

   ```bash
   # with message
   git commit -m "my first commit"
   ```

   - 커밋 메시지는 현재 변경사항들을 잘 나타낼 수 있도록 의미있게 작성하는 것을 권장.
   - 각각의 커밋은 SHA-1 알고리즘에 의해 반환된 고유의 해시값을 ID로 가진다.

5. `git status` 명령어로 현재 상태를 알 수 있다. 수시로 확인하면 좋다.

   - commit 전 단계들에 있는 파일의 상태를 알려준다.
   - 상태
     - Untracked : Git이 관리하지 않는 파일
     - Tracked : Git이 관리하는 파일
       - Unmodified : 최신상태
       - Modified : 수정되었지만 아직 Staging Area에는 반영하지 않음.
       - Staged : Staging Area에 올라간 상태 (commit해야함)

6. `git log` 명령어로 커밋의 내역을 조회할 수 있다.

   1. 명령어 옵션
      1. `--oneline` 한 줄로 요약해서 보여줍니다.
      2. `--graph` 브랜치와 머지 내역을 그래프로 보여줍니다.
      3. `--all` 현재 브랜치를 포함한 모든 브랜치의 내역을 보여줍니다.
      4. `--reverse` 커밋 내역의 순서를 반대로 보여줍니다. (최신이 가장 아래)
      5. `-p` 파일의 변경 내용도 같이 보여줍니다.
      6. `-3` 원하는 갯수만큼의 내역을 보여줍니다.



## Github

### 원격 저장소 (Remote Repository)

> 로컬 저장소에서 벗어나 Github 원격 저장소를 이용해 다른 사람과 공유하고 협업을 할 수 있습니다. 로컬 저장소와 원격 저장소의 연동 방법을 알아봅니다.



#### Github에서 원격 저장소 생성
1. 




### 주의사항

- git hub에서 수정하지 않기. 나중에 오류남.
  - 수정은 로컬에서 만들고 push하여 동기화.
- drag and drop으로 파일 넣지 않기. 오류날 수 있음.
- git init하고 또 init하면 안됨. (중첩선언no)

