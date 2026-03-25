 CONTEXT: 
 Starting a new React 18 frontend app. Vite has been initialized with: npm  create vite@latest frontend -- --template react 
 Backend API is running at http://localhost:8000 
 
 TASK: 
 Set up the complete React app scaffold. 
 STEP A — Install dependencies: 
 npm install react-router-dom@6 @tanstack/react-query@5 axios 
 react-hook-form zod @hookform/resolvers 
 react-hot-toast tailwindcss@3 postcss autoprefixer 
 npm install -D vitest @testing-library/react @testing-library/jest-dom 
 msw @testing-library/user-event 
 STEP B — Create these files: 
 src/api/client.js 
 - Axios instance with baseURL from import.meta.env.VITE_API_URL 
 - Request interceptor: read token from localStorage key 'access_token', 
 add Authorization: Bearer <token> header if token exists 
 - Response interceptor: on 401 response, remove token from localStorage 
 src/context/AuthContext.jsx 
 - React context with: user (object|null), token (string|null), isLoading 
 (bool) 
 - On mount: read token from localStorage, if found call GET /auth/me, 
 if successful set user, if failed clear token 
 - login(credentials): POST /auth/login, on success store token in 
 localStorage 
 and state, call GET /auth/me to get user object 
 - logout(): clear token from localStorage, set user and token to null 
 - isAdmin(): returns user?.role === 'admin' 
 - Export: AuthProvider component and useAuth hook 
 JUMP Vibe Coding Bootcamp  |  Page   |  github.com/becloudready/vibebuilder-fullstack 
 JUMP Bootcamp — Build Prompt Playbook 
 src/components/ProtectedRoute.jsx 
 - If isLoading: return <div>Loading...</div> 
 - If no user: return <Navigate to='/login' replace /> 
 - Otherwise: return <Outlet /> (or children prop) 
 src/App.jsx 
 - Wrap everything with QueryClientProvider and AuthProvider 
 - Routes: 
 /login → LoginPage (public) 
 /register → RegisterPage (public) 
 / → Dashboard (protected by ProtectedRoute) 
 /items → ItemsListPage (protected) 
 /items/new → ItemFormPage (protected) 
 /items/:id → ItemDetailPage (protected) 
 src/.env (or .env in root): 
 VITE_API_URL=http://localhost:8000 
 Create placeholder components for all pages (just return a <div> with the page 
 name). 
 Create src/tests/App.test.jsx with the 3 tests above. 
 Set up Vitest config in vite.config.js. 
 FORMAT: Complete content for every file. 