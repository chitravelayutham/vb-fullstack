You are a senior Full Stack React Engineer.

Build a production-ready frontend for an Employee Management System using:

- React (latest version with Vite)
- Axios for API calls
- React Router DOM (latest)
- Tailwind CSS for styling
- Recharts (for charts)
- Context API or Redux Toolkit for state management (prefer simple but scalable)
- JWT-based authentication (token stored securely in localStorage)

Backend is already implemented using FastAPI + MongoDB (MVC architecture) with the following APIs:

AUTH APIs:
- POST /register → register new user (name, email, password)
- POST /login → login user → returns JWT token + role (admin/user)

EMPLOYEE APIs:
- GET /employees → get all employees
- POST /employees → create employee (admin only)
- PUT /employees/{id} → update employee (admin only)
- DELETE /employees/{id} → delete employee (admin only)
- GET /employees/search?name=&department= → filter employees

User object:
- userId
- username
- email
- role (admin/user)

Employee object:
- employeeId
- name
- email
- department
- position
- status

----------------------------------

### 🎯 FEATURES TO IMPLEMENT

1. 🔐 Authentication
- Register Page:
  - Fields: name, email, password
  - Validation + error handling
- Login Page:
  - Fields: email, password
  - Store JWT token after login
  - Redirect to Home

2. 🏠 Home Page (Protected Route)
- Show:
  - Logout button
  - Employee table
- If role = user:
  - View employees
  - Search & filter (name, department)
- If role = admin:
  - Show "Employee Management" button

3. 👨‍💼 Employee Management Page (Admin Only)
- Table of employees
- Features:
  - Add Employee button
  - Edit Employee
  - Delete Employee
  - Search & filter (name, department)

4. ➕ Add/Edit Employee Modal/Form
- Fields:
  - name
  - email
  - department
  - position
  - status

5. 📊 Dashboard Page
- Display pie chart:
  - Total employees grouped by department
- Use Recharts

6. 🔒 Route Protection
- Redirect unauthenticated users to login
- Restrict admin routes

7. ⚙️ API Integration
- Use Axios instance with:
  - Base URL
  - Interceptors to attach JWT token

----------------------------------

### 🧱 PROJECT STRUCTURE

src/
│── api/
│   └── axios.js
│
│── components/
│   ├── Navbar.jsx
│   ├── EmployeeTable.jsx
│   ├── EmployeeForm.jsx
│   └── ProtectedRoute.jsx
│
│── pages/
│   ├── Login.jsx
│   ├── Register.jsx
│   ├── Home.jsx
│   ├── EmployeeManagement.jsx
│   └── Dashboard.jsx
│
│── context/
│   └── AuthContext.jsx
│
│── App.jsx
│── main.jsx

----------------------------------

### 🎨 UI REQUIREMENTS

- Clean, modern UI using Tailwind
- Responsive design
- Table:
  - Pagination (optional)
  - Search bar
  - Filter dropdown
- Buttons:
  - Clear role-based visibility
- Use modals for Add/Edit

----------------------------------

### 🔐 AUTH HANDLING

- Store JWT in localStorage
- Decode token to get user role
- Persist login state on refresh

----------------------------------

### 📡 AXIOS SETUP

- Create reusable axios instance
- Add interceptor to include token:
  Authorization: Bearer <token>

----------------------------------

### ⚠️ ERROR HANDLING

- Show API errors on UI
- Handle:
  - Invalid login
  - Unauthorized access
  - Network errors

----------------------------------

### 🧪 BONUS (if possible)

- Loading spinners
- Toast notifications
- Form validation (React Hook Form or simple validation)

----------------------------------

### 📦 OUTPUT EXPECTATION

- Provide complete working code
- All components fully implemented
- Routing configured
- API calls wired correctly
- No placeholders or pseudo code

Ensure code is clean, modular, and follows best practices.