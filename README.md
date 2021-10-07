# employeemanager
Backend of EmployeeManager app developed on the basis of a course by Junior on Amigoscode's YouTube channel: https://www.youtube.com/watch?v=Gx4iBLKLVHk

All credit goes to the respective creators of the course.

The course was published on February 5, 2021 and thus used older versions of programs and frameworks. This project aims to contribute to Junior's work by updating and fixing problems posed by outdated versions.

## Versions

- IntelliJ Ultimate 2021.2.2
- MySQL 8.0.26
- Java 16.0.1
- Spring Boot 2.5.4
- Bootstrap 4.2.1
- Apache Tomcat 9.0.52
- Hibernate ORM Core 5.4.32.Final

## Database

The MySQL configuration can be confirmed in `src/main/resources` under `application.properties`, including:

- Url: `jdbc:mysql://localhost:3306/employeemanager`
- Username: `root`
- Password: `password`

![Database Structure](D:\Users\Jan\Documents\GitHub\employeemanager\screenshots\database.png)

## Fixes

On the backend side of the EmployeeManager app, there was but only one problem to fix. Spring threw a persistence error when trying to delete Employees via the frontend. This was fixed by adding a `@Transactional`-annotation to the `deleteEmployee`-method in the `EmployeeService`-class.
