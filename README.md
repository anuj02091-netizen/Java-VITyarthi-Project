# 🎓 Student Management System

> **VITyarthi – Build Your Own Project**
> **VIT Bhopal University**

---

## 📌 Project Overview

The **Student Management System** is a web-based application developed using **Java and Spring Boot** to manage student information digitally.

The system provides a centralized platform for performing essential student record management operations such as **adding, viewing, searching, updating, and deleting student records**.

The project follows a modular architecture using **Spring Boot, Spring Data JPA, REST APIs, and MySQL**. It demonstrates the practical implementation of **CRUD operations, database connectivity, layered architecture, input validation, exception handling, and RESTful web services**.

---

# 🎯 Problem Statement

Managing student records manually using registers, spreadsheets, or separate files can be time-consuming and may result in data duplication, inconsistent information, and difficulty in retrieving records.

Educational institutions require an organized digital system to efficiently manage student information.

Therefore, this project aims to develop a **Student Management System using Spring Boot** that allows users to efficiently create, view, search, update, and delete student records through a structured web-based application.

---

# 🎯 Objectives

The main objectives of this project are:

* To develop a digital system for managing student records.
* To implement CRUD operations using Spring Boot.
* To provide RESTful APIs for student management.
* To connect the application with a relational database.
* To implement database operations using Spring Data JPA.
* To provide input validation and error handling.
* To design a modular and maintainable application.
* To reduce manual student record management.
* To demonstrate practical implementation of Java and Spring Boot concepts.

---

# ✨ Features

## 👨‍🎓 1. Student Registration

The system allows users to add new student records.

Student information may include:

* Student ID
* Student Name
* Email
* Phone Number
* Date of Birth
* Gender
* Course
* Branch
* Semester
* Address

---

## 📋 2. View Student Records

Users can retrieve and view stored student information.

The system provides:

* Complete student list
* Individual student details
* Student academic information
* Student contact information

---

## 🔍 3. Search Student

Students can be searched using different parameters such as:

* Student ID
* Name
* Email
* Course
* Branch

---

## ✏️ 4. Update Student Information

Existing student information can be modified when required.

Users can update:

* Name
* Email
* Phone
* Course
* Branch
* Semester
* Address
* Other student details

---

## 🗑️ 5. Delete Student

The system allows an existing student record to be deleted.

A confirmation mechanism can be used before deleting a record.

---

## 📊 6. Student Analytics

The system can provide basic student statistics such as:

* Total number of students
* Students by branch
* Students by course
* Students by semester

---

## ⚠️ 7. Validation & Error Handling

The application validates incoming data and handles errors such as:

* Empty fields
* Invalid email format
* Duplicate student records
* Student not found
* Invalid student ID
* Database errors
* Invalid API requests

---

# 🧩 Functional Modules

| Module                   | Description                              |
| ------------------------ | ---------------------------------------- |
| **Student Registration** | Creates new student records              |
| **Student Management**   | Displays and manages student information |
| **Search Module**        | Searches student records                 |
| **Update Module**        | Updates existing student information     |
| **Delete Module**        | Deletes student records                  |
| **Database Module**      | Handles database operations              |
| **Validation Module**    | Validates incoming data                  |
| **Exception Handling**   | Handles application errors               |

---

# 🏗️ System Architecture

The application follows a **layered architecture**.

```text
                    ┌─────────────────────┐
                    │        USER         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   REST Controller   │
                    │      Layer          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Service Layer    │
                    │                     │
                    │ Business Logic     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Repository Layer   │
                    │                     │
                    │ Spring Data JPA    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     MySQL Database │
                    └─────────────────────┘
```

---

# 🔄 System Workflow

```text
             START
               │
               ▼
       ┌───────────────┐
       │  User Request │
       └───────┬───────┘
               │
               ▼
       ┌───────────────┐
       │ REST Controller│
       └───────┬───────┘
               │
               ▼
       ┌───────────────┐
       │    Service    │
       │     Layer     │
       └───────┬───────┘
               │
               ▼
       ┌───────────────┐
       │  Validation   │
       └───────┬───────┘
               │
               ▼
       ┌───────────────┐
       │  Repository   │
       │     Layer     │
       └───────┬───────┘
               │
               ▼
       ┌───────────────┐
       │ MySQL Database│
       └───────┬───────┘
               │
               ▼
       ┌───────────────┐
       │     Result    │
       └───────┬───────┘
               │
               ▼
              END
```

---

# 🛠️ Technologies & Tools

### Backend

* **Java**
* **Spring Boot**
* **Spring Web**
* **Spring Data JPA**
* **Hibernate**

### Database

* **MySQL**

### Build Tool

* **Maven**

### Development Tools

* **IntelliJ IDEA / Eclipse / Visual Studio Code**
* **Git**
* **GitHub**
* **Postman**

### Concepts Used

* Object-Oriented Programming
* RESTful APIs
* CRUD Operations
* Spring Boot
* Dependency Injection
* Spring Data JPA
* Hibernate ORM
* Relational Database
* SQL
* Exception Handling
* Input Validation
* Layered Architecture

