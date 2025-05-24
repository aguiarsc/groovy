<p align="center">
  <img src="https://github.com/user-attachments/assets/27adf966-5e2f-4645-9f9a-ae003d7a0539" alt="Groovy Music Logo" />
</p>

<div>
  <img src="https://github.com/user-attachments/assets/b01ef6e2-1eaf-46b5-9f89-ea5640d528ad" align="left"
     alt="Groovy Favicon">
    <img src="https://github.com/user-attachments/assets/b01ef6e2-1eaf-46b5-9f89-ea5640d528ad" align="right"
     alt="Groovy Favicon">
    <h1 align="center">Groovy Music</h1> 
  <p align="center">🎵 A full‑stack music streaming application built with Spring Boot & React 🎵</p>
</div>


<p align="center">
  <a href="#overview"><strong>Overview</strong></a> •
  <a href="#features"><strong>Features</strong></a> •
  <a href="#architecture"><strong>Architecture</strong></a> •
  <a href="#tech-stack"><strong>Tech Stack</strong></a> •
  <a href="#api-documentation"><strong>API Docs</strong></a> •
  <a href="#deployment"><strong>Deployment</strong></a> •
  <a href="#project-structure"><strong>Project Structure</strong></a> •
  <a href="#acknowledgements"><strong>Acknowledgements</strong></a>
</p>

## Overview

Groovy is a modern music streaming platform where listeners discover and enjoy tunes, and artists showcase their art. It features robust user management (regular, artist, admin), music & playlist handling, and an interactive player.

> **Why Groovy?** Because music should be seamless, social, and soulful.

---

## Features

### For Listeners

* **🎵 Music Streaming**: Intuitive audio player with controls.
* **📚 Library Management**: Organize your personal music collection.
* **🔀 Playlist Creation**: Build, explore, and share playlists.
* **❤️ Favorites**: Mark songs for quick access.
* **🔍 Advanced Search**: Filter by artist, album, or track.
* **👥 Profiles**: Customize and view user profiles.

### For Artists

* **📂 Music Upload**: Add and manage your songs & albums.
* **📊 Dashboard**: Insights and statistics on your content.
* **👁️ Profile Management**: Update bios and images.

### For Administrators

* **👮 User Management**: Grant roles, review accounts.
* **🎭 Content Moderation**: Approve or reject uploads.
* **📏 System Configuration**: Tweak policies and settings.

---

## Architecture

```
+-----------------+     +-----------------+     +-----------------+
| React Frontend  | <-- | Spring Backend  | <-- |   H2 Database   |
+--------+--------+     +--------+--------+     +--------+--------+
         |                       |                       
         v                       v                       
+-----------------+     +-----------------+               
| User Interface  |     | File Storage    |               
+-----------------+     +-----------------+               
```

1. **Client-Server**: Decoupled frontend & backend.
2. **RESTful API**: Clean, versioned endpoints.
3. **MVC & Repository**: Backend design patterns.
4. **Component-Based**: Reusable UI in React.
5. **Flux (Zustand)**: Predictable data flow.
6. **JWT Auth**: Stateless security.

---

## Tech Stack

<details>
<summary>🔍 Click to Expand</summary>

### **Backend**

* Java 17 · Spring Boot 3.x · Spring Security · JPA · H2 · Lombok · JWT · Swagger · Maven

### **Frontend**

* React 18 · TypeScript · React Router · Zustand · TanStack Query · Axios · Tailwind CSS · React Icons · Vite

### **DevOps & Tools**

* Docker · Docker Compose · Nginx · Git · H2 Console

</details>

---

## API Documentation

> Available when the backend is running:

* **Swagger UI**: `http://localhost:8080/swagger-ui.html`
* **OpenAPI Spec**: `http://localhost:8080/v3/api-docs`

|       Category | Endpoint           | Description                     |
| -------------: | :----------------- | :------------------------------ |
| Authentication | `/api/auth/*`      | Register, login, refresh tokens |
|          Users | `/api/users/*`     | Profile & account management    |
|          Songs | `/api/songs/*`     | CRUD + streaming                |
|         Albums | `/api/albums/*`    | Album operations                |
|        Artists | `/api/artists/*`   | Artist profiles & content       |
|      Playlists | `/api/playlists/*` | Create & manage playlists       |
|      Favorites | `/api/favorites/*` | Favorite songs                  |
|          Files | `/api/files/*`     | Upload & management             |
|          Admin | `/api/admin/*`     | Admin operations                |

---

## Deployment

**Live Demo:** [groovymusic.onrender.com](https://groovymusic.onrender.com)

### Prerequisites

1. [Docker](https://www.docker.com/) & Docker Compose
2. [Git](https://git-scm.com/)

### Quick Start

```bash
# Clone & enter repo
git clone --recurse-submodules https://github.com/aguiarsc/groovy
cd groovy

# Build & run
docker-compose up --build
```

**Access:** `http://localhost:5173`

*Use provided credentials in project upload.*

<details>
<summary>🔧 Troubleshooting Commands</summary>

```bash
docker-compose down
docker-compose up --build --remove-orphans
```

</details>

---

## Project Structure

```
groovymusic/
├── groovy-backend/      # Spring Boot backend
│   ├── src/             # Source code
│   ├── uploads/         # Media storage
│   └── README.md        # Backend docs
├── groovy-frontend/     # React frontend
│   ├── src/             # Source code
│   ├── public/          # Static assets
│   └── README.md        # Frontend docs
├── docker-compose.yml   # Docker setup
└── README.md            # This file
```

---

## Acknowledgements

* Educational content: All music & artist rights retained by original owners.
