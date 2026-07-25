# 🚀 Expense Tracker - DevOps Deployment Guide

This project follows a modern DevOps workflow using Docker, GitHub Actions, Render, Neon PostgreSQL, and Vercel.

---

## 🏗️ Architecture

```text
               GitHub Repository
                      │
                git push main
                      │
                      ▼
             GitHub Actions (CI)
        ✔ Build Docker Image
        ✔ Validate Build
                      │
                      ▼
           GitHub Container Registry
                      │
                      ▼
         Render (Docker Web Service)
                      │
              Express REST API
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
     /health Endpoint        Neon PostgreSQL
                      ▲
                      │
           React Frontend (Vercel)
```

---

## ⚙️ Tech Stack

- React + Vite
- Node.js + Express
- PostgreSQL (Neon)
- Docker
- GitHub Actions
- Render
- Vercel
- JWT Authentication

---

## 🚀 Deployment Workflow

### 1. Push Code

```bash
git add .
git commit -m "Update project"
git push origin main
```

### 2. GitHub Actions

- Clone repository
- Build Docker image
- Verify Docker build
- Push image (optional)

### 3. Render

- Pull latest source
- Build Docker image
- Start Express container
- Deploy API

### 4. Database

- Connect to Neon PostgreSQL
- Initialize database schema automatically

### 5. Frontend

- Vercel builds and deploys React application
- Uses Render API

---

## 🔐 Environment Variables

```env
NODE_ENV=production
PORT=10000
DATABASE_URL=<Neon Connection String>
JWT_SECRET=<Strong Secret>
CORS_ORIGIN=<Frontend URL>
```

---

## ✅ Deployment Verification

- API is running
- Database connected
- User authentication works
- Expense CRUD works
- Docker image builds successfully
- GitHub Actions pipeline passes

---

## 📊 DevOps Features

- Docker containerization
- GitHub Actions CI pipeline
- Automated deployments
- Cloud hosting with Render
- Managed PostgreSQL (Neon)
- Separate frontend/backend deployment
- Environment variable management

---

## 📈 CI/CD Flow

```text
Developer
    │
git push
    │
    ▼
GitHub
    │
    ▼
GitHub Actions
(Build Docker Image)
    │
    ▼
Render
(Docker Deployment)
    │
    ▼
Neon PostgreSQL
    ▲
    │
Vercel Frontend
```