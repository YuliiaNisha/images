<h1>
  <img src="https://github.com/YuliiaNisha/images/blob/c7f4ba538e58973789d8ed363dc7a5e329ba8c13/icon-round-70height.png" style="vertical-align: middle;">
  <strong>Online Bookstore API</strong>
</h1>

![Java](https://img.shields.io/badge/Java-17-blue.svg)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.3-brightgreen)
![Maven](https://img.shields.io/badge/Maven-3+-blueviolet)
![MySQL](https://img.shields.io/badge/Database-MySQL-orange)
![JUnit](https://img.shields.io/badge/Tests-JUnit%205-green)
![Testcontainers](https://img.shields.io/badge/Testcontainers-Enabled-informational)
![Swagger](https://img.shields.io/badge/API-Swagger%20UI-lightgreen)

> Simple, efficient, and secure — the basic functionality of an online bookstore in one API.

---
## Table of Contents
- [Description](#description)
- [Technologies & Tools](#technologies--tools)
- [Controllers](#controllers)
- [How to use](#how-to-use)
- [Challenges & Solutions](#challenges--solutions)
- [API Documentation](#api-documentation)

## Description
Online Bookstore API is a **RESTful application** that provides the essential features of an online bookstore:  
- Browsing and searching for books  
- Managing categories  
- Placing orders  
- User registration and login  

Its strength lies in its **simplicity and efficiency**: the project is lightweight, easy to understand, and at the same time offers the **core functionality of a real-world e-commerce application**.
---

## Technologies & Tools
This project employs:  
- **Spring Boot**, **Spring Data JPA**, and **Spring Security** to simplify development and reduce boilerplate code while maintaining full functionality and security.  
- **MapStruct** to simplify mapping between entities and DTOs.  
- **Swagger** to provide clear and user-friendly API documentation.  
---

## Controllers
Controllers provide functionality to manage:  
- Books  
- Categories  
- Orders  
- Shopping cart  

Additionally, the **AuthenticationController** handles user registration and login.

All endpoints can be divided into three groups:  
1. **Publicly accessible** (AuthenticationController)  
2. Accessible only to users with the **ADMIN role**  
3. Accessible only to users with the **USER role**
---

## How to use
### 1. Run Locally
1. Clone the repository
   ```bash
   git clone https://github.com/your-username/online-bookstore.git
   cd online-bookstore
   ```
2. Configure the database in src/main/resources/application.properties

3. Configure Environment Variables
  - Create a `.env` file in the project root.  
  - Copy `.env.sample` into your `.env` file.  
  - Fill in the required credentials (database URL, username, password, etc.).

4. Build the project
```bash
mvn clean install
```

5. Run the application
```bash
mvn spring-boot:run
```

or
```bash
java -jar target/bookstore-0.0.1-SNAPSHOT.jar
```

6. Open Swagger UI in your browser:

http://localhost:8080/swagger-ui/index.html

### 2. Use the AWS Deployment

The project is hosted on AWS so you can test the API directly using the deployed Swagger UI:

👉 http://ec2-16-171-2-102.eu-north-1.compute.amazonaws.com/api/swagger-ui/index.html

From here you can:

Register a new user

Log in and get a JWT token

Browse/search books

Place and manage orders

Try out all endpoints directly in the browser


---

## Challenges & Solutions

### Restricting Access to Endpoints
#### Challenge: 
Certain endpoints needed to be accessible only to users with role ADMIN
#### Solution: 
Integrated Spring Security with JWT tokens and role-based access.

### Entity-to-DTO Mapping
#### Challenge: 
Default MapStruct mapping methods were insufficient for converting some entities to DTOs and back.
#### Solution: 
Implemented custom mapping methods.

---