---

# 📁 Project Structure

```text
student-management-system/
│
├── README.md
├── statement.md
├── pom.xml
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── studentmanagement/
│   │   │           │
│   │   │           ├── StudentManagementApplication.java
│   │   │           │
│   │   │           ├── controller/
│   │   │           │   └── StudentController.java
│   │   │           │
│   │   │           ├── service/
│   │   │           │   └── StudentService.java
│   │   │           │
│   │   │           ├── repository/
│   │   │           │   └── StudentRepository.java
│   │   │           │
│   │   │           ├── model/
│   │   │           │   └── Student.java
│   │   │           │
│   │   │           ├── exception/
│   │   │           │   └── StudentNotFoundException.java
│   │   │           │
│   │   │           └── config/
│   │   │
│   │   └── resources/
│   │       └── application.properties
│   │
│   └── test/
│       └── java/
│
└── diagrams/
    ├── use-case-diagram.png
    ├── class-diagram.png
    ├── sequence-diagram.png
    ├── workflow-diagram.png
    └── er-diagram.png
```

---

# 💾 Database Design

The application uses **MySQL** as the relational database.

## Student Table

| Field      | Data Type | Description      |
| ---------- | --------- | ---------------- |
| student_id | BIGINT    | Primary key      |
| name       | VARCHAR   | Student name     |
| email      | VARCHAR   | Student email    |
| phone      | VARCHAR   | Contact number   |
| dob        | DATE      | Date of birth    |
| gender     | VARCHAR   | Gender           |
| course     | VARCHAR   | Course           |
| branch     | VARCHAR   | Branch           |
| semester   | INT       | Current semester |
| address    | VARCHAR   | Student address  |

---

# 🔄 CRUD Operations

The application implements the four fundamental database operations.

## Create

Adds a new student.

```http
POST /api/students
```

Example request:

```json
{
  "name": "Anuj",
  "email": "anuj@example.com",
  "phone": "9876543210",
  "course": "B.Tech",
  "branch": "ECE",
  "semester": 3
}
```

---

## Read

Get all students:

```http
GET /api/students
```

Get a student by ID:

```http
GET /api/students/{id}
```

---

## Update

Update an existing student:

```http
PUT /api/students/{id}
```

---

## Delete

Delete a student:

```http
DELETE /api/students/{id}
```

---

# 🌐 REST API Endpoints

| HTTP Method | Endpoint             | Purpose           |
| ----------- | -------------------- | ----------------- |
| **POST**    | `/api/students`      | Add student       |
| **GET**     | `/api/students`      | Get all students  |
| **GET**     | `/api/students/{id}` | Get student by ID |
| **PUT**     | `/api/students/{id}` | Update student    |
| **DELETE**  | `/api/students/{id}` | Delete student    |

---

# 💻 Installation & Setup

## Prerequisites

Install the following:

* Java JDK 17 or later
* Maven
* MySQL
* Git
* IntelliJ IDEA / Eclipse / VS Code
* Postman (recommended)

---

## 1. Clone the Repository

```bash
git clone https://github.com/[YOUR-USERNAME]/student-management-system.git
```

Navigate to the project:

```bash
cd student-management-system
```

---

## 2. Create MySQL Database

Open MySQL and create the database:

```sql
CREATE DATABASE student_management;
```

---

## 3. Configure Database

Open:

```text
src/main/resources/application.properties
```

