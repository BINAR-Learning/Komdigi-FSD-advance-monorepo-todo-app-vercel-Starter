# Final Project Starter - Todo Application Fullstack Monorepo

**✅ Aplikasi sudah COMPLETE dan siap digunakan!**

**Tugas Anda:** Setup deployment (CI/CD, Vercel, GitHub Actions, MongoDB Atlas) - Berlatih menjadi DevOps Engineer

## 📋 Daftar Isi

1. [Overview](#overview)
2. [Status Project](#status-project)
3. [Prerequisites](#prerequisites)
4. [Struktur Project](#struktur-project)
5. [Instalasi dan Setup](#instalasi-dan-setup)
6. [Testing Aplikasi Lokal](#testing-aplikasi-lokal)
7. [Tugas Deployment - DevOps](#tugas-deployment---devops)
8. [Environment Variables](#environment-variables)
9. [Troubleshooting](#troubleshooting)

---

## 🎯 Overview

Project ini adalah **COMPLETE Fullstack Todo Application** dengan fitur:

- ✅ **User Authentication** (Register/Login dengan JWT)
- ✅ **Todo CRUD Operations** (Create, Read, Update, Delete)
- ✅ **Monorepo Structure** dengan PNPM dan Turbo
- ✅ **Backend API** dengan Express + MongoDB
- ✅ **Frontend** dengan React + Vite
- ✅ **CI/CD Pipeline** dengan GitHub Actions
- ✅ **Deployment** ke Vercel (Backend + Frontend)

### Tech Stack

**Backend:**
- Node.js 22 LTS
- Express 5
- MongoDB dengan Mongoose
- JWT Authentication
- Swagger/OpenAPI Documentation

**Frontend:**
- React 19
- Vite
- React Router
- Axios

**Infrastructure:**
- PNPM Workspace
- Turbo Build System
- GitHub Actions
- Vercel (Serverless)

---

## 📦 Prerequisites

Sebelum memulai, pastikan Anda sudah menginstall:

- **Node.js 22 LTS** atau lebih baru
- **PNPM 9** (atau npm 10)
- **Git**
- **MongoDB Atlas account** (Free Tier) - https://cloud.mongodb.com
- **Vercel account** (Free Tier) - https://vercel.com
- **GitHub account** (untuk CI/CD)

### Install PNPM

```bash
npm install -g pnpm
```

Verifikasi instalasi:

```bash
pnpm --version
```

---

## 📁 Struktur Project

```
monorepo-todo-auth-vercel-starter/
├── apps/
│   ├── backend/              # Express API Server
│   │   ├── api/              # Vercel serverless wrapper
│   │   │   └── index.js      # TODO: Vercel serverless handler
│   │   ├── src/
│   │   │   ├── app.js        # TODO: Express app setup
│   │   │   ├── index.js      # TODO: Server entry point
│   │   │   ├── models/       # MongoDB models
│   │   │   │   ├── User.js   # TODO: User model
│   │   │   │   └── Todo.js   # TODO: Todo model
│   │   │   ├── routes/       # API routes
│   │   │   │   ├── auth.js   # TODO: Auth routes (register, login)
│   │   │   │   └── todos.js  # TODO: Todo routes (CRUD)
│   │   │   └── middleware/
│   │   │       └── auth.js   # TODO: JWT authentication middleware
│   │   ├── tests/
│   │   │   ├── unit/         # TODO: Unit tests
│   │   │   └── integration/  # TODO: Integration tests
│   │   ├── package.json
│   │   ├── vercel.json       # Vercel configuration
│   │   └── env.example.txt   # Environment variables template
│   │
│   └── frontend/             # React Application
│       ├── src/
│       │   ├── pages/
│       │   │   ├── Login.jsx     # TODO: Login page
│       │   │   ├── Register.jsx  # TODO: Register page
│       │   │   └── Dashboard.jsx # TODO: Dashboard/Todo page
│       │   ├── utils/
│       │   │   ├── api.js    # TODO: API utility functions
│       │   │   └── auth.js   # TODO: Auth utility functions
│       │   ├── App.jsx       # TODO: Main app component with routing
│       │   ├── main.jsx      # TODO: Entry point
│       │   └── index.css     # TODO: Global styles
│       ├── index.html
│       ├── vite.config.js    # TODO: Vite configuration
│       ├── package.json
│       ├── vercel.json       # Vercel configuration
│       └── env.example.txt   # Environment variables template
│
├── packages/
│   └── shared/               # Shared utilities
│       ├── index.js          # TODO: Shared functions
│       └── package.json
│
├── .github/
│   └── workflows/
│       └── ci-cd.yml         # TODO: CI/CD pipeline
│
├── package.json              # Root package.json
├── pnpm-workspace.yaml       # PNPM workspace config
├── turbo.json                # Turbo build config
└── README.md                 # This file
```

---

## 🚀 Instalasi dan Setup

### Step 1: Clone atau Copy Project

```bash
# Jika menggunakan git
git clone <repository-url>
cd monorepo-todo-auth-vercel-starter

# Atau copy folder ini ke lokasi yang diinginkan
```

### Step 2: Install Dependencies

```bash
# Install semua dependencies untuk semua workspaces
pnpm install
```

### Step 3: Setup Environment Variables

**Backend:**

```bash
# Copy env example
cp apps/backend/env.example.txt apps/backend/.env

# Edit apps/backend/.env dengan editor Anda
# Isi dengan MongoDB URI dan JWT Secret
```

**Frontend:**

```bash
# Copy env example
cp apps/frontend/env.example.txt apps/frontend/.env

# Edit apps/frontend/.env dengan editor Anda
# Isi dengan backend API URL
```

### Step 4: Setup MongoDB Atlas

1. Sign up di https://cloud.mongodb.com
2. Create free cluster (M0)
3. Create database user (username & password)
4. Get connection string
5. **IMPORTANT:** Add IP whitelist `0.0.0.0/0` (allow from anywhere)
6. Update `MONGODB_URI` di `apps/backend/.env`

---

## ✅ Status Project

### **Aplikasi Sudah Complete! 🎉**

Semua kode aplikasi sudah diimplementasikan dan siap digunakan:

- ✅ **Backend API** - Express dengan MongoDB, JWT Auth, Swagger docs
- ✅ **Frontend** - React dengan routing, authentication, CRUD operations
- ✅ **Models** - User dan Todo models dengan validasi
- ✅ **Routes** - Auth routes (register/login) dan Todo routes (CRUD)
- ✅ **Middleware** - JWT authentication middleware
- ✅ **UI Components** - Login, Register, Dashboard pages
- ✅ **API Integration** - Axios dengan interceptors
- ✅ **Error Handling** - Complete error handling di semua layer

### **Yang Perlu Anda Lakukan:**

**Hanya Deployment & DevOps Setup!** 🚀

1. ✅ Setup MongoDB Atlas
2. ✅ Setup Vercel Projects (Backend + Frontend)
3. ✅ Setup GitHub Actions CI/CD Pipeline
4. ✅ Configure GitHub Secrets
5. ✅ Configure Vercel Environment Variables
6. ✅ Deploy dan Test

---

## 🧪 Testing Aplikasi Lokal

Sebelum deployment, test aplikasi di local terlebih dahulu:

### Step 1: Setup Environment Variables

**Backend (`apps/backend/.env`):**
```env
PORT=3001
NODE_ENV=development
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/todo-app
JWT_SECRET=your-super-secret-jwt-key-minimum-32-characters-long
JWT_EXPIRES_IN=7d
API_URL=http://localhost:3001
```

**Frontend (`apps/frontend/.env`):**
```env
VITE_API_URL=http://localhost:3001
```

### Step 2: Install Dependencies

```bash
pnpm install
```

### Step 3: Run Applications

**Terminal 1 - Backend:**
```bash
pnpm --filter backend dev
```

**Terminal 2 - Frontend:**
```bash
pnpm --filter frontend dev
```

### Step 4: Test Aplikasi

1. **Backend:**
   - Health check: http://localhost:3001/health
   - API Docs: http://localhost:3001/api-docs

2. **Frontend:**
   - Open: http://localhost:5173
   - Register new user
   - Login
   - Create, update, delete todos

---

## 🚀 Tugas Deployment - DevOps

Ini adalah bagian utama yang perlu Anda kerjakan. Fokus pada **DevOps practices**:

### Phase 1: Setup MongoDB Atlas (Week 1)

#### Task 1.1: Create MongoDB Atlas Account

1. Sign up di https://cloud.mongodb.com
2. Create free cluster (M0)
3. Create database user (username & password)
4. Get connection string
5. **IMPORTANT:** Add IP whitelist `0.0.0.0/0` (allow from anywhere)

#### Task 1.2: Configure MongoDB

1. Copy connection string
2. Update `MONGODB_URI` di environment variables (akan digunakan di Vercel)

---

### Phase 2: Setup Vercel Projects (Week 2)

#### Task 2.1: Create Vercel Account

1. Sign up di https://vercel.com (Free, no credit card)
2. Connect GitHub account

#### Task 2.2: Deploy Backend ke Vercel

1. **Manual Deploy Pertama Kali:**
   - Go to Vercel Dashboard
   - Click "Add New Project"
   - Import repository dari GitHub
   - Configure:
     - **Project Name:** `your-repo-name-backend`
     - **Root Directory:** **KOSONGKAN** (biarkan kosong)
     - **Framework Preset:** Other
     - **Build Command:** (kosongkan)
     - **Output Directory:** (kosongkan)
   
2. **Environment Variables:**
   - `MONGODB_URI` - MongoDB connection string
   - `JWT_SECRET` - Random secret key (min 32 chars)
   - `JWT_EXPIRES_IN` - `7d`
   - `NODE_ENV` - `production`

3. **Settings:**
   - **Root Directory:** KOSONGKAN
   - **Git > Production Branch:** `main`
   - **Git > Auto Deploy:** **DISABLE**

4. **Deploy & Get Project ID:**
   - Deploy sekali secara manual
   - Copy **Project ID** dari Settings > General
   - Save untuk GitHub Secrets

#### Task 2.3: Deploy Frontend ke Vercel

1. **Manual Deploy Pertama Kali:**
   - Click "Add New Project" lagi
   - Import repository yang sama
   - Configure:
     - **Project Name:** `your-repo-name-frontend`
     - **Root Directory:** **KOSONGKAN**
     - **Framework Preset:** Vite (auto-detect)
     - **Build Command:** `pnpm build` (auto-detect)
     - **Output Directory:** `dist` (auto-detect)

2. **Environment Variables:**
   - `VITE_API_URL` - Backend Vercel URL (contoh: `https://your-backend.vercel.app`)

3. **Settings:**
   - **Root Directory:** KOSONGKAN
   - **Git > Production Branch:** `main`
   - **Git > Auto Deploy:** **DISABLE**

4. **Deploy & Get Project ID:**
   - Deploy sekali secara manual
   - Copy **Project ID** dari Settings > General
   - Save untuk GitHub Secrets

---

### Phase 3: Setup GitHub Actions CI/CD (Week 3)

#### Task 3.1: Get Vercel Credentials

1. **Vercel Token:**
   - Go to https://vercel.com/account/tokens
   - Create new token
   - Copy token

2. **Vercel User ID:**
   - Go to Vercel Dashboard > Settings > General
   - Copy User ID

3. **Vercel Org ID (Optional):**
   - Jika menggunakan team, copy Org ID

#### Task 3.2: Configure GitHub Secrets

Go to GitHub Repository > Settings > Secrets and variables > Actions:

**Required Secrets:**
- `VERCEL_TOKEN` - Vercel token dari step 3.1
- `VERCEL_USER_ID` - User ID dari Vercel
- `VERCEL_ORG_ID` - (Optional) Org ID jika menggunakan team
- `VERCEL_BACKEND_PROJECT_ID` - Backend Project ID dari Task 2.2
- `VERCEL_FRONTEND_PROJECT_ID` - Frontend Project ID dari Task 2.3
- `VITE_API_URL` - Backend Vercel URL (untuk frontend build)

#### Task 3.3: Complete CI/CD Workflow

**File:** `.github/workflows/ci-cd.yml`

**TODO:** Implementasi CI/CD pipeline:

1. **Test Job:**
   - Run tests pada setiap push
   - Setup Node.js 22
   - Install pnpm
   - Run `pnpm test`

2. **Build Frontend Job:**
   - Build frontend dengan Vite
   - Set environment variable `VITE_API_URL`
   - Only run on `main` branch

3. **Deploy Frontend Job:**
   - Deploy frontend ke Vercel
   - Use `amondnet/vercel-action@v25`
   - Configure dengan secrets
   - Only run on `main` branch

4. **Deploy Backend Job:**
   - Deploy backend ke Vercel
   - Use `amondnet/vercel-action@v25`
   - Set `working-directory: ./apps/backend`
   - Configure dengan secrets
   - Only run on `main` branch

5. **Notify Job:**
   - Show deployment status
   - Notify success/failure

**Reference:** Lihat finished project untuk implementasi lengkap

---

### Phase 4: Testing & Verification (Week 4)

#### Task 4.1: Test Deployment

1. Push code ke `main` branch
2. Check GitHub Actions logs
3. Verify deployments di Vercel
4. Test deployed applications:
   - Backend: `https://your-backend.vercel.app/health`
   - Frontend: `https://your-frontend.vercel.app`
   - API Docs: `https://your-backend.vercel.app/api-docs`

#### Task 4.2: End-to-End Testing

1. Register new user di production
2. Login
3. Create todos
4. Update todos
5. Delete todos
6. Test error cases

#### Task 4.3: Monitor & Debug

1. Check Vercel logs untuk errors
2. Check MongoDB Atlas logs
3. Monitor GitHub Actions runs
4. Fix any issues

---

## 📝 Tugas Development - Sequential Guide (ARCHIVED)

> **Note:** Kode aplikasi sudah complete. Bagian ini hanya untuk referensi jika ingin memahami implementasi.

<details>
<summary>Klik untuk melihat detail implementasi (sudah complete)</summary>

### Phase 1: Backend Setup (Week 1)

#### Task 1.1: Setup Express Application

**File:** `apps/backend/src/app.js`

1. Import semua module yang diperlukan
2. Setup Swagger/OpenAPI configuration
3. Initialize Express app
4. Setup middleware (CORS, JSON parser, Swagger UI)
5. Setup database connection function
6. Setup health check routes
7. Mount API routes
8. Setup error handling
9. Export startServer function

**Testing:**
```bash
cd apps/backend
pnpm dev
# Test: http://localhost:3001/health
```

#### Task 1.2: User Model

**File:** `apps/backend/src/models/User.js`

1. Define User schema (email, password)
2. Setup password hashing middleware (pre-save hook)
3. Create comparePassword method
4. Export User model

**Testing:**
- Test di MongoDB Compass atau via API

#### Task 1.3: Todo Model

**File:** `apps/backend/src/models/Todo.js`

1. Define Todo schema (title, completed, user)
2. Setup relationship dengan User model
3. Export Todo model

#### Task 1.4: Authentication Middleware

**File:** `apps/backend/src/middleware/auth.js`

1. Extract JWT token dari Authorization header
2. Verify JWT token
3. Find user dari database
4. Attach user ke request object
5. Handle errors

**Testing:**
- Test dengan protected route

#### Task 1.5: Auth Routes

**File:** `apps/backend/src/routes/auth.js`

1. **POST /register:**
   - Validate input (email, password)
   - Check if user exists
   - Create new user
   - Hash password
   - Generate JWT token
   - Return token and user info

2. **POST /login:**
   - Validate input
   - Find user by email
   - Compare password
   - Generate JWT token
   - Return token and user info

3. Add Swagger documentation

**Testing:**
```bash
# Test register
curl -X POST http://localhost:3001/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{"email":"test@example.com","password":"password123"}'

# Test login
curl -X POST http://localhost:3001/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{"email":"test@example.com","password":"password123"}'
```

#### Task 1.6: Todo Routes

**File:** `apps/backend/src/routes/todos.js`

1. Apply authentication middleware to all routes
2. **GET /todos:** Get all todos for authenticated user
3. **POST /todos:** Create new todo
4. **GET /todos/:id:** Get todo by ID (with ownership check)
5. **PUT /todos/:id:** Update todo (with ownership check)
6. **DELETE /todos/:id:** Delete todo (with ownership check)
7. Add Swagger documentation

**Testing:**
```bash
# Get token from login first
TOKEN="your-jwt-token"

# Get all todos
curl -X GET http://localhost:3001/api/todos \
  -H "Authorization: Bearer $TOKEN"

# Create todo
curl -X POST http://localhost:3001/api/todos \
  -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"title":"My first todo"}'
```

#### Task 1.7: Server Entry Point

**File:** `apps/backend/src/index.js`

1. Import startServer from app.js
2. Call startServer()

**Testing:**
```bash
pnpm --filter backend dev
# Server should start on port 3001
```

#### Task 1.8: Vercel Serverless Wrapper

**File:** `apps/backend/api/index.js`

1. Import serverless-http
2. Import Express app
3. Wrap app with serverless-http
4. Export handler

**Note:** Pastikan app.js juga export Express app instance (bukan hanya startServer)

---

### Phase 2: Frontend Setup (Week 2)

#### Task 2.1: Vite Configuration

**File:** `apps/frontend/vite.config.js`

1. Import defineConfig and react plugin
2. Setup plugins
3. Configure server with proxy for /api
4. Export configuration

**Testing:**
```bash
pnpm --filter frontend dev
# Frontend should start on port 5173
```

#### Task 2.2: Auth Utilities

**File:** `apps/frontend/src/utils/auth.js`

1. saveToken(token) - Save to localStorage
2. getToken() - Get from localStorage
3. removeToken() - Remove from localStorage
4. isAuthenticated() - Check if token exists
5. logout() - Clear all auth data

#### Task 2.3: API Utilities

**File:** `apps/frontend/src/utils/api.js`

1. Setup axios instance with baseURL
2. Setup request interceptor (attach token)
3. Setup response interceptor (handle 401)
4. registerUser(email, password)
5. loginUser(email, password)
6. getTodos()
7. createTodo(title)
8. updateTodo(id, data)
9. deleteTodo(id)

#### Task 2.4: Login Page

**File:** `apps/frontend/src/pages/Login.jsx`

1. Create form with email and password inputs
2. Handle form submission
3. Call loginUser API
4. Save token
5. Redirect to dashboard
6. Handle errors
7. Add loading state
8. Link to register page

**Testing:**
- Test login dengan user yang sudah terdaftar

#### Task 2.5: Register Page

**File:** `apps/frontend/src/pages/Register.jsx`

1. Create form with email, password, confirmPassword
2. Validate password match
3. Handle form submission
4. Call registerUser API
5. Save token
6. Redirect to dashboard
7. Handle errors
8. Add loading state
9. Link to login page

**Testing:**
- Test register new user

#### Task 2.6: Dashboard Page

**File:** `apps/frontend/src/pages/Dashboard.jsx`

1. Check authentication on mount
2. Fetch todos on mount
3. Create todo form
4. Display todos list
5. Toggle todo completed status
6. Edit todo title
7. Delete todo
8. Logout functionality
9. Handle loading and error states

**Testing:**
- Test semua CRUD operations
- Test authentication check

#### Task 2.7: App Component with Routing

**File:** `apps/frontend/src/App.jsx`

1. Setup BrowserRouter
2. Create Routes:
   - `/login` - Login page
   - `/register` - Register page
   - `/dashboard` - Dashboard page (protected)
3. Setup authentication check
4. Redirect logic

#### Task 2.8: Entry Point

**File:** `apps/frontend/src/main.jsx`

1. Import React and ReactDOM
2. Import App component
3. Render App to root element

**Testing:**
```bash
pnpm --filter frontend dev
# Test semua routes
```

---

### Phase 3: Integration & Testing (Week 3)

#### Task 3.1: End-to-End Testing

1. Test complete user flow:
   - Register → Login → Create Todo → Update Todo → Delete Todo → Logout
2. Test error cases:
   - Invalid credentials
   - Unauthorized access
   - Network errors

#### Task 3.2: Unit Tests (Optional)

**Files:** `apps/backend/tests/unit/`

1. Test User model methods
2. Test authentication middleware
3. Test utility functions

#### Task 3.3: Integration Tests (Optional)

**Files:** `apps/backend/tests/integration/`

1. Test auth routes
2. Test todo routes
3. Test database operations

---

### Phase 4: Deployment Setup (Week 4)

#### Task 4.1: Setup Vercel Projects

1. **Backend Project:**
   - Create project di Vercel
   - Set root directory: KOSONGKAN
   - Disable auto deploy
   - Add environment variables
   - Deploy manually
   - Copy Project ID

2. **Frontend Project:**
   - Create project di Vercel
   - Set root directory: KOSONGKAN
   - Disable auto deploy
   - Add environment variables
   - Deploy manually
   - Copy Project ID

#### Task 4.2: Setup GitHub Secrets

Go to GitHub Repository > Settings > Secrets and variables > Actions:

- `VERCEL_TOKEN` - Get dari https://vercel.com/account/tokens
- `VERCEL_USER_ID` - Get dari Vercel Dashboard
- `VERCEL_ORG_ID` - (Optional) Jika menggunakan team
- `VERCEL_BACKEND_PROJECT_ID` - Backend project ID
- `VERCEL_FRONTEND_PROJECT_ID` - Frontend project ID
- `VITE_API_URL` - Backend Vercel URL (untuk frontend build)

#### Task 4.3: CI/CD Pipeline

**File:** `.github/workflows/ci-cd.yml`

1. Setup workflow triggers
2. Test job
3. Build frontend job
4. Deploy frontend job
5. Deploy backend job
6. Notify job

**Testing:**
- Push to main branch
- Check GitHub Actions logs
- Verify deployments di Vercel

---

## 🔐 Environment Variables

### Backend (`apps/backend/.env`)

```env
PORT=3001
NODE_ENV=development
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/todo-app
JWT_SECRET=your-super-secret-jwt-key-minimum-32-characters-long
JWT_EXPIRES_IN=7d
API_URL=http://localhost:3001
```

### Frontend (`apps/frontend/.env`)

```env
VITE_API_URL=http://localhost:3001
```

**Untuk Production:**
- Update `VITE_API_URL` dengan backend Vercel URL
- Set environment variables di Vercel Dashboard

---

## 🧪 Testing

### Manual Testing

**Backend:**
```bash
# Start backend
pnpm --filter backend dev

# Test health check
curl http://localhost:3001/health

# Test API docs
# Open: http://localhost:3001/api-docs
```

**Frontend:**
```bash
# Start frontend
pnpm --filter frontend dev

# Open: http://localhost:5173
```

### Automated Testing

```bash
# Run all tests
pnpm test

# Run unit tests
pnpm test:unit

# Run integration tests
pnpm test:integration
```

---

## 🚀 Deployment

### Prerequisites

1. ✅ MongoDB Atlas setup
2. ✅ Vercel account
3. ✅ GitHub repository
4. ✅ GitHub Secrets configured
5. ✅ Vercel projects created

### Deployment Steps

1. **Push code to GitHub:**
   ```bash
   git add .
   git commit -m "Complete final project"
   git push origin main
   ```

2. **GitHub Actions will automatically:**
   - Run tests
   - Build frontend
   - Deploy frontend to Vercel
   - Deploy backend to Vercel

3. **Verify deployment:**
   - Check GitHub Actions logs
   - Check Vercel Dashboard
   - Test deployed applications

---

## 🐛 Troubleshooting

### Backend Issues

**Database Connection Error:**
- Verify `MONGODB_URI` di `.env`
- Check MongoDB Atlas IP whitelist (`0.0.0.0/0`)
- Verify database user credentials

**JWT Authentication Error:**
- Verify `JWT_SECRET` is set (min 32 characters)
- Check token format in Authorization header

**Port Already in Use:**
- Change PORT di `.env`
- Or kill process using port 3001

### Frontend Issues

**API Connection Error:**
- Verify `VITE_API_URL` di `.env`
- Check backend is running
- Check CORS configuration

**Build Errors:**
- Clear `node_modules` and reinstall
- Check Node version (22+)
- Check environment variables

### Deployment Issues

**Vercel Deployment Failed:**
- Check GitHub Secrets
- Verify Vercel Token
- Check Project IDs
- Review Vercel logs

**CI/CD Pipeline Failed:**
- Check GitHub Actions logs
- Verify all secrets are set
- Check workflow file syntax

---

## 📚 Resources

- [Express Documentation](https://expressjs.com)
- [React Documentation](https://react.dev)
- [MongoDB Atlas Documentation](https://docs.atlas.mongodb.com)
- [Vercel Documentation](https://vercel.com/docs)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [PNPM Documentation](https://pnpm.io)
- [Turbo Documentation](https://turbo.build)

---

## ✅ Checklist Final Project

### ✅ Aplikasi (Sudah Complete)
- [x] Express app setup complete
- [x] User model dengan password hashing
- [x] Todo model dengan user relationship
- [x] Authentication middleware
- [x] Auth routes (register, login)
- [x] Todo routes (CRUD) dengan authentication
- [x] Swagger documentation
- [x] Error handling
- [x] Vercel serverless wrapper
- [x] Vite configuration
- [x] Auth utilities
- [x] API utilities dengan interceptors
- [x] Login page
- [x] Register page
- [x] Dashboard page dengan CRUD
- [x] Routing setup
- [x] Error handling
- [x] Loading states

### 🚀 Deployment (Tugas Anda)
- [ ] MongoDB Atlas setup
- [ ] Vercel projects created (Backend + Frontend)
- [ ] Environment variables configured di Vercel
- [ ] GitHub Secrets configured
- [ ] CI/CD pipeline implemented (`.github/workflows/ci-cd.yml`)
- [ ] Both apps deployed successfully
- [ ] End-to-end testing di production
- [ ] Monitoring & debugging setup

---

## 🎓 Learning Objectives

Setelah menyelesaikan deployment tasks, Anda akan memahami:

1. ✅ **DevOps Practices:**
   - CI/CD pipeline setup dengan GitHub Actions
   - Environment variables management
   - Secrets management
   - Deployment automation

2. ✅ **Cloud Services:**
   - MongoDB Atlas setup dan configuration
   - Vercel serverless deployment
   - Static site deployment
   - Environment configuration

3. ✅ **Infrastructure:**
   - Monorepo deployment strategy
   - Separate backend/frontend deployments
   - Production environment setup
   - Monitoring dan debugging

4. ✅ **Best Practices:**
   - Secure credential management
   - Automated testing in CI/CD
   - Production deployment workflow
   - Error monitoring

---

**Selamat berlatih menjadi DevOps Engineer! 🚀**

Aplikasi sudah complete dan siap digunakan. Fokus Anda adalah:
- ✅ Setup infrastructure (MongoDB, Vercel)
- ✅ Configure CI/CD pipeline
- ✅ Deploy ke production
- ✅ Monitor dan maintain

Jika ada pertanyaan atau kesulitan, jangan ragu untuk bertanya atau melihat referensi dari finished project.

---

## 📚 Quick Reference

### Local Development

```bash
# Install dependencies
pnpm install

# Run backend
pnpm --filter backend dev

# Run frontend
pnpm --filter frontend dev

# Run both
pnpm dev
```

### Deployment Commands

```bash
# Build all
pnpm build

# Test
pnpm test

# Deploy (via GitHub Actions)
git push origin main
```

### Important URLs

**Local:**
- Frontend: http://localhost:5173
- Backend: http://localhost:3001
- API Docs: http://localhost:3001/api-docs

**Production (setelah deployment):**
- Frontend: `https://your-frontend.vercel.app`
- Backend: `https://your-backend.vercel.app`
- API Docs: `https://your-backend.vercel.app/api-docs`

