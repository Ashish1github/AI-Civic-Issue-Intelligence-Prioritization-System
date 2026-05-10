# AI-Civic-Issue-Intelligence-Prioritization-System

An AI-powered civic complaint management platform where users can submit public issues and receive intelligent analysis using OpenAI.

Built as a full-stack MERN + AI project 

---
# 📌 Features

##  Authentication
- JWT-based Login & Signup
- Role-based access:
  - User
  - Admin

---

##  Complaint Management
Users can submit civic complaints with:
- Title
- Description
- Area/Location

---

## 🤖 AI-Powered Analysis
Every complaint is automatically analyzed using OpenAI:

- Complaint Category
  - Electricity
  - Water
  - Roads
  - Internet
  - Other

- Severity Detection
  - Low
  - Medium
  - High

- Priority Score (1–10)

- Suggested Action

---

##  Duplicate Complaint Detection
System detects similar complaints using AI/text similarity.

Example:
- “No electricity in Sector 5”
- “Power outage in Sector 5”

→ Marked as duplicate.

---

##  Redis Caching
AI analysis results are cached using Redis:
- Faster response
- Reduced OpenAI API calls
- TTL = 1 hour

---

##  Analytics Dashboard
Dashboard includes:
- Total complaints
- High-priority complaints
- Category distribution
- Area-wise complaint insights
- Complaint status tracking

---

##  Area-Based Insights
Shows locations with highest complaints.

Example:
- Sector 5 → 12 complaints
- Sector 8 → 5 complaints

---

##  Admin Panel
Admins can:
- View all complaints
- Update complaint status
- Filter complaints
- Sort complaints

---

# 🧩 Tech Stack

## Frontend
- React (Vite)
- Tailwind CSS
- Recharts

## Backend
- Node.js
- Express.js

## Database
- MongoDB

## AI
- OpenAI API

## Caching
- Redis

## DevOps
- Docker
- GitHub Actions

## Deployment
- AWS EC2

---

# 📂 Project Structure

## Backend

```bash
backend/
│
├── config/
├── controllers/
├── middleware/
├── models/
├── routes/
├── services/
├── utils/
├── app.js
└── server.js
```

---

## Frontend

```bash
frontend/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── context/
│   ├── layouts/
│   └── App.jsx
```

---

#  API Endpoints

## Authentication

### Signup
```http
POST /auth/signup
```

### Login
```http
POST /auth/login
```

---

## Complaints

### Create Complaint
```http
POST /complaints
```

### Get All Complaints
```http
GET /complaints
```

### Update Status
```http
PATCH /complaints/:id/status
```

### Area Insights
```http
GET /complaints/area-insights
```

---

#  Environment Variables

Create `.env` file inside backend:

```env
PORT=5000

MONGO_URI=your_mongodb_uri

JWT_SECRET=your_jwt_secret

OPENAI_API_KEY=your_openai_key

REDIS_URL=your_redis_url
```

---

#  Docker Setup

## Run using Docker Compose

```bash
docker-compose up --build
```

---

#  CI/CD

GitHub Actions workflow includes:
- Install dependencies
- Build frontend
- Run backend checks
- Optional Docker build

---

#  AWS Deployment

Deployment Steps:
1. Launch EC2 instance
2. Install Docker
3. Clone repository
4. Add `.env`
5. Run docker-compose

---

#  UI Preview

## Submit Complaint Page
- Complaint form
- AI analysis loading state
- Responsive UI

## Dashboard
- Complaint cards
- Severity badges
- Pie charts
- Area-based analytics
- Filters & sorting

---

# 📸 Screenshots


```

---

# 🚀 Installation Guide

## Clone Repository

```bash
git clone https://github.com/Ashish1github/AI-Civic-Issue-Intelligence-Prioritization-System.git
```

---

## Backend Setup

```bash
cd backend
npm install
npm run dev
```

---

## Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

# Future Improvements

- Email notifications
- Real-time updates using Socket.io
- Complaint image upload
- AI chatbot assistant
- Multi-language support

---

#  Author

Ashish Kumar

- GitHub: https://github.com/Ashish1github
- LinkedIn:https://www.linkedin.com/in/ashish-kumar-775168270/

---

# ⭐ If You Like This Project

Give this repository a star ⭐
