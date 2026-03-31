# 📢 Campus Notice File Sharing System

A cloud-ready microservice-based campus notice and file sharing management system built using Spring Boot and Spring Cloud.

---

# 🌐 Platform Components

| Service          | Port | Description                          |
| ---------------- | ---- | ------------------------------------ |
| ⚙️ Config Server | 8888 | Centralized configuration management |
| 🟢 Eureka Server | 8761 | Service registration and discovery   |
| 🌐 API Gateway   | 8080 | Single entry point for all services  |

---

# 🏗️ Architecture Overview

This system follows **Microservice Architecture** using **Spring Boot + Spring Cloud**.

```text
Frontend (HTML / CSS / JavaScript)
        ↓
   API Gateway (:8080)
        ↓
 ┌────────┬──────────┬──────────┐
 ↓        ↓          ↓
User   Notice      File
Service Service    Service
```

---

# 🧩 Microservices

## 1. User Service — MySQL

Handles:

* Save user
* Get all users
* Get user by id
* Update user
* Delete user

Database: MySQL

---

## 2. Notice Service — MongoDB

Handles:

* Save notice
* Get all notices
* Get notice by id
* Update notice
* Delete notice

Database: MongoDB (`eca_notice_db` → `notices` collection)

---

## 3. File Service — Local File Storage

Handles:

* Upload files
* View uploaded files
* Delete files

Storage: Local file system

---

# 🗄️ Database

| Type           | Technology | Usage          |
| -------------- | ---------- | -------------- |
| Relational     | MySQL      | User Service   |
| Non-Relational | MongoDB    | Notice Service |

---

# 📦 Repository Structure (Polyrepo + Git Submodules)

```text
Campus-Notice-File-Sharing-System/
├── api-gateway/
├── config-server/
├── eureka-server/
├── user-service/
├── notice-service/
├── file-service/
├── frontend/
└── .gitmodules
```

---

# 🔌 API Flow

| Request         | Routed Through               |
| --------------- | ---------------------------- |
| User Requests   | API Gateway → User Service   |
| Notice Requests | API Gateway → Notice Service |
| File Requests   | API Gateway → File Service   |

---

# 🚀 Local Run Order

1. Start Config Server
2. Start Eureka Server
3. Start API Gateway
4. Start User Service
5. Start Notice Service
6. Start File Service
7. Open Frontend

---

# 🛠️ Tech Stack

* Java 21
* Spring Boot
* Spring Cloud
* Eureka Server
* API Gateway
* Maven
* Git Submodules
* HTML
* CSS
* JavaScript
* MySQL
* MongoDB

---


# 👩‍💻 Author

Dilsha Perera
Higher Diploma in Software Engineering
Enterprise Cloud Architecture
IJSE
