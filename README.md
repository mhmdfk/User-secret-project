# Secrets Web App

This is a web application where users can register or log in using their email or Google authentication. Once authorized, users can submit their secrets, which are anonymized and stored in the database. Only logged-in users can view and submit secrets.

## Features

- **User Authentication**:
  - Users can register with email and password or log in using Google authentication.
  - Secure password storage using bcrypt hashing.
  
- **Authorization**:
  - Only authorized users can view and submit secrets.
  
- **Submit Anonymous Secrets**:
  - Users can submit secrets, and the app will anonymize and store them in the database.
  
- **Sessions**:
  - User sessions are maintained using `express-session`, allowing users to remain logged in.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/mhmdfk/User-secret-project.git
   cd User-secret-project
   
2.Install the dependencies:
   npm i

3.Set up the PostgreSQL database:
  Create a database called your_database_name.
  Create a users table with columns email, password, and secret

4.Run the application:
  npm nodemon index.js

5.Open your browser and navigate to http://localhost:3000.

## Routes

- **`/`**: Home page.
- **`/login`**: Login page for email login.
- **`/register`**: Register page for email registration.
- **`/secrets`**: Displays the user's secret if logged in, otherwise redirects to the login page.
- **`/submit`**: Submit a new secret (only accessible to authorized users).
- **`/auth/google`**: Redirects users to Google for OAuth authentication.
- **`/auth/google/secrets`**: Redirects users to the secrets page after successful Google authentication.

## Technologies Used

- **Node.js**: JavaScript runtime for the backend.
- **Express**: Web framework for building the server and routing.
- **Passport.js**: Authentication middleware for handling local and Google OAuth authentication.
- **PostgreSQL**: Database for storing user information and secrets.
- **bcrypt**: Library for hashing passwords securely.
- **EJS**: Templating engine for rendering dynamic HTML content.
- **dotenv**: Loads environment variables from a `.env` file.

## How It Works

1. **Register/Login**: Users can sign up using their email and password or log in with Google. The password is hashed using bcrypt before saving to the database.
2. **Submit Secrets**: Once logged in, users can enter a secret. The secret is saved in the database and associated with the user's account.
3. **View Secrets**: Users can view their own secrets after logging in. If no secret is submitted, users are prompted to submit one.

## Contributing

Feel free to submit issues or pull requests to improve the project or fix bugs.

