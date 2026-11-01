# 🎓 Student Management System

A full-stack web application for managing student records, built with React, Express, PostgreSQL, and Prisma.

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React.js, Tailwind CSS, Vite |
| Backend | Node.js, Express.js |
| Database | PostgreSQL, Prisma ORM |
| Auth | JWT, bcrypt |

## 📁 Project Structure

```
website/
├── backend/           # Express API server
│   ├── prisma/        # Database schema & migrations
│   ├── src/
│   │   ├── controllers/   # Route handlers
│   │   ├── middleware/    # Auth & validation
│   │   ├── routes/        # API routes
│   │   └── server.js      # Entry point
│   └── .env.example
├── frontend/          # React application
│   ├── src/
│   │   ├── components/    # Reusable UI
│   │   ├── context/       # Auth context
│   │   ├── pages/         # Page views
│   │   ├── services/      # API calls
│   │   └── App.jsx
│   └── .env
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- PostgreSQL database (local or [Neon](https://neon.tech))

### Backend Setup
```bash
cd backend
cp .env.example .env     # Edit with your database URL
npm install
npx prisma migrate dev   # Create database tables
npm run dev              # Start on port 5000
```

### Frontend Setup
```bash
cd frontend
npm install
npm run dev              # Start on port 5173
```

## 🔌 API Endpoints

### Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/auth/register | Register new user |
| POST | /api/auth/login | Login |
| GET | /api/auth/profile | Get profile |

### Students (requires auth)
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/students | List all (with search) |
| GET | /api/students/:id | Get by ID |
| POST | /api/students | Create |
| PUT | /api/students/:id | Update |
| DELETE | /api/students/:id | Delete |

## 🌐 Deployment

- **Frontend**: Vercel
- **Backend**: Render
- **Database**: Neon PostgreSQL

## 📝 License

MIT

