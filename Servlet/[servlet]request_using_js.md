# 자바스크립트로 서블릿 요청

## 1. DOM 사용하는 방법

```java
<script type="text/javascript">
	// 자바스크립트로 서블릿에 요청 : DOM 사용
	window.onload = function() {
		// 양식 변수로 가져오기
		const frmLogin = document.getElementById("frmLogin");

		frmLogin.onsubmit = function() {
			// id : 참조객체 변수
			// user_id : 태그의 id 속성값
			const id = document.getElementById("id");
			const pw = document.getElementById("pw");

			if(id.value=="" || pw.value=="") {
				alert("아이디와 비밀번호는 필수입니다.")
				return false;
			} else {
				frmLogin.method = "post";
				frmLogin.action = "LoginJs";
				frmLogin.submit();
			}
		} // onsubmit End.
	} // window.onload End.
</script>
```

## 2. name 속성 사용

1.  document.frmLogin
2.  frmLogin.user_id.value

- name 속성 사용 예제
  loginJs2_name.html

## 3. jQuery 사용해서 서블릿에 요청 예제

- loginJs.html
