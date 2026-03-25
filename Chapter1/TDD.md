Prompt1:

Context: You are a React developer building an Employee Management System frontend using React + Vite + Tailwind + Axios + JWT authentication. The Login page is fully implemented and functional.

Task: Create **unit tests for the Login page** using **Vitest** and **React Testing Library**. The tests should cover:

1. Rendering the login form correctly (email, password, submit button)
2. Validating input fields (required fields)
3. Displaying error message when login fails
4. Successful login calls the backend and stores JWT and role in localStorage
5. Redirects to home page on successful login

Requirements:

- Include **step-by-step instructions** to set up Vitest and React Testing Library
- Include explanations for each step
- Provide a copy-paste **ready-to-use test file** for Login.jsx
- Mock API calls using **Vitest mocks**
- Ensure tests are runnable with Vite

Output: A beginner-friendly setup for unit testing the Login page that can be immediately added to the project and executed.


Prompt 2: 
Context: FastAPI backend, MongoDB Motor, pytest. 
We are building authentication. User document: {username, email, hashed_password, 
role} 
 
Task: Write complete pytest tests for: 
  test_register_user_success 
  test_register_duplicate_username_returns_409 
  test_register_weak_password_returns_422 
  test_login_success_returns_jwt 
  test_login_wrong_password_returns_401 
  test_login_nonexistent_user_returns_401 
  test_protected_route_without_token_returns_401 
  test_protected_route_with_valid_token_succeeds 
  test_protected_route_with_expired_token_returns_401 
  test_admin_route_with_user_role_returns_403 
 
Important: Use same 401 response for wrong password AND nonexistent user. 
Never reveal which one failed — this is a security requirement. 
Format: Full test file with fixtures 