# User Registration System

A User Registration System built with Node.js, Express, MongoDB, and JWT for authentication. This system allows users to sign up, log in, and manage their profiles with secure password hashing.

## Table of Contents

* Features
* Installation
* Usage
* API Endpoints
* Technologies Used
* Contributing
* Acknowledgements

## Features

* User Registration
* User Login
* User Profile Management
* Password Hashing
* JWT Authentication
* Input Validation
  
## Installation

1. Clone the Repository:

   git clone https://github.com/username/repository.git
  
   cd repository

2. Install dependencies:

   npm install

3. Set up environment variables:

   Create a '.env' file in the root directory and add the following variables:

   MONGO_URI=your_mongodb_connection_string
   
   JWT_SECRET=your_jwt_secret
   
   PORT=5000

4. Start the server:

   npm start

## Usage

* Register a new user:

  Send a POST request to '/api/auth/register' with the following JSON body

  {
  
    "username": "testuser",
  
    "email": "test@example.com",
  
    "password": "password123"
  
  }

* Login with existing user:

  Send a POST request to '/api/auth/login' with the following JSON body:

  {
  
    "email": "test@example.com",
  
    "password": "password123"
  
  }

  The response will contain a JWT token which should be used for authenticated requests.

* Accessing protected routes:

  Add the JWT token to the x-auth-token header for accessing protected routes like 
  '/api/users/profile'.

## API Endpoints

### Authentication

* POST /api/auth/register
  
  Registers a new user.

* POST /api/auth/login

  Logs in a user and returns a JWT token.

## User Management

* GET '/api/users/profile'

  Retrieves the profile of the logged-in user. Requires x-auth-token header.

* PUT '/api/users/profile'

  Updates the profile of the logged-in user. Requires x-auth-token header.

* DELETE '/api/users/profile'

  Deletes the profile of the logged-in user. Requires x-auth-token header.

* GET '/api/users'

  Retrieves all users. Typically used for admin purposes.

## Technologies Used

* Node.js
* Express
* MongoDB
* Mongoose
* bcryptjs
* JWT (jsonwebtoken)
* express-validator
* body-parser

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.


    



