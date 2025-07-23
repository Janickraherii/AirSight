# AirSight
Flight delay tracking and analysis app built with Microsoft Power Platform
# ✈ AirSight – Flight Operations Tracker

**AirSight** is a Power Platform-based application designed to track and analyze airline delays and their causes (weather, company, airport). This project simulates a real use case in the aviation sector and was developed to demonstrate data integration, visualization, and automation using Microsoft technologies.

---

## Use Case – Simulated Scenario

> A logistics team working in air operations needs to monitor flights departing from Paris (CDG and Orly). The goal is to detect major delays, understand contributing factors (like weather or airline), and anticipate operational impacts.  
>  
> The team requires a mobile-friendly web app to consult flight data in real-time, receive alerts, and track performance indicators.

---

## 🛠 Tech Stack

| Tool | Role |
|------|------|
| **Power Apps (Canvas App)** | Main user interface to consult flights and delays |
| **Power Automate** | Automates API calls (AviationStack, OpenWeatherMap) to fetch data |
| **Dataverse** | Central database (flights, airlines, weather, delay reasons) |
| **Power Pages (PWA enabled)** | Public/internal web access for dashboards or reports |
| **Power BI (optional)** | Advanced analytics and trend visualization |
| **GitHub + Notion** | Project documentation and tracking |

---

## 📊 Dataverse Tables

### 🛫 Flights
- FlightNumber (Text)
- DepartureAirport (Text)
- ArrivalAirport (Text)
- ScheduledTime (DateTime)
- DelayMinutes (Number)
- Airline (Text)
- WeatherFlag (Yes/No)

### 🌦 Weather
- Airport (Text)
- Temperature (Number)
- Wind (Number)
- Rain (Yes/No)
- RecordedAt (DateTime)

### 🏢 Airlines
- AirlineName (Text)
- IATAcode (Text)

---

## 🔄 Power Automate Logic

1. Daily scheduled flow (e.g. 07:00 AM)
2. Call [AviationStack](https://aviationstack.com/) API for current flight data
3. Call [OpenWeatherMap](https://openweathermap.org/api) for weather data
4. Merge and process JSON response
5. Store data in **Dataverse**
6. If `Delay > 30 minutes` → send email alert to internal team

---

## 🌐 Power Pages (as a PWA)

- Responsive web portal to display summaries, KPIs, and flight status
- Can be installed on mobile as a Progressive Web App
- Connected to Dataverse tables in real time

---

## 📸 Screenshots

→ Available in `/screenshots` folder  
*(To be added during development: Power Apps interface, flows, tables, PWA view)*

---

## 💼 Learning Objectives

- Practice **Microsoft Power Platform** (Apps, Automate, Dataverse, Pages)
- Simulate a real-world use case in the **aerospace industry**
- Master API integration and data structuring
- Learn to design a mobile-first web app using Power Pages + PWA
- Build a complete documented GitHub project

---

## 📅 Project Timeline

| Week | Focus |
|------|-------|
| Week 1 | Set up Power Platform environment + Dataverse tables + Canvas App base |
| Week 2 | Integrate APIs with Power Automate + populate Dataverse |
| Week 3 | Build Power Pages portal + enable PWA + polish UX/UI |
| Week 4 | Add documentation (GitHub + Notion) + screenshots + optional Power BI |

---

## 📁 Repository Structure
/AirSight
│
├── /screenshots/ # App and flow screenshots
├── /data/ # Sample flight data (JSON, Excel, etc.)
├── /doc/ # Use case, architecture diagrams, wireframes
├── README.md # Project overview (this file)
├── LICENSE # MIT License

