Context: Working auth system with get_current_user and require_admin dependencies. 
Employees router at backend/app/routers/employees_routes.py currently has no auth. 
 
Task: Add RBAC to the items router: 
  GET /items/ — any authenticated user 
  GET /items/{id} — any authenticated user 
  POST /items/ — admin role only 
  PUT /items/{id} — admin role only 
  DELETE /items/{id} — admin role only 
 
Constraints: 
  - Use FastAPI Depends() injection — no inline token parsing 
  - Return 401 for missing/invalid token, 403 for wrong role 
  - Add created_by field to items, populated from JWT sub on creation 
  - Add audit log: each state-changing operation logs {user, action, item_id, 
timestamp} 
 
Also update the test file to include auth headers in all requests. 