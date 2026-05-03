# TaskFlow – Full-Stack Task Manager

A full-stack task management application built with React, Node.js, Express, and MongoDB. Features complete CRUD operations, status/priority filtering, and a responsive dark UI.

## Tech Stack

**Frontend:** React · JavaScript · CSS3  
**Backend:** Node.js · Express.js  
**Database:** MongoDB · Mongoose  
**Tools:** Git · REST API · dotenv · CORS

## Features

- ✅ Create, read, update, and delete tasks
- 🔍 Filter tasks by status (To Do / In Progress / Done)
- 🎯 Priority levels (High / Medium / Low) with visual indicators
- 📊 Live stats dashboard (task counts per status)
- 📱 Responsive design — works on mobile and desktop
- 🌙 Dark theme UI

## Getting Started

### Prerequisites

- Node.js v18+
- MongoDB (local or [MongoDB Atlas](https://www.mongodb.com/atlas))

### Backend Setup

```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your MongoDB URI
npm start
```

### Frontend Setup

```bash
cd frontend
npm install
npm start
```

> The frontend runs on `http://localhost:3000` and the API on `http://localhost:5000`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/tasks` | Get all tasks (supports `?status=` filter) |
| GET | `/api/tasks/:id` | Get a single task |
| POST | `/api/tasks` | Create a new task |
| PUT | `/api/tasks/:id` | Update a task |
| DELETE | `/api/tasks/:id` | Delete a task |

### Example Request

```bash
# Create a task
curl -X POST http://localhost:5000/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title": "Review PR", "status": "todo", "priority": "high"}'
```

## Project Structure

```
taskmanager/
├── backend/
│   ├── models/
│   │   └── Task.js          # Mongoose schema
│   ├── routes/
│   │   └── tasks.js         # CRUD routes
│   ├── server.js            # Express entry point
│   └── .env.example
└── frontend/
    ├── src/
    │   ├── components/
    │   │   ├── TaskCard.jsx
    │   │   ├── TaskModal.jsx
    │   │   └── FilterBar.jsx
    │   ├── services/
    │   │   └── api.js       # Fetch wrapper
    │   └── App.jsx
    └── public/
```

## Author

**Ingrid Vitória Guimarães**  
[LinkedIn]([https://linkedin.com/in/ingrid-vitoriaguimaraes](https://www.linkedin.com/in/ingrid-vitoria-guimaraes/)) · [GitHub](https://github.com/IngridVih)
