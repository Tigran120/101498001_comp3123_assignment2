# Employee Management System - Backend API

Backend API for Employee Management System built with Node.js, Express, and MongoDB.

## Features

- User authentication (Signup/Login) with JWT tokens
- Employee CRUD operations
- RESTful API design
- Input validation and error handling
- MongoDB integration

## Tech Stack

- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Express Validator for input validation
- Bcrypt for password hashing

## Installation

```bash
npm install
```

## Configuration

Create a `.env` file:

```env
PORT=3001
MONGODB_URI=mongodb://localhost:27017/employee_management
JWT_SECRET=your_super_secret_jwt_key_change_this_in_production
NODE_ENV=development
```

## Running the Server

```bash
# Development
npm run dev

# Production
npm start
```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login

### Employees
- `POST /api/employees` - Create employee (requires auth)
- `GET /api/employees` - Get all employees (requires auth)
- `GET /api/employees/:id` - Get employee by ID (requires auth)
- `PUT /api/employees/:id` - Update employee (requires auth)
- `DELETE /api/employees/:id` - Delete employee (requires auth)

## Project Structure

```
backend/
├── models/          # MongoDB models (User, Employee)
├── routes/          # API routes (auth, employees)
├── middleware/      # Auth and upload middleware
├── server.js        # Main server file
└── package.json
```

## Docker

To run with Docker:

```bash
docker build -t employee-backend .
docker run -p 3001:3001 employee-backend
```

Or use docker-compose from the root directory.

