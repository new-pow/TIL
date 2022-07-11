# Synchronous 동기식통신 vs Asynchronous 비동기식통신

## 동기식 통신

- Request를 보내고 Request에 대한 Response를 받는 것으로 두 서버 사이의 Transaction을 맞추는 통신 방식
- Request를 보낸 Thread는 Response가 도착하기 전까지는 아무것도 하지 못하는 Block 상태가 됨을 의미

```
 Request1 → Response1, Request2 → Response2
```

- 요청과 응답값의 순서를 보장하고, 보낸 요청에 대한 처리 결과 값을 보장받을 수 있기 때문에
- Response에 대한 처리 결과를 보장받고 처리해야 하는 서비스에 적합

## 비동기식 통신

- Request를 보내고 Request에 대한 Response를 받지 않고도 **다른 일 처리 가능한 통신 방식**

```
 Request1 → Response1
 Request2 → Response2
```

- 따라서 처리 속도가 빠름
- Response에 대한 처리 결과를 보장받고 처리해야 되는 서비스에는 적합하지 않음

## 비동기식 통신을 하기 위한 방법 on STS

- 클라이언트에서 서버로 메시지를 보낼 때, 본문에 데이터를 담아서 보내야 하고, 서버에서 클라이언트로 응답을 보낼 때에도 본문에 데이터를 담아서 보내야 함.
- 이 본문이 바로 body에 해당
- 즉, 요청 본문은 `requestBody`. 응답 본문은 `response Body`를 담아서 보냄
- `@RequestBody` 어노테이션과 `@ResponseBody` 어노테이션이 각각 HTTP 요청 바디를 자바 객체로 변환하고, 자바 객체를 다시 HTTP 응답 바디로 변환
- `@ResponseBody`가 붙은 파라미터에는 HTTP 요청의 본문 body부분이 그대로 전달
