# 🏋️ AI-Powered Fitness Tracking System

## 1. Short Description

An AI-powered fitness tracking application built using Java and Spring Boot microservices. The system provides user authentication, fitness activity management, and activity data storage through a distributed backend architecture. It uses MySQL and MongoDB for data persistence and RabbitMQ for asynchronous communication between services.

## 2. Tools and Technologies

- **Language:** Java
- **Backend Framework:** Spring Boot
- **Architecture:** Microservices
- **Service Discovery:** Netflix Eureka
- **API Gateway:** Spring Cloud Gateway
- **Inter-Service Communication:** OpenFeign, RabbitMQ
- **Security:** Spring Security, JWT
- **Databases:** MySQL, MongoDB
- **Build Tool:** Maven
- **API Testing:** Postman
- **Containerization:** Docker

## 3. Features

- **User Authentication:** Secure authentication and authorization using Spring Security and JWT.
- **Activity Management:** Create and manage fitness activity records through REST APIs.
- **Microservices Architecture:** Separates application functionality into independently managed services.
- **Service Discovery:** Uses Netflix Eureka to register and discover microservices.
- **API Gateway:** Provides a centralized entry point for client requests.
- **Inter-Service Communication:** Uses OpenFeign and RabbitMQ for communication between services.
- **Data Persistence:** Stores application data using MySQL and MongoDB.

## 4. Process

1. **User Authentication:** Users authenticate through the authentication service, which uses JWT-based security.
2. **Request Routing:** Client requests are routed through the API Gateway to the appropriate microservice.
3. **Service Discovery:** Eureka helps services locate and communicate with one another.
4. **Activity Management:** The activity service processes fitness activity requests and manages activity records.
5. **Data Storage:** MySQL and MongoDB store the relevant application data.
6. **Asynchronous Communication:** RabbitMQ facilitates message-based communication between services where required.
7. **API Validation:** Postman is used to test endpoints and verify service responses.

## 5. How to Run the Project

### Prerequisites

- Java JDK
- Maven
- MySQL
- MongoDB
- RabbitMQ
- IDE such as IntelliJ IDEA
- Postman (optional, for API testing)

### Step 1: Clone the Repository

```bash
git clone <your-repository-url>
cd <project-folder>
```

### Step 2: Configure the Databases

- Start MySQL and create the required database.
- Start MongoDB and configure the appropriate database connection.
- Update the database credentials and connection URLs in the relevant service configuration files.

### Step 3: Configure RabbitMQ

Start RabbitMQ and configure the connection settings in the application properties. Ensure that the required exchanges and queues are declared by the application or configured before use.

### Step 4: Configure Application Properties

Update each microservice's configuration with the appropriate database credentials, service URLs, ports, and security settings.

### Step 5: Build the Services

From each Spring Boot service directory, run:

```bash
mvn clean install
```

### Step 6: Start the Microservices

Start the services in the order required by your configuration, typically:

1. Eureka Server
2. API Gateway
3. Authentication Service
4. Activity Service
5. Any additional dependent services

Run each service using your IDE or the Maven command:

```bash
mvn spring-boot:run
```

### Step 7: Test the APIs

Open Postman and test the authentication and activity management endpoints. Verify that requests are routed correctly, activity records are stored, and inter-service communication works as expected.

---

**Note:** Update the repository URL, database names, service directories, and configuration details according to your actual project setup. Never commit database passwords, JWT secrets, or other sensitive credentials to GitHub.
