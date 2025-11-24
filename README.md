# Employee Management System

A full-stack employee management application built with Node.js, Express, MongoDB, and React.

## Features

- User authentication (Signup/Login)
- Employee CRUD operations (Create, Read, Update, Delete)
- RESTful API
- React frontend with Material-UI

## Tech Stack

- **Backend:** Node.js, Express, MongoDB
- **Frontend:** React, Material-UI, React Router
- **Deployment:** Docker Compose

## Quick Start

### Using Docker Compose

1. Clone the repository
2. Run: `docker-compose up --build`
3. Access the application at: http://localhost:3000
4. Backend API: http://localhost:3001

### Manual Setup

**Backend:**
```bash
cd backend
npm install
npm start
```

**Frontend:**
```bash
cd frontend
npm install
npm start
```

## API Endpoints

- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/employees` - Create employee
- `GET /api/employees` - Get all employees
- `GET /api/employees/:id` - Get employee by ID
- `PUT /api/employees/:id` - Update employee
- `DELETE /api/employees/:id` - Delete employee

## Project Structure

```
├── backend/          # Node.js/Express API
├── frontend/         # React application
└── docker-compose.yml
```
