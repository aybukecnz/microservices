# Microservices Project

This project demonstrates a **microservices architecture** using independent services with **Docker**.  
It includes **user_service** and **payment_service**, each running in its own container, with clearly defined API endpoints for interaction.

## ✨ Features
- Independent microservices:
  - `user_service` – handles user registration, authentication, and management
  - `payment_service` – handles payment processing and related operations
- Dockerized services for easy deployment
- RESTful API endpoints for inter-service communication
- Environment configuration using **Docker Compose**
- Simple testing using `curl` or Postman

## 🛠️ Technologies Used
- Python (FastAPI / Flask or your chosen framework)
- Docker & Docker Compose
- REST API principles
- Optional: Jenkins / CI-CD for automation

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/aybukecnz/microservices.git
   cd microservices
```
2. Build and run services using Docker Compose:
  ```bash
docker-compose up --build
  ```
3. Access services:
user_service: http://localhost:...
payment_service: http://localhost:...

4. Test endpoints using curl or Postman:
  ```bash
curl -X POST http://localhost:.../users -H "Content-Type: application/json" -d '{"username":"...","password":"..."}'

  ```
## 💻 Example API Endpoints
User Service

- POST /users – Register a new user
  
- GET /users/{id} – Get user details
  
- POST /login – Authenticate user

Payment Service

- POST /payments – Create a new payment

- GET /payments/{id} – Get payment details

<img width="1800" height="197" alt="image" src="https://github.com/user-attachments/assets/92a19c4f-4f4a-42bd-9a89-24e7bb9b1618" />
<img width="1257" height="295" alt="image" src="https://github.com/user-attachments/assets/eb6521d7-bf9e-455d-87ea-a6ddfb8d24fe" />



## 📂 Project Structure
  ```bash
microservices/
 ├── user_service/       # User service code and Dockerfile
 ├── payment_service/    # Payment service code and Dockerfile
 ├── docker-compose.yml  # Docker Compose configuration
 ├── README.md           # Documentation
 └── Other files         # Utilities, environment configs
  ```

## 📈 Future Improvements

- Add more microservices (e.g., notification_service, order_service)

- Implement authentication/authorization across services

- Add database integration for persistent storage

- Add unit and integration tests for all services
