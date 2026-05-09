# UI/UX Design
## Public Transport Delay Predictor

---

## 1. Introduction

### 1.1 Purpose
This document explains the UI/UX design for the Public Transport Delay Predictor system. It describes the main screens, user navigation flow, wireframes, and UI components used in the application.

### 1.2 Scope
The UI/UX design focuses on creating a simple, responsive, and user-friendly interface that allows users to search transport routes, view predicted delays, save preferred routes, and receive alerts.

---

## 2. Design Goals

The system interface is designed to:
- be simple and easy to use
- provide quick access to route information
- display delay predictions clearly
- support responsive web design
- improve user experience with clean navigation

---

## 3. Main Screens

### 3.1 Login Screen
The login screen allows users to access their accounts securely.

#### Features
- email input field
- password input field
- login button
- register link

---

### 3.2 Register Screen
The register screen allows new users to create an account.

#### Features
- full name input
- email input
- password input
- confirm password field
- register button

---

### 3.3 Dashboard Screen
The dashboard is the main screen of the system.

#### Features
- route search bar
- delay summary cards
- saved routes section
- transport status overview
- navigation menu

---

### 3.4 Route Search Screen
Users can search transport routes and stations.

#### Features
- search input
- route results list
- route details
- predicted delay information

---

### 3.5 Delay Prediction Screen
Displays predicted delay details for selected routes.

#### Features
- route information
- predicted delay time
- delay probability
- charts and graphs
- traffic or weather information

---

### 3.6 Saved Routes Screen
Displays user saved routes.

#### Features
- saved route list
- route status
- delete saved route button

---

### 3.7 Notification Screen
Shows personalized delay alerts.

#### Features
- alert messages
- route notifications
- delay warnings

---

## 4. User Navigation Flow

### Main User Flow

1. User opens the application.
2. User registers or logs in.
3. User accesses dashboard.
4. User searches transport routes.
5. User views predicted delays.
6. User saves preferred routes.
7. User receives notifications and alerts.

---

## 5. Navigation Structure

```text
Login/Register
       |
       v
   Dashboard
       |
------------------------------------------------
|            |            |                    |
v            v            v                    v
Search    Predictions   Saved Routes     Notifications
```

---

## 6. UI Components

### Buttons
- login button
- register button
- search button
- save route button

### Forms
- login form
- registration form
- route search form

### Cards
- delay information cards
- dashboard summary cards
- route status cards

### Navigation Components
- top navigation bar
- sidebar menu
- footer section

### Charts and Visuals
- delay trend charts
- route performance graphs
- transport status indicators

---

## 7. Wireframe Descriptions

### Login Wireframe
```text
--------------------------------
|          Logo                |
|                              |
|  Email Input                 |
|  Password Input              |
|                              |
|  [ Login Button ]            |
|                              |
|  Register Link               |
--------------------------------
```

---

### Dashboard Wireframe
```text
------------------------------------------------
| Navbar                                       |
------------------------------------------------
| Search Bar                                   |
------------------------------------------------
| Delay Summary | Saved Routes | Notifications |
------------------------------------------------
| Charts and Delay Predictions                 |
------------------------------------------------
```

---

### Route Search Wireframe
```text
------------------------------------------------
| Search Route Input                           |
------------------------------------------------
| Route Results                                |
| - Route Name                                 |
| - Predicted Delay                            |
| - Status                                     |
------------------------------------------------
```

---

## 8. Responsive Design

The system will support:
- desktop screens
- tablet screens
- mobile screens

Responsive design will ensure the interface adjusts correctly for different screen sizes.

---

## 9. Design Tools

The following tools will be used:
- Figma for wireframes and UI design
- React for frontend implementation
- CSS for styling

---

## 10. Conclusion

The UI/UX design focuses on creating a clean, responsive, and user-friendly experience for commuters using the Public Transport Delay Predictor system. The design includes important screens such as login, dashboard, route search, predictions, saved routes, and notifications. The interface supports easy navigation and clear display of delay information.