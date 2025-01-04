# Password Reset System

This project implements a complete Password Reset Flow using Node.js, Express.js, MongoDB, and React. It allows users to securely reset their passwords through email verification.

---

## Features

- **User Registration and Login**: Secure authentication for users.
- **Forgot Password Functionality**: Sends reset links to the user's registered email.
- **Secure Password Reset Flow**: Validates reset tokens and updates passwords securely.
- **Modern UI**: Built with React and styled using Bootstrap for a clean and responsive design.

---

## Project Workflow

### 1. Forget Password Page
- Users enter their registered email address.
- Backend checks if the email exists in the database.

### 2. Check User Existence
- **If not found**: Returns an error message.
- **If found**: Generates a secure random string.

### 3. Send Reset Link
- The random string is stored in the database and sent as part of a reset link to the user’s email.

### 4. User Clicks Reset Link
- Redirects the user to the Password Reset page on the frontend.

### 5. Validate Reset Token
- Backend verifies the reset token:
  - **If valid**: Displays a password reset form.
  - **If invalid/expired**: Shows an error message.

### 6. Password Reset
- Users submit a new password.
- Backend securely updates the password in the database.

---

## Technical Specifications

### Frontend
- **Framework**: React.js
- **Styling**: Bootstrap
- **Features**:
  - Intuitive forms for Forget Password and Reset Password.
  - Responsive design with modern styling.

### Backend
- **Framework**: Node.js and Express.js
- **Database**: MongoDB with Mongoose
- **Libraries Used**:
  - `bcrypt` for password hashing.
  - `jsonwebtoken` for token-based authentication.
  - `nodemailer` for sending emails.
  - `crypto` for generating secure random strings.