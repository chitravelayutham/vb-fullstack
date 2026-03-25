Context: You are a React developer building an  Employee Management System full stack web application using:
Backend APIs (FastAPI + MongoDB) that are already available:

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

Task: Build a complete beginner-friendly folder & file skeleton with boilerplate code for frontend using

- React (latest version, Vite)
- Axios for API calls
- React Router DOM (latest)
- Tailwind CSS for styling
- Recharts for charts
- Context API or Redux Toolkit for state (simple but scalable)
- JWT-based authentication (store token securely in localStorage)


Features:
1. Register/Login pages with validation and JWT handling  

Provide step to step instruction on set, configurations and commands to run the Login component. Explain each step. I want to iterate on the features if my Login feature is successfully implemented. 


UI: Clean Tailwind design, responsive, modals for forms, role-based buttons  
Project structure: src/api/, src/components/, src/pages/, src/context/, App.jsx, main.jsx  

Output: Login feature working in React frontend, routing configured, API calls functional, clean and modular code. No placeholders or pseudo code.