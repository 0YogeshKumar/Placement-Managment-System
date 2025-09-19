# Placement Management System API

A robust backend system for a web-based Placement Management System, built with Java and Spring Boot. This project provides RESTful APIs to manage students, colleges, companies, and placement schedules, streamlining the campus recruitment process.

---

## ✨ Features

* **Student Management**: Perform CRUD (Create, Read, Update, Delete) operations for student profiles.
* **Placement Scheduling**: Manage and schedule campus placement drives.
* **Certificate Handling**: Authenticate and manage student certificates.
* **College & Company Management**: Onboard and manage college and corporate partner information.
* **Secure**: Uses environment variables to protect sensitive data like database credentials.

---

## 🛠️ Technologies Used

* **Backend**: Java 21, Spring Boot 3
* **Database**: PostgreSQL
* **Data Access**: Spring Data JPA (Hibernate)
* **API Testing**: Postman
* **Build Tool**: Apache Maven
* **Utilities**: Lombok

---

## 🚀 Getting Started

Follow these instructions to get a local copy up and running.

### **Prerequisites**

* Java Development Kit (JDK) 21 or later
* Apache Maven
* PostgreSQL
* Postman (for API testing)

### **Setup and Installation**

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd placement-management
    ```

2.  **Database Configuration:**
    * Open PostgreSQL and create a new database named `placement_db`.
    * Navigate to `src/main/resources/`.

3.  **Create a local properties file:**
    * Create a new file named `application-local.properties`.
    * Add your database password to this file:
        ```properties
        spring.datasource.password=your_secret_password_here
        ```
    * The main `application.properties` is already configured to use this file, which is ignored by Git.

4.  **Run the application:**
    ```sh
    mvn spring-boot:run
    ```
    The application will start on `http://localhost:8080`.

---

## 📋 API Endpoints

Here are the primary API endpoints available:

| Method | Endpoint                       | Description                               |
| :----- | :----------------------------- | :---------------------------------------- |
| `POST` | `/api/students/`               | Adds a new student.                       |
| `GET`  | `/api/students/`               | Retrieves all students.                   |
| `GET`  | `/api/students/{id}`           | Retrieves a student by their ID.          |
| `GET`  | `/api/students/hallticket/{ht}` | Retrieves a student by hall ticket number. |
| `POST` | `/api/placements/`             | Adds a new placement drive.               |
| `GET`  | `/api/placements/`             | Retrieves all placements.                 |
| `POST` | `/api/certificates/`           | Adds a new certificate.                   |
| `GET`  | `/api/certificates/`           | Retrieves all certificates.               |
| `PUT`  | `/api/certificates/{id}`       | Updates an existing certificate.          |
