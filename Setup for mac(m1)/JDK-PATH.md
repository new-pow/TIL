# JDK 환경변수 설정 for Mac M1

## 1. JDK를 설치한 디렉토리와 폴더명 확인

## 2. 터미널 실행

## 3. JDK 디렉토리 경로로 이동

```
cd /Library/Java/JavaVirtualMachines/jdk-11.0.15.jdk/Contents/Home/bin
```

## 4. 파일 생성 후, 환경변수 등록

- 영구 환경변수 편집

```
vi ~/.zshrc
```

1. 위의 명령어로 파일을 열고
2. `i`를 입력하여 insert 모드로 변경
3. 맨 밑에 원하는 환경변수를 다음과 같이 추가해준다. (파일 디렉토리는 정확하게 확인하여 넣어주자.)

```
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-11.0.15.jdk/Contents/Home
export PATH=${PATH}:$JAVA_HOME/bin
```

4. `esc`를 눌러 insert 모드 해제
5. `:wq`을 입력하여 저장후 종료한다.

## 5. 적용

```
source ~/.zshrc
```

## 6. 확인

```
echo $JAVA_HOME
echo $PATH
java -version
```

---

# 참고

- [Bash vs Zsh : 두 개의 명령 줄 셸 비교 (2019)](https://sunlightmedia.org/ko/bash-%EB%8C%80-zsh/)
  - 궁금해져서 서치하여 첨부
