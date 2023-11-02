```
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>

	<%@ page autoFlush="false" buffer="1kb"  errorPage="error.jsp"%>
	<%
		for (int i = 1; i < 25; i++) {
				out.println("남은 출력 버퍼 크기(out.getRemaining()) : " + out.getRemaining() + "<br>");
		}
	%>

</body>
</html>
```
```
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>
<%@ page isErrorPage="true" %>
	<h1> 예외처리 페이지</h1>
	
	 오류 문자열[exception.toString()] : <%= exception.toString() %><br>
	 오류 메시지[exception.getMessage()] : <%= exception.getMessage() %><br>
</body>
</html>
```
