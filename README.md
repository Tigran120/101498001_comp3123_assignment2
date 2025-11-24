# Employee Management System

A full-stack employee management application built with Node.js, Express, MongoDB, and React.

## Features

### Backend
- User authentication (Signup/Login) with JWT tokens
- CRUD operations for employees
- File upload for employee profile pictures
- Search functionality for employees by department or position
- RESTful API design
- Input validation and error handling

### Frontend
- React Router for navigation
- Material-UI for professional UI/UX
- TanStack Query for data fetching
- Session management with Context API
- Responsive design
- Employee CRUD operations
- Search functionality
- Profile picture upload

## Project Structure

```
studentID_comp3123_assignment/
├── docker-compose.yml
├── backend/
│   ├── models/
│   │   ├── User.js
│   │   └── Employee.js
│   ├── routes/
│   │   ├── auth.js
│   │   └── employees.js
│   ├── middleware/
│   │   ├── auth.js
│   │   └── upload.js
│   ├── uploads/
│   ├── server.js
│   ├── package.json
│   └── Dockerfile
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── Login.js
    │   │   ├── Signup.js
    │   │   ├── EmployeeList.js
    │   │   ├── AddEmployee.js
    │   │   ├── UpdateEmployee.js
    │   │   ├── ViewEmployee.js
    │   │   └── PrivateRoute.js
    │   ├── context/
    │   │   └── AuthContext.js
    │   ├── services/
    │   │   └── api.js
    │   ├── App.js
    │   └── index.js
    ├── package.json
    └── Dockerfile
```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login

### Employees
- `POST /api/employees` - Create new employee
- `GET /api/employees` - Get all employees
- `GET /api/employees/:id` - Get employee by ID
- `PUT /api/employees/:id` - Update employee
- `DELETE /api/employees/:id` - Delete employee
- `GET /api/employees/search?department=&position=` - Search employees

## Quick Start

### Using Docker Compose (Recommended)

1. **Prerequisites**: Make sure Docker and Docker Compose are installed on your system.

2. **Navigate to project directory**:
   ```bash
   cd COMP3123_Assignment2
   ```

3. **Start all services**:
   ```bash
   docker-compose up --build
   ```
   
   This will:
   - Build the backend Docker image
   - Build the frontend Docker image
   - Start MongoDB container
   - Start backend container
   - Start frontend container

4. **Access the application**:
   - **Frontend**: http://localhost:3000
   - **Backend API**: http://localhost:3001
   - **MongoDB**: localhost:27017

5. **Stop services**:
   ```bash
   docker-compose down
   ```

6. **View logs**:
   ```bash
   docker-compose logs -f
   ```

### Manual Setup (Without Docker)

#### Prerequisites
- Node.js (v18 or higher)
- MongoDB (running locally or connection string)
- npm or yarn

#### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file:
   ```env
   PORT=3001
   MONGODB_URI=mongodb://localhost:27017/employee_management
   JWT_SECRET=your_super_secret_jwt_key_change_this_in_production
   NODE_ENV=development
   ```

4. Make sure MongoDB is running locally (or update MONGODB_URI with your connection string)

5. Create uploads directory:
   ```bash
   mkdir uploads
   ```

6. Start the backend server:
   ```bash
   npm start
   # or for development with auto-reload
   npm run dev
   ```

   The backend will run on http://localhost:3001

#### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file (optional, defaults to http://localhost:3001/api):
   ```env
   REACT_APP_API_URL=http://localhost:3001/api
   ```

4. Start the development server:
   ```bash
   npm start
   ```

5. The app will automatically open at http://localhost:3000

## Usage

1. **Sign Up**: Create a new account with email and password
2. **Login**: Sign in with your credentials
3. **View Employees**: See all employees in a table format
4. **Add Employee**: Click "Add Employee" to create a new employee record
5. **View Details**: Click the "View" button to see employee details
6. **Update Employee**: Click the "Update" button to edit employee information
7. **Delete Employee**: Click the "Delete" button to remove an employee
8. **Search**: Use the search fields to filter employees by department or position
9. **Logout**: Click the logout button to sign out

## Technologies Used

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Multer for file uploads
- Express Validator for input validation
- Bcrypt for password hashing

### Frontend
- React 18
- React Router DOM
- TanStack Query (React Query)
- Material-UI (MUI)
- Axios for HTTP requests
- Context API for state management

### Deployment
- Docker & Docker Compose
- Nginx (for frontend in production)

## Notes

- The backend API requires authentication for all employee endpoints
- JWT tokens are stored in localStorage
- Profile pictures are stored in the `backend/uploads` directory
- The application uses CORS to allow frontend-backend communication
- All API responses follow RESTful conventions

## Development

For development, you can run the backend and frontend separately:

- Backend: `cd backend && npm run dev`
- Frontend: `cd frontend && npm start`

Make sure MongoDB is running before starting the backend.

