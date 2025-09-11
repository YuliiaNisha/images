# ![Icon](https://raw.githubusercontent.com/YuliiaNisha/images/c7f4ba538e58973789d8ed363dc7a5e329ba8c13/icon-round-70height.png) Online Bookstore API

![Java](https://img.shields.io/badge/Java-17-green.svg)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.3-green)
![Maven](https://img.shields.io/badge/Maven-3+-green)
![MySQL](https://img.shields.io/badge/Database-MySQL-green)
![JUnit](https://img.shields.io/badge/Tests-JUnit%205-green)
![Swagger](https://img.shields.io/badge/API-Swagger%20UI-green)

> Simple, efficient, and secure — the basic functionality of an online bookstore in one API.

---
## Table of Contents
- [Description](#description)
- [Technologies & Tools](#technologies--tools)
- [Controllers](#controllers)
- [Postman](#postman)
- [How to use the API](#how-to-use-the-api)
- [Challenges & Solutions](#challenges--solutions)
- [API Documentation](#api-documentation)

## Description
Online Bookstore API is a RESTful application that provides the essential features of an online bookstore:  
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

| 🌐 PUBLIC Endpoints | 🔒 ADMIN Role Endpoints | 👤 USER Role Endpoints |
|---------------------|-------------------------|---------------------|
| Register         | Create Book          | Get Book By ID      |
| Login            | Update Book          | Get All Books       |
|                  | Delete Book          | Search for Books    |
|                  | Create Category      | Get All Categories  |
|                  | Update Category      | Get Category By ID  |
|                  | Delete Category      | Get Books By Category ID |
|                  | Update Order Status  | Create Order        |
|                  |                      | Get All Orders      |
|                  |                      | Get Order Items By Order ID |
|                  |                      | Get Order Item By ID |
|                  |                      | Get Shopping Cart |
|                  |                      | Add Book To Cart |
|                  |                      | Update Book Quantity in Cart |
|                  |                      | Delete Book From Cart |

---

## Postman  
A Postman collection is available to simplify testing the API.  
👉 [Open Online Bookstore Postman Collection](https://postman.co/workspace/My-Workspace~49ed7a22-2d52-45ef-8ca1-c68f46105379/collection/40367151-d5b4ff87-5102-4633-b53f-afb2a9a5b27e?action=share&creator=40367151)  

How to use this Postman collection:  
1. Click the link above.  
2. Import the collection into your Postman app.  
3. Run requests against http://localhost:8080/api   
4. Authenticate by registering and/or logging in to get a JWT token.
5. Go to the **Authorization** tab.
6. Choose **Bearer Token** as the Auth Type.
7. Paste the JWT token you received into the token field to access all protected endpoints.

👉![Token Flow Diagram](https://raw.githubusercontent.com/YuliiaNisha/images/main/token-flow.png)

---

## How to use the API
### Run Locally
1. Clone the repository
   ```bash
   git clone https://github.com/YuliiaNisha/online-bookstore.git
   cd online-bookstore
   ```
2. Configure the database in src/main/resources/application.properties

3. Configure Environment Variables
  - Create a `.env` file in the project root.  
  - Copy `.env.sample` into your `.env` file.  
  - Fill in the required credentials (database URL, username, password, etc.).

4. Build the project
```bash
mvn clean package
```
5. Run the application
   
6. Open Swagger UI in your browser: http://localhost:8080/swagger-ui/index.html
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
