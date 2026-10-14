# 🛍️ CartNova — Full-Stack E-Commerce Microservices

A full-stack e-commerce application built with **Java, Spring Boot Microservices, React, and MySQL**. CartNova demonstrates product browsing, shopping cart management, order processing, JWT-based authentication, and simulated checkout.

## ✨ Features

- **Authentication:** Login and JWT-based authentication.
- **Product Catalog:** Browse products, search, filter by category, and view stock.
- **Shopping Cart:** Add items, update quantities, remove products, and calculate totals.
- **Order Management:** Place orders and view order history.
- **Checkout:** Cash on Delivery and simulated online payment.
- **Microservices:** Separate services for users, products, carts, orders, and payments.
- **Service Discovery:** Eureka Server for registering and discovering services.
- **API Gateway:** Centralized entry point for backend API requests.
- **Frontend:** Responsive React shopping interface.

## 🧰 Tech Stack

| Area | Technologies |
|---|---|
| Backend | Java 21, Spring Boot, Spring Cloud |
| Security | Spring Security, JWT |
| Architecture | REST APIs, Microservices, Eureka, API Gateway |
| Database | MySQL |
| Frontend | React, Vite, JavaScript, HTML, CSS |
| Build Tools | Maven, npm |
| Development Tools | IntelliJ IDEA, VS Code, Postman, Git, GitHub |

## 🏗️ Architecture

```text
             React Frontend
                    |
                    v
              API Gateway
                    |
      +-------------+-------------+
      |             |             |
      v             v             v
 User Service  Product Service  Cart Service
      |             |             |
      +-------------+-------------+
                    |
          Order Service
                    |
          Payment Service

       Eureka Service Discovery
       MySQL for persistent data
```

*Conceptual overview. Actual service-to-service communication and database ownership depend on each service's implementation.*

### Backend Services

- **Eureka Server:** Service registration and discovery.
- **API Gateway:** Routes requests to backend services.
- **User Service:** User management and authentication.
- **Product Service:** Product catalog and stock management.
- **Cart Service:** Shopping cart operations.
- **Order Service:** Order creation and management.
- **Payment Service:** Payment records and simulated payment processing.

## 🚀 Getting Started

### Prerequisites

Install the following:

- Java Development Kit (JDK) 21
- Maven
- Node.js and npm
- MySQL Server
- Git
- IntelliJ IDEA and VS Code (recommended)

### 1. Clone the repository

```bash
git clone https://github.com/gayatrikotnana/CartNova-Ecommerce.git
cd CartNova-Ecommerce
```

### 2. Configure the database

Create the MySQL databases required by the services, using the database names specified in each service's configuration.

Configure your local environment variables as required by the application. For example:

```text
DB_USERNAME=your_local_database_username
DB_PASSWORD=your_local_database_password
JWT_SECRET=your_generated_base64_secret
```

Use your own local values. Do not commit real credentials or signing keys to GitHub. The JWT secret must be a strong random Base64-encoded key compatible with the application's signing configuration.

### 3. Start the backend

Open each backend project in IntelliJ IDEA and configure its environment variables.

Start the services in a suitable order:

1. Eureka Server
2. User, product, cart, order, and payment services
3. API Gateway

Confirm each service's configured port, database settings, and required environment variables before starting it.

The API Gateway is configured on port `8087` in the development setup.

### 4. Start the React frontend

Open a terminal in the frontend folder:

```bash
cd cartnova-react
npm install
npm run dev
```

Open the local URL printed by Vite in your terminal. Make sure the frontend API base URL matches your running API Gateway.

## 🔐 Security Notes

- Keep database passwords and JWT signing keys outside source control.
- Use environment variables for sensitive configuration.
- Configure authentication and authorization appropriately for protected endpoints.
- Never commit real user tokens, credentials, or production secrets.

## 💳 Payment Disclaimer

CartNova's online payment and QR functionality is for demonstration and learning purposes only. The demo QR code is not payable, and the application does not transfer real money.

## 🎯 What This Project Demonstrates

- Building REST APIs with Spring Boot.
- Designing a microservices-based application.
- Service discovery and API Gateway routing.
- JWT authentication with Spring Security.
- React frontend and backend integration.
- MySQL database integration.
- API testing with Postman.
- Version control using Git and GitHub.

## 🔮 Future Improvements

- Docker containerization.
- Kafka-based asynchronous communication.
- Automated unit and integration testing.
- AWS deployment.
- Integration with a payment provider's test environment.

## 👩‍💻 Author

**Gayatri Kotnana**

GitHub: [@gayatrikotnana](https://github.com/gayatrikotnana)

---

⭐ If you find this project useful, consider starring the repository.
