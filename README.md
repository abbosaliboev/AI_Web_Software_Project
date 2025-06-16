# 🛡️ Real-Time Safety Monitoring System

Welcome to the **Real-Time Safety Monitoring System**, a web-based application designed to detect and monitor PPE (Personal Protective Equipment) compliance in real-time. The system leverages computer vision (YOLO model), a modern web frontend (React + SCSS), and a FastAPI backend to ensure on-site safety monitoring through live camera feeds, alert tracking, and incident reporting.

---

## 📸 System Demo

> ⚠️ demo GIF 
![System Demo](./assets/screenshots/demo.gif)

---

## 🌐 Features

- 🔐 **User Authentication**: Secure login system with role-based access
- 🖥️ **Real-Time Camera Feed**: Display up to 6 live streams with alert overlays
- 🚨 **PPE Violation Alerts**: Real-time detection of no helmet, vest, or glasses
- 📊 **Summary Dashboard**: Safety score, trend analysis, violation ranking, heatmaps
- 📆 **Timeline Page**: Chronological view of incidents per camera
- 📁 **Report Page**: Searchable worker alert logs with manual report submission
- 🌍 **Multi-language Support**: English 🇺🇸 and Korean 🇰🇷 via `react-i18next`
- 📤 **CSV Download**: Export alert data for reports or audits

---

## 🏗️ System Architecture

```plaintext
Frontend (React.js)     <->    FastAPI Backend    <->    YOLO AI Detection
     |                                 |                     |
  React Router                  SQLAlchemy ORM         Camera Stream + Alert Engine
     |                                 |
LocalStorage, Axios             MySQL Database
