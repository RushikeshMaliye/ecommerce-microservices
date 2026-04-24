# 🧩 E-Commerce Microservices System

A distributed microservices-based backend system built using Spring Boot, demonstrating real-world architecture patterns like service isolation, database per service, and scalable infrastructure setup.

---

## 📦 Services

This system is composed of the following independent microservices:

* **User Service**
  Handles user registration, authentication, and profile management
  🔗 https://github.com/RushikeshMaliye/user-service

* **Product Service**
  Manages product catalog, pricing, and inventory
  🔗 https://github.com/RushikeshMaliye/product-service

* **Order Service**
  Handles order placement and order lifecycle
  🔗 https://github.com/RushikeshMaliye/order-service

---

## 🏗️ Architecture Overview

* Each microservice is independently deployable
* Database per service (PostgreSQL)
* Services communicate via REST (Feign integration planned)
* Infrastructure managed using Docker

---

## 🐳 Infrastructure Setup (PostgreSQL via Docker)

### ▶ Start Database

```bash
docker-compose up -d
```

---

### 🗄️ Databases Created Automatically

* `userdb`
* `productdb`
* `orderdb`

> These are initialized using `db-init/init.sql`

---

### ⏹️ Stop Containers

```bash
docker-compose down
```

---

## 🚀 Running the Services

Run each service locally from your IDE:

| Service         | Port |
| --------------- | ---- |
| User Service    | 8081 |
| Product Service | 8082 |
| Order Service   | 8083 |

---

## ⚙️ Configuration

All services connect to PostgreSQL running on:

```yaml
jdbc:postgresql://localhost:5432/<service-db>
```

Default credentials:

```
username: postgres
password: postgres
```

---

## 🛠️ Tech Stack

* Java 17
* Spring Boot
* Spring Data JPA
* PostgreSQL
* Docker

---

## 📌 Key Features

* Microservices architecture
* Database per service pattern
* Docker-based infrastructure setup
* Clean separation of concerns

---

## 🚧 Upcoming Enhancements

* Service Discovery (Eureka)
* API Gateway (Spring Cloud Gateway)
* Inter-service communication using OpenFeign
* Event-driven architecture using Kafka
* Centralized configuration (Config Server)
* Dockerizing all microservices

---

## 👨‍💻 Author

Rushikesh
Shraddha

---

## ⭐ How to Use

1. Clone this repository
2. Run `docker-compose up -d`
3. Start each microservice locally
4. Test APIs using Postman or Swagger

---

## 📈 Goal of This Project

To demonstrate production-grade microservices architecture and best practices for scalable backend systems.
