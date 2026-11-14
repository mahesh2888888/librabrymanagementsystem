# Library Management System

A console-based Java application using Core Java, OOP, Collections, JDBC and MySQL.

## Features
- Add and list books
- Search books by title
- Register and list members
- Issue and return books
- Track issue history and availability
- Persist data in MySQL

## Requirements
- JDK 17+
- Maven
- MySQL Server 8+
- Eclipse, IntelliJ IDEA or VS Code

## Setup
1. Open MySQL Workbench or the MySQL command line.
2. Run `database/library.sql`.
3. Open `DBConnection.java` and replace `YOUR_MYSQL_PASSWORD` with your MySQL password.
4. Import this folder as an existing Maven project in your IDE.
5. Allow Maven to download dependencies.
6. Run `com.library.Main`.

Database URL: `jdbc:mysql://localhost:3306/library_db`

## Menu
1. Add Book
2. View All Books
3. Search Book by Title
4. Register Member
5. View All Members
6. Issue Book
7. Return Book (enter the Issue ID shown in issue records)
8. View Issue Records
0. Exit

## OOP concepts demonstrated
- Encapsulation: private fields with getters and setters in model classes.
- Abstraction: abstract `Person` class and abstract `displayRole()` method.
- Inheritance: `Librarian` extends `Person`.
- Polymorphism: `Librarian` overrides `displayRole()`.

## Collections
`ArrayList` is used to collect book and member records returned from MySQL. The in-memory lists are populated from database query results.

## JDBC
DAO classes use JDBC, `PreparedStatement`, `ResultSet`, and try-with-resources. Issue and return operations use database transactions to keep book stock and issue records consistent.

## Important note
This is an educational starter project. For a production system, add authentication, role-based access, input validation, logging, due dates, fines, and stronger transaction/concurrency tests.
