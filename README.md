# Node.js API Project

A simple Node.js API with Express.js featuring a healthcheck endpoint and user management API.

## Installation

1. Install dependencies:
```bash
npm install
```

## Running the Server

**Development mode** (with auto-reload):
```bash
npm run dev
```

**Production mode**:
```bash
npm start
```

The server will start on `http://localhost:3000` (or custom PORT in environment variables).

## API Endpoints

### Health Check
- **GET** `/health` - Returns server health status
  ```json
  {
    "status": "healthy",
    "timestamp": "2026-05-23T10:30:45.123Z",
    "uptime": 125.456
  }
  ```

### Users API
- **GET** `/api/users` - Get all users
  ```json
  {
    "success": true,
    "data": [...],
    "count": 3
  }
  ```

- **GET** `/api/users/:id` - Get user by ID
  ```json
  {
    "success": true,
    "data": {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com"
    }
  }
  ```

## Environment Variables

- `PORT` - Server port (default: 3000)
- `NODE_ENV` - Environment mode (development/production)

## Project Structure

```
.
├── server.js          # Main application file
├── package.json       # Project dependencies
├── .gitignore         # Git ignore rules
└── README.md          # This file
```
