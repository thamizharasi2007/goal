Here's the README in pure text format for your MicroGoals project:


---

MicroGoals - Backend API

Description

MicroGoals is a backend API for managing personal goals. Users can register, login, and perform CRUD operations on their goals. The system is built using Node.js, Express.js, and MongoDB with JWT authentication to ensure secure access to the user's personal data.

Features

User Registration: Allows users to create an account with their name, email, and password.

User Login: Allows users to log in and receive a JWT token for authentication.

Goal Management: Users can create, view, update, and delete their goals.

JWT Authentication: Protects all the routes, ensuring that only authorized users can access or modify their data.

MongoDB: Stores user and goal data.


Technologies Used

Node.js: JavaScript runtime environment to run the backend.

Express.js: Web framework for Node.js.

MongoDB: NoSQL database to store data.

JWT: JSON Web Token for secure user authentication.

bcryptjs: For hashing passwords securely.


Setup and Installation

Prerequisites

Node.js

MongoDB or a MongoDB Atlas account for cloud database


Installation Steps

1. Clone the repository to your local machine:

git clone https://github.com/yourusername/microgoals.git


2. Navigate to the project directory:

cd microgoals


3. Install the required dependencies:

npm install


4. Set up the .env file with the following configuration:

MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key


5. Run the server:

npm start


6. The server will run on http://localhost:5000.



API Documentation

Authentication

POST /api/auth/register

Registers a new user.

Request Body:

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}

POST /api/auth/login

Logs in an existing user and returns a JWT token.

Request Body:

{
  "email": "john@example.com",
  "password": "password123"
}

Response:

{
  "token": "your_jwt_token"
}


---

Goal Management

POST /api/goals/create

Creates a new goal for the authenticated user.

Request Body:

{
  "title": "Learn Node.js"
}

GET /api/goals

Retrieves all goals for the authenticated user.

Response:

[
  {
    "title": "Learn Node.js",
    "completed": false
  }
]

PUT /api/goals/:id

Updates the specified goal.

Request Body:

{
  "title": "Master Node.js",
  "completed": true
}

DELETE /api/goals/:id

Deletes the specified goal.

Response:

{
  "message": "Goal deleted"
}

License

This project is licensed under the MIT License.

Acknowledgments

Node.js

Express.js

MongoDB

JWT

bcryptjs



---

You can copy this into any text file (for example, README.txt) and use it for your project. Let me know if you'd like to adjust anything!
