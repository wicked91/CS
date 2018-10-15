## WebServer/ WebContainer/ WAS

1. **Web Server**
웹 서버란 웹 브라우저와 같은 클라이언트로부터 HTTP요청을 받아들이고, HTML 문서와 같은 웹 페이지를 반환하는 것
웹 페이지, 이미지 등 **정적인 페이지**를 생성한다.
<br>

2. **Web Container**
웹 컨테이너란 JSP와 서블릿을 실행시킬 수 있는 소프트웨어를 웹 컨테이너 혹은 서블릿 컨테이너 라고한다.
웹 서버에서 JSP를 요청하면 JSP 파일을 서블릿으로 변환시켜 컴파일을 수행하고 수행결과를 웹 서버에 전달한다.
<br> ex) Servlet 컨테이너, JSP 컨테이너, EJB 컨테이너

<br>

3. **WAS(Web Application Server)**
`웹 서버와 웹 컨테이너의 결합`으로 다양한 기능을 컨테이너에 구현하여 다양한 역할을 수행할 수 있는 서버
웹 애플리케이션 서버는 **동적 서버 콘텐츠**를 수행하는 것으로 일반적인 웹 서버와 구별이 되며, 주로 데이터베이스 서버와 같이 수행이 된다. 
<br> ex) tomcat, tMax jeus, BEA Web Logic, IBM Webspere