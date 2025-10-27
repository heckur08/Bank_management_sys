# Bank Management System

A full-stack **Bank Management System** built using **Spring Boot (backend)** and **Angular (frontend)**.
This application supports account creation, deposits, withdrawals, fund transfers, and user authentication with API documentation via Swagger.

---

## Tech Stack

### Backend (Spring Boot)
* **Java 17+**
* **Spring Boot**
* **Spring Data JPA**
* **PostgreSQL** (Database)
* **Maven** (Build Tool)
* **REST API**
* **Swagger UI** (API Documentation)

### Frontend (Angular)
* **Angular** Framework
* **TypeScript**
* **HTML, CSS**
* **Bootstrap**
* **jQuery**

---

## 📂 Project Structure

The repository is organized into a monorepo structure for easy management of the independent frontend and backend services:

```
Bank_management_sys/
│
├── backend/                  → Spring Boot project (REST API)
│   ├── src/                  → Java source code (controllers, services, models)
│   ├── pom.xml               → Maven build configuration
│   └── ...                   → Other backend resources
│
├── frontend/                 → Angular application (Client UI)
│   ├── src/                  → Angular source code (components, services, routing)
│   ├── angular.json          → Angular workspace configuration
│   ├── package.json          → Node.js dependencies and scripts
│   └── ...                   → Other frontend assets
│
└── README.md                 → Main documentation
```
## 🛠 Prerequisites

Before running the application, ensure you have the following installed on your system:

* **Java 17+**
* **Maven**
* **Node.js & npm**
* **Angular CLI** (`npm install -g @angular/cli`)
* **PostgreSQL**

---

## 🚀 Setup & Run Instructions

### 1. Database Setup (PostgreSQL)

1.  Create a database instance in PostgreSQL:
    ```sql
    CREATE DATABASE bank_management;
    ```
2.  Update your database connection credentials in the Spring Boot configuration file:
    `backend/src/main/resources/application.properties`

    ```properties
    spring.datasource.url=jdbc:postgresql://localhost:5432/bank_management
    spring.datasource.username=your_username
    spring.datasource.password=your_password
    ```

### 2. Backend Setup (Port: 8080)

1.  Navigate to the backend project directory:
    ```bash
    cd backend
    ```
2.  Build and run the application using Maven:
    ```bash
    mvn spring-boot:run
    ```
    Alternatively, run the application directly via your favorite IDE (IntelliJ, VS Code, etc.).

> **API Documentation:** Once the backend is running, the **Swagger UI** documentation will be available at:
> `http://localhost:8080/swagger-ui/`

### 3. Frontend Setup (Port: 4200)

1.  Navigate to the frontend project directory:
    ```bash
    cd ../frontend
    ```
2.  Install the necessary Node.js packages:
    ```bash
    npm install
    ```
3.  Start the Angular development server:
    ```bash
    ng serve --port 4200
    ```
4.  Access the application in your web browser at:
    `http://localhost:4200/`

> **Note:** Ensure your Angular application's API base URL is correctly configured to point to the Spring Boot server: `http://localhost:8080`.

---

## ⭐ Features

The system currently supports the following core banking functionalities:

*  **Account Creation**
*  **Deposit & Withdrawal** operations
*  **Fund Transfer** between accounts
*  **Secure User Authentication**
*  **Multi-Account Support** for users
*  **Swagger API Docs** for all backend endpoints

---

## How to Contribute

We welcome contributions! To get started:

1.  **Fork** the repository.
2.  Create a new feature branch: `git checkout -b feature/your-feature-name`
3.  Commit your changes: `git commit -m 'feat: Add new feature'`
4.  Push to the branch: `git push origin feature/your-feature-name`
5.  Open a **Pull Request** explaining your changes.

---

## License

This project is intended for **academic and learning purposes** only.
