<h2>Overview</h2>
A simple web application that allows you to display all employees in your mySQL database on the page and perform all CRUD operations (add, read, update and delete employees) with them. The first page displays the list of all employees and the buttons "Add", "Update", "Delete"
<br>
<br>
When you click on "Add", a new page with empty fields for entering information is displayed. After entering the information and clicking on the "Ok" button, the employee is added to the database. when you click on "Add", a new page with empty fields for entering information is displayed
<br>
<br>
If you click on "Update", a new page is displayed with fields filled with the information about the employee that is currently in the database. On this page you can change any information and after pressing the "Ok" button this information will be updated in the database
<br>
<br>
If you press the "Delete" button, the information about the employee is deleted from the database and, accordingly, from the page
<br>
<br>
"all-employees.jsp" is responsible for displaying the main page, "employee-info" is responsible for displaying the page where we enter or change employee information
<br>
<br>
Our application communicates with the database using Hibernate
<br>
<br>
All CRUD operations are performed using interfaces "EmployeeDAO", "EmployeeService" and classes "EmployeeDAOImpl", "EmployeeServiceImpl" that implements these interfaces
<br>
Class "MyController" is responsible for switching views
<br>
<br>
Class "MyLoggingAspect" adds some cross-cutting functionality to our project:
<br>
<ul>
<li>before and after the execution of any CRUD operation it shows a message on the terminal, that method has started or finished</li>
</ul>
<h3>Configuration</h3>
Project is created from Maven archetype "maven-archetype-webapp"
<br>
Deployment to the server is performed by Tomcat
<br>
DispatcherServlet is configured by file web.xml (/src/main/webapp/WEB-INF/web.xml)
<br>
Spring Container is configured by file applicationContext.xml (/src/main/webapp/WEB-INF/applicationContext.xml)
