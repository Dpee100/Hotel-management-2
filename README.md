# Project Readme

## Introduction
This is a simple Express.js application for managing room types and rooms. It provides APIs to create, read, update, and delete room types and rooms. Additionally, it includes authentication and authorization middleware for securing routes.

## Prerequisites
Before running this application, ensure you have the following installed:
- Node.js
- npm (Node Package Manager)

## Getting Started
1. Clone the repository to your local machine:
    ```bash
    git clone <repository_url>
    ```
2. Navigate to the project directory:
    ```bash
    cd <project_directory>
    ```
3. Install dependencies:
    ```bash
    npm install
    ```
4. Start the server:
    ```bash
    npm start
    ```
5. The server will start running on `http://localhost:3000`.

## Usage
The following APIs are available:

### Room Types
- `POST /api/v1/room-types`: Create a new room type.
- `GET /api/v1/room-types`: Get all room types.

### Rooms
- `POST /api/v1/rooms`: Create a new room. (Authentication and Authorization required for admin)
- `GET /api/v1/rooms`: Get all rooms.
- `GET /api/v1/rooms/:roomId`: Get a room by ID.
- `PATCH /api/v1/rooms/:roomId`: Update a room by ID. (Authentication and Authorization required for admin)
- `DELETE /api/v1/rooms/:roomId`: Delete a room by ID. (Authentication and Authorization required for admin)

### Authentication & Authorization
- Authentication middleware is applied to routes requiring authentication.
- Authorization middleware is applied to routes requiring specific roles (e.g., admin).

### Request/Response
- Request and response payloads are in JSON format.

## Middlewares
- `authenticate`: Middleware for authenticating users.
- `authorize`: Middleware for authorizing users based on roles.
- `validate`: Middleware for validating request payloads.

## Dependencies
- Express.js: Fast, unopinionated, minimalist web framework for Node.js.
- Body-parser: Node.js body parsing middleware.
- Others: Refer to `package.json` for additional dependencies.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request for any enhancements or bug fixes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author
[Your Name/Username] - [Your Contact Information]
