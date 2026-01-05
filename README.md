# Transcendence

A full-stack web application featuring multiplayer gaming experiences with Pong and Tic-Tac-Toe, user authentication, and social features.

## Overview

Transcendence is a modern web platform that combines classic games with real-time multiplayer capabilities, user profiles, match history, and friend management.

## Features

- **Game Modes**: Play Pong and Tic-Tac-Toe in PvP, PvE, or tournament modes
- **User Authentication**: Secure registration and login with JWT tokens and optional 2FA
- **User Profiles**: Customizable avatars and detailed statistics
- **Social Features**: Friend requests, friendships, and match history
- **Real-time Gameplay**: Interactive gaming experience with live updates
- **Responsive Design**: Built with TypeScript and modern web technologies

## Tech Stack

### Frontend

- TypeScript
- Vite
- TailwindCSS
- Custom routing system

### Backend

- Node.js
- Fastify
- SQLite
- JWT Authentication
- Bcrypt for password hashing

### Infrastructure

- Docker & Docker Compose
- Three-service architecture (Frontend, Game, Backend)

## Getting Started

### Prerequisites

- Docker
- Docker Compose

### Installation

1. Clone the repository

```bash
git clone <repository-url>
cd transcendence
```

2. Create environment file

```bash
cp .env.example .env
# Edit .env with your configuration
```

3. Build and start the services

```bash
make all
```

Or manually:

```bash
docker compose up -d --build
```

### Access the Application

- Frontend: http://localhost:5173
- Game Interface: http://localhost:5174
- Backend API: http://localhost:4999

## Development

### Available Commands

```bash
make all    # Build and start all services
make up     # Start services
make down   # Stop services
make re     # Restart all services
make clean  # Remove all containers, volumes, and images
```

### Project Structure

```
transcendence/
├── frontend/          # Main application frontend
│   └── ft_front/     # Vite + TypeScript app
├── GAME/             # Game interface and logic
│   ├── backend/      # API server
│   └── games/        # Pong and Tic-Tac-Toe implementations
└── infrastructure/   # Docker configurations
```

## API Endpoints

The backend provides RESTful endpoints for:

- Authentication (`/auth`)
- User management (`/users`)
- Match tracking (`/matches`)
- Friend system (`/friendships`)

## Database Schema

SQLite database with tables for:

- Users (with 2FA support)
- Matches (Pong)
- Tic-Tac-Toe matches
- Friendships

## License

This project is part of the 42 school curriculum.
