# Bimarakshak_AI
# BimaRakshak AI

## AI-Driven Motor Insurance Risk Assessment System

BimaRakshak AI is a Database Engineering project that combines Artificial Intelligence, Database Management, GPS/IoT data, and web technologies to analyze driving behavior and assess motor insurance risk.

The system collects driving-related information such as distance, average speed, acceleration events, braking events, and speeding behavior. This data is stored in a structured database and used to generate a driver risk score.

The project demonstrates how database systems and intelligent data analysis can be integrated to support accurate and behavior-based motor insurance risk assessment.

---

## Objectives

- Analyze driver behavior using trip and driving data.
- Store driver, vehicle, trip, and risk information efficiently.
- Generate risk scores based on driving behavior.
- Provide driver-level risk analysis and reports.
- Demonstrate database normalization and relational database concepts.
- Provide an admin dashboard for viewing stored data.
- Promote safer driving through behavioral feedback.

---

## System Architecture

The major components of BimaRakshak AI are:

Driver
   |
   v
Vehicle
   |
   v
Trip Data
   |
   v
Driving Behavior Analysis
   |
   v
Risk Score
   |
   v
Reports and Dashboard

---

## Database Design

The system uses a relational database consisting of the following major entities.

### 1. Drivers

Stores driver information.

- DriverID (Primary Key)
- Name
- Age
- LicenseNo
- Contact

### 2. Vehicles

Stores vehicle information.

- VehicleID (Primary Key)
- DriverID (Foreign Key)
- VehicleType
- RegistrationNo

### 3. Trips

Stores trip-related information.

- TripID (Primary Key)
- DriverID (Foreign Key)
- VehicleID (Foreign Key)
- StartTime
- EndTime
- Distance
- AverageSpeed

### 4. RiskScores

Stores risk assessment information.

- ScoreID (Primary Key)
- TripID (Foreign Key)
- RiskScore
- AccelerationEvents
- BrakingEvents
- SpeedingEvents

### Database Relationships

Drivers 1 ----- M Vehicles

Drivers 1 ----- M Trips

Vehicles 1 ----- M Trips

Trips 1 ----- 1 RiskScores

---

## Risk Assessment

The system considers driving behavior indicators such as:

- Harsh acceleration
- Sudden braking
- Speeding
- Average speed
- Distance travelled

These parameters are analyzed to generate a risk score for each trip.

The current project prototype uses a rule-based risk calculation. The architecture can later be extended with machine learning models trained on larger driving datasets.

---

## Technology Stack

| Component | Technology |
|-----------|------------|
| Database | MySQL / SQLite |
| Backend | Python / Django |
| Frontend | Flutter / HTML, CSS |
| Authentication | Firebase |
| AI and ML | Google Gemini API |
| Tracking | GPS and IoT APIs |
| Version Control | Git and GitHub |

---

## Main Features

### Driver Module

- Driver registration and login
- Enter trip information
- Record driving behavior
- View previous trips
- View generated risk scores

### Risk Assessment Module

- Analyze driving behavior
- Calculate trip risk score
- Store risk assessment results
- Generate driver-level risk information

### Admin Module

- Admin login
- View driver information
- View vehicle information
- View trip records
- View risk scores
- Access database-related information

---

## Example Risk Factors

| Parameter | Example |
|-----------|---------|
| Distance | 42.5 km |
| Average Speed | 50.5 km/h |
| Acceleration Events | 3 |
| Braking Events | 2 |
| Speeding Events | 1 |
| Risk Score | 7.5 |

---

## Project Workflow

User Registration and Login
          |
          v
Driver and Vehicle Information
          |
          v
Trip Data Collection
          |
          v
Driving Behavior Analysis
          |
          v
Risk Score Generation
          |
          v
Database Storage
          |
          v
Driver and Admin Dashboard
          |
          v
Reports and Insights

---

## Project Structure

BimaRakshak_AI/
|
+-- app.py
+-- database.db
+-- README.md
|
+-- templates/
|   +-- index.html
|   +-- login.html
|   +-- signup.html
|   +-- driver_dashboard.html
|   +-- admin_dashboard.html
|   +-- schema.html
|
+-- static/
|   +-- style.css
|
+-- .gitignore

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/Arpita-09-ai/Bimarakshak_AI.git
