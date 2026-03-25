You are a React developer building a full stack application. Build a complete beginner-friendly folder & file skeleton with boilerplate code frontend for an Employee Management System using:

- React (latest version, Vite)
- Axios for API calls
- React Router DOM (latest)
- Tailwind CSS for styling
- Recharts for charts
- Context API or Redux Toolkit for state (simple but scalable)
- JWT-based authentication (store token securely in localStorage)

Backend APIs (FastAPI + MongoDB) are already available:

AUTH:
- POST /register → register (name, email, password)
- POST /login → login → returns JWT + role (admin/user)

EMPLOYEES:
- GET /employees → list all
- POST /employees → create (admin only)
- PUT /employees/{id} → update (admin only)
- DELETE /employees/{id} → delete (admin only)
- GET /employees/search?name=&department= → filter

Users: userId, username, email, role  
Employees: employeeId, name, email, department, position, status  

Features:
1. Register/Login pages with validation and JWT handling  
2. Home page (protected) showing employee table, search & filter  
3. Employee Management page (admin only) with Add/Edit/Delete  
4. Add/Edit employee form modal  
5. Dashboard page with pie chart of employees by department  
6. Route protection: redirect unauthenticated users, restrict admin routes  
7. Axios instance with JWT interceptor  
8. Show API errors on UI, handle invalid login, unauthorized access, network errors  

UI: Clean Tailwind design, responsive, modals for forms, role-based buttons  
Project structure: src/api/, src/components/, src/pages/, src/context/, App.jsx, main.jsx  

Output: Complete working React frontend, routing configured, API calls functional, clean and modular code. No placeholders or pseudo code.