
# 🏠 Airbnb Clone Project

## 📌 Project Overview

The Airbnb Clone Project is a full-stack web development project inspired by Airbnb. It aims to simulate a scalable and secure booking platform with core features such as property listings, bookings, user management, and payments.

## 🎯 Project Goals

- Understand and implement backend architecture using Django
- Design and manage a relational database with MySQL
- Practice collaborative development and GitHub workflows
- Implement secure APIs and CI/CD pipelines for deployment

## ⚙️ Tech Stack

- Django (Backend Framework)
- MySQL (Database)
- GraphQL (API Layer)
- Docker (Containerization)
- GitHub Actions (CI/CD)


👥 Team Roles


| Role                             | Responsibility                                                                    |
| -------------------------------- | --------------------------------------------------------------------------------- |
| **Backend Developer**            | Develop the business logic, APIs, and integrate with the database                 |
| **Database Administrator (DBA)** | Design and maintain the database schema and ensure data integrity                 |
| **DevOps Engineer**              | Set up and manage CI/CD pipelines, Docker containers, and deployment environments |
| **Security Analyst**             | Ensure secure authentication, authorization, and safe data handling               |
| **Project Manager**              | Oversee project progress, coordinate tasks, and manage team communication         |




## ⚙️ Technology Stack


| Technology     | Purpose |
|----------------|---------|
| **Django**     | A high-level Python web framework used to build robust and scalable backend systems and REST APIs. |
| **MySQL**      | A relational database management system for storing user data, properties, bookings, and payments. |
| **GraphQL**    | A modern API query language for efficient and flexible data retrieval between the client and server. |
| **Docker**     | Used for containerizing the application, ensuring consistency across development and deployment environments. |
| **GitHub Actions** | Automates testing, building, and deployment as part of the CI/CD pipeline. |
| **Markdown**   | Used for project documentation like this README file. |
| **Git**        | Version control system for tracking code changes and collaborating with team members. |



## 🗃️ Database Design

### 🔹 Users
- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `role` (e.g., host or guest)

### 🔹 Properties
- `id` (Primary Key)
- `owner_id` (Foreign Key → Users)
- `title`
- `location`
- `price_per_night`

### 🔹 Bookings
- `id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `property_id` (Foreign Key → Properties)
- `start_date`
- `end_date`

### 🔹 Reviews
- `id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `property_id` (Foreign Key → Properties)
- `rating`
- `comment`

### 🔹 Payments
- `id` (Primary Key)
- `booking_id` (Foreign Key → Bookings)
- `amount`
- `payment_method`
- `status`

### 🔗 Relationships
- A **user** can list multiple **properties**.
- A **user** can make multiple **bookings**.
- Each **booking** is tied to a **property**.
- Each **booking** has a **payment** record.
- A **user** can leave multiple **reviews** for different **properties**.




