Makom Lanefesh - Mental Health Platform
Project Overview
Makom Lanefesh is a professional mental health platform that connects clients with therapists and mental health professionals. The platform enables therapists to manage their profiles and schedules, allows clients to search and book sessions, and provides a comprehensive solution for the mental health industry in Israel.
Key Features
For Therapists

Professional profile creation and management
Calendar and appointment scheduling
Integrated payment system
Client management tools
Analytics and reporting

For Clients

Search therapists by location, specialization, and price
Online appointment booking
Review and rating system
Treatment history tracking
Automated reminders

For Administrators

User and content management
Professional admin panel
Data analytics and reports
Support system

Project Structure
makom-lanefesh/
├── backend/                     # Server Layer (C# .NET Core)
│   ├── MakomLanefesh.API/      # Web API Controllers
│   ├── MakomLanefesh.Core/     # Business Logic & Models
│   ├── MakomLanefesh.Data/     # Data Access Layer
│   └── MakomLanefesh.Tests/    # Unit & Integration Tests
├── frontend/                   # Client Layer (React TypeScript)
│   ├── public/                 # Static files
│   ├── src/                    # Source code
│   │   ├── components/         # React components
│   │   ├── pages/              # Page components
│   │   ├── hooks/              # Custom hooks
│   │   ├── services/           # API services
│   │   ├── utils/              # Utility functions
│   │   └── assets/             # Images, fonts, etc.
│   └── package.json
├── docs/                       # Project Documentation
│   ├── API.md                  # API Documentation
│   ├── DATABASE.md             # Database Schema
│   └── DEPLOYMENT.md           # Deployment Guide
├── docker-compose.yml          # Docker configuration
├── .gitignore                  # Git ignore rules
└── README.md                   # This document
Technology Stack
Backend

Framework: .NET 8 Web API
Database: PostgreSQL
ORM: Entity Framework Core
Authentication: JWT + Identity
Cache: Redis
File Storage: AWS S3 / Azure Blob
Testing: xUnit, FluentAssertions

Frontend

Framework: React 18 + TypeScript
State Management: Redux Toolkit + RTK Query
UI Library: Material-UI (MUI)
Forms: React Hook Form + Yup
Testing: Jest + React Testing Library
Build Tool: Vite

DevOps & Infrastructure

Containerization: Docker + Docker Compose
CI/CD: GitHub Actions
Monitoring: Application Insights
Deployment: Azure App Service / AWS

Installation & Setup
Prerequisites

Node.js 18+
.NET 8 SDK
PostgreSQL 15+
Docker (optional)

Local Development Setup

Clone the repository:

bashgit clone https://github.com/your-username/makom-lanefesh-website.git
cd makom-lanefesh-website

Backend Setup:

bashcd backend
dotnet restore
dotnet ef database update
dotnet run --project MakomLanefesh.API

Frontend Setup:

bashcd frontend
npm install
npm run dev
Docker Setup
bashdocker-compose up -d
The application will be available at: http://localhost:3000
The API will be available at: http://localhost:5000
Contributing
Code Standards

Hebrew: Variable and function names in Hebrew for business logic
English: Technical names and framework-related code
Linting: ESLint (Frontend) + StyleCop (Backend)
Testing: Minimum 80% code coverage

Contribution Process

Create a new branch from develop
Make changes with clear commit messages
Write or update tests
Create Pull Request with detailed description
Wait for code review approval

Commit Conventions
feat: add new feature
fix: fix bug
docs: update documentation
test: add or update tests
refactor: improve existing code
style: styling changes
Environment Variables
Backend (.env)
envDATABASE_CONNECTION_STRING=Server=localhost;Database=makom_lanefesh;...
JWT_SECRET_KEY=your-secret-key
REDIS_CONNECTION_STRING=localhost:6379
AWS_S3_BUCKET=your-bucket-name
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
Frontend (.env)
envVITE_API_URL=http://localhost:5000/api
VITE_GOOGLE_MAPS_API_KEY=your-google-maps-key
VITE_STRIPE_PUBLISHABLE_KEY=your-stripe-key
Available Scripts
Backend
bashdotnet run                    # Run the API
dotnet test                   # Run tests
dotnet ef migrations add      # Add new migration
dotnet ef database update     # Update database
Frontend
bashnpm run dev                   # Start development server
npm run build                 # Build for production
npm run test                  # Run tests
npm run lint                  # Run linter
npm run preview               # Preview production build
API Documentation
The API documentation is automatically generated using Swagger/OpenAPI and is available at:

Development: http://localhost:5000/swagger
Production: https://api.makom-lanefesh.co.il/swagger

Database Schema
The database uses PostgreSQL with Entity Framework Core. Key entities include:

Users (Clients, Therapists, Admins)
Appointments
Reviews
Payments
Notifications

See DATABASE.md for detailed schema information.
Testing
Backend Testing
bashcd backend
dotnet test --collect:"XPlat Code Coverage"
Frontend Testing
bashcd frontend
npm run test
npm run test:coverage
Deployment
Production Deployment
The application is deployed using GitHub Actions CI/CD pipeline:

Tests are run automatically on PR
Build artifacts are created
Docker images are built and pushed
Deployment to Azure/AWS is triggered

See DEPLOYMENT.md for detailed deployment instructions.
Security

JWT token authentication
HTTPS enforcement
Input validation and sanitization
SQL injection prevention via EF Core
XSS protection
CSRF protection
Rate limiting

Performance

Database query optimization
Redis caching layer
Image compression and CDN
Code splitting and lazy loading
API response compression

License
This project is licensed under the MIT License. See the LICENSE file for details.
Development Team

Product Owner: [Name]
Tech Lead: [Name]
Frontend Developer: [Name]
Backend Developer: [Name]
UI/UX Designer: [Name]

Support & Links

API Documentation
Database Schema
Deployment Guide
Issues
Project Board

Project Status
🚧 In Development - Version 1.0.0 expected on [Date]
Current Version Goals

 User authentication system
 Therapist profile management
 Search and filtering system
 Basic booking system
 Admin management panel


📧 Contact: contact@makom-lanefesh.co.il
🌐 Website: https://makom-lanefesh.co.il