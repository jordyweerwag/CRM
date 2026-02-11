# Customer Relationship Management System (CRM) 🚀

[![Java](https://img.shields.io/badge/Java-17-blue.svg)](https://adoptium.net/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791.svg)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED.svg)](https://www.docker.com/)
[![Render](https://img.shields.io/badge/Render-Ready-46E3B7.svg)](https://render.com/)

> A **production-grade CRM backend** built with **Java 17** and **Spring Boot**.  
> Designed for enterprise scalability, this RESTful API handles customer management with precision, offering robust CRUD operations, advanced filtering, and analytics.  
> **Now optimized for cloud deployment with Docker and PostgreSQL!**

---

## 🎯 Features

- **Customer Management**:
  - Create, read, update, and delete customers.
  - Granular updates: `firstName`, `lastName`, `email`, `mobileNumber`, `age`.
- **Advanced Filtering**:
  - Search by first name, last name, email, or mobile number.
  - Filter by age ranges and thresholds.
- **Analytics**:
  - Total customer count.
  - Demographic insights (group by age).
- **Bulk Operations**:
  - Insert multiple customers in a single transaction.
- **Production Ready**:
  - **Dockerized**: Multi-stage Docker build for optimized images.
  - **PostgreSQL**: Transitioned from MySQL for better cloud compatibility.
  - **Environment Config**: Secure configuration using environment variables.

---

## ⚙️ Tech Stack

| Layer            | Technology |
|------------------|------------|
| **Backend**      | ![Java](https://img.shields.io/badge/Java-17-007396?logo=java&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?logo=springboot&logoColor=white) |
| **Database**     | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791?logo=postgresql&logoColor=white) |
| **Containerization** | ![Docker](https://img.shields.io/badge/Docker-Container-2496ED?logo=docker&logoColor=white) |
| **Cloud**        | ![Render](https://img.shields.io/badge/Render-Deploy-46E3B7?logo=render&logoColor=white) |
| **Build Tool**   | ![Maven](https://img.shields.io/badge/Maven-Build%20Tool-C71A36?logo=apachemaven&logoColor=white) |

---

## 🚀 Deployment Guide (Render)

This project is configured for seamless deployment on **Render**.

1. **Push to GitHub**: Ensure your code is in a GitHub repository.
2. **Create Web Service**:
   - Link your repo to Render.
   - Render will automatically detect the `render.yaml` Blueprint or `Dockerfile`.
3. **Environment Variables**:
   - You **MUST** set `DB_PASSWORD` in the Render Dashboard environment variables.
   - Other variables (`DB_HOST`, `DB_USER`, `DB_NAME`) are pre-configured in `render.yaml` but can be overridden.

---

## 🛠️ Local Development

1. **Clone & Configure**:
   ```bash
   git clone https://github.com/TanushreeSarkar/crm-system.git
   cd CRM-Sales-Pipeline-main
   ```

2. **Environment Setup**:
   - The project uses an `.env` file or environment variables for database connection.
   - **Important**: To run locally against the remote Render database, ensure your `.env` file uses the **External** database URL.

3. **Run with Maven**:
   ```bash
   mvn spring-boot:run
   ```

4. **Run with Docker**:
   ```bash
   docker build -t crm-app .
   docker run -p 8080:8080 --env-file .env crm-app
   ```

---

## 🧪 API Endpoints

| Method | Endpoint                             | Description                          |
|--------|--------------------------------------|--------------------------------------|
| POST   | `/api/customers/insert`              | Insert a single customer             |
| POST   | `/api/customers/bulk-insert`         | Insert multiple customers            |
| GET    | `/api/customers`                     | Get all customers                   |
| GET    | `/api/customers/{id}`                | Get customer by ID                   |
| PUT    | `/api/customers/update-email/{id}`   | Update email                        |
| GET    | `/api/customers/byage/{age}`         | Get customers by exact age           |
| GET    | `/api/customers/grouped-by-age`      | Group customers by age               |

---

## 🤝 Contributing

Contributions are welcome! Fork the repo, create a feature branch, and submit a PR.

---

## 📬 Contact

- **Email**: [2k22.csaiml.2212256@gmail.com](mailto:2k22.csaiml.2212256@gmail.com)
- **GitHub**: [TanushreeSarkar](https://github.com/TanushreeSarkar)

---
*Built with ❤️ and Spring Boot.*
