MY PROJECT NAME: ONLINE JOB PROTAL

Documentation for SignUp and Login Components
1. SignUp Component
Overview
The SignUp component allows users to register a new account by submitting their details through a form. It validates the input and sends a POST request to the backend server.

Key Features
Collects user details: username, email, password, first name, last name, date of birth, and phone number.
Validates the form to ensure all fields are filled before submission.
Displays success or error messages based on the server response.

Implementation
State Management
formData: Stores user input data.
errorMessage: Displays validation or server-side errors.
successMessage: Displays a success message after successful registration.
Event Handlers
handleChange: Updates the formData state when the user types in the input fields.
handleSubmit:
Validates that all fields are filled.
Sends a POST request to the backend API endpoint /signup.
Handles errors or success responses.
Backend API Endpoint
URL: https://backendapps-0d3a0920208f.herokuapp.com/signup
Method: POST
Request Body: JSON object containing the form data.
Styling
Inline styles are used for a responsive and visually appealing UI.
Includes grid-based input fields layout and a styled header and footer.
2. Login Component
Overview
The Login component allows users to sign into their accounts by providing email and password credentials.

Key Features
Validates user inputs.
Sends login data to the server for authentication.
Handles user roles (administrator, Customer, accountant, Manager) by redirecting to appropriate dashboards.
Implementation
State Management
email & password: Stores the login credentials.
errorMessage: Displays login validation or authentication errors.
isLoading: Tracks the loading state during the login process.
Event Handlers
handleSubmit:
Sends a POST request with login credentials to the /login endpoint.
Handles errors or success responses.
Stores user roles and allowed menus in localStorage.
Redirects users based on their roles.
Backend API Endpoint
URL: https://backendapps-0d3a0920208f.herokuapp.com/login
Method: POST
Request Body: JSON object containing email and password.
Role-Based Redirection
Administrator: Redirects to /AdminDaschboard.
Other Roles (Customer, accountant, Manager): Redirects to /UserDashboard.
Styling
Uses a clean and modern card-based layout.
Provides hover effects and transitions for buttons and links.
Common Features
Responsive Design: Both components are styled for desktop and mobile compatibility.
Error Handling: Displays errors gracefully to users in case of incomplete inputs or server issues.
Navigation: Includes links for navigation to related pages (Home, Sign Up, Login, Forgot Password).
Usage Instructions
SignUp Component:

Include <SignUp /> in the desired route or page.
Ensure the backend /signup API is configured and functional.
Login Component:

Include <Login /> in the desired route or page.
Ensure the backend /login API is configured and supports role-based authentication.
