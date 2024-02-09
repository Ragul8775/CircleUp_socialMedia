Certainly! Combining the frontend and backend README content, we can create a comprehensive guide for the entire CircleUp social networking platform project.

---

# CircleUp Social Networking Platform

CircleUp is a comprehensive social networking platform designed to connect users through posts, friend connections, and personal profiles. The platform features a dynamic theme switcher, user authentication, post creation and management, friends management, and more, all built with modern web technologies.

## Features

- **User Authentication**: Secure login and registration with form validation.
- **Dynamic Theming**: Users can switch between light and dark themes.
- **Post Management**: Users can view, create, and update posts.
- **Friend System**: Users can add or remove friends, view friend lists, and manage friend interactions.
- **Profile Management**: Users can view and update their profiles.
- **Secure Password Handling**: Passwords are securely hashed using bcrypt.
- **Middleware Authentication**: Protects routes with JWT token verification to ensure that requests are authenticated.
- **Image Uploads**: Supports profile and post picture uploads.
- **Responsive Design**: The UI is responsive and supports various device sizes.

## Technologies Used

- **Frontend**:
  - React.js
  - Redux Toolkit for state management
  - Material UI for component library
  - Formik and Yup for form handling and validation
  - react-dropzone for file uploads

- **Backend**:
  - Node.js and Express.js for the server
  - MongoDB with Mongoose for the database
  - JSON Web Tokens (JWT) for authentication
  - bcrypt for password hashing
  - multer for handling file uploads
  - dotenv for environment variable management
  - cors for cross-origin resource sharing
  - helmet for security headers
  - morgan for HTTP request logging

## Getting Started

### Prerequisites

- Node.js
- MongoDB instance (local or remote)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://your-repository-url.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd your-project-directory
   ```

3. **Install dependencies for both frontend and backend**:
   Navigate to each directory (`/client` and `/server`) and run:
   ```bash
   npm install
   ```

4. **Set up environment variables**:
   - For the **backend**, create a `.env` file in the root directory of `/server` and add:
     ```
     MONGO_URL=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret_key
     PORT=your_preferred_port (default is 6001)
     ```
   - For the **frontend**, if there are any environment variables (like API endpoints), ensure they are set in `.env` files as needed.

5. **Start the server and client**:
   - For the **backend**, navigate to the `/server` directory and run:
     ```bash
     npm start
     ```
   - For the **frontend**, navigate to the `/client` directory and run:
     ```bash
     npm start
     ```

### API Endpoints

A brief overview of key API endpoints. Refer to the specific sections above for more details.

- **Auth**:
  - Register: `POST /auth/register`
  - Login: `POST /auth/login`
- **Users**:
  - Get User: `GET /users/:id`
  - Get User Friends: `GET /users/:id/friends`
  - Add/Remove Friend: `PATCH /users/:id/:friendId`
- **Posts**:
  - Create Post: `POST /posts`
  - Get Feed Posts: `GET /posts`
  - Get User Posts: `GET /posts/:userId/posts`
  - Like Post: `PATCH /posts/:id/likes`

## Security

This application implements security best practices, including hashed passwords, token-based authentication, and security headers, to ensure user data protection and secure access to endpoints.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.

---

