# Groovy Music

<div align="center">

  ![Image](https://github.com/user-attachments/assets/27adf966-5e2f-4645-9f9a-ae003d7a0539)
  
  <h3>🎵 A full-stack music streaming application built with Spring Boot and React 🎵</h3>
</div>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#key-features">Key Features</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#api-documentation">API</a> •
  <a href="#user-journeys">User Journeys</a> •
  <a href="#security-implementation">Security</a> •
  <a href="#project-structure">Structure</a> •
  <a href="#license">License</a>
</p>

---

## Overview

Groovy is a modern music streaming platform that allows users to discover and enjoy music while providing artists with a platform to showcase their work. The application implements a robust user management system with different roles (regular user, artist, admin), comprehensive music management capabilities, playlist creation and sharing, and an interactive music player.

This project demonstrates integration of various technologies and architectural patterns to build a complete, production-ready web application with a focus on user experience and performance.

### Project Components

- **Backend**: REST API built with Spring Boot
- **Frontend**: React SPA with modern UI
- **Database**: H2 persistent in-memory database
- **Authentication**: JWT-based secure authentication and authorization
- **Media Storage**: File-based storage system for audio files and images

---

## Key Features

### For Listeners
- **🎵 Music Streaming**: Audio streaming with an intuitive player
- **📚 Library Management**: Create and organize personal music libraries
- **🔀 Playlist Creation**: Build and discover playlists
- **❤️ Favorites System**: Mark songs as favorites for quick access
- **🔍 Advanced Search**: Find music by artist, album, or song title
- **👥 User Profiles**: Personalized profiles

### For Artists
- **📂 Music Upload**: Upload and manage songs and albums
- **📊 Artist Dashboard**: Keep control of your art
- **👁️ Profile Management**: Create and update artist profiles with bio and images

### For Administrators
- **👮 User Management**: Manage user accounts and roles
- **🎭 Content Moderation**: Review and moderate uploaded content
- **📏 System Configuration**: Configure system parameters and policies

---

## Architecture

Groovy employs a modern, scalable architecture:

```
                            ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
                            │                 │     │                 │     │                 │
                            │  React Frontend │◄────┤  Spring Backend │◄────┤  H2 Database    │
                            │                 │     │                 │     │                 │
                            └────────┬────────┘     └────────┬────────┘     └─────────────────┘
                                     │                       │
                                     │                       │
                                     ▼                       ▼
                            ┌─────────────────┐     ┌─────────────────┐
                            │                 │     │                 │
                            │  User Interface │     │  File Storage   │
                            │                 │     │                 │
                            └─────────────────┘     └─────────────────┘
```

### Architectural Patterns

1. **Client-Server Architecture**: Clear separation of frontend and backend
2. **RESTful API**: Well-defined API for all system operations
3. **MVC Pattern**: Model-View-Controller pattern in the backend
4. **Repository Pattern**: Data access abstraction
5. **Component-Based Architecture**: Reusable UI components in the frontend
6. **Flux Architecture**: Unidirectional data flow using Zustand store
7. **JWT Authentication**: Stateless authentication mechanism

---

## Tech Stack

### Backend
- **Java 17**
- **Spring Boot 3.x**: Web application framework
- **Spring Security**: Authentication and authorization
- **Spring Data JPA**: Data persistence
- **H2 Database**: In-memory SQL database
- **Lombok**: Boilerplate code reduction
- **JWT**: JSON Web Tokens for stateless authentication
- **OpenAPI/Swagger**: API documentation
- **Maven**: Dependency management and build

### Frontend
- **React 18**: UI library
- **TypeScript**: Type-safe JavaScript
- **React Router**: Client-side routing
- **Zustand**: State management
- **TanStack Query**: Data fetching and caching
- **Axios**: HTTP client
- **Tailwind CSS**: Utility-first CSS framework
- **React Icons**: Icon library
- **Vite**: Build tool and development server

### DevOps & Tools
- **Docker**: Containerization
- **Nginx**: Web server for production deployment
- **Git**: Version control
- **H2 Console**: Database management interface

---

## API Documentation

The backend API is documented using OpenAPI/Swagger.

- **Swagger UI**: Available at http://localhost:8080/swagger-ui.html when the backend is running
- **OpenAPI Spec**: Available at http://localhost:8080/v3/api-docs

### API Endpoints Overview

| Category        | Endpoints                              | Description                               |
|-----------------|----------------------------------------|-------------------------------------------|
| Authentication  | `/api/auth/*`                          | User registration, login, token refresh   |
| Users           | `/api/users/*`                         | User profiles and management              |
| Songs           | `/api/songs/*`                         | Song CRUD and streaming                   |
| Albums          | `/api/albums/*`                        | Album management                          |
| Artists         | `/api/artists/*`                       | Artist profiles and content               |
| Playlists       | `/api/playlists/*`                     | Playlist creation and management          |
| Favorites       | `/api/favorites/*`                     | User favorites functionality              |
| Files           | `/api/files/*`                         | File upload and management                |
| Admin           | `/api/admin/*`                         | Administrative operations                 |

For complete details, refer to the Swagger documentation when the backend is running.

---

## User Journeys

### As a Listener

1. **Registration and Onboarding**:
   - Register a new account
   - Complete profile setup
   - Browse featured content on the homepage

2. **Music Discovery**:
   - Browse albums and artists
   - Search for specific songs
   - Explore curated playlists

3. **Playlist Management**:
   - Create personal playlists
   - Add/remove songs from playlists
   - Share playlists with others

4. **Listening Experience**:
   - Stream songs with the player
   - Use player controls (play/pause, skip, volume)
   - View song information in fullscreen mode
   - Mark songs as favorites

### As an Artist

1. **Artist Registration**:
   - Register as an artist
   - Complete artist profile with bio and images

2. **Content Management**:
   - Upload songs and create albums
   - Edit song metadata and album information
   - Manage content visibility

### As an Administrator

1. **User Management**:
   - View and manage user accounts
   - Modify user roles
   - Handle account issues

2. **Content Moderation**:
   - Review uploaded content
   - Approve or reject submissions
   - Manage content violations

---

## Security Implementation

Groovy implements a comprehensive security model:

### Authentication
- **JWT-based** authentication system
- Token generation, validation, and refresh mechanisms
- Secure password storage with BCrypt encoding

### Authorization
- **Role-based access control** (USER, ARTIST, ADMIN)
- Method-level security with Spring Security
- Protected API endpoints

### Data Security
- Input validation on all API endpoints
- Protection against common web vulnerabilities (CSRF, XSS)
- Secure handling of sensitive user data

### API Security
- CORS configuration for frontend-backend communication
- Rate limiting for API endpoints
- Proper error handling with controlled information exposure

---

## Deployment

### Containerization
Groovy is containerized using Docker, with separate containers for:
- Frontend (Nginx + React)
- Backend (Spring Boot)

### Production Considerations
- **Environment Variables**: Configuration via environment variables
- **Persistence**: Volume mapping for data persistence
- **SSL/TLS**: HTTPS configuration for production
- **Reverse Proxy**: Nginx configuration for routing
- **Monitoring**: Health check endpoints

### Deployment Options
- **Manual Deployment**: Step-by-step guide in respective READMEs
- **Docker Compose**: Single-command deployment with docker-compose

---

## Project Structure

The project follows a modular structure:

```
groovymusic/
├── groovy-backend/      # Spring Boot backend
│   ├── src/             # Source code
│   ├── uploads/         # Media storage
│   └── README.md        # Backend documentation
│
├── groovy-frontend/     # React frontend
│   ├── src/             # Source code
│   ├── public/          # Static assets
│   └── README.md        # Frontend documentation
│
├── docker-compose.yml   # Development docker setup
└── README.md            # This file
```

### Detailed Structure Documentation
For comprehensive structure details, see the backend and frontend READMEs.

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Acknowledgements

- All music and artist content is provided for educational purposes. This web will never be commercial but instead a study-case.
- All music and artist content rights belong to themselves.
- This project is production-ready with secured env variables. You will not be able to run locally this project. 
- Icon libraries: React Icons, Font Awesome
- Design inspiration: Spotify, Apple Music

---

<div align="center">
  <p>🎵 Developed as a final grade project for DAW course 🎵</p>
</div>
