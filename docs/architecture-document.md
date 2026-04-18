# Architecture Document
## Public Transport Delay Predictor

---

## 1. Introduction

### 1.1 Purpose
This document explains the technical architecture of the Public Transport Delay Predictor system. It describes the chosen technology stack, overall system design, main services and components, authentication method, and data flow.

### 1.2 Scope
The architecture supports a web-based application that allows users to search public transport routes, view predicted delays, save preferred routes, and receive personalized alerts. The system uses historical and real-time transport data to provide predictive insights.

---

## 2. Architecture Overview

The Public Transport Delay Predictor will use a **monolithic architecture**.

A monolithic architecture is suitable for this project because:
- it is easier to design and develop within a 12-week project timeline
- it is simpler for a student team to manage
- all modules can be built and deployed together
- it reduces complexity compared to microservices

In this architecture, the frontend, backend, authentication, prediction logic, and database will work as one integrated system.

---

## 3. Technology Stack

### 3.1 Frontend
- React
- HTML
- CSS
- JavaScript

### 3.2 Backend
- Node.js
- Express.js

### 3.3 Database
- MySQL or PostgreSQL

### 3.4 Authentication
- JWT (JSON Web Token)
- bcrypt for password hashing

### 3.5 Design and Collaboration Tools
- Figma
- GitHub

### 3.6 Deployment
- Render, Railway, or another cloud platform

---

## 4. Main Components

### 4.1 Frontend Application
The frontend is the user-facing part of the system. It allows users to:
- register and log in
- search routes and stations
- view predicted delays
- see route status and alerts
- access charts and dashboard information

### 4.2 Backend Application
The backend handles:
- API requests from the frontend
- business logic
- communication with the database
- authentication and authorization
- prediction processing

### 4.3 Database
The database stores:
- user account information
- saved routes
- route and station data
- historical delay data
- alert preferences

### 4.4 Prediction Module
The prediction module is responsible for:
- analyzing historical transport data
- using available real-time data
- calculating possible delay probability
- sending prediction results to the backend

### 4.5 Notification Module
The notification module handles:
- personalized delay alerts
- saved route alerts
- future notification support

---

## 5. System Architecture Choice

### Monolith or Microservices?
The system will use a **monolithic architecture**.

### Reason for Choosing Monolith
- easier to build and maintain for a team of 5
- faster development and deployment
- suitable for prototype-level application
- less complex than microservices

### Why Not Microservices?
- microservices require separate services and communication setup
- harder to manage within limited time
- more complex deployment process

---

## 6. Authentication Design

Authentication will work using **JWT-based authentication**.

### Authentication Process
1. User registers with email and password.
2. Password is hashed using bcrypt before storing in the database.
3. User logs in with valid credentials.
4. Backend checks user credentials.
5. JWT token is generated.
6. Token is sent to the frontend.
7. Frontend stores the token.
8. Protected requests include the token.
9. Backend verifies the token before giving access.

### Security Features
- password hashing with bcrypt
- token-based authentication
- protected routes
- input validation
- HTTPS in deployment

---

## 7. Data Flow

### 7.1 Route Search and Prediction Flow
1. User enters a route or station in the frontend.
2. Frontend sends request to the backend API.
3. Backend checks route data.
4. Backend fetches historical and/or real-time transport data.
5. Prediction module processes the data.
6. Delay probability or route status is generated.
7. Backend sends the result back to the frontend.
8. Frontend displays the result to the user.

### 7.2 Login Flow
1. User enters email and password.
2. Frontend sends login request to backend.
3. Backend checks credentials from the database.
4. If valid, a JWT token is generated.
5. Frontend stores the token and user gets access.

### 7.3 Save Route Flow
1. User selects a preferred route.
2. Frontend sends request with token.
3. Backend verifies the token.
4. Backend stores the route in the database.
5. Frontend shows confirmation.

---

## 8. High-Level Architecture Diagram

```text
+----------------------+
|      Frontend        |
|   React Web App      |
+----------+-----------+
           |
           | HTTP Requests
           v
+----------------------+
|       Backend        |
|   Node.js / Express  |
+-----+-----------+----+
      |           |
      |           |
      v           v
+-----------+  +------------------+
| Database  |  | Prediction Module|
| MySQL/PG  |  | Delay Analysis   |
+-----------+  +------------------+
      |
      v
+----------------------+
|   Authentication     |
|   JWT + bcrypt       |
+----------------------+
```

---

## 9. Services and Responsibilities

### Frontend Service
- displays user interface
- collects user input
- shows predictions, route status, and alerts

### Backend Service
- handles API requests
- processes business logic
- connects frontend with database and prediction module

### Database Service
- stores and retrieves application data

### Authentication Service
- manages login and registration
- protects secure routes

### Prediction Service
- analyzes delay-related data
- generates prediction results

### Notification Service
- manages user alerts and saved route updates

---

## 10. Proposed Folder Structure

```text
public-transport-delay-predictor/
│
├── README.md
├── problem-statement.md
├── market-research.md
├── srs.md
├── architecture-document.md
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/        # Reusable UI components
│   │   ├── pages/             # Main pages (Login, Dashboard, Route Search)
│   │   ├── services/          # API calls
│   │   ├── assets/            # Images, icons, styles
│   │   ├── hooks/             # Custom hooks (optional)
│   │   └── App.js
│   └── package.json
│
├── backend/
│   ├── routes/                # API routes
│   ├── controllers/           # Business logic
│   ├── models/                # Database models
│   ├── middleware/            # Auth middleware
│   ├── services/              # Prediction logic and external APIs
│   ├── config/                # DB config and environment setup
│   ├── server.js
│   └── package.json
│
└── database/
    ├── schema.sql             # Database structure
    └── seed.sql               # Sample data
```

### Why this Folder Structure?
This folder structure keeps the project organized by separating the frontend, backend, and database parts. It supports teamwork, makes the code easier to manage, and allows the system to grow in the future.

---

## 11. Non-Functional Considerations

### Performance
- search and prediction results should load quickly

### Security
- passwords must be stored securely
- routes should be protected with token validation

### Scalability
- the system should support more users and more data in future

### Maintainability
- code should be modular and easy to update

### Usability
- interface should be simple, clear, and responsive

---

## 12. Conclusion

The Public Transport Delay Predictor will use a monolithic architecture because it is simple, practical, and suitable for a student prototype project. React will be used for the frontend, Node.js and Express for the backend, and MySQL or PostgreSQL for the database. Authentication will use JWT and bcrypt, while the prediction module will process transport data and generate delay insights for users.
