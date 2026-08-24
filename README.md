# 🎓 SmartSchool MA

**Professional SaaS School Management & AI Education Platform**

A comprehensive, modern, and secure platform designed for educational institutions to manage academic operations, student progress, administrative tasks, and AI-powered learning experiences.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Quick Start](#quick-start)
- [Architecture](#architecture)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

---

## 🌟 Overview

SmartSchool MA is a **multi-tenant SaaS platform** for schools offering:

- 👥 **Complete User Management** (Students, Parents, Teachers, Administration, Employees)
- 📚 **Academic Management** (Courses, Homework, Exams, Grades, Attendance)
- 💳 **Financial Management** (Payments, Receipts, Invoicing)
- 🚌 **Transport & Pickup Management**
- 🤖 **AI-Powered Learning** (Tutoring, Content Generation, Assessment)
- 🎮 **Gamification** (XP, Badges, Levels, Leaderboards)
- 📊 **Analytics & Reporting**
- 🔐 **Enterprise-Grade Security**
- 📱 **Fully Responsive** (Desktop, Tablet, Mobile)

---

## ✨ Key Features

### For Students
- ✅ Personalized Dashboard with Progress Tracking
- ✅ Access to General & Teacher-Created Courses
- ✅ AI-Powered Tutor for Learning Support
- ✅ Homework & Exam Management
- ✅ Grade Tracking & Bulletins
- ✅ Study Tools (Flashcards, Pomodoro, Simulations)
- ✅ Gamification System
- ✅ Career Orientation Guidance

### For Parents
- ✅ Child Progress Monitoring
- ✅ Grades & Attendance Tracking
- ✅ Payment Management
- ✅ Transport & Pickup Requests
- ✅ School Communication
- ✅ Event Notifications

### For Teachers
- ✅ Class & Student Management
- ✅ Course Content Creation
- ✅ Homework & Exam Management
- ✅ AI-Assisted Content Generation
- ✅ Attendance Tracking
- ✅ Grade Management
- ✅ Student Assessment Tools

### For Administration
- ✅ Complete School Management
- ✅ User & Permission Management
- ✅ Financial Oversight
- ✅ Transport Management
- ✅ Analytics & Reporting
- ✅ Document Management

### For Super Admin
- ✅ Multi-School Management
- ✅ Subscription & Billing
- ✅ Platform Analytics
- ✅ Support Management

---

## 🛠 Tech Stack

### Frontend
- **Framework**: Next.js 14+ (React)
- **Styling**: Tailwind CSS + shadcn/ui
- **State Management**: Zustand
- **API Client**: TanStack Query
- **Forms**: React Hook Form + Zod
- **Auth**: NextAuth.js
- **Charts**: Recharts
- **Internationalization**: next-i18next

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js / Fastify
- **Database**: PostgreSQL
- **ORM**: Prisma
- **Authentication**: JWT + Refresh Tokens
- **File Storage**: S3 / Cloud Storage
- **Task Queue**: BullMQ
- **Caching**: Redis
- **Email**: Nodemailer / SendGrid

### DevOps & Infrastructure
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Deployment**: AWS / GCP / Azure
- **Database**: PostgreSQL + Migrations
- **Monitoring**: Sentry + LogRocket
- **APM**: New Relic / DataDog

### AI Integration
- **Provider Agnostic**: Support for Claude, GPT, Gemini
- **Vector DB**: Pinecone / Supabase (for embeddings)
- **PDF Processing**: pdf-parse / PyPDF2
- **Document Analysis**: LangChain

---

## 📁 Project Structure

```
smartschool-ma/
├── apps/
│   ├── web/                      # Next.js Frontend Application
│   │   ├── src/
│   │   │   ├── app/              # App Router (pages)
│   │   │   ├── components/       # Reusable Components
│   │   │   ├── features/         # Feature Modules
│   │   │   ├── hooks/            # Custom Hooks
│   │   │   ├── lib/              # Utilities & Helpers
│   │   │   ├── services/         # API Clients
│   │   │   ├── store/            # Zustand Stores
│   │   │   ├── styles/           # Global Styles
│   │   │   └── types/            # TypeScript Types
│   │   ├── public/               # Static Assets
│   │   ├── package.json
│   │   └── tsconfig.json
│   │
│   └── api/                      # Express.js Backend Application
│       ├── src/
│       │   ├── server.ts         # Express Configuration
│       │   ├── auth/             # Authentication Logic
│       │   ├── routes/           # API Routes
│       │   ├── controllers/      # Request Handlers
│       │   ├── services/         # Business Logic
│       │   ├── repositories/     # Database Queries
│       │   ├── middleware/       # Custom Middleware
│       │   ├── validators/       # Input Validation
│       │   ├── utils/            # Utilities
│       │   ├── ai/               # AI Integration
│       │   ├── jobs/             # Background Jobs
│       │   └── config/           # Configuration
│       ├── prisma/
│       │   ├── schema.prisma     # Database Schema
│       │   └── migrations/       # Database Migrations
│       ├── package.json
│       └── tsconfig.json
│
├── packages/
│   ├── shared/                   # Shared Types & Utils
│   │   ├── src/
│   │   │   ├── types/
│   │   │   ├── schemas/          # Zod Schemas
│   │   │   ├── constants/
│   │   │   └── utils/
│   │   └── package.json
│   │
│   ├── database/                 # Database Client & Utilities
│   │   ├── src/
│   │   │   ├── client.ts
│   │   │   ├── seed.ts
│   │   │   └── migrations/
│   │   └── package.json
│   │
│   └── ui/                       # Component Library & Design System
│       ├── src/
│       │   ├── components/
│       │   │   ├── Button/
│       │   │   ├── Input/
│       │   │   ├── Card/
│       │   │   ├── Modal/
│       │   │   ├── Table/
│       │   │   └── ...
│       │   ├── themes/
│       │   ├── styles/
│       │   └── index.ts
│       └── package.json
│
├── docs/
│   ├── architecture/
│   ├── api/
│   ├── database/
│   ├── deployment/
│   └── user-guides/
│
├── .github/
│   ├── workflows/
│   │   ├── ci.yml
│   │   ├── deploy.yml
│   │   └── security.yml
│   └── ISSUE_TEMPLATE/
│
├── docker-compose.yml
├── .env.example
├── package.json
├── pnpm-workspace.yaml
└── README.md
```

---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- pnpm 8+
- PostgreSQL 14+
- Docker & Docker Compose (optional)

### Installation

```bash
# Clone repository
git clone https://github.com/mohcinemed35-spec/SMARTSCHOOL.git
cd SMARTSCHOOL

# Install dependencies
pnpm install

# Setup environment variables
cp .env.example .env.local

# Setup database
pnpm db:push
pnpm db:seed

# Start development servers
pnpm dev
```

### Development Servers
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:3001
- **Database**: postgresql://localhost:5432/smartschool

---

## 🏗 Architecture

### Multi-Tenant Architecture
- **School Isolation**: Each school is a separate tenant with complete data isolation
- **Row-Level Security**: Database policies enforce tenant boundaries
- **Subdomain Routing**: Dynamic tenant routing via URL
- **Shared Infrastructure**: Efficient resource utilization across tenants

### Authentication & Authorization
- **JWT-based Authentication**: Secure token-based auth
- **RBAC**: Role-Based Access Control with custom permissions
- **Session Management**: Secure session handling with refresh tokens
- **2FA Ready**: Framework for two-factor authentication

### API Architecture
- **RESTful Design**: Clean, predictable API endpoints
- **Standardized Responses**: Consistent error and success formats
- **Pagination & Filtering**: Efficient data retrieval
- **API Versioning**: Support for multiple API versions

### Database Design
- **Normalized Schema**: ACID compliance and data integrity
- **Soft Deletes**: Preserve data history and allow recovery
- **Audit Logging**: Track all critical changes
- **Migrations**: Version-controlled schema changes

---

## 📚 API Documentation

See [API Documentation](./docs/api/) for detailed endpoint specifications.

### Core API Routes

```
/api/v1/auth/                    - Authentication
/api/v1/schools/                 - School Management
/api/v1/users/                   - User Management
/api/v1/students/                - Student Management
/api/v1/parents/                 - Parent Management
/api/v1/teachers/                - Teacher Management
/api/v1/employees/               - Employee Management
/api/v1/classes/                 - Class Management
/api/v1/courses/                 - Course Management
/api/v1/homework/                - Homework Management
/api/v1/exams/                   - Exam Management
/api/v1/grades/                  - Grade Management
/api/v1/attendance/              - Attendance Tracking
/api/v1/payments/                - Payment Management
/api/v1/transport/               - Transport Management
/api/v1/pickup/                  - Pickup Requests
/api/v1/ai/                      - AI Services
/api/v1/notifications/           - Notifications
/api/v1/documents/               - Document Management
/api/v1/analytics/               - Analytics
/api/v1/admin/                   - Administration
```

---

## 🔒 Security

- ✅ OWASP Top 10 Protection
- ✅ SQL Injection Prevention (Parameterized Queries)
- ✅ XSS Protection (Content Security Policy)
- ✅ CSRF Protection (Tokens)
- ✅ Rate Limiting & DDoS Protection
- ✅ Data Encryption (TLS/SSL)
- ✅ Password Hashing (bcrypt)
- ✅ Secure Session Management
- ✅ Audit Logging
- ✅ Regular Security Updates

---

## 📊 Development Status

| Module | Status | Priority |
|--------|--------|----------|
| Core Architecture | ⏳ In Progress | P0 |
| Authentication | ⏳ In Progress | P0 |
| Database Schema | ⏳ In Progress | P0 |
| API Framework | ⏳ In Progress | P0 |
| Design System | ⏳ In Progress | P1 |
| Student Dashboard | ⏳ Planned | P1 |
| Teacher Dashboard | ⏳ Planned | P1 |
| Admin Dashboard | ⏳ Planned | P1 |
| Course Management | ⏳ Planned | P1 |
| Payments | ⏳ Planned | P1 |
| Transport | ⏳ Planned | P2 |
| AI Integration | ⏳ Planned | P2 |
| Analytics | ⏳ Planned | P2 |

---

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

---

## 📧 Support

For support, please open an issue or contact support@smartschool.ma

---

**Built with ❤️ for Education | SmartSchool MA © 2026**
