# 포트를 사용중인 프로세스 확인하고 kill (m1 mac)

## 오류현상

- 상황1\_ 이클립스에서 톰캣 서버 중에 오류 발생

  - [Server at localhost are already in use ...]

- 상황2\_ 알 수 없는 이유로 프로그램 응답없음

  - 이후, 프로젝트를 다시 실행하면 이미 사용중이라는 위의 메시지가 발생
  - 작업관리자로 해결되지 않는다.

- 상황3\_ Web server failed to start. Port 8080 was already in use
  - 포트가 이미 실행 중일 때 스프링 Run하면 실행되는 에러

```
Web server failed to start. Port 3000 was already in use.
Action:
Identify and stop the process that's listening on port 3000 or configure this application to listen on another port.
2019-11-06 22:00:06.094  INFO 8996 --- [           main] o.s.s.concurrent.ThreadPoolTaskExecutor  : Shutting down ExecutorService 'applicationTaskExecutor'
```

## 해결방안

1. 터미널 열기

2. 다음의 명령어를 입력하여 어떤 프로세스가 포트를 점유 중인지 확인할 수 있다.

```cmd
$ sudo lsof -i:[PORT NUMBER]
$ sudo lsof -i:8080
```

3-1. 임시 방편으로 포트 번호 바꾸기

3-2. 프로세스 PID kill (for mac)

```cmd
kill [PID NUMBER]
> kill 4712
```

---

## 참조

- [[Mac] 포트를 사용중인 프로세스를 확인하고 종료해보자 (20-01-01)](https://velog.io/@todak/Mac-%ED%8F%AC%ED%8A%B8%EB%A5%BC-%EC%82%AC%EC%9A%A9%EC%A4%91%EC%9D%B8-%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4%EB%A5%BC-%ED%99%95%EC%9D%B8%ED%95%98%EA%B3%A0-%EC%A2%85%EB%A3%8C%ED%95%B4%EB%B3%B4%EC%9E%90)
  - (새해부터 공부라니, 대단하시다...)
- [[Tomcat] 이미 실행 중인 process kill (21-09-16)](https://studyingazae.tistory.com/54)
