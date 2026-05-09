# API Design
## Public Transport Delay Predictor

---

## 1. Introduction

### 1.1 Purpose
This document explains the API design for the Public Transport Delay Predictor system. It describes the main REST API endpoints used by the frontend to communicate with the backend and database.

### 1.2 Scope
The API supports user registration, login, route searching, delay prediction, saved routes, dashboard data, and notifications.

---

## 2. API Overview

The system will use REST APIs. The frontend React application will send HTTP requests to the backend Node.js and Express.js server. The backend will process the request, communicate with the database, and return a response to the frontend.

### Base URL

```text
http://localhost:3000/api
```

---

## 3. Authentication APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | /auth/register | Register a new user |
| POST | /auth/login | Login user and return JWT token |
| POST | /auth/logout | Logout user |

### Example Register Request

```json
{
  "name": "Dhiraj",
  "email": "dhiraj@example.com",
  "password": "Password123"
}
```

### Example Login Response

```json
{
  "success": true,
  "message": "Login successful",
  "token": "jwt_token_here"
}
```

---

## 4. Route APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /routes | Get all transport routes |
| GET | /routes/{route_id} | Get details of a selected route |
| GET | /routes/search?keyword=central | Search routes or stations |

### Example Route Response

```json
{
  "route_id": 1,
  "route_name": "Central to Parramatta",
  "start_station": "Central",
  "end_station": "Parramatta"
}
```

---

## 5. Delay Prediction APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /predictions | Get all delay predictions |
| GET | /predictions/{route_id} | Get predicted delay for a selected route |
| POST | /predictions/generate | Generate delay prediction for a route |

### Example Prediction Request

```json
{
  "route_id": 1,
  "weather_condition": "Rain",
  "time_of_day": "Morning Peak"
}
```

### Example Prediction Response

```json
{
  "route_id": 1,
  "route_name": "Central to Parramatta",
  "predicted_delay": "12 minutes",
  "delay_probability": "75%",
  "reason": "Rain and previous delay pattern"
}
```

---

## 6. Saved Route APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | /saved-routes | Save a preferred route |
| GET | /saved-routes/{user_id} | Get all saved routes for a user |
| DELETE | /saved-routes/{saved_route_id} | Remove a saved route |

### Example Save Route Request

```json
{
  "user_id": 1,
  "route_id": 3
}
```

---

## 7. Dashboard APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /dashboard/summary | Get summary of route delays |
| GET | /dashboard/trends | Get delay trend data for charts |
| GET | /dashboard/performance | Get transport performance metrics |

### Example Dashboard Response

```json
{
  "total_routes": 20,
  "delayed_routes": 5,
  "average_delay": "8 minutes"
}
```

---

## 8. Notification APIs

| Method | Endpoint | Description |
|---|---|---|
| GET | /notifications/{user_id} | Get user notifications |
| POST | /notifications | Create a delay notification |
| DELETE | /notifications/{notification_id} | Delete a notification |

### Example Notification Response

```json
{
  "notification_id": 1,
  "message": "Possible 10 minute delay on your saved route",
  "route_id": 3
}
```

---

## 9. Standard Response Format

### Success Response

```json
{
  "success": true,
  "message": "Data retrieved successfully",
  "data": {}
}
```

### Error Response

```json
{
  "success": false,
  "message": "Route not found"
}
```

---

## 10. API Security

The API will use JWT authentication for protected routes. Users must log in before they can save routes, view personal saved routes, or receive notifications.

Security features include:
- password hashing using bcrypt
- JWT token authentication
- protected API routes
- input validation
- HTTPS during deployment

---

## 11. API Data Flow

1. User interacts with the React frontend.
2. Frontend sends an API request to the backend.
3. Backend validates the request.
4. Backend communicates with the database.
5. Prediction module processes delay data if required.
6. Backend returns JSON response.
7. Frontend displays the result to the user.

---

## 12. Conclusion

The API design supports the main functions of the Public Transport Delay Predictor system. It allows users to register, log in, search routes, view delay predictions, save preferred routes, and receive notifications. The REST API structure is simple, clear, and suitable for a full-stack student prototype project.