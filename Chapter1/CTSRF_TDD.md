TEST SPEC — Write These Tests FIRST 
    •  test_app_renders_without_crashing — render <App />, expect no thrown error 
    •  test_login_route_renders_login_page — render <App /> with MemoryRouter at '/login', expect login form in DOM 
    •  test_protected_route_redirects_unauthenticated — render <App /> at '/', unauthenticated user, expect redirect to '/login'