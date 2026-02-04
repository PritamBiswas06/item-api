# 📦 Item API

A simple Spring Boot RESTful API for managing items using in-memory storage.  
This project demonstrates backend development skills including REST API design, input validation, and clean code structure.

---

## 🚀 Tech Stack
- Java 21
- Spring Boot 4.0.2
- Spring Web
- Jakarta Validation
- Maven

---

## 📌 Features
- Add a new item
- Get an item by ID
- Input validation for required fields
- In-memory data storage using ArrayList
- Clean layered architecture (Controller → Service → Model)

---

## ▶️ How to Run the Application

### Prerequisites
- Java 21
- Maven

### Run Locally
```bash
mvn spring-boot:run
```

The application will start at:
```
http://localhost:8080
```

---

## 🔌 API Endpoints

### 1️⃣ Add New Item
**POST** `/items`

**Request Body**
```json
{
  "name": "iPhone 15",
  "description": "Apple smartphone",
  "price": 79999
}
```

**Response**
```json
{
  "id": 1,
  "name": "iPhone 15",
  "description": "Apple smartphone",
  "price": 79999
}
```

---

### 2️⃣ Get Item by ID
**GET** `/items/{id}`

Example:
```
GET /items/1
```

**Response**
```json
{
  "id": 1,
  "name": "iPhone 15",
  "description": "Apple smartphone",
  "price": 79999
}
```

If the item does not exist:
```
404 Not Found
```

---

## ✅ Input Validation
- `name` and `description` must not be empty
- `price` must not be null

If validation fails, the API returns:
```
400 Bad Request
```

---

## 🌍 Live Application
```
https://<your-render-link>.onrender.com
```

---

## 📁 Project Structure
```
src/main/java/com/example/itemapi
 ├── controller
 │    └── ItemController.java
 ├── model
 │    └── Item.java
 ├── service
 │    └── ItemService.java
 └── ItemApiApplication.java
```

---

## 📝 Notes
- This application uses in-memory storage, so data will be lost when the application restarts.
- Designed as a sample backend task to demonstrate RESTful API development using Spring Boot.

---

## 👤 Author
Pritam Kumar Biswas
