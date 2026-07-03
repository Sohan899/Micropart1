# 🚀 Microservices E-Commerce Backend

A scalable **Microservices-based E-Commerce Backend** built using **Node.js**, **Express.js**, **RabbitMQ**, **Nginx**, and **Docker**. The application follows a distributed architecture where each service is independently deployable and communicates asynchronously through RabbitMQ.

---

## 📖 Overview

This project demonstrates how to build a production-ready backend using a **Microservices Architecture**. Each business domain is separated into its own service, improving scalability, maintainability, and fault isolation.

The services are orchestrated using **Docker Compose**, while **Nginx** acts as the API Gateway and Reverse Proxy.

---

## 🏗️ Architecture

```
                        Client
                           │
                           ▼
                    ┌──────────────┐
                    │    Nginx     │
                    │ Reverse Proxy│
                    └──────┬───────┘
                           │
      ┌──────────┬─────────┼──────────┬───────────┐
      ▼          ▼         ▼          ▼
 Customer     Product   Shopping   Gateway
 Service      Service    Service    Service
      │          │         │
      └──────────┼─────────┘
                 ▼
            RabbitMQ Broker
                 │
         Event-driven Communication
```

---

## ✨ Features

- ✅ Microservices Architecture
- ✅ API Gateway
- ✅ Reverse Proxy using Nginx
- ✅ RabbitMQ Message Broker
- ✅ RESTful APIs
- ✅ Dockerized Services
- ✅ Service Isolation
- ✅ Asynchronous Communication
- ✅ Easy Horizontal Scaling
- ✅ Modular Codebase

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| Node.js | Runtime Environment |
| Express.js | Backend Framework |
| RabbitMQ | Message Broker |
| Nginx | Reverse Proxy & Load Balancer |
| Docker | Containerization |
| Docker Compose | Service Orchestration |
| JavaScript | Programming Language |

---

## 📂 Project Structure

```
MicroPart1
│
├── customer/
│   ├── src/
│   ├── package.json
│   └── Dockerfile
│
├── products/
│   ├── src/
│   ├── package.json
│   └── Dockerfile
│
├── shopping/
│   ├── src/
│   ├── package.json
│   └── Dockerfile
│
├── gateway/
│   ├── src/
│   └── package.json
│
├── proxy/
│   └── nginx.conf
│
├── docker-compose.yml
└── README.md
```

---

## 📦 Microservices

### 👤 Customer Service

Responsible for

- Customer Registration
- Login
- Authentication
- Customer Profile Management

---

### 📦 Product Service

Responsible for

- Product Management
- Product Listing
- Inventory Information

---

### 🛒 Shopping Service

Responsible for

- Shopping Cart
- Orders
- Checkout
- Purchase Flow

---

### 🚪 Gateway Service

Acts as the central entry point.

Responsibilities:

- Route Requests
- Authentication Middleware
- Service Discovery
- API Aggregation

---

### 🌐 Nginx Proxy

Handles

- Reverse Proxy
- Request Routing
- Load Distribution
- Single Entry Point

---

### 🐇 RabbitMQ

Used for Event-Driven Communication.

Examples:

- Customer Created
- Product Updated
- Order Created
- Inventory Updated

---

## 🔄 Communication Flow

```
Client
   │
   ▼
Nginx
   │
   ▼
Gateway
   │
   ├────────► Customer Service
   │
   ├────────► Product Service
   │
   └────────► Shopping Service
                  │
                  ▼
             RabbitMQ Events
```

---

## 🚀 Getting Started

### Clone Repository

```bash
git clone https://github.com/Sohan899/Micropart1.git

cd Micropart1
```

---

## Install Dependencies

Inside each service

```bash
npm install
```

---

## Start RabbitMQ

RabbitMQ can be started using Docker.

```bash
docker-compose up
```

---

## Run Services

Example

```bash
cd customer
npm start
```

Similarly

```
customer
products
shopping
gateway
```

---

## 🐳 Run Entire Project

```bash
docker-compose up --build
```

---

## API Flow

```
Client

↓

Nginx

↓

Gateway

↓

Requested Microservice

↓

RabbitMQ (if event required)

↓

Response
```

---

## 📈 Advantages of This Architecture

- Independent deployment
- Better scalability
- Easier maintenance
- Fault isolation
- Event-driven communication
- Loose coupling
- High availability
- Better code organization

---

## 🔮 Future Improvements

- JWT Authentication
- Redis Caching
- Kubernetes Deployment
- CI/CD Pipeline
- Prometheus Monitoring
- Grafana Dashboards
- ELK Logging Stack
- API Documentation using Swagger
- Rate Limiting
- Circuit Breaker Pattern

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository

2. Create your feature branch

```bash
git checkout -b feature/NewFeature
```

3. Commit your changes

```bash
git commit -m "Added new feature"
```

4. Push

```bash
git push origin feature/NewFeature
```

5. Open a Pull Request

---

## 👨‍💻 Author

**Sohan Das**

GitHub: https://github.com/Sohan899
## Frontend part 
Github:-https://github.com/Sohan899/micropart2

---

## 📄 License

This project is licensed under the MIT License.

---
