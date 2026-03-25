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