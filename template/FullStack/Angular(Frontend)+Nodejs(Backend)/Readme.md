# FullStack Template: Angular + Node.js

This repository provides a simple FullStack template for building modern web applications using Angular for the frontend and Node.js for the backend. It includes essential features such as user authentication and a responsive user interface.

## Features

- **User Authentication**: Supports user registration and login with access token.
- **Frontend**: Built with Angular, offering a dynamic and responsive user interface.
- **Backend**: Powered by Node.js with Express, providing a robust RESTful API.
- **API Integration**: Seamless communication between the frontend and backend through API calls.
- **Responsive Design**: Ensures the application is accessible on various devices.

## Technologies Used

### Frontend

- **Angular**: A JavaScript library for building user interfaces.
- **Bootstrap**: For responsive and mobile-first UI design.

### Backend

- **Node.js**: A JavaScript runtime built on Chrome's V8 JavaScript engine.
- **Express**: A minimal and flexible Node.js web application framework.
- **MongoDB**: A NoSQL database known for its flexibility and scalability.
- **Mongoose**: An elegant MongoDB object modeling for Node.js.

## Installation
1. **Populate the .env.example file**:

   ```bash
   PORT=
    MONGODB_URI=<mongo-db-url>
    ACCESS_TOKEN_SECRET=<access-token-secret>
    ACCESS_TOKEN_EXPIRY=<access-token-expiry-duration>
   ```

   eg:
   ```bash
   PORT=8000
   MONGODB_URI=mongodb://localhost:27017/angular-nodejs
   ACCESS_TOKEN_SECRET=1234567890
   ACCESS_TOKEN_EXPIRY=1h
   ```
   
2. **Install the required dependencies**:

   ```bash
   npm install
   ```

3. **Ensure MongoDB is running**:
   - Make sure your MongoDB server is running locally or accessible remotely.

4. **Run the application**:

   For client:
   ```bash
   ng serve
   ```

   For server:
   ```bash
   npm run dev
   ```

5. **Access the application**:

   Visit `http://localhost:4200/` in your web browser.

## Routes and Functionalities

- **`/signup` [GET, POST]**:
  - **GET**: Renders the registration page where new users can sign up.
  - **POST**: Handles the form submission for user registration. If the username is already taken, it flashes an error message. Otherwise, it creates a new user and redirects to the login page with a success message.

- **`/signin` [POST]**:
  - **GET**: Renders the login page where users can log in with their credentials.
  - **POST**: Handles the login form submission. If the credentials are correct, it logs the user in by storing their user ID in the access token and redirects to the dashboard. If the credentials are incorrect, it flashes an error message.

- **`/` [GET]**:
  - Renders the homepage of the application.

## Database

The application uses MongoDB for storing user information. The `users` collection in the MongoDB database contains the following fields for each user:

- **_id**: ObjectId, the unique identifier for each document (user).
- **username**: String, unique, cannot be null.
- **emailid**: String, unique, cannot be null.
- **password**: String, hashed, cannot be null.

---

Made using [Universal-Box](https://github.com/Abhishek-Mallick/universal-box)
