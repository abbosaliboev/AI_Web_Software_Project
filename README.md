Here is a complete, polished, and professional README.md file for your Real-Time Safety Monitoring System project based on the information provided in your presentations and gifs:

⸻

🛡️ Real-Time Safety Monitoring System

Welcome to the Real-Time Safety Monitoring System, a comprehensive web-based application built to enhance workplace safety through real-time detection and monitoring of PPE (Personal Protective Equipment) compliance using AI-powered computer vision.

Developed as part of our Web Software Capstone Project, the system combines modern web development practices, real-time camera integration, and AI (YOLOv8) to provide a smart and accessible safety solution for environments such as construction sites, factories, and warehouses.

⸻

📽️ System Demo
	•	Welcome Page

	•	Login, Dashboard, Summary Page

	•	Timeline & Report Page


⸻

👥 Team MEERKAT

Name	Role	Responsibilities
Aliboev Abbos	Team Leader, AI & Frontend	Project coordination, frontend logic, AI integration
김태영	AI & Backend	YOLO model training, backend connection
전설민	Backend & DB	API implementation, MySQL DB design


⸻

💡 Motivation & Goals

Modern companies demand smart safety systems to reduce risks and ensure compliance. PPE is crucial to protect workers, but manual monitoring is inefficient.

We envisioned a real-time, web-based, AI-enhanced solution to:
	•	Automate PPE compliance checks
	•	Monitor multiple cameras simultaneously
	•	Store and analyze safety data for insights and reporting

⸻

🌐 Key Features

Feature	Description
🔐 User Authentication	Secure login with role-based access
📸 Live Camera Monitoring	Real-time video stream (up to 6 feeds)
🚨 AI-based PPE Detection	Detects absence of helmet, vest, or glasses using YOLO
📊 Summary Dashboard	Safety scores, violation trends, rankings, heatmaps
📆 Timeline View	Chronological incident logs per camera
📁 Worker Reports	Searchable alert logs and manual report form
🌍 Multi-language Support	English 🇺🇸 and Korean 🇰🇷 via react-i18next
📤 CSV Export	Downloadable reports for audits and analysis
🌓 Dark & Light Mode	Theming support for user preference
📱 Responsive UI	Mobile-friendly layout via Bootstrap + media queries


⸻

⚙️ Tools & Technologies

Layer	Tools / Frameworks
🎨 Design	Figma, Blue & White Minimalism
🖥️ Frontend	React.js, SCSS, Bootstrap, Recharts, React Router, Axios, i18next
🧠 AI	YOLOv8n, Python, Custom Dataset (3.7K+ images)
🔧 Backend	FastAPI, Python Multiprocessing, REST API
💾 Database	MySQL, SQLAlchemy ORM
🔗 Others	GitHub, LocalStorage, Hooks (useState, useEffect, useMemo, etc.)


⸻

🧠 AI Integration: YOLOv8

The AI module is trained using a custom dataset for PPE detection:
	•	Phase 1: 1,176 images (initial model)
	•	Phase 2: 2,551 images (improved head detection)
	•	YOLOv8n was chosen for its speed and lightweight nature.

🧪 Inference Pipeline:

[Camera Stream] --> [YOLO AI (Sub Process)] --> [Annotated Frame + Label] --> [FastAPI Backend] --> [Frontend]

⚙️ AI Logic:
	•	Subprocess inference via PIPE
	•	Data is parsed and sent to backend for logging and frontend visualization
	•	Multi-label detection with bounding box overlays

⸻

🏗️ System Architecture

Frontend (React.js)     <->    FastAPI Backend    <->    YOLO AI Detection
     |                                 |                     |
  React Router                  SQLAlchemy ORM         Camera Stream + Alert Engine
     |                                 |
LocalStorage, Axios             MySQL Database

Each camera feed is analyzed in real time. Alerts are pushed to the backend and reflected instantly in the frontend.

⸻

📈 Website Overview

The system includes the following main pages:

Page	Purpose
Welcome	Intro animation and feature overview
Login	Secure access with form validation
Dashboard	Live camera feed and statistics
Camera Detail	Individual stream view + alert filter
Summary	Trend graphs (Recharts)
Timeline	Camera-wise chronological log
Report	Worker alert records + manual reporting
Info	System introduction and FAQ
Settings	Language switch, preferences (WIP)


⸻

🔍 Hooks & Logic Highlights
	•	useState — manage alerts, filters
	•	useEffect — auto-fetch alerts every 10 seconds
	•	useMemo — optimize sorting/counting of alerts
	•	useParams — extract camera ID from route
	•	useOutletContext — share layout data across nested components

⸻

🚀 Future Work
	•	Add more detection classes (e.g., fire, fall, smoke)
	•	Implement user analytics dashboard
	•	Enhance admin controls (permission levels, alert zones)
	•	Cloud deployment for global access
	•	Notification system (email/SMS for severe alerts)

⸻

🔗 Repository

📁 GitHub Repo: Web Software Project

⸻

📣 Final Notes

This project reflects our team’s passion for real-world impact, combining AI + Web + UX to create a product that not only meets academic goals but also addresses genuine safety concerns in industrial settings.

Built with ❤️ by Team MEERKAT.

⸻

Would you like this README in markdown (.md) file format or pasted into a Notion page or GitHub directly?
