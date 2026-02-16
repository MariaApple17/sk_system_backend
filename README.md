# 🚀 SK System Backend  
**Express + Prisma + MySQL**

Backend API for **SK System**, built with **Express.js**, **Prisma ORM**, **MySQL**, and **JWT Authentication**.  
Supports **Role-Based Access Control (RBAC)**, **Budgeting**, **Procurement**, **Approval Workflow**, and **System Settings**.

---

## 🛠 Tech Stack

- Node.js (v18+)
- Express.js
- Prisma ORM
- MySQL
- JWT Authentication
- bcrypt
- ES Modules

---

## 📁 Project Structure

```
sk_system_backend/
├─ prisma/
│  ├─ schema.prisma
│  ├─ seed.js
│  └─ prisma.config.ts
├─ src/
│  ├─ controllers/
│  ├─ services/
│  ├─ routes/
│  ├─ middlewares/
│  ├─ constants/
│  │  └─ permission.constant.js
│  ├─ config/
│  │  └─ db.config.js
│  └─ app.js
├─ server.js
├─ .env
├─ package.json
└─ README.md
```

---

## ✅ Prerequisites

- Node.js **v18+**
- MySQL **v8+**
- npm or yarn

---

## 📦 Installation Guide

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/MariaApple17/sk_system_backend.git
cd sk_system_backend
```

---

### 2️⃣ Install Dependencies

```bash
npm install
```

---

### 3️⃣ Environment Variables

Create a `.env` file in the root directory:

```env
# =====================================================
# Environment Variables Template
# Copy this file to .env and fill in real values locally
# =====================================================

# Database connection (Neon / PostgreSQL)
DATABASE_URL="postgresql://<DB_USER>:<DB_PASSWORD>@<DB_HOST>/<DB_NAME>?sslmode=require"
PORT=3001
NODE_ENV=development

# JWT configuration
JWT_SECRET="<YOUR_JWT_SECRET>"
JWT_EXPIRES_IN="1d"

# Bcrypt salt rounds for password hashing
BCRYPT_SALT_ROUNDS=10

# Cloudinary access credentials
#CLOUDINARY_CLOUD_NAME="<CLOUDINARY_CLOUD_NAME>"
#CLOUDINARY_API_KEY="<CLOUDINARY_API_KEY>"
#CLOUDINARY_API_SECRET="<CLOUDINARY_API_SECRET>"

# Cloudinary root folder
#CLOUDINARY_ROOT_FOLDER="sk_systems"

# Feature subfolders
#CLOUDINARY_SK_OFFICIALS_FOLDER=sk-officials
#CLOUDINARY_PROGRAMS_FOLDER=programs
#CLOUDINARY_PROCUREMENT_FOLDER=procurement-proofs
#CLOUDINARY_SYSTEM_PROFILE_FOLDER=system-profile


```

⚠️ **Never commit `.env` to version control**

---

## 🗄 Database Setup

```sql
CREATE DATABASE sk_system_db;
```

---

## 🧬 Prisma Setup & Migration

```bash
npx prisma generate
npx prisma migrate dev --name init
```

---

## 🌱 Database Seeding

Default SUPER ADMIN is created.

```
Email: admin@system.local
Password: Admin@12345
Role: SUPER_ADMIN
```

```bash
npx prisma db seed
```

---

## ▶️ Running the Server

```bash
npm run dev
```

Server:
```
http://localhost:3001
```

---

## 🔐 Authentication

```
Authorization: Bearer <token>
```

---

## 🚀 Production Notes

- Change default admin password
- Use strong secrets
- Enable rate limiting

---

## 📌 Common Commands

```bash
npm install
npx prisma generate
npx prisma migrate dev
npx prisma db seed
npm run dev
```
