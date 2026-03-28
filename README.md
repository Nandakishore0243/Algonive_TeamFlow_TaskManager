# 🚀 TeamFlow – Task Management System for Small Teams
### Algonive Internship Project – Web Development Task 2

---

## 📁 Project Structure
```
task-manager/
├── index.html        ← Login / Sign-up page
├── dashboard.html    ← Main app (tasks, stats, filters)
└── README.md         ← This file
```

---

## ⚙️ Firebase Setup (Step-by-Step)

### Step 1 — Create Firebase Project
1. Go to https://console.firebase.google.com
2. Click **"Add project"** → Name it `teamflow-app` → Continue
3. Disable Google Analytics (not needed) → Create project

### Step 2 — Enable Authentication
1. In left sidebar → **Build → Authentication**
2. Click **"Get started"**
3. Under **Sign-in method** → Enable **Email/Password** → Save

### Step 3 — Create Firestore Database
1. In left sidebar → **Build → Firestore Database**
2. Click **"Create database"**
3. Select **"Start in test mode"** → Next → Choose your region → Done

### Step 4 — Add Firestore Security Rules (Optional but recommended)
In Firestore → Rules tab, paste:
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /tasks/{taskId} {
      allow read, write: if request.auth != null;
    }
    match /users/{userId} {
      allow read, write: if request.auth.uid == userId;
    }
  }
}
```

### Step 5 — Get Your Firebase Config
1. In Firebase Console → Project Settings (gear icon)
2. Under **"Your apps"** → Click **"</>"** (Web app)
3. Register app → Name it `teamflow`
4. Copy the `firebaseConfig` object

### Step 6 — Add Config to Your Project
Open **both** `index.html` and `dashboard.html`
Find this section (appears in both files):

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

Replace `YOUR_API_KEY`, `YOUR_PROJECT_ID`, etc. with your actual values.

---

## ▶️ Running the Project
Since the project uses ES Modules (import/export), you **cannot** open the files directly.

### Option A – VS Code Live Server (Recommended)
1. Install **Live Server** extension in VS Code
2. Right-click `index.html` → **"Open with Live Server"**

### Option B – Python HTTP Server
```bash
cd task-manager
python -m http.server 5500
# Open http://localhost:5500
```

### Option C – Node.js
```bash
npx serve .
```

---

## ✨ Features Implemented
- ✅ **User Authentication** — Sign up & login with email/password via Firebase Auth
- ✅ **Task Creation** — Title, description, assignee, status, due date
- ✅ **Task Assignment** — Assign tasks to any team member by name
- ✅ **Status Updates** — Pending → In Progress → Completed (one-click cycle)
- ✅ **Filter & View** — Filter by status, overdue, or assigned to you
- ✅ **Deadline Reminders** — Visual warning banner for overdue/upcoming tasks
- ✅ **Real-time Updates** — Firestore `onSnapshot` keeps all users in sync
- ✅ **Delete & Edit Tasks** — Full CRUD operations
- ✅ **Stats Dashboard** — Live counts of tasks by status
- ✅ **Toast Notifications** — Feedback on every action
- ✅ **Responsive UI** — Works on desktop and mobile

---

## 📤 Submission Checklist
- [ ] Push to GitHub: `Algonive_TaskManagement`
- [ ] Post on LinkedIn mentioning @Algonive
- [ ] Record a video walkthrough showing all features
- [ ] Include GitHub link in the LinkedIn post

---

## 🤝 Contact
services.algonivetech@gmail.com | +91 7834847081
