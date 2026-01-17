# Full-Stack Movie Platform

A comprehensive full-stack web application for discovering, browsing, and managing movie collections. Built with React, Node.js, Express, and MongoDB, integrating with The Movie Database (TMDB) API.

## 🎬 Features

### Frontend (React)
- **Movie Discovery**: Browse movies from TMDB API
- **Multiple Views**: 
  - Now Playing
  - Upcoming Movies
  - Popular Movies
  - Top Rated Movies
- **Movie Details**: View comprehensive information about each movie
- **Favorites System**: Save and manage favorite movies
- **Must-Watch List**: Track movies you want to watch
- **Recommendations**: Get personalized movie suggestions
- **Reviews**: Read and write movie reviews
- **Responsive Design**: Fully responsive UI for all devices

### Backend (Node.js/Express)
- **RESTful API**: Clean API architecture
- **MongoDB Integration**: Persistent data storage with Mongoose
- **Authentication**: Secure JWT-based authentication
- **Password Security**: bcrypt password hashing
- **CORS Support**: Cross-origin resource sharing enabled

## 🛠️ Tech Stack

### Frontend
- **React** (with Vite)
- **React Router** - Client-side routing
- **TanStack Query** (React Query) - Data fetching and caching
- **TMDB API** - Movie data source

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication tokens
- **bcrypt** - Password hashing

## 📁 Project Structure

```
full-stack-movie-platform/
├── movies-api/          # Backend Node.js API
│   ├── api/            # API routes
│   ├── authenticate/   # Authentication logic
│   ├── db/             # Database models
│   ├── public/         # Static files
│   ├── index.js        # Server entry point
│   └── package.json
│
├── react-movies/       # Frontend React application
│   ├── src/
│   │   ├── api/       # API integration
│   │   ├── components/# React components
│   │   ├── contexts/  # React context providers
│   │   ├── pages/     # Page components
│   │   └── main.jsx   # App entry point
│   └── package.json
│
├── package.json        # Root package (orchestrates both apps)
├── README.md
└── .gitignore
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v20.19.0 or higher)
- MongoDB
- TMDB API Key ([Get one here](https://www.themoviedb.org/settings/api))

### Installation

#### 1. Clone the repository
```bash
git clone https://github.com/Elijah-Destigni/full-stack-movie-platform
cd full-stack-movie-platform
```

#### 2. Install all dependencies
```bash
npm run install-all
```

#### 3. Setup Environment Variables

##### Backend Environment Variables

**Windows (Command Prompt):**
```
cd movies-api
echo. > .env
```
**Mac/Linux:**
```
cd movies-api
touch .env
```

Add the following to your `.env` file:
```env
PORT=8080
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key

```

**Getting MongoDB URI:**
- **Local MongoDB:** `mongodb://localhost:27017/moviedb`
- **MongoDB Atlas:** Get from your Atlas dashboard (see [Atlas Setup Guide](#mongodb-atlas-setup))

**JWT_SECRET:** Any random string (example: `kj34h5kj2h3k4jh5k2j3h4k5jhkj2h3k4`)

---

##### Frontend Environment Variables

**Windows (Command Prompt):**
```
cd ..\react-movies
echo. > .env
```

**Mac/Linux:**
```
cd ../react-movies
touch .env
```

Then open `react-movies/.env` and add:
```env
VITE_TMDB_KEY=your_tmdb_api_key_here
```

#### 4. Start the Application

Open **two terminal windows**:

**Terminal 1 - Start Backend:**
```bash
npm run dev-api
```
Backend runs on `http://localhost:8080`

**Terminal 2 - Start Frontend:**
```bash
npm run dev-client
```
Frontend runs on `http://localhost:5173`

## 🔧 Available Scripts

### Frontend (react-movies)
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
```

### Backend (movies-api)
```bash
npm start           # Start server with Babel
npm run dev         # Start with nodemon (auto-restart)
```

## 🌐 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `GET /api/auth/verify` - Verify JWT token

### Movies
- `GET /api/movies/discover` - Get discover movies
- `GET /api/movies/:id` - Get movie details
- `GET /api/movies/favorites` - Get user's favorite movies
- `POST /api/movies/favorites` - Add movie to favorites
- `DELETE /api/movies/favorites/:id` - Remove from favorites

### Reviews
- `GET /api/reviews/:movieId` - Get reviews for a movie
- `POST /api/reviews` - Create a new review
- `PUT /api/reviews/:id` - Update a review
- `DELETE /api/reviews/:id` - Delete a review

---

---

## 🔒 Security Features

- **Password Hashing:** bcrypt with salt rounds
- **JWT Authentication:** Stateless token-based auth
- **Environment Variables:** Sensitive data kept secure
- **CORS:** Configured for secure cross-origin requests
- **Input Validation:** Protected against common vulnerabilities

---


## 👨‍💻 Author

**Elijah Destigni**

- GitHub: https://github.com/Elijah-Destigni
- LinkedIn: https://www.linkedin.com/in/elijahdestigni/

