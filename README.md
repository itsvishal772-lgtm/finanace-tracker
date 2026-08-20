# 💰 Personal Finance Tracker

A full-stack Personal Finance Tracker that helps user to manage expenses, track monthly budgets, and track spending trends. The application is built using **React**, **Node.js**, **Express**, and **PostgreSQL**, with a modern **Docker-based DevOps workflow**.

🔗 **Live Demo:** https://personal-finance-tracker-cyan-tau.vercel.app/login

🔗 **GitHub Repository:** https://github.com/sakib1133/personal-finance-tracker

---

# 🚀 Features

- 🔐 JWT Authentication
- 👤 User Registration & Login
- 💸 Add, Edit & Delete Expenses
- 📊 Monthly Expense Summary
- 🥧 Expense Analytics with Pie Charts
- 📂 Category-wise Expense Tracking
- 📅 Filter Expenses by Date
- 📥 Export Expenses as CSV
- 📱 Responsive UI

---

# 🏗️ System Architecture

```text
                GitHub Repository
                       │
                 git push (main)
                       │
                       ▼
              GitHub Actions
         (Build Docker Image)
                       │
                       ▼
          Docker Image Validation
                       │
                       ▼
         Render (Docker Container)
                       │
               Express REST API
                       │
                       ▼
             Neon PostgreSQL
                       ▲
                       │
       React + Vite Frontend (Vercel)
```

---

# ⚙️ DevOps Workflow

```text
Developer
    │
    ▼
Write Code
    │
    ▼
Git Commit
    │
    ▼
Git Push
    │
    ▼
GitHub Actions
(Build Docker Image)
    │
    ▼
Render Deploys Docker Container
    │
    ▼
Express Backend
    │
    ▼
Neon PostgreSQL
    ▲
    │
React Frontend (Vercel)
```

---

# 🛠️ Tech Stack

## Frontend

- React.js
- Vite
- Tailwind CSS
- Axios
- Recharts

## Backend

- Node.js
- Express.js
- PostgreSQL (pg)
- JWT Authentication
- bcryptjs
- UUID

## Database

- Neon PostgreSQL

## DevOps

- Git
- GitHub
- Docker
- Docker Compose
- GitHub Actions
- Render
- Vercel

---

# 📁 Project Structure

```text
personal-finance-tracker/
│
├── client/                  # React Frontend
│
├── server/                  # Express Backend
│   ├── Dockerfile
│   ├── .dockerignore
│   ├── db.js
│   └── server.js
│
├── .github/
│   └── workflows/
│       └── docker.yml
│
├── docker-compose.yml
├── render.yaml
├── README.md
└── DEPLOYMENT.md
```

---

# 🚀 Local Setup

## Clone Repository

```bash
git clone https://github.com/sakib1133/personal-finance-tracker.git

cd personal-finance-tracker
```

---

## Backend

```bash
cd server

npm install

npm start
```

---

## Frontend

```bash
cd client

npm install

npm run dev
```

---

# 🐳 Docker

## Build Docker Image

```bash
docker build -t finance-backend ./server
```

## Run Container

```bash
docker run --rm \
-p 5001:5001 \
--env-file server/.env \
finance-backend
```

## Docker Compose

```bash
docker compose up --build
```

Stop

```bash
docker compose down
```

---

# ☁️ Deployment

| Service | Platform |
|----------|----------|
| Frontend | Vercel |
| Backend | Render (Docker) |
| Database | Neon PostgreSQL |
| CI | GitHub Actions |

---

# 📈 DevOps Highlights

- Dockerized Express Backend
- GitHub Actions for automated Docker image builds
- Render Docker deployment
- Cloud-hosted PostgreSQL using Neon
- Environment variable management
- Version-controlled infrastructure configuration

---

# 👨‍💻 Author

**Mohd Sakib Malik**

- GitHub: https://github.com/sakib1133
- LinkedIn: https://www.linkedin.com/in/mohd-sakib-malik-97ab4a283/
- LeetCode: https://leetcode.com/u/sakib_malik79/
