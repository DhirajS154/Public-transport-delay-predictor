# Software Requirements Specification (SRS)
## Public Transport Delay Predictor

---

## 1. Introduction

### 1.1 Purpose
The purpose of this project is to design and develop a web-based Public Transport Delay Predictor that helps users identify and understand possible transport delays before they happen. The system will use historical and real-time transport data to provide predictive delay information and help users make better travel decisions. :contentReference[oaicite:0]{index=0}

### 1.2 Scope
The Public Transport Delay Predictor is a full-stack web application. It allows users to search routes and stations, view predicted delays, save preferred routes, and access transport performance information through charts and dashboards. The system aims to improve commuter convenience, travel planning, and decision-making. :contentReference[oaicite:1]{index=1}

### 1.3 Intended Audience
This document is intended for:
- Project team members
- Lecturers and assessors
- Developers and testers
- Stakeholders involved in the project

### 1.4 Definitions, Acronyms, and Abbreviations
- **SRS**: Software Requirements Specification
- **SDLC**: Software Development Life Cycle
- **UI**: User Interface
- **API**: Application Programming Interface
- **DB**: Database

---

## 2. Overall Description

### 2.1 Product Perspective
This system is a standalone web-based platform that predicts public transport delays using available datasets. It combines route searching, data analysis, prediction, and dashboard visualization in one solution. :contentReference[oaicite:2]{index=2}

### 2.2 Product Functions
The main functions of the system are:
- User registration and login
- Search transport routes and stations
- Predict possible delays
- Display delay probabilities
- Save preferred routes
- Show charts and visual reports
- Optional notifications for saved routes :contentReference[oaicite:3]{index=3}

### 2.3 User Classes and Characteristics
The main users of the system are:

#### Daily Commuters
People who use buses, trains, or metro services regularly for work or study.

#### Students
Students who depend on public transport to travel to university or college.

#### Tourists and Visitors
People unfamiliar with the public transport system who need route and delay guidance.

#### Transport Administrators (Optional)
System managers or admins who manage transport data and monitor the platform.

### 2.4 Operating Environment
- Frontend: Web browser
- Backend: Server-side application
- Database: Relational database
- Hosting: Cloud deployment environment :contentReference[oaicite:4]{index=4}

### 2.5 Constraints
- The project must be completed within 12 weeks.
- The product is a prototype web application.
- It should use modern development frameworks.
- Real-time data may depend on API availability.
- The system should be simple and easy to use.

### 2.6 Assumptions and Dependencies
- Historical transport data is available.
- Real-time transport data is available or can be simulated.
- Users have internet access.
- Cloud hosting is available for deployment.

---

## 3. User Personas

### Persona 1: Daily Commuter
**Name:** Sarah  
**Age:** 28  
**Occupation:** Office Worker  
**Goal:** Reach work on time and avoid delayed routes  
**Needs:** Quick route search, delay prediction, and notifications  

### Persona 2: Student
**Name:** James  
**Age:** 21  
**Occupation:** University Student  
**Goal:** Plan travel to class efficiently  
**Needs:** Easy delay checking and alternative route awareness  

### Persona 3: Tourist
**Name:** Anna  
**Age:** 32  
**Occupation:** Visitor  
**Goal:** Understand public transport routes and avoid disruptions  
**Needs:** Simple interface and route search with predictions  

---

## 4. User Stories

- As a commuter, I want to search my route so that I can check whether delays are likely.
- As a student, I want to save my preferred route so that I can quickly view updates later.
- As a user, I want to see delay probability so that I can decide whether to leave earlier.
- As a tourist, I want to search stations easily so that I can plan my journey.
- As a user, I want to see transport performance charts so that I can understand common delay patterns.
- As a user, I want notifications for my saved routes so that I can stay informed about possible delays.

---

## 5. Functional Requirements

### 5.1 User Registration and Login
- The system shall allow users to create an account using email and password.
- The system shall allow registered users to log in securely.
- The system shall allow users to log out.

### 5.2 Route Search
- The system shall allow users to search for transport routes.
- The system shall allow users to search for stations or stops.
- The system shall display relevant route information.

### 5.3 Delay Prediction
- The system shall analyze historical transport data.
- The system shall use real-time data where available.
- The system shall predict possible delays for selected routes.
- The system shall display delay probability or estimated risk level.

### 5.4 Save Preferred Routes
- The system shall allow users to save preferred routes.
- The system shall allow users to view saved routes.
- The system shall allow users to delete saved routes.

### 5.5 Dashboard and Visualization
- The system shall display delay trends using charts or graphs.
- The system shall show route performance information.
- The system shall present prediction results clearly.

### 5.6 Notifications (Optional)
- The system shall notify users about predicted delays for saved routes.
- The system shall allow users to enable or disable notifications.

---

## 6. Non-Functional Requirements

### 6.1 Performance Requirements
- The system should display search and prediction results quickly.
- The system should support multiple users at the same time.

### 6.2 Usability Requirements
- The system should be simple, clear, and easy to navigate.
- The interface should be suitable for desktop and mobile browsers.

### 6.3 Security Requirements
- User passwords must be stored securely.
- The system should use secure authentication.
- Data transfer should use HTTPS.

### 6.4 Reliability Requirements
- The system should provide consistent results.
- The system should handle missing or incomplete data properly.

### 6.5 Scalability Requirements
- The system should be able to support more users and more routes in the future.

### 6.6 Maintainability Requirements
- The system should be built with clean and modular code.
- The system should be easy to update and improve.

---

## 7. External Interface Requirements

### 7.1 User Interface
The system interface should include:
- Login and registration page
- Route and station search page
- Delay prediction results page
- Dashboard page with graphs and charts
- Saved routes page

### 7.2 Software Interface
The system may connect with:
- Transport data APIs
- Authentication services
- Database system
- Cloud hosting platform

### 7.3 Communication Interface
- The system shall use internet-based communication.
- The system shall support secure API communication using HTTPS.

---

## 8. Core Features Summary
The core features of the project are:
- User account management
- Route and station search
- Delay prediction
- Delay probability display
- Dashboard and data visualization
- Saved routes
- Optional notifications :contentReference[oaicite:5]{index=5}

---

## 9. Primary Users and Their Goals

### Primary Users
- Daily commuters
- Students
- Tourists

### Their Goals
- Check possible delays before travel
- Save regular routes
- Plan trips more efficiently
- Avoid disruptions and missed connections

### Actions They Will Perform
- Create an account
- Log in
- Search routes and stations
- View delay predictions
- Save routes
- Check dashboard reports
- Receive notifications

---

## 10. Conclusion
This SRS defines the main requirements for the Public Transport Delay Predictor. The system is designed to help public transport users make smarter travel decisions by predicting delays before they occur. It provides useful features such as route search, saved routes, delay prediction, and dashboard visualization, making it a practical and user-friendly transport solution. :contentReference[oaicite:6]{index=6}