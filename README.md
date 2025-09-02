<h1>
  <img src="https://github.com/YuliiaNisha/images/blob/99649a30cef8beb0bb4728d4afd4801861e0b408/icon-black150height.png" style="vertical-align: middle;">
  Online Bookstore API 
</h1>


# 📚 Online Bookstore API

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/YuliiaNisha/online-bookstore)
[![Java](https://img.shields.io/badge/Java-17-orange)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.1.0-brightgreen)](https://spring.io/projects/spring-boot)
[![Swagger](https://img.shields.io/badge/Swagger-API-blueviolet)](http://localhost:8080/swagger-ui.html)
[![GitHub issues](https://img.shields.io/github/issues/YuliiaNisha/online-bookstore)](https://github.com/YuliiaNisha/online-bookstore/issues)

<p align="center">
  <img src="https://github.com/YuliiaNisha/images/blob/99649a30cef8beb0bb4728d4afd4801861e0b408/icon-black150height.png">
</p>


> Simple, efficient, and secure — the basic functionality of an online bookstore in one API.

---

## Description

Online Bookstore API is a **RESTful application** that provides the essential features of an online bookstore:  
- Browsing and searching for books  
- Managing categories  
- Placing orders  
- User registration and login  

Its strength lies in its **simplicity and efficiency**: the project is lightweight, easy to understand, and at the same time offers the **core functionality of a real-world e-commerce application**.

This project employs:  
- **Spring Boot**, **Spring Data JPA**, and **Spring Security** to simplify development and reduce boilerplate code while maintaining full functionality and security.  
- **Swagger** to provide clear and user-friendly API documentation.  
- **MapStruct** to simplify mapping between entities and DTOs.  

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
2. **Accessible only to users with the ADMIN role**  
3. **Accessible only to users with the USER role**

---

## Setup & Usage

### Environment Variables
1. Create a `.env` file in the project root.  
2. Copy `.env.sample` into your `.env` file.  
3. Fill in the required credentials (database URL, username, password, etc.).
