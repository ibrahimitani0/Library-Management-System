# Library Management System

A full-stack **Library Management System (LMS)** built using **Angular**, **Java**, **Spring Boot**, and **MySQL**.
The application allows users to browse books, manage orders, and interact with a modern library platform while providing administrators and librarians with management tools and analytics.

---

## Tech Stack

### Frontend

* Angular

### Backend

* Java
* Spring Boot
* Spring Data JPA / Hibernate
* Spring Security (role-based authentication)

### Database

* MySQL

### Analytics / Visualization

* Chart-based dashboards (planned)

---

## Project Architecture

The application follows a **layered architecture** separating the frontend, backend API, and database.

```
Angular Frontend
        |
        v
Spring Boot REST API
        |
        v
MySQL Database
```

The backend exposes REST APIs which are consumed by the Angular frontend.

---

## Core Features

### User Features

* Browse and search books
* Filter books by category
* View latest books
* View most searched books
* Add books to cart
* Place orders
* Manage account information

### Librarian Features

* Manage book inventory
* Update book availability
* Manage library catalog

### Admin Features

* Manage users and roles
* View analytics dashboard
* Monitor book popularity and order trends

---

## Pages / Modules

### Public Pages

* Homepage
* Book search and filtering
* Books grid page
* Book details

### User Pages

* Login
* Registration
* Account page
* Cart
* Orders

### Admin / Librarian Pages

* Book management
* Inventory control
* Metrics and analytics dashboard

---

## Authentication & Roles

Role-based access control is implemented with three user roles:

```
Admin
Librarian
User
```

### Permissions

**User**

* Browse books
* Search books
* Add to cart
* Place orders

**Librarian**

* Add or update books
* Manage inventory
* Monitor borrowing activity

**Admin**

* Manage users
* Manage system data
* View analytics and metrics

---

## Analytics Dashboard

The system includes a metrics page showing:

* Book popularity
* Top searched books
* Orders over time
* Market trends

Data is visualized using chart components in the frontend.

---

## Database Design

The system uses **MySQL** as the primary relational database.

Main tables include:

```
users
roles
books
authors
categories
book_copies
orders
order_items
cart
borrow_records
reviews
search_logs
```

These tables support authentication, book management, order processing, and analytics tracking.

---

## Backend Structure (Spring Boot)

```
src/main/java/com/lms

controller
service
repository
entity
dto
config
security
```

### Layers

**Controller**
Handles REST API endpoints.

**Service**
Contains business logic.

**Repository**
Handles database access using Spring Data JPA.

**Entity**
Represents database tables.

---

## Frontend Structure (Angular)

```
src/app

pages
services
models
components
guards
```

### Major Modules

* Home
* Books
* Cart
* Orders
* Account
* Admin Dashboard
* Analytics

---

## Installation & Setup

### Prerequisites

Make sure you have the following installed:

* Node.js
* Angular CLI
* Java 17+
* Maven
* MySQL

---

### 1. Clone the Repository

```
git clone https://github.com/ibrahimitani0/library-management-system.git
cd library-management-system
```

---

### 2. Database Setup

Create a MySQL database:

```
CREATE DATABASE lms_db;
```

Update `application.properties` in the Spring Boot project:

```
spring.datasource.url=jdbc:mysql://localhost:3306/lms_db
spring.datasource.username=[root]
spring.datasource.password=[example-password]

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
```

---

### 3. Run Backend (Spring Boot)

```
cd backend
mvn spring-boot:run
```

Backend will start on:

```
http://localhost:8080
```

---

### 4. Run Frontend (Angular)

```
cd frontend
npm install
ng serve
```

Frontend will start on:

```
http://localhost:4200
```

---

## Author

Developed by **Ibrahim Itani**.
