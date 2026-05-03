# Queue Management System

## Overview

The Queue Management System is a full-stack web application designed to digitize and optimize queue handling in service environments such as banks, hospitals, and government offices.

Instead of physical waiting lines, customers can generate digital tokens and monitor their position in real-time, significantly improving efficiency and user experience.

---

## Objectives

- Eliminate long physical queues
- Provide real-time queue tracking
- Improve service efficiency
- Enhance customer satisfaction
- Enable better resource management

---

## Features

### Authentication System
- Secure login and registration
- Role-based access control (Admin, Agent, Customer)
- Persistent login using localStorage

---

### Token Management
- Digital token generation
- Automatic token numbering
- Queue positioning
- Token status updates (waiting, serving, completed)

---

### Real-Time Queue Tracking
- Live queue updates
- Current serving token display
- Waiting queue list
- Automatic refresh

---

### Waiting Time Estimation
- Dynamic calculation based on actual data
- Improves transparency for users

---

### Admin Dashboard
- View total customers
- Monitor active counters
- Analyze system performance
- Assign agents to counters
- Generate reports
- View charts (weekly data, satisfaction ratings)

---

### Agent Dashboard
- View assigned counter
- Call next token
- Mark token as completed
- Manage availability (Available / Break)
- View waiting queue

---

### Customer Interface
- Generate token
- Track position
- View waiting time
- Monitor queue status

---

### Analytics & Visualization
- Pie chart (customer satisfaction)
- Bar chart (weekly traffic)
- Performance metrics

---

### Notifications
- Real-time alerts for token updates
- Priority notifications for long waits

---

### System Management
- Counter status management (open, busy, break)
- Agent assignment system
- Queue flow control

---

## Tech Stack

### Frontend
- React.js
- Tailwind CSS
- Recharts
- React Router

### Backend
- Node.js
- Express.js

### Database
- MongoDB Atlas
- Mongoose

---

## Project Structure

Queue-Management-System/
│
├── backend/
│   ├── models/
│   │   ├── Queue.js
│   │   ├── QueueAnalytics.js
│   │   ├── ServiceCounter.js
│   │   └── User.js
│   │
│   ├── routes/
│   │   ├── analyticsRoutes.js
│   │   ├── authRoutes.js
│   │   ├── counterRoutes.js
│   │   └── queueRoutes.js
│   │
│   ├── .env
│   ├── package.json
│   ├── package-lock.json
│   ├── seed.js
│   └── server.js
│
├── frontend/
│   ├── node_modules/
│   ├── public/
│   │
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   │   ├── Card.jsx
│   │   │   ├── Layout.jsx
│   │   │   ├── Navbar.jsx
│   │   │   ├── Sidebar.jsx
│   │   │   └── Stat.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Admin.jsx
│   │   │   ├── AgentDashboard.jsx
│   │   │   ├── CustomerDashboard.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── Token.jsx
│   │   │   ├── Monitoring.jsx
│   │   │   ├── Notifications.jsx
│   │   │   └── Settings.jsx
│   │   │
│   │   ├── utils/
│   │   │   └── avgWait.js
│   │   │
│   │   ├── App.css
│   │   ├── index.css
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   └── .gitignore
│
└── README.md

## Setup Instructions
1.  Clone the project
    git clone https://github.com/your-username/queue-management-system.git

    cd queue-management-system
2.  Backend Setup
    Navigate to backend folder
    cd backend

    Install dependencies
    npm install

    Create a .env file and add:
    MONGO_URI=your_mongodb_connection_string
    PORT=5000

    Start backend server
    node server.js

    (Optional) Seed initial data
    node seed.js

3.  Frontend Setup
    Navigate to frontend folder
    cd frontend

    Install dependencies
    npm install

    Start frontend server
    npm run dev

4.  Open in browser
    http://localhost:5173

## System Workflow

1. User generates token
2. Token stored in database
3. Agent calls next token
4. Admin monitors system
5. Data updates dynamically

---

## Database Collections

- Users
- Queue
- ServiceCounters
- QueueAnalytics

---

## Future Enhancements

- Mobile app support
- AI predictions

---
