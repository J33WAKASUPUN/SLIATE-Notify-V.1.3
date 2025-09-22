# SLIATE-Notify V.1.3

![SLIATE-Notify](SLIATENotifyBanner.png)

<div align="center">
  <img src="https://img.shields.io/badge/version-1.3.0-blue.svg" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-green.svg" alt="License">
  <img src="https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen.svg" alt="Node Version">
  <img src="https://img.shields.io/badge/security-enhanced-red.svg" alt="Security">
</div>

## 🎯 Overview

**SLIATE-Notify** is a comprehensive notice management system designed specifically for Sri Lanka Institute of Advanced Technological Education (SLIATE) Kandy. The system provides a secure platform for administrators to create, manage, and publish official notices while offering a public interface for students and staff to view announcements.

### ✨ Key Features

- **🔐 Secure Notice Management** - Complete CRUD operations with draft/published workflow
- **📝 Rich Text Editor** - Markdown support with file attachments
- **🌐 Public Access** - Non-authenticated viewing of published notices
- **🔍 Advanced Search** - Full-text search with filtering and pagination
- **📁 File Upload System** - Secure file handling with multi-layer validation
- **📊 Analytics Dashboard** - Site visit tracking and usage statistics
- **🛡️ Enterprise Security** - Role-based access control with comprehensive audit trail

## 🏗️ Architecture

The system follows a **three-tier architecture** with clear separation of concerns:

- **Frontend**: React 18 + TypeScript with Vite
- **Backend**: Node.js + Express.js with comprehensive security layers
- **Database**: MySQL with optimized queries and data integrity

## 🚀 Technology Stack

### Frontend
- **Framework**: React 18.3.1 with TypeScript
- **Build Tool**: Vite 5.4.1 for lightning-fast development
- **UI Library**: Radix UI primitives with shadcn/ui components
- **Styling**: Tailwind CSS with custom animations
- **State Management**: Redux Toolkit + React Query
- **Routing**: React Router DOM
- **Forms**: React Hook Form + Zod validation

### Backend
- **Runtime**: Node.js (≥18.0.0)
- **Framework**: Express.js 4.19.2
- **Database**: MySQL2 3.14.1 with connection pooling
- **Authentication**: JWT tokens + bcryptjs hashing
- **File Processing**: Multer 2.0.1 + Sharp 0.34.2
- **Security**: Helmet, CORS, express-validator
- **Session Management**: Redis with express-session
- **Rate Limiting**: Advanced rate limiting and slow-down protection

## 📋 Prerequisites

Before installation, ensure you have:

- **Node.js** ≥ 18.0.0
- **npm** ≥ 8.0.0
- **MySQL** database server
- **Redis** server (for session management)

## ⚡ Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/J33WAKASUPUN/sliate-notice-system.git
cd SLIATE-Notify-V.1.3
```

### 2. Backend Setup

```bash
cd server
npm install
npm run setup:env
npm run db:migrate
npm run dev
```

### 3. Frontend Setup

```bash
cd ../client
npm install
npm run dev
```

The application will be available at:
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:3000

## 🔧 Development Scripts

### Backend Commands

```bash
npm start              # Production server
npm run dev           # Development with auto-reload
npm test              # Run complete test suite
npm run test:security # Security-focused testing
npm run lint          # Code quality analysis
npm run security:check # Comprehensive security audit
```

### Frontend Commands

```bash
npm run dev           # Vite development server
npm run build         # Production build
npm run lint          # ESLint analysis
npm run preview       # Preview production build
```

## 🧪 Testing & Quality Assurance

Our testing strategy ensures **80% minimum coverage** across all metrics:

- **API Testing**: Complete endpoint coverage
- **Security Testing**: SQL injection, XSS, authentication tests
- **Unit Testing**: Individual component testing
- **Integration Testing**: End-to-end workflow validation

```bash
npm test                    # Run all tests
npm run test:security      # Security-focused tests
npm run test:coverage      # Generate coverage report
npm run test:ci           # CI/CD optimized testing
```

## 📚 API Documentation

### Public Endpoints (No Authentication)
```
GET  /api/public/notices        # Retrieve published notices
GET  /api/public/notices/:slug  # Get specific notice
GET  /api/public/search         # Search published notices
GET  /api/public/info          # Site information
```

### Admin Endpoints (Authentication Required)
```
POST   /api/notices            # Create new notice
PUT    /api/notices/:id        # Update existing notice
DELETE /api/notices/:id        # Delete notice
GET    /api/notices/search     # Admin search with filters
POST   /api/upload             # File upload functionality
```

## 🔒 Security Features

SLIATE-Notify implements **enterprise-grade security**:

- **Authentication & Authorization**: Role-based access (admin, super_admin)
- **SQL Injection Prevention**: Parameterized queries + input sanitization
- **XSS Protection**: Content sanitization + security headers
- **File Security**: Multi-layer validation + secure upload handling
- **Rate Limiting**: API protection against abuse
- **Security Logging**: Comprehensive audit trail
- **CSRF Protection**: Cross-site request forgery prevention

### Security Testing

```bash
npm run test:sql              # SQL injection tests
npm run test:xss              # XSS protection tests
npm run test:auth             # Authentication tests
npm run security:scan         # Vulnerability scanning
```

## 📊 Project Statistics

- **Lines of Code**: 15,000+ (Backend + Frontend)
- **Test Coverage**: 80%+ across all metrics
- **Security Rules**: 14+ ESLint security rules enforced
- **API Endpoints**: 12+ fully documented endpoints

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Implement** changes with comprehensive tests
4. **Run** security checks (`npm run security:check`)
5. **Submit** a pull request with detailed description

### Code Standards

- ESLint with Airbnb base configuration
- Security plugin enforcement
- Comprehensive test coverage required
- Security-first development approach

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Authors

**J33WAKASUPUN**
- GitHub: [@J33WAKASUPUN](https://github.com/J33WAKASUPUN)

**Thisara404**
- GitHub: [@Thisara404](https://github.com/Thisara404)

## 💖 Support

If you find this project helpful, consider:
- ⭐ Starring the repository
- 🐛 Reporting issues
- 💡 Suggesting improvements

## 📞 Support & Issues

- **Bug Reports**: [GitHub Issues](https://github.com/J33WAKASUPUN/sliate-notice-system/issues)
- **Feature Requests**: [GitHub Discussions](https://github.com/J33WAKASUPUN/sliate-notice-system/discussions)
- **Email**: j33wakasupun@sliate.ac.lk

---

<div align="center">
  <strong>Built with ❤️ for SLIATE Kandy</strong>
  <br>
  <em>Fast. Simple. Reliable. Secure.</em>
</div>
