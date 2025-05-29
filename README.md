# Dockerized MERN Chat Application

A real-time chat application built with the MERN stack (MongoDB, Express.js, React, Node.js) and containerized using Docker. This application features real-time messaging capabilities, user authentication, and a modern UI.

## Features

- Real-time chat functionality using Socket.IO
- User authentication and authorization
- Modern React frontend with Vite
- Docker containerization for easy deployment
- MongoDB database integration

## Tech Stack

- **Frontend**: React, Vite
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Real-time Communication**: Socket.IO
- **Containerization**: Docker, Docker Compose

## Prerequisites

- Docker and Docker Compose installed on your system
- Git for version control
- Node.js (for local development)

## Project Structure

```
├── frontend/          # React frontend application
│   ├── src/          # Source files
│   ├── public/       # Static files
│   └── Dockerfile    # Frontend container configuration
├── backend/          # Node.js backend application
│   ├── controllers/  # Route controllers
│   ├── models/       # Database models
│   ├── routes/       # API routes
│   ├── middleware/   # Custom middleware
│   ├── utils/        # Utility functions
│   ├── socket/       # Socket.IO configuration
│   └── Dockerfile    # Backend container configuration
└── docker-compose.yml # Docker services configuration
```

## Environment Variables

Create a `.env` file in the root directory with the following variables:

```
MONGO_DB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
```

## Running with Docker

From the root of the project, where the docker-compose file lies, run:
```bash
docker-compose up --build
```

This command will:
1. Build the Docker images for both frontend and backend
2. Create and start the containers
3. Set up the network between containers
4. Connect to your MongoDB database

## Accessing the Application

- Frontend: http://localhost:5173
- Backend API: http://localhost:3000

## Development

For local development without Docker:

### Backend
```bash
cd backend
npm install
npm run dev
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

## API Endpoints

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `GET /api/messages` - Get chat messages
- `POST /api/messages` - Send a new message

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
