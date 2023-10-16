<h1>jsp</h1>

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
	String URL = "http://search.naver.com/search.naver?where=nexearch";
	String keyword = request.getParameter("word");
	URL += "&" + "query=" + keyword;
	response.sendRedirect(URL);
%>

</body>
</html>
```
<h2>html</h2>

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>
<h2> 검색할 단어를 입력하세요.</h2>

<form method="get" action="abc1.jsp">
	검색 키워드: <input type="text" name="word">
	<input type="submit" value="보내기">
	<input type="reset" value="취소">
</form>

</body>
</html>
```