Configure the database connection:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/student_management
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8080
```

Replace `YOUR_PASSWORD` with your MySQL password.

---

# ▶️ Running the Application

Using Maven:

```bash
mvn spring-boot:run
```

Or run the main class:

```text
StudentManagementApplication.java
```

The application will start on:

```text
http://localhost:8080
```

---

# 🧪 Testing

The REST APIs can be tested using **Postman**.

### Test Cases

| Test Case | Operation             | Expected Result            |
| --------- | --------------------- | -------------------------- |
| TC01      | Add valid student     | Student created            |
| TC02      | Add duplicate student | Validation/error response  |
| TC03      | Get all students      | Student list displayed     |
| TC04      | Get student by ID     | Correct student returned   |
| TC05      | Search invalid ID     | Student not found response |
| TC06      | Update student        | Student updated            |
| TC07      | Delete student        | Student deleted            |
| TC08      | Invalid input         | Validation error           |

---

# 🔐 Non-Functional Requirements

## 1. Performance

The application should process common CRUD requests efficiently and provide responses within a reasonable time.

## 2. Usability

REST APIs are designed with simple and predictable endpoints that are easy to understand and test.

## 3. Reliability

The system should maintain data consistency and return appropriate responses for successful and unsuccessful operations.

## 4. Security

Student information should be protected from unauthorized access. Authentication and authorization can be integrated in future versions using Spring Security.

## 5. Maintainability

The application follows a layered architecture separating controllers, services, repositories, and models.

## 6. Scalability

Spring Boot and the layered architecture allow additional modules and functionality to be added without redesigning the complete application.

## 7. Error Handling

The application handles situations such as:

* Student not found
* Invalid input
* Duplicate records
* Database errors
* Invalid API requests

## 8. Resource Efficiency

Spring Data JPA is used to simplify database interaction and reduce unnecessary database-management code.

---

# 🧠 Design Diagrams

The project documentation includes the following diagrams:

### 1. Use Case Diagram

Shows interactions between users and the Student Management System.

### 2. Workflow Diagram

Shows the complete flow of student management operations.

### 3. Sequence Diagram

Shows communication between:

```text
Client
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
Database
```

### 4. Class Diagram

Shows the classes and relationships used in the Spring Boot application.

### 5. ER Diagram

Shows the structure of the student database and its entities.

Diagrams can be stored in:

```text
diagrams/
```

---

# ⚙️ Design Decisions & Rationale

### Spring Boot

Spring Boot was selected to simplify Java backend development and provide a structured framework for building RESTful applications.

### Spring Data JPA

Spring Data JPA reduces boilerplate database-access code and provides convenient repository-based operations.

### Hibernate

Hibernate acts as the ORM layer between Java objects and relational database tables.

### MySQL

MySQL provides reliable relational data storage for student records.

### REST API

RESTful APIs provide a standardized way for clients to communicate with the backend.

### Layered Architecture

The Controller-Service-Repository structure separates responsibilities and improves maintainability.

---

# 🚧 Challenges Faced

During development, the following challenges were addressed:

* Understanding Spring Boot project structure.
* Configuring the MySQL database.
* Connecting Spring Boot with MySQL.
* Implementing CRUD operations.
* Creating REST API endpoints.
* Handling database exceptions.
* Implementing input validation.
* Testing APIs using Postman.
* Maintaining proper project structure.
* Managing the project using Git and GitHub.

---

# 📚 Learnings & Key Takeaways

Through this project, the following concepts were learned and applied:

* Java programming
* Object-Oriented Programming
* Spring Boot
* RESTful API development
* Spring Data JPA
* Hibernate
* MySQL
* CRUD operations
* Dependency Injection
* Layered architecture
* Input validation
* Exception handling
* API testing using Postman
* Git and GitHub
* Software documentation

---

# 🔮 Future Enhancements

The system can be further enhanced with:

* 🔐 User authentication and authorization using Spring Security.
* 👨‍💼 Admin and student roles.
* 📚 Course management.
* 📝 Marks and examination management.
* 📅 Attendance management.
* 📊 Student performance dashboard.
* 📧 Email notifications.
* 📄 PDF report generation.
* 🔎 Advanced search and filtering.
* ☁️ Cloud deployment.
* 📱 Mobile application integration.
* 📈 Advanced analytics.

---

# 📸 Screenshots

Screenshots of the working application and API testing can be added here.

### API Testing – Add Student

![Add Student](screenshots/add-student.png)

### Get Students

![Get Students](screenshots/get-students.png)

### Update Student

![Update Student](screenshots/update-student.png)

### Delete Student

![Delete Student](screenshots/delete-student.png)

> Add your actual screenshots to the `screenshots/` folder.

---

# 📈 VITyarthi Requirement Coverage

| Requirement                 | Status |
| --------------------------- | ------ |
| Problem Statement           | ✅      |
| Objectives                  | ✅      |
| 3+ Functional Modules       | ✅      |
| Input / Output Structure    | ✅      |
| System Architecture         | ✅      |
| Workflow                    | ✅      |
| Use Case Diagram            | ✅      |
| Class Diagram               | ✅      |
| Sequence Diagram            | ✅      |
| ER Diagram                  | ✅      |
| Database Design             | ✅      |
| Non-Functional Requirements | ✅      |
| Validation & Error Handling | ✅      |
| Testing                     | ✅      |
| GitHub Version Control      | ✅      |
| Future Enhancements         | ✅      |

---

# 👨‍💻 Project Information

| Detail                  | Information                             |
| ----------------------- | --------------------------------------- |
| **Project Title**       | Student Management System               |
| **Student Name**        | **Anuj**                                |
| **Registration Number** | **24BEC10114**                          |
| **Branch**              | Electronics & Communication Engineering |
| **Year**                | 2nd Year                                |
| **University**          | VIT Bhopal University                   |
| **Course**              | [COURSE NAME]                           |
| **Academic Year**       | 2026–27                                 |

---

# 📜 License

This project is developed for academic purposes as part of the **VITyarthi – Build Your Own Project** evaluation at **VIT Bhopal University**.

---

# 🙏 Acknowledgement

This project was developed as part of the **VITyarthi – Build Your Own Project** evaluation at VIT Bhopal University.

The project provided an opportunity to apply Java, Spring Boot, database management, REST API development, software architecture, testing, and version-control concepts to a practical real-world problem.

---

# ⭐ Conclusion

The **Student Management System** provides a structured digital solution for managing student records.

By using **Java, Spring Boot, Spring Data JPA, Hibernate, MySQL, and REST APIs**, the project demonstrates how software engineering and database concepts can be combined to develop a modular and maintainable application.

The project fulfills the major technical and documentation requirements of the **VITyarthi – Build Your Own Project** evaluation.
