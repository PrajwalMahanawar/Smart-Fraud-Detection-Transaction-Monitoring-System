# Smart Fraud Detection & Transaction Monitoring System

A Java Spring Boot backend application that simulates banking-style transaction monitoring and fraud-risk analysis. The system processes financial transactions, evaluates fraud risk using rule-based detection logic, flags suspicious activities, and generates fraud alerts for operational monitoring.

## Features

* Transaction processing APIs
* Fraud-risk scoring engine
* Rule-based suspicious transaction detection
* Fraud alert generation
* RESTful backend APIs
* PostgreSQL database integration
* Layered Spring Boot architecture
* JPA/Hibernate persistence
* Postman API testing support

---

## Tech Stack

* Java 17
* Spring Boot
* Spring Data JPA
* PostgreSQL
* Maven
* Lombok
* REST APIs
* Postman

---

## Project Structure

```bash
src/main/java/com/prajwal/frauddetection
│
├── controller
├── dto
├── entity
├── repository
├── service
├── security
└── FraudDetectionApplication.java
```

---

## Fraud Detection Rules

The system currently evaluates fraud risk based on:

* High-value transactions
* Multiple rapid transactions within short time windows
* Transactions from suspicious or unknown locations

Transactions exceeding the configured fraud threshold are automatically flagged and stored as fraud alerts.

---

## API Endpoints

### Transactions

#### Create Transaction

```http
POST /api/transactions
```

#### Get All Transactions

```http
GET /api/transactions
```

---

### Fraud Alerts

#### Get All Fraud Alerts

```http
GET /api/alerts
```

---

## Sample Transaction Request

```json
{
  "accountNumber": "ACC1001",
  "amount": 9000,
  "transactionType": "TRANSFER",
  "location": "Unknown"
}
```

---

## Sample Response

```json
{
  "id": 1,
  "accountNumber": "ACC1001",
  "amount": 9000,
  "transactionType": "TRANSFER",
  "location": "Unknown",
  "status": "FLAGGED",
  "riskScore": 65
}
```

---

## Database Setup

Create PostgreSQL database:

```sql
CREATE DATABASE fraud_detection_db;
```

---

## Configure application.properties

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/fraud_detection_db
spring.datasource.username=postgres
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## Run the Project

### Clone Repository

```bash
git clone https://github.com/PrajwalMahanawar/Smart-Fraud-Detection-Transaction-Monitoring-System.git
```

### Navigate to Project

```bash
cd Smart-Fraud-Detection-Transaction-Monitoring-System
```

### Run Spring Boot Application

```bash
./mvnw spring-boot:run
```

---

## Future Improvements

* Spring Security + JWT Authentication
* Role-based access control
* Kafka-based real-time transaction streaming
* Redis caching
* ML-based anomaly detection
* Docker containerization
* Swagger/OpenAPI documentation
* Unit and integration testing

---

## Learning Outcomes

This project helped strengthen understanding of:

* Java Spring Boot backend development
* REST API architecture
* Enterprise transaction workflows
* Fraud monitoring systems
* PostgreSQL database integration
* Layered application design
* API testing and debugging

---

## Author

### Prajwal Mahanawar

* GitHub: https://github.com/PrajwalMahanawar
* LinkedIn: https://www.linkedin.com/in/prajwal-mahanawar-710325222/
