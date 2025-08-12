# SpotlessWorld

Welcome to the official repository of **SpotlessWorld**, a modern cleaning service platform built with **React**, **TypeScript**, **TanStack Start**, **Tailwind CSS**, and a robust **Node.js + Express + PostgreSQL** backend.
This documentation provides a comprehensive guide to the project’s structure, components, and setup instructions.

---

## Table of Contents

1. Introduction
2. Project Structure
3. Installation
4. Usage
5. Components
6. Assets
7. Dependencies
8. Database & Data Models
9. Contributing
10. Progress

---

## Introduction

SpotlessWorld is a full-featured cleaning services platform that connects clients with professional cleaners for **home**, **industrial**, and **event/party** cleaning.
The platform includes an intuitive booking system, role-based dashboards for **Super Admin**, **Admin**, **Workers**, and **Customers**, as well as order tracking, online payment integration, and a company blog.

---

## Project Structure

```
spotlessworld/
├── client/                      # Frontend (React + TypeScript + TanStack Start)
│   ├── public/                   # Public assets
│   ├── src/
│   │   ├── api/                  # API integration services
│   │   ├── assets/               # Static assets (images, fonts, icons)
│   │   ├── components/           # Reusable UI components
│   │   │   ├── Navbar.tsx
│   │   │   ├── Footer.tsx
│   │   │   ├── ServiceCard.tsx
│   │   │   ├── DashboardSidebar.tsx
│   │   │   └── OrderCard.tsx
│   │   ├── hooks/                # Custom React hooks
│   │   ├── pages/                # Page components
│   │   │   ├── Home.tsx
│   │   │   ├── About.tsx
│   │   │   ├── Contact.tsx
│   │   │   ├── Blog.tsx
│   │   │   ├── Services.tsx
│   │   │   ├── Dashboard.tsx
│   │   │   └── Login.tsx
│   │   ├── store/                # State management (Zustand or Redux)
│   │   ├── utils/                 # Utility functions
│   │   ├── App.tsx                # Root component
│   │   └── main.tsx               # App entry point
│   └── package.json
│
├── server/                       # Backend (Node.js + Express + TypeScript)
│   ├── src/
│   │   ├── config/                # Database, environment configs
│   │   ├── controllers/           # Business logic
│   │   ├── middlewares/           # Auth, error handling
│   │   ├── models/                # Database models (Prisma / TypeORM)
│   │   ├── routes/                # API endpoints
│   │   ├── utils/                  # Helpers
│   │   └── server.ts               # Server entry point
│   └── package.json
│
├── prisma/                        # Prisma schema & migrations
├── .gitignore
├── README.md
└── package.json
```

---

## Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/spotlessworld.git
```

### 2️⃣ Navigate to the project directory

```bash
cd spotlessworld
```

### 3️⃣ Install dependencies for both frontend & backend

```bash
cd client && npm install
cd ../server && npm install
```

### 4️⃣ Set up environment variables

Create a `.env` file in the `server/` folder:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/spotlessworld
JWT_SECRET=your_jwt_secret
```

---

## Usage

### Run backend

```bash
cd server
npm run dev
```

### Run frontend

```bash
cd client
npm run dev
```

---

## Components

**Navbar** – Main navigation across public pages.
**ServiceCard** – Displays service details, pricing, and booking button.
**DashboardSidebar** – Navigation for role-based dashboards.
**OrderCard** – Shows booking details and status.

---

## Assets

All images, logos, and icons are stored in `client/src/assets/`.

---

## Dependencies

**Frontend:**

- React 19
- TypeScript
- TanStack Start
- Tailwind CSS
- Zustand / Redux
- React Query
- React Router
- Framer Motion

**Backend:**

- Node.js + Express
- TypeScript
- Prisma (PostgreSQL ORM)
- bcrypt & jsonwebtoken (Auth)
- Multer (Image uploads)

---

## Database & Data Models

**Core Tables:**

- `User` (SuperAdmin, Admin, Worker, Customer)
- `Service` (title, description, price)
- `Order` (serviceId, customerId, workerId, status)
- `Payment`
- `BlogPost`

---

## Contributing

We welcome contributions from developers.

1. Fork the repo
2. Create a new branch:

   ```bash
   git checkout -b feature/your-feature
   ```

3. Commit changes:

   ```bash
   git commit -m "Added new feature"
   ```

4. Push to branch:

   ```bash
   git push origin feature/your-feature
   ```

5. Open a PR

---

## Progress

**✅ Completed:**

- Home, About, Contact, Blog pages
- Authentication system with RBAC
- Booking system
- Admin & Worker dashboards
- Payment integration

**🚧 In Progress:**

- Real-time order tracking
- Email/SMS notifications
- Performance optimization
