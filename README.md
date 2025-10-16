# Secure Todo Application

A full-stack, secure Todo list application built with a .NET Core API and a React frontend. This project demonstrates best practices in web security, API design, and modern frontend development.

**Live Demo:** [Link to your live demo here]

![Secure Todo App Screenshot](https://raw.githubusercontent.com/atiq296/Secure-Todo/main/Screenshot%20(20).png)

## Overview

This application provides a secure platform for users to manage their daily tasks. It features robust user authentication, secure API endpoints, and a clean, responsive user interface. The primary focus of this project is to implement security best practices at every layer of the application stack.

## Key Features

-   **Secure User Authentication:** JWT-based authentication for secure user login and registration.
-   **CRUD Functionality:** Create, Read, Update, and Delete todo items.
-   **Todo Sharing:** Users can securely share their todo lists with other users.
-   **Responsive UI:** A modern and intuitive user interface built with React and Tailwind CSS.
-   **Role-Based Access Control (RBAC):** Secure endpoints that are accessible based on user roles.

## Security Features

Security is the cornerstone of this project. The following measures have been implemented:

-   **JWT Authentication:** Ensures that all API requests are properly authenticated and authorized.
-   **Secure Headers:** Implemented middleware to add security-related HTTP headers (like CSP, X-Frame-Options, etc.) to prevent common web vulnerabilities.
-   **Input Sanitization:** All user inputs are sanitized to protect against Cross-Site Scripting (XSS) attacks.
-   **Anti-Forgery Tokens:** Protection against Cross-Site Request Forgery (CSRF) attacks.
-   **HTTPS Enforced:** API and frontend are configured to enforce HTTPS in production.

## Tech Stack

### Backend
-   **.NET 9.0**
-   **ASP.NET Core Web API**
-   **Entity Framework Core:** For data access and object-relational mapping.
-   **PostgreSQL/SQLite:** Flexible database provider configuration.
-   **Serilog:** For structured logging.
-   **xUnit/NUnit:** For unit and integration testing.

### Frontend
-   **React.js**
-   **TypeScript**
-   **Tailwind CSS:** For utility-first styling.
-   **Axios:** For making API requests.

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

-   [.NET SDK 9.0](https://dotnet.microsoft.com/download)
-   [Node.js](https://nodejs.org/)

### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/atiq296/Secure-Todo.git
    cd Secure-Todo
    ```

2.  **Setup the Backend API:**
    - Navigate to the API directory:
      ```sh
      cd Todo.Api
      ```
    - Restore dependencies:
      ```sh
      dotnet restore
      ```
    - Update the database. (Ensure your `appsettings.json` has the correct connection string).
      ```sh
      dotnet ef database update
      ```
    - Run the API:
      ```sh
      dotnet run
      ```
      The API will be available at `https://localhost:5001`.

3.  **Setup the Frontend:**
    - In a new terminal, navigate to the frontend directory:
      ```sh
      cd frontend
      ```
    - Install NPM packages:
      ```sh
      npm install
      ```
    - Start the development server:
      ```sh
      npm start
      ```
      The application will open in your browser at `http://localhost:3000`.

## API Endpoints

The backend exposes the following RESTful endpoints:

-   `POST /api/auth/register`: Register a new user.
-   `POST /api/auth/login`: Log in an existing user and receive a JWT.
-   `GET /api/todos`: Get all todos for the authenticated user.
-   `POST /api/todos`: Create a new todo.
-   `PUT /api/todos/{id}`: Update an existing todo.
-   `DELETE /api/todos/{id}`: Delete a todo.
-   `POST /api/share`: Share a todo list with another user.

---

This project was built with security and scalability in mind. It serves as a strong example of a modern, full-stack web application.
