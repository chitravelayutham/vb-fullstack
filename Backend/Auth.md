Context: FastAPI app. Tests in tests/test_auth.py all failing. 
Error output: [paste failing test output] 
 
Task: Create backend/app/routers/auth.py and backend/app/security/auth.py 
 
Auth router endpoints: 
  POST /auth/register — create user 
  POST /auth/login — return access_token 
  GET /auth/me — return current user (protected) 
 
Security module functions: 
  hash_password(password: str) -> str (use passlib bcrypt) 
  verify_password(plain: str, hashed: str) -> bool 
  create_access_token(data: dict, expires_delta: timedelta) -> str 
  get_current_user(token: str) -> User (FastAPI dependency) 
  require_admin(user: User) -> User (dependency, raises 403 if not admin) 
 
Security requirements: 
  - bcrypt with cost factor 12 (not default 10) 
  - JWT HS256, 24h expiry for access token 
  - Minimum password length: 8 chars, must contain number and letter 
  - Email must be valid format (use Pydantic EmailStr) 
  - Usernames: alphanumeric + underscore, 3-20 chars 
  - Same 401 response body for wrong password and missing user 
  - Never log passwords or tokens 
Tests: All tests in tests/test_auth.py must pass 