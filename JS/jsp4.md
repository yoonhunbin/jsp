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
	<%@ page autoFlush="false" buffer="1kb" %>
	<h2>현재 aufoFlush = <%=out.isAutoFlush() %></h2><p>
	
	<%
		for (int i = 1; i < 25; i++) {
				out.println("남은 출력 버퍼 크기(out.getRemaining()) : " + out.getRemaining() + "<br>");
				if (out.getRemaining () < 100) {
						out.println("<br>");
						out.flush ();
				}
		}
	%>
	
	<hr>
	초기 출력 버퍼 크기 : <%= out.getBufferSize() %> byte<br>
	남은 출력 버퍼 크기 : <%= out.getRemaining() %> byte
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
	<%
		out.println("이 부분은 출력되지 않습니다.");
		out.clear();
	%>
	
	<h2>현재 페이지의 출력 버퍼 상태</h2>
		
	초기 출력 버퍼 크기: <%=out.getBufferSize() %> byte<p>
	남은 출력 버퍼 크기: <%=out.getRemaining() %> byte<p>
	autoFlush : <%=out.isAutoFlush() %><p>
	
</body>
</html>
```
