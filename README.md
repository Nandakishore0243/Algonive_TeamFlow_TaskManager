# 🚀 TeamFlow – Task Management System for Small Teams

### Algonive Internship Project – Web Development Task 2

---

## 🌐 Live Demo

https://teamflow-35004.web.app

## 📂 GitHub Repository

https://github.com/Nandakishore0243/Algonive_TeamFlow_TaskManager

---

## 📌 Overview

TeamFlow is a modern task management web application designed for small teams and startups to efficiently assign, track, and manage their daily work.

It provides real-time updates, intuitive dashboard analytics, and a clean UI for seamless collaboration.

---

## ✨ Features Implemented

* User Authentication (Firebase Auth)
* Task Creation (title, description, assignee, due date)
* Task Assignment to team members
* Status Tracking (Pending → In Progress → Completed)
* Filters (status, overdue, assigned tasks)
* Deadline Alerts (visual warnings)
* Real-time Updates (Firestore onSnapshot)
* Edit & Delete Tasks (CRUD operations)
* Dashboard Statistics
* Responsive UI
* Toast Notifications

---

## 🛠 Tech Stack

* HTML
* CSS
* JavaScript
* Firebase Authentication
* Firebase Firestore
* Firebase Hosting

---

## 📁 Project Structure

task-manager/
│── index.html        (Login / Signup page)
│── dashboard.html    (Main dashboard)
│── firebase.json     (Firebase config)
│── README.md         (Documentation)

---

## ⚙️ Firebase Setup

### Step 1 — Create Project

Go to: https://console.firebase.google.com
Create project → `teamflow-app`

### Step 2 — Enable Auth

Authentication → Enable Email/Password

### Step 3 — Firestore DB

Create database → Start in test mode

### Step 4 — Add Config

Replace in index.html & dashboard.html:

const firebaseConfig = {
apiKey: "YOUR_API_KEY",
authDomain: "YOUR_PROJECT.firebaseapp.com",
projectId: "YOUR_PROJECT_ID",
storageBucket: "YOUR_PROJECT.appspot.com",
messagingSenderId: "YOUR_SENDER_ID",
appId: "YOUR_APP_ID"
};

---

## ▶️ Run Project

### Option 1 (Recommended)

Use VS Code Live Server

### Option 2

python -m http.server 5500

---

## 🎯 Highlights

* Real-world team collaboration system
* Real-time database integration
* Clean modern UI
* Fully deployed project

---

## 📤 Submission Checklist

* GitHub Repo Created
* Project Deployed
* LinkedIn Post (pending)
* Video Explanation (pending)

---

## 👨‍💻 Author

Nanda Kishore

---

## 📞 Contact

[services.algonivetech@gmail.com](mailto:services.algonivetech@gmail.com)
+91 7834847081
