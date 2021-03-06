# .gitignore
> 특정 파일 혹은 폴더에 대해 Git이 버전관리를 하지 못하도록 지정한다.

## 용도
* `git add .`를 이용해 github repository에 삽입을 할때 `git add .`을 통해 수정 사항을 추가하고 커밋한다.
* 여기서 일부 파일을 포함하고 싶지 않을 때, `.gitignore`라는 디렉토리를 만들어 무시할 파일을 넣어줄 수 있다.

<br>

주로 다음의 상황에서 많이 사용한다.  
- 보안상으로 위험성이 있는 파일 (민감한 개인정보)
- 프로젝트와 관계없는 파일
- 용량이 너무 커서 제외해야하는 파일
- 운영체제 OS에서 활용되는 파일
- 개발언어 혹은 프레임워크에서 사용되는 파일
- IDE 혹은 Text editor 등에서 활용되는 파일

## 사용법
1. 반드시 `.gitignore` 이름의 파일을 만들어준다.
    * 앞에 온점(.)은 숨김 파일이라는 뜻
2. 그 안에 한 줄씩 제외할 파일 혹은 폴더를 쓴다.

### 주의사항
* `.gitignore` 파일은 `.git` 폴더와 동일한 위치에 생성합니다.
* 제외하고 싶은 파일은 `git add` 전에 `.gitignore`에 작성
    + 미리 add할 시, 이미 관리되고 있어 계속 버전 관리의 대상으로 인식됨

## 코드
- 특정 파일 제외
```
# .gitignore


# 확장자가 txt인 파일 무시
*.txt

# 현재 확장자가 txt인 파일이 무시되지만, 느낌표를 사용하여 test.txt는 무시하지 않음
!test.txt

# 현재 디렉터리에 있는 TODO 파일은 무시하고, folder/TODO 처럼 하위 디렉터리에 있는 파일은 무시하지 않음
/TODO

# build/ 디렉터리에 있는 모든 파일은 무시
build/

# folder/notes.txt 파일은 무시하고 folder/child/arch.txt 파일은 무시하지 않음
folder/*.txt

# folder 디렉터리 아래의 모든 .pdf 파일을 무시
folder/**/*.pdf
```
