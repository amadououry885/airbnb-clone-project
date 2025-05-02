
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



## 🧩 Feature Breakdown

### 👤 User Management
Handles user registration, login, profile updates, and role distinction (e.g., host vs. guest). Ensures user data is stored securely with proper authentication and authorization.

### 🏠 Property Management
Allows hosts to list properties with details like location, price, and availability. Enables CRUD (Create, Read, Update, Delete) operations on property listings.

### 📅 Booking System
Guests can search for available properties, select dates, and make bookings. Prevents overlapping bookings and ensures accurate availability tracking.

### 💳 Payment Integration
Enables secure payment processing for bookings. Stores payment history and links each transaction to a booking for transparency.

### ⭐ Review & Rating System
Users can leave reviews and ratings for properties they’ve booked. Helps build trust in the platform and provides feedback to hosts.

### 🔍 Search and Filters
Users can search properties by location, date, price range, and amenities. Improves the user experience by helping guests find exactly what they need.

### 🔐 Admin Dashboard (Optional)
Provides admins with tools to monitor users, properties, reviews, and payments. Ensures overall platform health and quick response to issues.



## 🔐 API Security

To protect user data and ensure secure transactions, the following security measures will be implemented in the backend APIs:

- **Authentication**: Only registered users can access protected endpoints using token-based systems like JWT (JSON Web Tokens).
- **Authorization**: Role-based access control ensures that only users with appropriate permissions (e.g., host, guest, admin) can perform specific actions.
- **Input Validation & Sanitization**: All user inputs are validated and sanitized to prevent common attacks like SQL Injection and Cross-Site Scripting (XSS).
- **Rate Limiting**: API usage will be rate-limited to prevent abuse and brute-force attacks.
- **HTTPS Encryption**: All data in transit will be encrypted using HTTPS to protect sensitive information like passwords and payments.
- **Secure Password Storage**: Passwords are hashed using strong algorithms (e.g., bcrypt) before being stored in the database.

These measures are vital to maintaining the integrity, availability, and confidentiality of the system.


## 🔁 CI/CD Pipeline

CI/CD stands for **Continuous Integration** and **Continuous Deployment**. It is a development practice that allows developers to integrate code changes frequently and automatically test and deploy them. This helps catch bugs early, speeds up delivery, and improves collaboration.

For the Airbnb Clone project, we plan to implement the following CI/CD workflow:

- **Continuous Integration**: Code is automatically tested whenever a new change is pushed to the repository.
- **Continuous Deployment**: Once code passes all tests, it can be deployed automatically to a staging or production environment.

### 🛠 Tools Used:
- **GitHub Actions**: Automates testing and deployment pipelines.
- **Docker**: Ensures the application runs consistently across different environments by containerizing it.
- **Heroku / AWS / Render (optional)**: Can be used for automated deployment and hosting.

This setup allows for faster iterations, fewer bugs in production, and better team productivity.


