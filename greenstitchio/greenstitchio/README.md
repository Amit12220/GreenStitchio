# REST API for manage a simple "Employee" entity.

# Tech Stack
- Java
- Hibernate
- Spring Framework
- Spring Boot
- Spring Data JPA
- MySQL
- Maven
- Spring Security

# Installation & Run
- Before running the API server, you should update the database config inside the application.properties file.
- Update the port number, username and password as per your local database configuration.

# Note

   spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.h2.console.enabled=true
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

# STEPS :
- First we run the application
- Insert The roles through Hard coded
-   INSERT INTO role_master (id,name,status,is_delete) VALUES (1,'EMPLOYEE_ADMIN',1,0);

-   INSERT INTO role_master (id,name,status,is_delete) VALUES (2,'EMPLOYEE_FRONTEND',1,0);

-   INSERT INTO role_master (id,name,status,is_delete) VALUES (3,'EMPLOYEE_BACKEND',1,0); 

-   After that Do Sign Up Use Below Dummy Details
-   Then Do Sign In
-   Then Save the Employees In the Database



# API Root Endpoint
```
Sign Up :
           http://localhost:8080/Employee/api/v1/signup
           {
             "username":"Amit",
             "email":"ajha.9614938@gmail.com",
             "password":"br09pa2655",
             "name":["EMPLOYEE_ADMIN"]
            }
```
```
Login :
                 http://localhost:8080/Employee/api/v1/signin

                 {
                   "username":"Amit",
                   "password":"br09pa2655"
                 }
                 
        Note : Please Copy the JWT Token and paste it into the Authentication
```
```
step 5 : save the employee :

http://localhost:8080/api/employee/saveemployee

{
    "employeeEmail": "amit@gmail.com",
    "employeeName": "Amit Kumar",
    "employeeDepartment": "CSE"
}
Note : Id Is Autogenerated

```
```
Step 6 : Get the Employee By Id

       http://localhost:8080/api/employee/getEmployeeById/{{id}}
```
```
Step 7 : getAllEmployee

       http://localhost:8080/api/employee/getAllEmployees
```
```

step 8 : For Delete
       http://localhost:8080/api/employee/deleteEmployee/{{id}}
   
```   

# Collaborators

- [Amit Kumar](https://github.com/)Amit12220
